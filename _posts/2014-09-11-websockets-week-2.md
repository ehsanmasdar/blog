---
layout: post
title: "Work on GameHost: Our second week with websockets"
quote: It works!... kinda
image: /blog/media/2014-09-11-websockets-week-2/tictactoe.png
video: false
---

#Week in review
This week was marked by a bunch of client and server side development to get a basic implementation of Tic-Tac-Toe working. This involved writing systems to identify users, store state information, and organize game sessions. 
##User/Room Identification
One of the largest accomplishments of this week was the user and room identifications system. Each user is assigned a random, unique id by the server which is used to identify them during a game session (and eventually will be persistent across the platform). Each room is also assigned an internal id, but displays a more user friendly and reusable name to the client.
##Game Creation
Another large focus of the week was implementing a basic Tic-Tac-Toe game in javascript to test our platform framework on. While the system is not modularized yet and is instead heavily tied to the custom Tic-Tac-Toe game, it serves as a point from which we can rapidly prototype systems. We picked Tic-Tac-Toe as our first game to develop for the platform due to it's simplicity-not just from a player standpoint, but also because the field is static and only changes upon user interaction. We hope to implement that require more complex networking, such as pong, in the next couple weeks. 
