---
title:  "The Development of Pre-Alpha v.0.0.6.0"
author: Tadukoo
date:   2015-12-30 15:33:00 -0300
old_blog: true
categories: blog
tags: [games, programming, T.A.D.U.K.O.O. I.S. T.H.E. G.R.E.A.T.E.S.T. P.E.R.S.O.N. W.H.O. E.V.E.R. L.I.V.E.D.]
comment_issue_id: 6
---
The goal of v.0.0.6.0 started out innocent enough: Make extras and optimize the game. (Note: The extras were planned to be tic-tac-toe, snake, and moon 
lander). Eventually, the goal expanded to include adding sounds, a player select menu, being able to "hack" objects using codes for special easter eggs 
(or in some cases to progress the game perhaps?), achievements, improving the debugging stuff, improving the save system, making the controls configurable, 
making animations for going between areas, and having the areas mapped out in text files as a grid.

So in the first revision (0.0.5.1R99), I added the basics of the Sound system, adding the background music and a jumping sound (temporary for now). The next 
three updates were very long, making numerous changes in order to make it so the R number wasn't updated as often (I thought it was too much at the time). 
In R101 and 102 I decided that the versions working towards v.0.0.6.0 should have "DEV" in the title as well to show they're progressing towards it.

In making v.0.0.5.5R103 DEV, I decided that the R number can change a lot, but the base version number shouldn't. I decided that there would be minor goals 
to change the base version number, and that only updates working towards those (before completion) would have "DEV" in the title.

Because of this, I had to pick a goal for v.0.0.5.5. By this point, I was already working on an API, as that came about from the optimization idea, and the 
goal of v.0.0.6.0 was changed to separating API, Engine, and Game. The goal of v.0.0.5.5 became implementing the interact functions in my 
InteractableObjects. Basically I had set up "InteractableObject" as an API class, but hadn't used the interact function defined in it, so it wasn't much 
better than a generic object.

From that point, I removed the extras stuff I had put in (as I decided that if extras are put in, they're for much later). I then improved the Object API I 
was developing. At that point, I made an Event API, for use in cutscenes and interactions. I improved this Event API until I was satisfied with it, and then 
moved on to Location API for the Chapters and Areas. Once I had finished the Location API, I made the collision class into an API class, and made a Game API 
class. I also made an API for the Box.

By this point, I had a nice API going, but no engine yet (at least the engine was combined with the game at this point). I decided to start on making a 
Drawing Engine. I didn't realize how major a change the Drawing Engine would bring to the code, so I was surprised when I edited the vast majority of the 
classes. Eventually I settled on just having a partial Draw Engine, as I realized the anniversary of R1 was coming up.

I decided to make a special anniversary edition on the actual anniversary, where I would re-add the Test area (having test areas would help me out anyway) 
and add a few other special things. At this point, I had to make a new Object API class for the Lava to use (I had a Block class and an InteractableObject 
class, but Lava was a combination of both). I also had to fix the save system at this point, as it broke from some API changes.

After the anniversary, I decided on making GameState API, so that I could have a general GameStateClass that the base engine (when it's made) could use for 
running the current game state. In making the GameState API, I realized that it would be better to make the base engine before I finish the GameState API or 
other API and Engine sections.

So that's where I'm at now. I'm working on the base engine, as I've learned it's easier to work top-down than bottom-up. In another post (probably tomorrow), 
I'll write about how I learned this and why it makes sense. As a note, in making my own engine, I'll be removing the framework that came from the moon lander 
game upon which I built this game.
