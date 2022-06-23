---
layout: post
title: I Made My Own GitHub, Not Really (It Only Lets You Clone)
description: Trying to remake github, only close functionality
image: /post_images/2020/Mar/gits_http_request.png
comments: false
categories: Linux|Systems
location: DUET, Bangladesh
---

I always wandered how `git` worked internally. It's a beautiful piece of software, great craftsmanship, great engineering throughout! While I still have a lot to know on how `git` deals with `files` and `blobs`, I started gathering information on how `GitHub` worked on the other hand. I wanted to make my own GitHub.

GitHub is HUGE too, too many constrains, user authentication, inter-GitHub cloning-pushing, authentication of  push requests, merging data from various users, data compression and delivery over the network, I mean it is the peak for Computer Science and Software Engineering as far as I can imagine. I just wanted to know how `git` sent HTTP requests (if it was the case) to a server and how the server responded. So I didn't need to code awfully lot details. I just needed to respond to a Git CLI client's request and work accordingly. That's what I did. 

I used `python3 flask` on the backend. I ran a local web server with `python3 -m http.server` and checked if I could detect any requests sent from the **Git CLI** with this command: `git clone http://0.0.0.0:8000`. And it did surprisingly.

![Gits HTTP Request to the Server](/post_images/2020/Mar/gits_http_request.png){:.center-image}

And our Git CLI's HTTP request found on the **server log** is `GET /info/refs?service=git-upload-pack HTTP/1.1`. It's a GET request on the `/info/` directory possible inside `/.git/` directory. Everything is self-explanatory except that `git-upload-pack` keyword, what's that? Let's Google then.

<center>A few days of goggling!</center><br>

I've found there's an article on <a href="https://git-scm.com/book/en/v2/Git-on-the-Server-The-Protocols">Official Git Site</a> where they talks about how to host **Git on Servers -  The Protocols**. Basically there are two HTTP protocols - a Dumb HTTP and a Smart HTTP.

The Smart HTTP requires CGI programming which can respond to `git push` as well.

I coded my version of GitHub with Dumb HTTP protocol (only `git clone` support without authentication) that just requires a basic HTTP Server serving from the `.git/` folder within a repository, with some minor tweaks, here: <a href="https://github.com/ovebepari/Git_Clone">GitHub Clone - Ovebepari</a>. Here are some screen-shots.

![Githubclone login](/post_images/2020/Mar/gitclone_one.png){:.center-image} <br>
![Githubclone dashboard](/post_images/2020/Mar/gitclone_two.png){:.center-image} <br>
![Githubclone a repo](/post_images/2020/Mar/gitclone_three.png){:.center-image} <br>
![Githubclone cloningdd](/post_images/2020/Mar/gitclone_four.png){:.center-image}
<center> <small>The clone button spawns a basic HTTP web server</small> </center> <br>

A full-fledged server that supports `git push` too would take a bit of CGI programming. Can't wait to get on to that as well.