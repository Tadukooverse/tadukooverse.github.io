---
title:  "The Flaws of Developing an API and Engine Bottom-Up Rather than Top-Down"
author: Tadukoo
date:   2015-12-31 12:08:00 -0300
old_blog: true
categories: blog
tags: [games, programming, T.A.D.U.K.O.O. I.S. T.H.E. G.R.E.A.T.E.S.T. P.E.R.S.O.N. W.H.O. E.V.E.R. L.I.V.E.D.]
comment_issue_id: 8
---
When I first set out to develop an API for my game, I figured it wouldn't be that hard. I wasn't even thinking about separating the engine as well. When I 
realized I wanted to separate the engine, I thought I could just continue developing the API and the engine would drop out of it.

But it's not that simple. See, first I started with an Object API, making a TangibleObject upon which all in-game objects are built off of. Then I made the 
Event API to go along with the InteractableObjects in the Object API, and I had to change things in the Game/Engine mixture so that the Events would properly 
happen. Then I made Location API, which further affected the Game/Engine mixture, forcing a Game API class before I was ready for one.

At that point, I decided I'd make a Drawing Engine. As I made the Drawing Engine, I realized that every single API class had to be changed to fit the Drawing 
Engine and a new base Object API class had to be made (DrawableObject). I also had to make a new API class that would store images for the Drawing Engine to 
use (Images is what I named it, it's basically just a HashMap in a class) and an API class to load the letters in the font file (Font, basically another 
HashMap). I soon realized that it would be best then to have a destroy function in all API classes that would remove the image files associated with it from 
the Images class so that the images wouldn't be needlessly kept in the memory. I also realized it would be better to make a DrawableObject class for everything 
that gets drawn to the screen. Due to this, I stopped working on the Drawing Engine at that point.

I then moved to GameState API. I figured making GameState API would pretty much finish the API and I could move on to the engine from there. I was wrong. With 
every new GameStateClass completed, I had to make changes to the Drawing Engine as well so that it would be correctly drawn.

Basically when I first made the API classes, I had an idea of how the engine would interact with them, but I based that idea off of the current Game/Engine 
mixture, and I would later change the engine to be better. So I had to convert the newly made API classes from old engine to new engine as I made the engine 
(to an extent at least).

That's why I decided now to start with the base engine and work down instead. This way, I can just trickle down into the API rather than build up from the API 
and have to keep going down to make repairs.

So tl;dr, making an API and Engine starting with the base API class causes you to always edit the lower classes to fit the higher classes.
