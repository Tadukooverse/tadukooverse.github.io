---
title:  "Java Components & Layouts: Labels, Text Fields, and Buttons! Oh My! (The Basics)"
author: Tadukoo
date:   2020-05-10 14:48:00 -0300
old_blog: true
series: "Java Components & Layouts"
index: 1
categories: blog
tags: 
- Components and Layouts
- Java
- programming
- Tutorial
comment_issue_id: 35
---
*This post is part of my Java Components & Layouts Tutorial. This tutorial is slightly linked to my Java Look & Feel Journey. See [this post]({% post_url 2020-05-03-java-look-and-feel-journey %}) for table of contents and 
more details about both this tutorial and my look and feel journey.*

In Java, there are various components you can use to create a GUI or form for the user to use. Today, we'll be going over the label, text field, and button (mainly because I think of these 3 components first). Now in my 
early programming, at first I didn't know about these, and then after that I didn't know they could be customized (and didn't like the regular look), so I didn't use them until less than two months ago. With work, I decided 
I wanted to do less work to make a GUI for a small utility program, so I started learning how to use these, and now I'm working on making my own Look and Feel to use these all the time moving forward.

To start, we're going to make a class called MainFrame that extends JFrame. Note that we're not making it the main class (with a public static void main method), but that is an option available. In our MainFrame, we're going 
to store a JLabel, a JTextField, and a JButton. The label is used to give information to the user (and usually is used to label a place for them to input information, such as the text field). The text field is used for the 
user to input text, and the button would run whatever logic we tell it to. In this tutorial, we're not going to have the button do anything when you click it (maybe in a later post?). We're also storing a JPanel. The panel 
is used to store the other components, and in a bigger program we could use multiple panels, so that the components are lumped together properly (e.g. if you have an options menu where you separate the audio settings into 
an upper panel and visual settings into a lower panel). In this program (at least for now), we're only going to use a single panel.

In the constructor for MainFrame, I'm adding setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE). This tells the program to end when the user closes the window. Now I make a new JPanel and add it to the frame. The panel being 
kept as a field in the MainFrame means it can be used elsewhere in the code here, rather than just doing add(new JPanel()). After this, I'm adding the three components. I'm just going to have the JLabel say "Example Label", 
give the JTextField 20 columns, and have the JButton named "Submit". All three components need added to the panel (via panel.add), and after that we call pack(). Calling pack changes the window size to the appropriate size for 
everything contained in it. Here's what MainFrame looks like after these additions:

<script src="https://gist.github.com/Tadukoo/61c1e2c63e9679186c7616c129fac9d9.js"></script>

Now to actually get this to display to the screen, we make another class (I'm calling it TadukooLookAndFeelTest because I'm using it to test out my Look & Feel I'm working on, but you can call it something else). In the main 
method, we call SwingUtilities.invokeLater and have it create our MainFrame and set it to visible. If you want to use a Look & Feel other than the default, you can call UIManager.setLookAndFeel. My example below sets the L&F 
to the TadukooLookAndFeel that I'm working on:

<script src="https://gist.github.com/Tadukoo/1d531516cd459294aa04934dab59434c.js"></script>

Next time, I'll go over using SpringLayout to have more control over how the components are laid out in the panel/frame.
