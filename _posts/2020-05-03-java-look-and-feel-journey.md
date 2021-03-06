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
- Programming
- Tutorial
comment_issue_id: 31
---
I've been working on slowly creating my own API from the ground up (as opposed to [before](https://tadukoo.github.io/blog/2015/12/31/the-flaws-of-developing-api-and-engine.html), where I had a functioning program and tried 
to separate out an API), and I've realized I'm still doing it wrong. I've been creating my own classes for various menu functionality (e.g. Button, Text input, etc.) because I didn't know much about using the default 
Java Swing components and how to customize the looks of them.

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

### The Journey: The Quest to Build a Look & Feel
These posts detail my journey of building a Look & Feel and include anecdotes and other details that may not be necessary for you to know in building a look & feel. They also may include misinformation that'll be corrected 
in a later post (notes will be made in the original post linking to the corrections). This set of posts is primarily more like a journal of me working this out than an actual tutorial, which is why they're not under one of the 
"tutorial" sections.

{% assign lookAndFeelPosts = site.posts | where:"series", "Tadukoo Look & Feel Journey" | sort:"index" %}
{% for lookAndFeelPost in lookAndFeelPosts %}{{lookAndFeelPost.index}}. [{{lookAndFeelPost.title | remove:"Java Look and Feel: " | remove:"Java Look & Feel: "}}]({{lookAndFeelPost.url}}) - 
{{lookAndFeelPost.date | date_to_string}}
{% endfor %}

### The Tutorial: How to Do It Yourself in a More Clear Way
These posts are an actual tutorial on how to create your own custom look & feel from scratch. They're more formal than the journey posts, and will tell you in a more clear and concise way how to make a look & feel. Any 
misinformation will be corrected in the post itself, unlike the journey posts.

1. TBD - Coming Soon

### Tadukoo Look and Feel Tutorial: Using My L&F to Work for You
My goal in building a look & feel is to create a version that is easily customizable. The Synth Look & Feel is customizable via xml or programmatically, but it doesn't seem to be as customizable as I plan the Tadukoo 
Look & Feel (working title) to be. These posts will teach you how to use my look & feel for your own purposes (once my look & feel is released at least).

1. TBD - Coming Eventually (maybe sooner than I think due to already having a basic plan for it)

### Components & Layouts: Another Tutorial about what can be shown
Since we're dealing with changing the Look & Feel of the components, we'll need to actually create components and put them in a layout in order to show what our Look & Feel actually looks and feels like. This is another 
tutorial series that simply creates a small program that shows off all of the available components and puts them in a nice layout.

{% assign componentsAndLayoutsPosts = site.posts | where:"series", "Java Components & Layouts" | sort:"index" %}
{% for componentsAndLayoutsPost in componentsAndLayoutsPosts %}{{componentsAndLayoutsPost.index}}. [{{componentsAndLayoutsPost.title | remove:"Java Components & Layouts: "}}]({{componentsAndLayoutsPost.url}}) - 
{{componentsAndLayoutsPost.date | date_to_string}}
{% endfor %}
