---
title:  "Java Look and Feel: Building the Border Wall"
author: Tadukoo
date:   2020-05-17 10:15:00 -0300
old_blog: true
series: "Tadukoo Look & Feel Journey"
index: 3
categories: blog
tags: 
- Java
- Journey
- Look and Feel
- Programming
- Tutorial
comment_issue_id: 34
---
*This post is part of my Java Look and Feel Journey. See [this post]({% post_url 2020-05-03-java-look-and-feel-journey %})for more details and table of contents (and to find a proper tutorial when it's available).*

*That post will also guide you to another tutorial on using Java's Components & Layouts, so you can make a program to actually see the Look & Feel changes. At this point in the journey, you'd only need the
[first post]({% post_url 2020-05-10-java-components-layouts-labels-text %}), to have a button on screen to see the changes to it, but going further in that series is fine too.*

*This is part 3 of the "Journey" posts. Follow this link for part 1: [Getting Started]({% post_url 2020-05-03-java-look-and-feel-getting-started %}) or this link for the previous part: 
[2. Button Journey]({% post_url 2020-05-10-java-look-and-feel-button-journey %})*

Okay, so it's not exactly a wall, but we're talking about making the border for the button now, and hopefully by extension all of the components.

I'm calling it TadukooBorder at the moment, but the name will likely change later. I started working on the border before finishing the button changes, so I had a rectangular button coloring with a border that ignored two 
of the colored corners when I finished this. It's still like that based on the previous code until you click the button (at which point the coloring no longer does those corners because we changed it).

Anyway, at first I was creating the polygon in the paint method instead of having the button do it for me. It was the first spot to get the shape, before the button itself even had it. But now that the button does have it, 
we can do something similar to what TadukooButtonUI does to grab the shape to be drawn. This time we're doing a draw instead of a fill though. This is also where we set the brush size to 2 and had to move the polygon 1 pixel 
from some edges. We set the border insets as 10 pixels on every side because that's the size the cut corners take up (a 10x10 space in those corners).

Metal Look & Feel stores all their borders into one class, but I don't think I'll be doing that with my L&F. Here's what the TadukooBorder looks like so far:

<script src="https://gist.github.com/Tadukoo/babd8186faf03541dbcca4bf1dca9e7b.js"></script>

Something I don't think I went into detail on was how to set the default button ui in the previous post. You can just use the button object's setUI method for it instead, but for the L&F you should set it as the default 
instead. The same applies to the button's border. To set both, you need to add information to the UIDefaults table. In Metal L&F (which we are currently extending), the UI defaults (e.g. ButtonUI, etc.) are set via 
initClassDefaults and you use the full classpath to the class you want to use. The component settings (border, etc.) are set via initComponentDefaults and in the case of the border, you send an actual instance of the border 
class. Here's what this looks like for us:

<script src="https://gist.github.com/Tadukoo/3a947364be5e56c5b7c13ba55d5af392.js"></script>

And [here's a link](https://gist.github.com/Tadukoo/07276fc7f2b6e01bcd349663388abec6) to the Tadukoo Look & Feel classes we have so far (for reference purposes)

[Next time]({% post_url 2020-05-24-java-look-and-feel-customizability %}), we'll be reworking some of this to start on making it more customizable (and probably work on improving the Shaped stuff and improving the 
button ui and border code).
