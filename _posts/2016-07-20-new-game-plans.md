---
title:  "New Game Plans"
author: Tadukoo
date:   2016-07-20 14:40:00 -0300
old_blog: true
categories: blog
tags: [API, engine, games, programming, T.A.D.U.K.O.O. I.S. T.H.E. G.R.E.A.T.E.S.T. P.E.R.S.O.N. W.H.O. E.V.E.R. L.I.V.E.D., Tadukoo RPGs, TAG]
comment_issue_id: 22
---
This post is to talk about my current plans for games. I'll start by going over the plan for TAG and any changes to it, then into the other games, and a 
little bit about the current API and Engine plans.

<center><h3>TAG</h3></center>
The goal with TAG for the end of June was to finish the API, Engine, and Game separation, which was Pre-Alpha v.0.0.6.0 of the game. I did separate them, 
but the meaning of that changed. The original idea was that the API and Engine would be completed (for now at least), which did not happen. There are about 
20 changes to the API and 3 changes to the Engine that I'd like to make in order to complete them (when I say complete, I mean get them to a point I'm 
comfortable with for now, there will of course be more changes in the future). I will consider the API and Engine to be in Beta when I get them to that point.

Since v.0.0.6.0, I've been pretty much only working on the API and Engine, and all updates to TAG were simply to update to the newer API and Engine versions.

The next goal is for Prologue Area Completion (v.0.0.7.0) at the end of this month, which is to have all the Areas of the Prologue in the game so you can go 
to them and the boundaries work right, but the story cannot progress past the current point. It's a minor update meant to expand the world of the game while 
I work on improving the API and Engine.

v.0.0.7.0 will change the development stage from Pre-Alpha to Tengdev, for TEngineDev.

The rest of the plans with TAG from <a href="{{ site.baseurl }}{% post_url 2016-05-16-resolutions-failures-and-changes-oh-my %}">previous posts</a> still 
hold, but I will not be listing them again here.

<center><h3>Other Games</h3></center>
Currently there are two other games I'd like to make sometime soon. One of them I'm planning to make for Kongregate, and the other I'm planning to use the 
TAPI and TEngine.

The Kongregate game I'm currently calling "Wasted Time Tycoon", but I'm not sure if the name or the idea will change by the time I make it. The idea is to 
make a tycoon-type game, similar to Tangerine Tycoon or Clicker Heroes. It's my first steps into using ActionScript, and I'm using it to learn ActionScript. 
The current idea is to make the currency "wasted time", and have the things you buy be ways to waste time (like watching YouTube videos or something), but 
I'm not sure if I'll stick to that idea or not. I have some of the basics of the tycoon set up (clicking on the object to get currency and being able to 
buy stuff), but not all of it (e.g. the stuff you can buy doesn't automatically get currency for you).

The TAPI and TEngine game I'm planning is similar to Pokemon. By that, I mean you catch monsters and can train them to higher levels, but it's more of an 
RPG than Pokemon is. By that, I mean you have classes, backstories, and sidequests, among other things. Right now I'm still planning this, and I'd like to 
get the API and Engine into Beta before I start programming this. Currently what I have planned is some of the backstory and classes. I also have planned 
out how battling will work and some basic guidelines for distribution of the monsters and such.

<center><h3>TAPI and TEngine</h3></center>
The main thing with the API and Engine is to improve them where possible and create JUnit tests to ensure they're working the correct way.

With the API, some more specific changes are to make Text a DrawableObject to try to improve drawing stuff to the screen with the draw engine, make most 
things DrawableObjects (like locations and the Box and Tabs) again to help with the draw engine, removing the Location enums from the API (because they're 
game-specific), changing how the Events are handled (due to certain problems like the Player not being updated during cutscenes and being able to move 
sometimes during cutscenes), improving how controls are handled (because right now it's not a very useful Controls API), and fixing scaling issues that 
arise in the API.

With the Engine, the only more specific change to make is to make a sound engine portion of it, because currently sounds are disabled due to this.
