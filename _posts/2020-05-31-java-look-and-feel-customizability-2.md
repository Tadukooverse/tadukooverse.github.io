---
title:  "Java Look and Feel: Customizability 2: Electric Boogaloo"
author: Tadukoo
date:   2020-05-31 15:42:00 -0300
old_blog: true
series: "Tadukoo Look & Feel Journey"
index: 5
categories: blog
tags: 
- Java
- Journey
- Look and Feel
- programming
- Tutorial
comment_issue_id: 37
---
*This post is part of my Java Look and Feel Journey. See [this post]({% post_url 2020-05-03-java-look-and-feel-journey %}) for more details and table of contents (and to find a proper tutorial when it's available).*

*That post will also guide you to another tutorial on using Java's Components & Layouts, so you can make a program to actually see the Look & Feel changes. At this point in the journey, you'd only need the 
[first post]({% post_url 2020-05-10-java-components-layouts-labels-text %}), to have a button on screen to see the changes to it, but going further in that series is fine too.*

*This is part 5 of the "Journey" posts. Follow this link for part 1: [Getting Started]({% post_url 2020-05-03-java-look-and-feel-getting-started %}) or this link for the previous part: 
[4. Customizability]({% post_url 2020-05-24-java-look-and-feel-customizability %})*

Now it's time to look at the current themes that exist in the Java API. If you look at MetalTheme (the abstract class), OceanTheme, and DefaultMetalTheme, you'll see that most of what they store is a bunch of 
ColorUIResource and FontUIResource values, which determine the colors and fonts to use in various components. I actually looked into this back at the start, but I wanted to look more into making more drastic 
changes than simply changing the colors. The strange thing for me is that it's not simply Color and Font classes, they're special UIResource objects. Essentially UIResource is an interface that has no methods 
or fields in it, and is just simply used to mark the class as special. This marking has special meaning for UI classes, and if you want to know more, you can look for yourself 
([this](https://docs.oracle.com/javase/8/docs/api/javax/swing/plaf/UIResource.html) may be a good starting point). Anyway, for the purposes of this  journey/tutorial, I'll need to keep in mind that if I add 
custom classes to the theme, they'll need to implement UIResource.

I'm going to start by adding the UIResources relevant for the TadukooButtonUI. For this, there's Button.select (color), Button.gradient (which is actually a List, I'll come back to this), and Button.focus 
(color). Obviously, these aren't all of the Button resources, but they <i>are </i>the only ones referenced specifically in TadukooButtonUI. For the select color and focus color, I'm adding a buttonSelectColor 
and buttonFocusColor to the TadukooTheme class as ColorUIResources. I'm also adding defaultSelectColor and defaultFocusColor, since there are other select and focus related colors to be added later.

For each of the four colors, I'm creating four methods in the builder. For example, defaultFocusColor has defaultFocusColor(Color defaultFocusColor), defaultFocusColorRGB(int rgb), 
defaultFocusColorRGB(int r, int g, int b), and defaultFocusColorRGB(float r, float g, float b). The reason for this is to make it easier on the person creating the TadukooTheme. When creating a ColorUIResource, 
these are the parameters of the 4 different constructors. I'm also adding a fifth method for each of the colors, which is defaultFocusColor(ColorUIResource) for defaultFocusColor. This method makes it so that 
the user can create the ColorUIResource themselves if they so desire, or if they are using a custom ColorUIResource (perhaps one that uses a different method to create it, such as taking doubles instead of 
floats?). At some point I may write a small program to automate creating these methods, since it's five per color. Here's the 5 methods for defaultFocusColor:

<script src="https://gist.github.com/Tadukoo/2800cf6e83bd5ee26d2c127dc7b6fb72.js"></script>

In the build method, I'm setting buttonFocusColor to defaultFocusColor if it's null, and the same with buttonSelectColor and defaultSelectColor. Also, buttonFocusColor and buttonSelectColor (and getters for 
them) are added to TadukooTheme. Here's the build method after making these changes:

<script src="https://gist.github.com/Tadukoo/9dea4ccfc0a7a7583831b3b6d6944ff2.js"></script>

After these changes, TadukooLookAndFeel needs changed to set these values. These will be added to the initComponentDefaults method, as Button.focus and Button.select. Since we have more than one now, I'm 
creating an Object[] with them and using the UIDefaults table's setDefaults method to set them (instead of making several put(String key, Object value) calls). Here's the initComponentDefaults method after 
these changes:

<script src="https://gist.github.com/Tadukoo/e984a8e67fbeee5b4f286ba10ea70d9c.js"></script>

One thing you'll notice if you run an example program now is that the select color isn't working for the button (assuming you're using TadukooButtonUI with a custom Shaped button). This is because I'm ignoring 
it in order to use Button.gradient instead in the current code. The Button.gradient is not used in this way in MetalButtonUI, so if you mix the MetalButtonUI and a custom select color, you'll see the change right 
now (if you want to check it now instead of later).

Button.gradient will wait for the next post, because I have a rant about it and it's a more complex customization change than the color. Instead, I'm going to look at text settings now.

In MetalLookAndFeel, Button.font is being set, which is used on our button, but it is being created as a FontActiveValue, which is a private class inside MetalLookAndFeel. We can't use the same FontActiveValue 
class since it's private. But using the ActiveValue interface (as the FontActiveValue class does) is to make it so the FontUIResource is recreated every time the value's grabbed. I don't see why this would need 
done on a font, so I'm not planning to reuse it, and I'll just use FontUIResource directly instead.

Thankfully, FontUIResource doesn't have as many constructors as ColorUIResource had. It just has one that takes a Font and one that takes the font name, style, and size. So for every font to be included in 
TadukooThemeBuilder, I need 3 methods: 1 that takes a FontUIResource directly, one that takes a Font, and one that takes the font information. I'm making two Font settings for now: the defaultFont and buttonFont. 
buttonFont defaults to defaultFont if not specified. Here's the 3 methods for defaultFont:

<script src="https://gist.github.com/Tadukoo/7b38e6675b5a01f910c8670f5c81d199.js"></script>

When I changed the Button.font resource, the text is no longer positioned correctly in the select box (or the select box isn't positioned correctly around the text, it's a glass half full/empty situation). I 
tried creating a FontActiveValue in TadukooTheme and using that instead, but that doesn't fix it either. I'll be coming back to this problem in a future post, but for now I'm leaving it as is (this font stuff 
was a late addition to this post in the first place to give gradients their own post). The main point of talking about fonts here was to be able to change them in the theme, which is successful.
