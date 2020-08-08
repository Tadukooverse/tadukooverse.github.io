---
title:  "Java Look and Feel: Getting Started"
author: Tadukoo
date:   2020-05-03 20:46:00 -0300
old_blog: true
categories: blog
tags: 
- Java
- Journey
- Look and Feel
- programming
- Tutorial
comment_issue_id: 32
---
*This post is part of my Java Look and Feel Journey. See [this post]({% post_url 2020-05-03-java-look-and-feel-journey %}) for more details and table of contents.*

When I first started with the Java Look and Feel (L&F), I found that if you're making a fully unique Look and Feel, you'll want to extend BasicLookAndFeel (from the javax.swing.plaf.basic package). 
If you use BasicLookAndFeel though, you need to create literally everything else needed for the look and feel in your own custom classes. This is probably the end goal (for me at least), but doing 
this would take a long time, and it'd be easier to just extend an existing look and feel and modify it slowly over time, making sure each piece is modified correctly before moving on.

We'll be using the Metal Look and Feel for our new L&F, so we need to extend MetalLookAndFeel from the javax.swing.plaf.metal package. Because we're creating our own custom look and feel, we'll need to 
override getName(), getID(), and getDescription(). These can return whatever strings you want them to return since it's our custom L&F, but for mine, I'll be returning "Tadukoo" for name and ID, and 
"The Tadukoo Look and Feel" for description.

Also, we're going to override isNativeLookAndFeel to return false and isSupportedLookAndFeel to return true. isNativeLookAndFeel would return true if you're creating an L&F that is platform-dependent 
(e.g. only runs on Windows), and isSupportedLookAndFeel would return false if you're creating an L&F that's either platform-dependent or it requires some license agreement or something (basically you'd 
implement custom logic to return true in certain circumstances only). Note that these two methods already return these values in MetalLookAndFeel, but we're overriding them now since our ultimate goal 
is to create a full L&F, free from MetalLookAndFeel. Whenever we switch to extending BasicLookAndFeel, we'll need to override these methods, so we're doing it now to get it over with.

At this point, the class should look like this so far:

<script src="https://gist.github.com/Tadukoo/05cbc1e9480ab651574968a6a76f76cd.js"></script>

I've realized because of the nature of this project, we'll need to also create a program that displays the various components in order to demonstrate progress on our new look and feel. For this reason, 
I'll be making another tutorial in parallel with this one on how to setup components and layouts. I will be linking to the appropriate posts from that tutorial within this tutorial when relevant.

The other tutorial will basically add components as we need them for here, but this first version has a JLabel, JTextArea, and JButton. JButton is the only one relevant for a bit in this look & feel 
journey, so you could just make a simple program that displays a JButton for now. Basically for this first post, there's no visible difference between this and the MetalLookAndFeel. Next post for the 
Look & Feel I'll have the appropriate component tutorial available.