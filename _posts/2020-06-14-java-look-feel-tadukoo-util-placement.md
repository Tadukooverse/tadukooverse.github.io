---
title:  "Java Look & Feel: Tadukoo Util Placement"
author: Tadukoo
date:   2020-06-14 15:37:00 -0300
old_blog: true
series: "Tadukoo Look & Feel Journey"
index: 7
categories: blog
tags: 
- Java
- Journey
- Look and Feel
- programming
- Tutorial
comment_issue_id: 39
---
*This post is part of my Java Look and Feel Journey. See [this post]({% post_url 2020-05-03-java-look-and-feel-journey %}) for more details and table of contents (and to find a proper tutorial when it's available).*

*That post will also guide you to another tutorial on using Java's Components & Layouts, so you can make a program to actually see the Look & Feel changes. At this point in the journey, you'd only need the 
[first post]({% post_url 2020-05-10-java-components-layouts-labels-text %}), to have a button on screen to see the changes to it, but going further in that series is fine too.*

*This is part 7 of the "Journey" posts. Follow this link for part 1: [Getting Started]({% post_url 2020-05-03-java-look-and-feel-getting-started %}) or this link for the previous part: 
[6. Gradients]({% post_url 2020-06-07-java-look-feel-gradients %})*

Last time I said I'd be moving the Tadukoo Look & Feel to Tadukoo Util. First of all, I had to commit FloatUtil to it, because that was just local so far (not a big deal). I decided to merge all the branches together, 
as they were mostly separate for Tadukoo View, which will be deprecated now. Tadukoo View is a project I was working on to make my own stuff to display to the screen (buttons, text input prompts, etc.). Some of the 
stuff in it may be useful still, but the majority of it isn't at this point, with me finally switching to using Java's default components instead. I'll likely remake a new view package later for some of the functionality, 
but for now it's all deprecated in favor of default Java.

So I'm making a separate project called OldTadukooUtil, for storing deprecated modules. I'm also renaming TadukooView to OldTadukooView and renaming the packages in it to have view-old. This is because to some extent I 
would like to make a new View module, just in a different way. Doing this allows me to reuse the package and module names (and even the class names, as they'll be in a different package now). As a note, both TadukooUtil 
and OldTadukooUtil are being released under the MIT license. [This commit](https://github.com/Tadukoo/TadukooUtil/commit/4539c5c7f893c1746fb76d550cfe757ae9a0d393) contains all the Look & Feel work so far (as of last post).

Now that Tadukoo View's out of the picture, I'm moving Tadukoo Look & Feel over, but I'm splitting it into multiple packages. At first, I was thinking of splitting it into multiple modules, but I realized that without the 
Look & Feel, the Components wouldn't be able to be used anyway. Note: My idea had been to separate it into Tadukoo Look & Feel and Tadukoo Components at the least.

I'm making a new package called com.gmail.realtadukoo.components and moving Shaped, TadukooShape, and TadukooButton into it. Also making a subpackage under lookandfeel called componentui, which currently will just have 
TadukooButtonUI. Another subpackage called paintui will contain PaintUIResource and Gradient (and some changes will be made in that package next time). TadukooBorder doesn't feel like it belongs where it is, but it also 
doesn't feel like it deserves its own package. Perhaps at some point we'll make more borders that mimic the existing borders, but allowing shapes like TadukooBorder currently does.

To see the changes made with this version, check out [this commit](https://github.com/Tadukoo/TadukooUtil/commit/4bd17838ce8d548e3022cc1e2a80caab1c724ced)

Next time will be more about the gradient and paint stuff.
