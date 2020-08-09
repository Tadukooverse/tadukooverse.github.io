---
title:  "Java Look & Feel: Make Paint Great Again"
author: Tadukoo
date:   2020-08-09 16:37:00 -0300
series: "Tadukoo Look & Feel Journey"
index: 8
categories: blog
tags: 
- Java
- Journey
- Look and Feel
- programming
- Tutorial
comment_issue_id: 42
---
*This post is part of my Java Look and Feel Journey. See [this post]({% post_url 2020-05-03-java-look-and-feel-journey %}) for more details and table of contents (and to find a proper tutorial when it's available).*

*That post will also guide you to another tutorial on using Java's Components & Layouts, so you can make a program to actually see the Look & Feel changes. At this point in the journey, you'd only need the 
[first post]({% post_url 2020-05-10-java-components-layouts-labels-text %}), to have a button on screen to see the changes to it, but going further in that series is fine too.*

*This is part 8 of the "Journey" posts. Follow this link for part 1: [Getting Started]({% post_url 2020-05-03-java-look-and-feel-getting-started %}) or this link for the previous part: 
[7. Tadukoo Util Placement]({% post_url 2020-06-14-java-look-feel-tadukoo-util-placement %})*

Apparently I dumped the old "Make Paint Great Again" post in transferring my blog posts over to this new blog. I hadn't posted it over on blogger yet, but I had definitely written it up and created the commit in 
Tadukoo Look & Feel for it. Unfortunately, I deleted the old blogger drafts and posts at this point, so I'm writing this much later after the fact.

The goal to "make paint great again" was to make it so that all the paint/color/gradient UI resources would exist through a standard interface so that I wouldn't have to be checking if I was given a paint, gradient, 
or simple color. That's what PaintUIResource is for. It's now an interface that extends UIResource (because that's how you do it in Java to let it know it's a UIResource). The main method in the interface that's 
relevant is getPaint(Dimension size), which returns a Paint object to use in painting. The dimensions are given because gradients require a size to determine where certain points are.

<script src="https://gist.github.com/Tadukoo/8b8612ceca3530bfabf0b54abde2497d.js"></script>

getColorUIResource() and getMetalGradientList() exist so that I can still support component UI objects from other Look & Feels (e.g. MetalLookAndFeel). A lot of the Look & Feel UI components require a plain color, 
which is what the ColorUIResource is for. MetalLookAndFeel requires a stupid List<Object> for certain Gradients it does, which I ranted about [previously]({% post_url 2020-06-07-java-look-feel-gradients %}). The 
getMetalGradientList() method is deprecated because I absolutely hate it, and its only purpose is to be used for supporting the Metal Look & Feel components. It should never be used for anything else, as my 
gradient system (which I'll discuss shortly) is better.

So now that I had a PaintUIResource interface, I had to create a new class to handle basic colors under this interface. Hence ColorPaintUIResource. It extends ColorUIResource (and initializes itself with one, or 
with some parameters to create a Color. For getPaint and getColorUIResource it returns itself (since it is itself a Paint and ColorUIResource). For getMetalGradientList it sets up the List<Object> in a way so 
that it just produces a solid color anyway (by making all 3 colors itself).

<script src="https://gist.github.com/Tadukoo/c889941972b24714fd66c4a56f1eba42.js"></script>

After this, I modified my GradientUIResource class (static within Gradient) to be a PaintUIResource properly, which just meant moving the getMetalGradientList() method into it instead of the Gradient itself, and 
to add the new getColorUIResource method, which just uses the first color of the Gradient.

<script src="https://gist.github.com/Tadukoo/2159847b15659722fcfd4da841542332.js"></script>

TadukooTheme underwent massive changes, as I no longer had to have a ton of methods for each color resource in it, just one to handle a PaintUIResource for each unique color/paint/gradient. So it really slimmed 
down that class:

<script src="https://gist.github.com/Tadukoo/1fa1ca4298fcb9cfd675695923b8818f.js"></script>

In TadukooLookAndFeel, I changed the initComponentDefaults method so it will set the new PaintUIResources for use by it, and also set the proper old UIResources in case we're going to use some of the component 
UI classes from other Look & Feels. This provides support for using any of them:

<script src="https://gist.github.com/Tadukoo/d4f65d06d9fb4767ee1aa075ae4ab35c.js"></script>

And finally for this change, I modified TadukooButtonUI so that it will use the new PaintUIResource instead of trying to use the old select ColorUIResource and/or Metal's gradient list:

<script src="https://gist.github.com/Tadukoo/960aea7a7c882b3c8d2bb4d2b91a8fb8.js"></script>

[Here's a link to the GitHub commit](https://github.com/Tadukoo/TadukooUtil/commit/1b6a7996b0c80da661a4802ade30f829f7ad13fc) for the changes made in this post.

Next time, we'll be dealing more with shapes of components. Also next time should be a more detailed/interesting post, since I won't be writing it months after the fact.
