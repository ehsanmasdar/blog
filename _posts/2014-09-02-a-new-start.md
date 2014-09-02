---
layout: post
title: "A new start - Welcome back to the work of node (and websockets)"
quote: A couple brave souls embark on the adventure of a 6 weeks.
image: /blog/media/2014-09-02-a-new-start/cover.jpg
video: false
---

#Hello World! (Again)
Welcome to my blog. This blog will be used to document the creation of <strong>Game Host</strong> (working title) an educational game ai creation platform which encourages students to write a simple client in their language of choice to play games. The purpose of the project is to write the sever side api to make the "magic" of connecting clients work for this, and we spent most of the week choosing our platform (nodejs, due to our previous experiences as a group) and thinking out the networking protocol, which I will discuss below.
## Platform of choice
We chose node because of its ease of setup, hosting and flexibility. I have worked with node before (as evidenced by this blog) and I find that it is great to use for almost and project requiring servers. We setup a basic [Express.js](http://expressjs.com/) server and then proceeded to discussing network protocol.
## Network Protocol/ API 
We wanted an api that would require the least work for clients to get connected, as our idea relies on a student being able to connect to the server using any language they could dream of. Here is the image of what we came up with:
{% include image.html url="/blog/media/2014-09-02-a-new-start/network.jpg" width="100%" description="Our (rough) sketch of the networking setup" %}
It relies on having two clients connect via [Websockets](http://en.wikipedia.org/wiki/WebSocket) a html 5 protocol for client-server communication. Once connected, the clients exchange ids, game lobby information, and board state information to sync. Their ais send moves to the server, which rejects or accepts the move based on the current turn, and game being played (cant move a pawn across the board in one move of chess, for example). Next week we hope to start working on websockets implementation, and prototyping a basic Tic-Tac-Toe game.
