---
title:  "Java Look and Feel: Customizability"
author: Tadukoo
date:   2020-05-24 14:24:00 -0300
old_blog: true
series: "Tadukoo Look & Feel Journey"
index: 4
categories: blog
tags: 
- Java
- Journey
- Look and Feel
- Programming
- Tutorial
comment_issue_id: 36
---
*This post is part of my Java Look and Feel Journey. See [this post]({% post_url 2020-05-03-java-look-and-feel-journey %}) for more details and table of contents (and to find a proper tutorial when it's available).*

*That post will also guide you to another tutorial on using Java's Components & Layouts, so you can make a program to actually see the Look & Feel changes. At this point in the journey, you'd only need the 
[first post]({% post_url 2020-05-10-java-components-layouts-labels-text %}), to have a button on screen to see the changes to it, but going further in that series is fine too.*

*This is part 4 of the "Journey" posts. Follow this link for part 1: [Getting Started]({% post_url 2020-05-03-java-look-and-feel-getting-started %}) or this link for the previous part: 
[3. Building the Border Wall]({% post_url 2020-05-17-java-look-and-feel-building-border-wall %})

When working on making a look and feel, one of the first things I looked at was the MetalTheme. I'm not sure why I skipped over it in these journey posts, but in actually using it, I decided from the start I'd be 
making my own theme. So with this post, we'll start making our own TadukooTheme and using it in TadukooLookAndFeel. We're also going to include more information in TadukooTheme than what's included in MetalTheme.

First of all, TadukooTheme will have a builder in it. Later, we'll be creating a factory for the default themes that simply calls the builders to create them. We're going to have the builder default to using our 
TadukooButtonUI as the ButtonUI class (Class&lt;? extends ButtonUI&gt;). The reason we're taking in a Class is to make it simpler to use this builder without messing up (we control turning the class into the canonical 
class name, instead of allowing people to enter in a manual class name with mistakes).

We'll also store 2 AbstractBorders. One is the default (to use for all other unspecified borders), and the other is specifically for button borders. The button border defaults to null in this, and in the build method 
we check for null to set it to the default border (which is set to a new TadukooBorder by default). Here's what the builder class looks like after these changes (including an empty error check currently and the proper 
method to instantiate a TadukooTheme for the changes to it below):

<script src="https://gist.github.com/Tadukoo/1011346544113983890ba3f1451829ee.js"></script>

Now I personally put the builders in the same class as the actual class they're building, but you don't need to of course. In TadukooTheme we're storing the canonical class name of the ButtonUI to be used, and we're 
storing an actual instance of an AbstractBorder. The reason for doing this is that it's the way these items already work. I'm also going to be adding getters for these methods to be called in the Tadukoo Look & Feel 
class itself for setting these variables. I'm not adding setters, because these values aren't to be modified later (and doing so wouldn't really make a difference without also calling a L&F method to actually reset the 
defaults in the UIDefaults object). If for some reason you do want to make changes and reset the defaults later in the program, you should keep an instance of the builder class and just change the variables on that and 
recall the build method when you want to create the modified version. Anyway, here's the TadukooTheme class now (note that mine includes the TadukooThemeBuilder class which you may include outside instead):

<script src="https://gist.github.com/Tadukoo/8e10c780d30848f7ef0cd886d875f9ea.js"></script>

Before we get to modifying TadukooLookAndFeel, I'm going to make the TadukooThemeFactory. For now, it'll have 6 methods. These methods will be createDefaultTheme, defaultThemeBuilder, createMetalTheme, metalThemeBuilder, 
createBasicTheme, and basicThemeBuilder. The three builder methods will return a TadukooThemeBuilder object setup with the defaults for that type of theme, and the create methods will just go one step further and fully 
build those themes. The point of using just the plain Metal theme or Basic theme is... well right now there's no real purpose other than to prove multiple themes work I guess, but maybe in the future at some point there'll 
be more reason? Maybe I'll end up creating my own components that have unique component ui's that metal doesn't have by default? I don't know. We'll see eventually. Anyway, here's the code for this factory:

<script src="https://gist.github.com/Tadukoo/aaae165f7d9d5afdbc2584a452062ae7.js"></script>

Now MetalLookAndFeel has a static method to set the MetalTheme, then uses AppContext to store it and retrieve later. You have to recreate the L&F anyway when you use this (e.g. when resetting theme at runtime), so we're 
just going to take the TadukooTheme as a parameter in the constructor (and allow not specifying it to default to our default theme). Here's those constructors:

<script src="https://gist.github.com/Tadukoo/0c4c1b62edd001827e43658652d1a650.js"></script>

The main reason for specifying the buttonUI (and eventually other component UI classes) in the theme is for if someone decides to make their own custom UI for certain components in the future, but still use my L&F base 
(e.g. if a new ButtonUI is created that's better than mine). Using Metal's component UI's will nullify some of the other settings in the theme we'll get to later (e.g. shape), but I'm going to make it so the themes can 
fully support the existing L&F's (so that someone could use my L&F to pick and choose various pieces of the existing versions if they choose to).

That's enough of a start on the customization for now. We'll also be putting more button customization information in the theme [next time]({% post_url 2020-05-31-java-look-and-feel-customizability-2 %}), 
including colors, gradients, shapes, etc.
