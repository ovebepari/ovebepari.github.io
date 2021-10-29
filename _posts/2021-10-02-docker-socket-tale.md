---
layout: post
title: A Tale on /var/run/docker.sock 
comments: true
categories: Linux|Systems
location: DUET, Bangladesh
---

If you're reading this text then you know what `docker` is. I'll slowly move toward the point of the article, which is one of many Inter Process Communication (IPC) mechanism: Unix Domain Sockets (loosely, Network Sockets) and how it can be used in communication among various abstraction layers in a Computer System. I'll talk about how docker achieves this but it'll be helpful to understand how an abstraction nightmare system (such as Windows 11) can use it (or some other IPC mechanisms) to communicate among various abstraction layers, architectures, filesystems etc.

## Prerequisite Wikis
- [Client Server Model](https://en.wikipedia.org/wiki/Client%E2%80%93server_model)
- [Daemon](https://en.wikipedia.org/wiki/Daemon_(computing))
- [Inter Process Communication, IPC](https://en.wikipedia.org/wiki/Inter-process_communication)
- [Unix Domain Socket, an unix IPC model](https://en.wikipedia.org/wiki/Unix_domain_socket)
