---
title:  "The Development of My Game"
author: Tadukoo
date:   2015-12-30 14:07:00 -0300
old_blog: true
categories: blog
tags: [games, programming, T.A.D.U.K.O.O. I.S. T.H.E. G.R.E.A.T.E.S.T. P.E.R.S.O.N. W.H.O. E.V.E.R. L.I.V.E.D.]
comment_issue_id: 5
---
The game has come a long way from the beginning until now. I ended up calling it "TAG" as a way to say it quickly. TAG came from the way I named the project 
folder in eclipse. I named it "TadukooAGame", because I already had "TadukooGame" and A was the first letter of the alphabet.

Back when I started on TAG, I had already wanted to make a game, I just didn't have an idea yet. I had looked up tutorials on making games, and I found one 
that essentially had the code and graphics in it for a moon lander game. What I did was I copied the code from that (by physically typing it), that way I'd 
be able to better understand it and read it as I go along. After that, I modified the game to be a better moon lander (in my opinion). I also changed the 
graphics to be in my style. That is what "TadukooGame" had become. I didn't claim the game as my own or share it anywhere, I simply used it to help me better 
understand programming. Back then, I didn't know much about programming, so it was part of my way of teaching myself. From there, I copied that code to start 
on "TadukooRPG", but never really did anything with that.

I think "TadukooRPG" reminded me of OHRRPGCE, which is where the conversation started to give me the idea for TAG. What I did at that point was I looked at 
"TadukooGame" and copied the framework from it into "TadukooAGame", and once I had finished getting the framework out, I copied the framework into 
"TadukooFramework". Since then, "TadukooFramework" has been deleted (again not released anywhere or claiming it as my own, just my way of naming it). I built 
TAG off of that framework from the start.

With the framework, I already had a playable game. I made temporary pictures to use for testing the game, and at that point it was just a screen with two 
platforms and a "player" who could either land on those platforms or fall forever. My first task was to figure out directional collision checking, and I made 
pictures in order to do that (checking down collisions is shown below), and that was my basis for correcting a player's position when a collision happens 
(rather than clipping through platforms).

![Checking Down Collision](/assets/down_collision.png)
Checking Down Collisions

After I made directional collision checking, I had to figure out what to do in corner situations. I'd figure out later that I left out a specific type of 
collision.

Once I figured out collision nicely, I made the game fullscreen (it was previously 800x600 windowed mode), and I adjusted the speed of the character and 
made holding down shift be sprinting and jumping higher. Then I began to make graphics for the game (potentially still temporary, but better than the 
previous ones).

Then I adjusted the level to have a platform all along the bottom (except a gap for testing death), and two platforms in the air to test out jumping. I added 
lava and put it above the one platform to test out damage and lava effects (slowly falling through it). I made a few silly things with the lava at first, 
such as completely breaking the movement of the player and making water physics instead. Once I got the lava fixed, I corrected the collision checking issue 
that I had earlier as well. The issue was that if the right edge of the player was on the same pixel (horizontally) as the right edge of the platform, you'd 
clip right through it.

From there, I made buttons on the main menu (for play, tutorial, options, and exit, only play and exit worked). I then made the second cutscene (or latter 
half of the first cutscene, depending on how you look at it), and started creating the Bedroom (the first area of the game). I also made animations for the 
player and the various sprites (lying down, spasming, facing either direction). I added dialog and the basics of interacting with objects. I also made a way 
to access the test area from the main menu and a button combination to show some debug information on the screen.

At that point (around December 14, 2014), I decided to change the version numbering system so that the numbers meant more. I made the next version as 
Pre-Alpha v.0.0.0.15R37, and the goal of v.0.0.1.0 as finishing the Bedroom and adding a sort of time system to it. V.0.0.1.0 came the very next day.

For v.0.0.2.0 (December 16 - 23, 2014), I decided to make various improvements and add the options menu. Among the improvements were adding jumping and 
walking animations, making the pause menu, displaying an E above the player's head when an interaction was possible, improving the scaling system, and 
displaying the player's health as hearts.

For v.0.0.3.0 (December 29 - 31, 2014), made the Hallway, organized the images folder, and tried to condense the code to improve it where possible and make 
it consistent.

For v.0.0.4.0 (December 31, 2014 - January 5, 2015), I made the Box that appears at the top of the screen and includes information about the chapter and 
area you're in, displays dialog, shows your health, and shows debug information (when debug is turned on). It would also show when you can interact with 
something.

For v.0.0.5.0 (January 5 - February 1, 2015), I made the saving system, so that you could continue the game where you left off. Also the font was improved 
and more widely used in the game at this point.

For v.0.0.6.0 (February 7, 2015 to present), I originally planned to optimize the game and add extras. Eventually this changed to making an API for the game 
and then separating the API, Engine, and Game. Due to this, I'm creating my own API and Engine at this point. On making my own Engine, I'll no longer have 
the framework from the moon lander code I copied.

The development of v.0.0.6.0 will be further discussed in other posts.
