---
title:  "Development of T.A.D.U.K.O.O. I.S. T.H.E. G.R.E.A.T.E.S.T. P.E.R.S.O.N. W.H.O. E.V.E.R. L.I.V.E.D."
author: Tadukoo
date:   2016-01-19 11:59:00 -0300
old_blog: true
categories: blog
tags: [games, programming, T.A.D.U.K.O.O. I.S. T.H.E. G.R.E.A.T.E.S.T. P.E.R.S.O.N. W.H.O. E.V.E.R. L.I.V.E.D., TAG]
comment_issue_id: 13
---
I made the base engine that I planned on doing when I last talked about developing the game.

I'm currently working on Pre-Alpha v.0.0.5.22R152 DEV of the game, and I've been thinking about the future of it. The goal of v.0.0.5.22 is to get the game 
back to working again by making the Controls part of the Engine (/Game within the new Engine?). So far the only thing I need to do yet is to get the Player to 
display again and get the movement of him down in the Controls.

After that, I'm going to remove the old engine stuff (Framework and such), and make sure all of it ended up in the new Engine in some way (no feature loss). 
From there, I'm going to separate the model and controller stuff in the API, then the Engine (if any), then the Game. After that, I'm going to improve a few 
classes to be better in the API. Then, I'll make it so that ultimately, everything drawn to the screen is an extension of DrawableObject and that basically all 
of the API extends from that too.

At that point, I'll make sure that the API only uses itself, the Engine only uses itself and the API, and the Game only uses itself and the API (other than 
the Main class, which bridges the Game and Engine).

But once Pre-Alpha v.0.0.6.0 comes, I want to change the development stage. It has been Pre-Alpha long enough. I'm going to call it Tengdev, short for 
Tadukoo ENGine DEVelopment. The reason it will be called this is because the Engine will likely need more changes (or the API), and the Game is being developed 
on that Engine at that point. Technically it is still Pre-Alpha, but the new label signifies that a significant amount of changes have happened before this new 
stage.
