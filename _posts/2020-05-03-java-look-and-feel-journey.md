---
title:  "Java Look and Feel Journey"
author: Tadukoo
date:   2020-05-03 20:45:00 -0300
old_blog: true
categories: blog
tags: 
- Components and Layouts
- Java
- Journey
- Look and Feel
- programming
- Tutorial
comment_issue_id: 31
---
I've been working on slowly creating my own API from the ground up (as opposed to [before]({% post_url 2015-12-31-the-flaws-of-developing-api-and-engine %}), where I had a functioning program and tried to separate out an API), 
and I've realized I'm still doing it wrong. I've been creating my own classes for various menu functionality (e.g. Button, Text input, etc.) because I didn't know much about using the default Java Swing components and how to 
customize the looks of them.

Long story short, for something at work I started to create a program with the default Java components (JTextField, JLabel, etc.) and I learned about Java's Look and Feel. Because of using this, I wanted to customize my own 
Look and Feel, but in my googling, I haven't found any good tutorials on how to do it. I'm ultimately finding bits and pieces of how to do it, and warnings that it's a massive undertaking. I have a history of wanting to program 
various projects that turn out to be massive undertakings, so this is nothing new to me, but I don't like the idea that some of the Java API is considered too difficult to customize.

Because of this, I've decided I'll create my own tutorial on how to create a custom look and feel in Java. Since it's a massive undertaking and the information seems to be somewhat scattered, this tutorial may be somewhat 
unconventional. It will end up being more of a journal of my journey to figure out how to do it moreso than it is a tutorial, at least at first. As I go, I'll likely make corrections or simplify/clarify certain parts of the 
tutorials as I learn the correct ways or practices to use this. This post will be updated as my journey progresses, and include 2 tables of contents (at least eventually). The first table of contents will be the most up-to-date 
version of the tutorial with any corrections, clarifications, and simplifications made up to that point. The latter table will be all the posts chronologically along in the journey. Note that because of this, some content may be 
duplicated or even triplicated, as the "journey" posts may be more informal and include anecdotes unnecessary for a tutorial, while the "tutorial" posts will be more concise and to the point on how you can create your own look 
and feel.

Note: While I will have a tutorial for how to create your own custom look and feel using the Java API, my goal will be to create my own API to make it simpler for others to create extensions. When I get to a point of releasing my 
own API, I'll include a separate tutorial for that.

<b>Note: Sometime soon, I will be removing the tables of contents from this post. I've created a page titled Java Programming that contains these tables of contents, and that page will maintain the links (so I don't have to keep 
updating an old post). I'll update this post when that happens, along with updating the appropriate links/headers on the various posts.</b>

### The Journey: The Quest to Build a Look & Feel
These posts detail my journey of building a Look & Feel and include anecdotes and other details that may not be necessary for you to know in building a look & feel. They also may include misinformation that'll be corrected 
in a later post (notes will be made in the original post linking to the corrections). This set of posts is primarily more like a journal of me working this out than an actual tutorial, which is why they're not under one of the 
"tutorial" sections.

1. [Getting Started]({% post_url 2020-05-03-java-look-and-feel-getting-started %}) - 5/3/2020
2. [Button Journey]({% post_url 2020-05-10-java-look-and-feel-button-journey %}) - 5/10/2020
3. [Building the Border Wall]({% post_url 2020-05-17-java-look-and-feel-building-border-wall %}) - 5/17/2020
4. [Customizability]({% post_url 2020-05-24-java-look-and-feel-customizability %}) - 5/24/2020
5. [Customizability 2: Electric Boogaloo]({% post_url 2020-5-31-java-look-and-feel-customizability-2 %}) - 5/31/2020
6. [Gradients]({% post_url 2020-06-07-java-look-feel-gradients %}) - 6/7/2020
7. [Tadukoo Util Placement]({% post_url 2020-06-14-java-look-feel-tadukoo-util-placement %}) - 6/14/2020
8. Make Paint Great Again - Coming 6/21/2020
9. TBD - Coming 6/28/2020

### The Tutorial: How to Do It Yourself in a More Clear Way
These posts are an actual tutorial on how to create your own custom look & feel from scratch. They're more formal than the journey posts, and will tell you in a more clear and concise way how to make a look & feel. Any 
misinformation will be corrected in the post itself, unlike the journey posts.

1. TBD - Coming Soon<

### Tadukoo Look and Feel Tutorial: Using My L&F to Work for You
My goal in building a look & feel is to create a version that is easily customizable. The Synth Look & Feel is customizable via xml or programmatically, but it doesn't seem to be as customizable as I plan the Tadukoo 
Look & Feel (working title) to be. These posts will teach you how to use my look & feel for your own purposes (once my look & feel is released at least).

1. TBD - Coming Eventually (maybe sooner than I think due to already having a basic plan for it)

### Components & Layouts: Another Tutorial about what can be shown
Since we're dealing with changing the Look & Feel of the components, we'll need to actually create components and put them in a layout in order to show what our Look & Feel actually looks and feels like. This is another 
tutorial series that simply creates a small program that shows off all of the available components and puts them in a nice layout.

1. [Labels, Text Fields, and Buttons! Oh My!]({% post_url 2020-05-10-java-components-layouts-labels-text %}) - 5/10/2020
2. TBD - Coming Soon
