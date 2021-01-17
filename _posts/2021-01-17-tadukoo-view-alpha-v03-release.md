---
title:  "Tadukoo View Alpha v.0.3 Release"
author: Tadukoo
date:   2021-01-17 15:29
series: "Releases"
index: 7
categories: blog
tags: 
- News
- Programming
comment_issue_id: 51
---
Tadukoo View Alpha v.0.3 was [released today](https://github.com/Tadukooverse/TadukooView/releases/tag/v.0.3-Alpha).

Tadukoo View is a collection of view utilities. It's released under the MIT license so it's very free for anyone to use for their projects. For more information about 
Tadukoo View, check out its [project page](/projects/TadukooView.html). For Javadocs for Tadukoo View, visit [this page](/docs/TadukooView/current/index.html).

Tadukoo View has the following modules:
- Tadukoo View - A collection of utilities for basic View stuff, and contains code to make it easier to customize fonts, paints, etc.
- Tadukoo Components - A collection of components that are more customizable than Java's default versions
- Tadukoo Form - Makes it easy to setup Forms with various fields
- Tadukoo Look & Feel - allows you to customize the look & feel of view components more easily than the default Java look & feels allow for

## Changes
### Tadukoo Look & Feel / All Modules
The reason this is "/ All Modules" is because these changes were wide-reaching with how they were implemented.
#### Button Customizations
On Buttons (via TadukooButton), Button Form Field, and via the Tadukoo Look & Feel, you can now specify the font, shape, border, and the following paints: 
focus, select, foreground, background, and disabled text.

#### Label Customizations
On Labels (via TadukooLabel), including the Labels on Form Fields, and via Tadukoo Look & Feel, you can now specify the font, shape, border, and the following paints: 
background, foreground, and disabled foreground.

### Tadukoo View
#### Added Component (and Related) Interfaces
For the new customizations, new interfaces were added to be used for getters and setters for the customizations. They are:
* HasSizablePaints - includes getters + setters for background and foreground SizablePaints
* HasSelectAndFocusPaints - includes getters + setters for focus and select SizablePaints
* HasDisabledTextPaint - includes getter + setter for disabledText SizablePaint
* HasDisabledForegroundPaint - includes getter + setter for disabledForeground SizablePaint

Then interfaces were also made for different components, that combine the different customization interfaces
* TComponent - includes HasSizablePaints and Shaped, and includes methods for getting proper Insets using the Border and ShapeInfo
* TButton - includes TComponent, HasSelectAndFocusPaints, and HasDisabledTextPaint
* TLabel - includes TComponent and HasDisabledForegroundPaint

#### Added ShapeInfo UIResource
This is so that it can be specified in the Look & Feel as a UIResource to distinguish between one set on the component vs. a default one (for the purposes of install/uninstall 
in the component UI classes).

#### NoPaint and NoBorder
NoPaint (and NoPaintUIResource) are SizablePaints used for when you must specify a non-null SizablePaint, but do not want to actually have a Paint involved. They return null 
for their Paints, and were added so we could avoid painting the Label background by default in the Look & Feel.

NoBorder (and NoBorderUIResource) are used for the same purpose, but with Borders. They were also added to avoid having a Border on Labels by default in the Look & Feel.

### Tadukoo Form
#### Custom Form Fields
Added CUSTOM to the Field Type enum to allow for custom form fields that don't fall under existing Field Types.
#### Font Resource Loading on Form Fields
You can now specify a Font Resource Loader (or the settings for one) when setting up a Form Field, rather than using the default one, for the purposes 
of fonts specified in the customizations listed above.

### Tadukoo Look & Feel
#### TComponentUIUtil
Created a new interface called TComponentUIUtil that is used by component UI classes for common functionality between them.
It includes functions for grabbing the customizations off of the components and installing/uninstalling defaults using the customization interfaces 
listed previously.

### Technical/Other
* Cleaned up some of the code
* Now using Tadukoo Util Alpha v.0.3
* Added some missing Javadoc info (e.g. package info for Tadukoo Look & Feel, TadukooButtonUI, etc.)
* Moved TitlePosition enum to its own file (was previously inside TadukooTheme)
* More JUnit testing for previously untested code (e.g. TadukooTheme, ColorPaintUIResource, etc.)
