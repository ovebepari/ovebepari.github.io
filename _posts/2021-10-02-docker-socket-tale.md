---
layout: post
title: A Tale on /var/run/docker.sock, from system architechture POV
comments: true
categories: Linux|Systems
location: DUET, Bangladesh
---

If you're reading this text then you know what `docker` is. The point of the article is one of many Inter Process Communication (IPC) mechanism: Unix Domain Sockets (loosely, Network Sockets) and how it can be used in communication among various abstraction layers in a Computer System. The goal is to understand how an abstraction nightmare system (such as Windows 11) can use it (or some other IPC mechanisms) to communicate among various abstraction layers, architectures, filesystems etc.

## Prerequisite Wikis
- [Client Server Model](https://en.wikipedia.org/wiki/Client%E2%80%93server_model)
- [Daemon](https://en.wikipedia.org/wiki/Daemon_(computing))
- [Inter Process Communication, IPC](https://en.wikipedia.org/wiki/Inter-process_communication)
- [Unix Domain Socket, an unix IPC model](https://en.wikipedia.org/wiki/Unix_domain_socket)

Docker follows a client-server architechture. The docker cli binary that runs `docker run`, `docker build`, etc is the *docker client*. The server is a daemon that always runs in the background, listening for anything asked by the *docker client* through an API ([REST](https://en.wikipedia.org/wiki/Representational_state_transfer)?). Here's a fun question:

> When to build a daemon for a cli application?
>
> Docker has a daemon, Git Doesn't. Both are extreamly wonderful CLI applications.

*Docker server* exposes a socket file in unix systems to talk to the *docker client*. This socket file `/var/run/docker.sock` is INDEPENDENT, with appropriate READ/WRITE access, speaking in a language both the client and then server understand (Protocol), works as a bridge between them.