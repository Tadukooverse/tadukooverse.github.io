---
title:  "Java Look and Feel: Button Journey"
author: Tadukoo
date:   2020-05-10 14:49:00 -0300
old_blog: true
series: "Tadukoo Look & Feel Journey"
index: 2
categories: blog
tags: 
- Java
- Journey
- Look and Feel
- Programming
- Tutorial
comment_issue_id: 33
---
*This post is part of my Java Look and Feel Journey. See [this post]({% post_url 2020-05-03-java-look-and-feel-journey %}) for more details and table of contents (and to find a proper tutorial 
when it's available). That post will also guide you to another tutorial on using Java's Components & Layouts, so you can make a program to actually see the Look & Feel changes. At this point in 
the journey, you'd only need the <a href="http://tadukoo.blogspot.com/2020/05/java-components-layouts-labels-text.html">first post</a>, to have a button on screen to see the changes to it.*

*This is part 2 of the "Journey" posts. Follow this link for part 1: [Getting Started]({% post_url 2020-05-03-java-look-and-feel-getting-started %})*

With the Look and Feel, the first thing I decided to do was to change the style of a button. I wanted to make it look like this (which comes from previous projects I've worked on where I made 
custom buttons before fully knowing about JButton):

![Green Button](/assets/images/tinyGreen.png)

Basically it's a rectangle, but the top right and bottom left corners have triangles cut out (as you can obviously see). When I made this kind of button in my own projects in the past, I had a few 
preset sizes and stored images for them in a resources folder. In hindsight, that's obviously not the best way to do it.

So to start making changes, I decided to make a custom ButtonUI class. I overrode paintFocus and copied the MetalLookAndFeel version, but changed the color to yellow. That did nothing, so I overrode 
paintButtonPressed, again changing it to paint as yellow. Again, no change. At first, I was trying to change the default UI class via the TadukooLookAndFeel defaults, but I started setting the ui 
directly on the button via setUI with no results either. Turns out that the ui components have a createUI function that is used to instantiate new UI's. Since TadukooButtonUI didn't have this method, 
it was going to the MetalButtonUI version, which instantiated a new MetalButtonUI instance.

In making the TadukooButtonUI, I tried to basically copy the createUI method that MetalButtonUI does, but that method uses sun.awt.AppContext, which is not pure Java. For that reason, we can't fully 
replicate it (without the problems that come with not using pure Java, which are basically likelihood to break and/or loss of cross-platform compatibility). BasicButtonUI does the same thing that we're 
unable to copy. ButtonUI doesn't have implemented methods, and I'm assuming other LookAndFeels will have the same type of method that we can't copy without issues.

Once I got this working, I figured out that the borders aren't controlled in the ButtonUI class. Due to this, we can't fully draw the cut corners we want. But before we go to that part of the journey, 
let me share the TadukooButtonUI class I made. With this version, when you click it, you can see that the gradient switches from vertical to horizontal and the corners are cut (when not clicked, the 
gradient still includes the corners).

<script src="https://gist.github.com/Tadukoo/42cc30f33a7e39c319862fc65311c9a9.js"></script>

Changes will be made to this in the future, but this is what I have right now in this journey. Although, this will not work unless you also have the Shaped interface. Whoops. Well, we'll go there next 
instead of going to the Borders. Just note (if you care) that the Borders happened before the TadukooButtonUI (though the journey documented here is already out of order then anyway).

To make the cut corners, we created an interface called Shaped. It has one method called getShape that takes in x, y, width, height, and returns a Polygon. Here's the code for it:

<script src="https://gist.github.com/Tadukoo/14bed5adcadcc60775fdedeb6a84759f.js"></script>

After that, we make an interface that extends it called TadukooShape. TadukooShape overrides the getShape method from Shaped and creates a default implementation of it that creates a rectangle with those 
2 cut corners. The reason it's in 1 pixel from some edges is because using a brush size of 2 for drawing the border works the way we want this way, and not if it's exactly against the edges (not 100% sure 
why, maybe we'll do this better in the future). Here's the TadukooShape code:

<script src="https://gist.github.com/Tadukoo/140afe94e04b316fc65f1f68b391ec8b.js"></script>

From there, whatever components where we want to include this shape, we just need to have it implement TadukooShape and it'll have those cut corners. Honestly, I'm not very happy with this method and will 
likely change it later, but this is how it is for now. Perhaps it'd be better to make a util class that holds various shape methods?

In the middle of all this, we handled the border to see that it worked correctly, so that's what we'll tackle in the next post since this one is long enough already (and since as of writing this, the border 
logic isn't fully cleaned up anyway). [Click here for the next part]({% post_url 2020-05-17-java-look-and-feel-building-border-wall %})
