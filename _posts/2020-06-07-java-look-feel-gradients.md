---
title:  "Java Look & Feel: Gradients"
author: Tadukoo
date:   2020-06-07 14:07:00 -0300
old_blog: true
series: "Tadukoo Look & Feel Journey"
index: 6
categories: blog
tags: 
- Java
- Journey
- Look and Feel
- programming
- Tutorial
comment_issue_id: 38
---
*This post is part of my Java Look and Feel Journey. See [this post]({% post_url 2020-05-03-java-look-and-feel-journey %}) for more details and table of contents (and to find a proper tutorial when it's available).*

*That post will also guide you to another tutorial on using Java's Components & Layouts, so you can make a program to actually see the Look & Feel changes. At this point in the journey, you'd only need the 
[first post]({% post_url 2020-05-10-java-components-layouts-labels-text %}), to have a button on screen to see the changes to it, but going further in that series is fine too.*

*This is part 6 of the "Journey" posts. Follow this link for part 1: [Getting Started]({% post_url 2020-05-03-java-look-and-feel-getting-started %}) or this link for the previous part: 
[5. Customizability 2: Electric Boogaloo]({% post_url 2020-05-31-java-look-and-feel-customizability-2 %})*

Now to get back to the Button.gradient, I don't like the way that it's a List. The format used by Metal is a List of two floats and three Colors. This may be unique to OceanTheme (I haven't checked in DefaultMetalTheme 
for a while), but it's restrictive, only allowing 3 colors and not being able to specify the direction (the direction is hard-coded for each component). The colors work as the 3 gradient colors used, and the floats 
represent the first midpoint percentage and the second midpoint percentage after the first is doubled. The float nonsense means that float values of 0.33 and 0.0 would mean the midpoint percentages are 0.33 and 0.66 
(because the second is 0.33*2 + 0.0). Nonsense. Now another thing, two midpoints = four colors (because of 0.0, midpoint1, midpoint2, 1.0). So how do you place 3 colors onto 4 spots? If you guessed you do 1, 2, 1, 3, 
you cheated. Unfortunately, since I'm allowing people to use the MetalButtonUI, I have to support this trash.

I want to make it so that for every color, you can instead opt to use a gradient. So the previous buttonFocusColor and buttonSelectColor will also potentially be gradients instead of solid colors if someone chooses that. 
Ultimately, there will be a new item in the UIDefaults to check, and if it's a ColorUIResource, we use Graphics.setColor for it, but if it's a gradient, we use Graphics.setPaint with the proper gradient method. The 
reason for creating a new item instead of using Button.focus and others is that using those with new class types won't work correctly for the existing java L&F's out there such as Metal. So if someone chooses a 
gradient for a normal color and uses Metal's ButtonUI, having a gradient in Button.focus would cause runtime errors. I'm going to use "paint" in my new items, e.g. Button.focusPaint, Button.selectPaint, etc.

Turns out there's an interface called Paint and Color is already a descendant of it, so in my UI classes I can just use setPaint every time instead of having to worry about what type it is. Color looks like the only one 
to already have a UIResource version, so I'll still need to make UIResource versions of the gradients. I'd also like to create a builder for Paints instead of having to make a ton of methods to allow them in TadukooTheme 
(as in the many methods created for the colors a couple posts back).

Unfortunately, the gradients take dimensions via endX and endY values, which would be determined by the dimensions of the component, so I can't simply use setPaint on whatever is returned from the UIDefaults. Instead, 
I'll be creating a pojo to store the gradient variables. This is probably why Metal doesn't do it this way, but Metal is still restrictive compared to how I want to do it.

I've created Gradient with its own builder. Basically it allows you to create a LinearGradientPaint, and it also can create one of Metal Look & Feel's garbage lists. I store a direction enum to determine which way 
the gradient goes, the colors and fraction pairs, cycle method, color space type, and affine transform. Note that in this I used FloatUtil.convertListToArray. This is a method from TadukooLang, which is part of my util 
project I've been working on. Basically it just iterates through the List&lt;Float&gt; to setup a float array, because you can't do List&lt;Float&gt; .toArray(new float[0]), because of primitives vs. objects. 
TadukooLang is part of TadukooUtils, a project I'm working on. I'll be moving Tadukoo Look & Feel to that project probably by the next post, so I guess stay tuned for that? One other thing done with my Gradient 
class was to make a UIResource version, which is buildable from the builder. Here's my Gradient class:

<script src="https://gist.github.com/Tadukoo/62d99507c170e539a5fcd02650eed224.js"></script>

I'm not connecting this to the theme code yet, because I want to add support for RadialGradientPaint, and make an easier way to have a standard PaintUIResource so the UI classes don't have to check what type they're 
looking at. Also, since this class uses Tadukoo Util stuff, I want to integrate Tadukoo Look & Feel into Tadukoo Util properly before moving on. Doing this will also make it easier to look at the code progress so far, 
by me just referencing commits instead of trying to make a Gist containing all the classes.

So [next time]({% post_url 2020-06-14-java-look-feel-tadukoo-util-placement %}) will be integrating Tadukoo Look & Feel into Tadukoo Util, and the time after that will be more gradient stuff.
