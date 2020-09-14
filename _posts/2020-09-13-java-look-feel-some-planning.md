---
title:  "Java Look & Feel: Some Planning"
author: Tadukoo
date:   2020-09-13 21:07
series: "Tadukoo Look & Feel Journey"
index: 9
categories: blog
tags: 
- Java
- Journey
- Look and Feel
- Programming
- Tutorial
comment_issue_id: 45
---
*This post is part of my Java Look and Feel Journey. See [this post]({% post_url 2020-05-03-java-look-and-feel-journey %}) for more details and table of contents (and to find a proper tutorial when it's available).*

*That post will also guide you to another tutorial on using Java's Components & Layouts, so you can make a program to actually see the Look & Feel changes. At this point in the journey, you'd only need the 
[first post]({% post_url 2020-05-10-java-components-layouts-labels-text %}), to have a button on screen to see the changes to it, but going further in that series is fine too.*

*This is part 9 of the "Journey" posts. Follow this link for part 1: [Getting Started]({% post_url 2020-05-03-java-look-and-feel-getting-started %}) or this link for the previous part: 
[8. Make Paint Great Again]({% post_url 2020-08-09-java-look-feel-make-paint-great-again %})*

In case you missed it, [Tadukoo Util](/projects/TadukooUtil.html) had its Alpha v.0.1 release recently. ([See here for Releases post]({% post_url 2020-09-05-tadukoo-util-alpha-v01-release %})). Also, if you look at 
[The Tadukooverse Master Plan]({% post_url 2020-08-14-the-tadukooverse-master-plan %}), you'll see that Tadukoo Look & Feel is the next milestone in Tadukoo Util. So basically now I need to focus on Tadukoo Look & 
Feel according to my own plans. I took a break for a while to setup this website and [my personal website](https://tadukoo.github.io), along with getting Tadukoo Util to a decent state, but now I'm back to this.

Anyway, I'm trying to be more professional about Tadukoo Util at this point, so I need to do proper planning for Tadukoo Look & Feel now. So the basic overview of how it'll progress is like this:
* Extend/Override MetalLookAndFeel
* Extend/Override BasicLookAndFeel
* Extend LookAndFeel directly
* Enable functionaliy present in other Java Look & Feels (e.g. Nimbus, Synth, etc.)

Basically right now we're using MetalLookAndFeel for most of the work, but the ultimate goal with that is to replace Metal with our L&F, at which point we can extend BasicLookAndFeel and replace that with our L&F. 
Once we replace that with ours, we can just extend LookAndFeel directly, and at that point we can add more functionality from the other Look & Feels. The ultimate goal is for Tadukoo Look & Feel to be able to support 
any L&F needs, so that people can use it to have an easier time making a custom look & feel.

I just looked through some of the code for MetalLookAndFeel and BasicLookAndFeel, and I will probably be splitting this project into multiple milestones now that I look at it closer. At the very least, we'll probably 
split it into three milestones: 1 to get MetalLookAndFeel functionality, 1 to get BasicLookAndFeel functionality, and 1 for the other L&F's. That last milestone may be split for each L&F as well when I look closer at 
them too. I'm not sure yet how this will impact [The Tadukooverse Master Plan]({% post_url 2020-08-14-the-tadukooverse-master-plan %}) (whether to just do the MetalLookAndFeel functionality for it, or to include all 
the milestones, where they fit, etc.). Sometime soon I'll make an update to that plan based on the milestone plans here.

Milestones:
1. Customizable version of MetalLookAndFeel
2. Customizable version of BasicLookAndFeel (that can do everything MetalLookAndFeel and BasicLookAndFeel can do)
3. Customizable version of any LookAndFeel (a LookAndFeel that can support any of the default L&F's in the Java API, and hopefully general ones too)

As for what can be customized, ultimately you would be able to customize the following:
- All colors / gradients / paints, to be able to use any Paint for them
  - With this, you would not be restricted to a limited set of colors like Metal does (i.e. choosing primary, secondary, white, black, etc.)
    - You would still be able to do it this way to have an easier time, but would not be required to
- All fonts
  - For this, I'd like to make it so you can specify specific standard fonts without worrying about if it's on the system you're using or not
    - e.g. in case you want Calibri, and that's not on Mac (I don't know if it's on Mac or not, just an example), you'd no longer have a cross-platform program, also it could represent a different font on different 
platforms, causing things to look weird
    - I'll likely provide some standard fonts and allow the programmer to specify to use the provided one vs. search the system
      - Searching the system would check if the system has the font (and if so, use it), or default to using the one I provide
      - The fonts would be in an enum (or somewhere) to have a simple full list of them
- Shapes of components
- Borders
- Allow the above to be customized on the component itself
- What UI classes are used
  - i.e. if you like the Button look from Metal, you can use it, and use everything else from Tadukoo L&F (if you want to)
- More TBA
  - There's likely more that can be customized that I will come across as I work on this project, and could be in any of the three milestones

For the customizations, part of the work is already done from my previous posts for having it setup generally, but once the general stuff is setup for it, the main way of progress will be in making my own versions of 
the Component UI classes present in Metal L&F, Basic L&F, etc.

Metal has the following Component UI classes (in alphabetical order):
- ButtonUI
- CheckBoxUI
- ComboBoxUI
- DesktopIconUI
- FileChooserUI
- InternalFrameUI
- LabelUI
- PopupMenuSeparatorUI
- ProgressBarUI
- RadioButtonUI
- RootPaneUI
- ScrollBarUI
- ScrollPaneUI
- SeparatorUI
- SliderUI
- SplitPaneUI
- TabbedPaneUI
- TextFieldUI
- ToggleButtonUI
- ToolBarUI
- ToolTipUI
- TreeUI

So far, the ButtonUI is the only one I've worked on, but all of those will need supported for the first milestone in the list. In addition to that, I need to support all of Metal's component defaults, such as 
theme colors and fonts, and input maps for the components (which I will be looking at closer in the future). I wouldn't be surprised if I'm leaving out other details too, but I'll get to them at some point in the 
planning in the future.

For now I'm not going to go into detail on the other two milestones (I might in near future posts or somewhere soon, but not right now). Instead I need to look at what's done vs. what needs done more specifically 
for some of this plan. (e.g. Is the paint customizability stuff done? What changes need made to my ButtonUI class yet? etc.). One of the reasons for doing this is it's been a bit since I worked on the Tadukoo Look 
& Feel due to setting up the Tadukooverse website and [my personal website](https://tadukoo.github.io), along with getting [Tadukoo Util](/projects/TadukooUtil.html) to Alpha v.0.1.

The basics of milestone 1 are done:
- setting up Tadukoo Look and Feel to extend Metal Look and Feel and overriding the default and necessary methods
- creating TadukooTheme to hold the customizable settings via a builder

In general, something that needs done properly is Javadocing. It's lacking in multiple places in the code I have so far. For the most part, I can't really do JUnit testing, because a bunch of this is GUI related, 
but there probably is some testing that can be done (will require looking into it more as I go).

As for colors, I planned to change my Gradient class to support building a RadialGradientPaint (currently it only supports LinearGradientPaint). Other than that, the only other paint to support should be TexturePaint 
I think (using a texture/image to paint instead of a solid color/gradient). Other custom paints would just need to be wrapped in a PaintUIResource to be supported in TadukooTheme.

As for fonts, there's a lot of work to do. Currently I just have it setup to support a FontUIResource in TadukooTheme. I don't have the setup for supporting some standard fonts cross-platform. Also I'm not currently 
doing anything to properly handle changing the font in the ButtonUI (I'm not sure if it needs it, or if it uses the FontMetrics enough for it to work properly, probably not since you can change the font size and style).

As for shapes and borders, I'll have to think more about supporting them. For shapes, it'll likely be an enum or similar thing to choose from that has standard shapes (rectangle, rounded rectangle, ellipse, etc.), but 
you would be able to substitute a method for a Polygon to be drawn (or something like that). Borders may be something similar, but I need to look into the existing borders more.

For UI classes as far as customization is concerned, it's just the ability to switch them out in the TadukooTheme, which is being done for the Button UI already. So all that needs done for the UI classes then is to 
finish any changes to the new Tadukoo Button UI class and to create the others to allow for customization.

Allowing the components to have all the customizations will require extending the default Java components to support this (e.g. extending JButton to support specifying its own Border or Shape). It would also be 
beneficial to create interfaces to allow for others to make custom components that allow for these customizations (e.g. if someone wants customizable shapes on an already custom button they have). I had started 
this process with the Shaped interface and the TadukooButton class, but obviously it needs a lot more work to be completed. I should probably just create a custom interface for each component, and if someone 
doesn't want to support customization for certain things (e.g. no custom borders on buttons), just make a final method that returns null for it. (null will default to using the default in TadukooTheme). 
With those though, I don't like the current setup for Shaped/TadukooShape. If I'm going to have an enum of standard shapes, it should return a functional interface instead.

If you want more details (and updates in case they don't make it into the blog), check [this issue](https://github.com/Tadukooverse/TadukooUtil/issues/16) and the ones related to it on the Tadukoo Util project.

For now I'll wrap this up. Next time will hopefully be more about creating the actual customizations (i.e. working on the paints, fonts, etc.) instead of more planning. I know this time was supposed to be shapes, 
but I'm trying to be more professional about the process now and this planning was overdue anyway.
