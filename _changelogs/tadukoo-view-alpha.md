---
title: Tadukoo View Alpha Changelog
project: TadukooView
version_range: Alpha
blurb: Tadukoo View's Alpha changelog
changelog:
- version: Alpha v.0.3.4
  blurb: Java 17
  released: November 19, 2021 10:26 PM
  github: 
  details: | 
    ### Other/Technical
    * Tadukoo Util updated to Beta v.0.5.1
    * Tadukoo Maven Library POM updated to Alpha v.0.3.1 (for Java 17 + updated dependencies)
- version: Alpha v.0.3.3
  blurb: Update to Tadukoo Util Beta v.0.5 (and some changes)
  released: July 15, 2021 8:42 PM
  github: https://github.com/Tadukooverse/TadukooView/releases/tag/v.0.3.3-Alpha
  details: | 
    ### Overall
    * Changed Table references to List (due to the change in Tadukoo Util)
    
    ### Tadukoo Form
    * Added new Form interface (previous renamed to SimpleForm) and added TabbedForm
    * Added MainForm, SimpleMainForm, TabbedMainForm
    * Added FileDownloader
    
    ### Other/Technical
    * Tadukoo Util updated to Beta v.0.5
    * Now using Tadukoo Maven Library POM (Alpha v.0.2)
    * Improved Javadocs
    * Rearranged some code
- version: Alpha v.0.3.2
  blurb: Update to Tadukoo Util Alpha v.0.4 (and some changes)
  released: April 25, 2021 2:20 PM
  github: https://github.com/Tadukooverse/TadukooView/releases/tag/v.0.3.2-Alpha
  details: | 
    * Tadukoo Util updated to Alpha v.0.4
    * Updated to Java 16
- version: Alpha v.0.3.1
  blurb: Update to Tadukoo Util Alpha v.0.3.1
  released: February 6, 2021 5:50 PM
  github: https://github.com/Tadukooverse/TadukooView/releases/tag/v.0.3.1-Alpha
  details: |
    ### Updated Tadukoo Util Dependency
    - Tadukoo Util updated to Alpha v.0.3.1
    
    ### Technical/Other
    * Cleaned up the poms
- version: Alpha v.0.3
  blurb: Complete Button + Label Customizations
  released: January 17, 2021 3:29 PM
  github: https://github.com/Tadukooverse/TadukooView/releases/tag/v.0.3-Alpha
  details: |
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
- version: Alpha v.0.2.2
  blurb: Moved from Tadukoo Util
  released: December 13, 2020 8:48 PM
  github: https://github.com/Tadukooverse/TadukooView/releases/tag/v.0.2.2-Alpha
  details: | 
    This is the official release of the following modules:
    
    - Tadukoo View - A collection of utilities for basic View stuff, and contains code to make it easier to customize fonts, paints, etc.
    - Tadukoo Components - A collection of components that are more customizable than Java's default versions
    - Tadukoo Form - Makes it easy to setup Forms with various fields
    
    It is not yet the official release of Tadukoo Look & Feel, though it is included here.
    
    Note that all of this code came over from Tadukoo Util and has not been modified from Tadukoo Util's Alpha v.0.2.1 release
---
