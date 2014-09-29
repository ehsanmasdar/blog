---
layout: post
title: "Websockets-Week 3"
quote: Modularization
image: /blog/media/2014-09-28-websockets-week-3/header.jpg
video: false
---

#Week in review
This week we worked a lot on modularization of the server and client to support multiple games. After completing our prototype of Tic-Tac-Toe we had to rework many of the systems so that they would scale to multiple games. We also developed and finalized the second game we would write, and worked on user registration
##Modularization
To modularize the code we had to completely rework the server side JavaScript. We created a class based system for loading games, where all of the code for one game goes in one file. This file contains methods for initial setup, handling moves, and controls what user sees what data on the game board. We also had to implement a modularized system for matchmaking, where a user could sign up for multiple games or game modes and the matchmaking system would match them with whichever system is available first.
##Registration
Another thing we started working on this week was formal user registration- that is, a user could browse to a page to receive a UUID(Unique Universal ID) that was bound to them by a password. This UUID is required to be send with every request to the server, ensuring that no user can be impersonated on the site.
##Dots and Boxes
Finally, we started work on the game "Dots and Boxes" which has users placing lines and trying to box off the corner of a grid. This represents a much harder game to create a "perfect" ai for than Tic-Tac-Toe, which is why we felt it was a good game to write next.
