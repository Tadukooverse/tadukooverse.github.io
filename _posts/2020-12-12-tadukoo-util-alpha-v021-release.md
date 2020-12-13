---
title:  "Tadukoo Util Alpha v.0.2.1 Release"
author: Tadukoo
date:   2020-12-12 19:33
series: "Releases"
index: 4
categories: blog
tags: 
- News
- Programming
comment_issue_id: 48
---
Tadukoo Util Alpha v.0.2.1 was [released today](https://github.com/Tadukooverse/TadukooUtil/releases/tag/v.0.2.1-Alpha).

Tadukoo Util is a collection of useful utilities for any project. It's released under the MIT license so it's very free for anyone to use for their projects. For more information about 
Tadukoo Util, check out its [project page](/projects/TadukooUtil.html). For Javadocs for Tadukoo Util, visit [this page](/docs/TadukooUtil/current/index.html).

This release represents the third release for Tadukoo Util, and is an official release of the following modules:
- Tadukoo Annotation Processor - provides @AnnotationProcessor and AnnotationUtil for making Annotations
- Tadukoo Lang - provides common basic utilities such as StringUtil and Tuples
- Tadukoo Util - provides common utilities that are more advanced, such as MultiMap, ManyToManyMap, and Throwing Functional Interfaces
- Tadukoo View - provides utilities for drawing items to the screen, and for building forms

While the following modules are included, they should not be considered officially released with this release, and will be completed in future Alpha releases leading up to Beta. Use 
them at your own risk, understanding they may change entirely.
- Tadukoo Database - utilities for communicating with a SQL database
- Tadukoo File Format - allows you to create your own file formats
- Tadukoo Look & Feel - a customizable Look & Feel

The first set of modules will be fully supported, while the second set will not. Tadukoo Util (the project) is in kind of a weird state at the moment, See 
[the Tadukooverse Master Plan]({% post_url 2020-08-14-the-tadukooverse-master-plan %}) for more details on what's going on.

Note that now Tadukoo Util releases are available from Maven Central.

## Changes
### Tadukoo Util
#### MappedPojo Constructors
AbstractMappedPojo, AbstractOrderedMappedPojo, and AbstractForm now have constructors that take in a MappedPojo. When taking in the MappedPojo, they use its map to set their map values. 
This can be used by subclasses to more easily cast to a subclass if needed, e.g.:
```
MappedPojo pojo; // <- Pretend this is a pojo that already exists, and that it's an instance of AbstractMappedPojo
PojoSubclass realPojo = new PojoSubclass(pojo); // <- PojoSubclass is a subclass of AbstractMappedPojo, and is using the new constructor to get the mapped values to easily turn pojo into a PojoSubclass
```

This is also used in a new MappedPojo method - getPojoItem(String key, Class<T extends MappedPojo> clazz), which will convert the item to the proper pojo class if it's not already and store it in the 
MappedPojo if a conversion happened.

There's another new MappedPojo method for dealing with tables - getTableItem(String key, Class<T extends MappedPojo> clazz), which will convert the item into a proper Table with T items instead of 
generic MappedPojos (that are added to the Table by some methods)
#### Time Utils
Created DateUtil and MonthUtil with utilty methods for dealing with Dates and Months, respectively.
### Tadukoo View
#### Sizable Paint
SizablePaint is a new interface used as a general class to hold a SizablePaint. It has a single method: getPaint(Dimension size), used to create classes for general paints that can 
vary by size.

SizableColor was created as a simple SizablePaint that's just a solid color. This is used for places where SizablePaint is needed, but you just want a solid color instead.

Gradient now extends SizablePaint (doesn't change Gradient's getPaint method or anything like that, just now it is a SizablePaint).

Gradient classes were moved to a different subpackage (now in com.github.tadukoo.util.view.paint.gradient)

PaintUIResource is now an extension of SizablePaint (again, no change to its getPaint method, just now it is a SizablePaint).

TadukooButtonUI is now expecting a SizablePaint to be used to paint, instead of a PaintUIResource. This is because PaintUIResource is meant only for default UI settings, and not for 
general use (such as being contained in a button class as it will be eventually).

ShapedBevelBorder, ShapedLineBorder, and ShapedEtchedBorder now use SizablePaint instead of PaintUIResource.

#### Shaped Borders Moved
ShapedBevelBorder, ShapedLineBorder, and ShapedEtchedBorder were moved from Tadukoo Look & Feel to Tadukoo View. This is so you can set borders on the custom components in Tadukoo View 
without requiring Tadukoo Look & Feel.

#### Gradient Changes
Gradient now has methods for getting the cycleMethod, colorSpace, and gradientTransform values, and LinearGradient and RadialGradient have methods for getting their specific parameters.

GradientUIResource has the methods for cycleMethod, colorSpace, and gradientTransform as well.

GradientBuilder now has a type parameter for what type of Gradient it returns when building, so you don't have to cast it.

#### Date Form
Created DateForm, a Form that uses a drop-down menu for month and integer JSpinners for day and year

#### New Form Fields
##### Number Form Fields
Created NumberFormField, which uses JSpinner to display a number. It takes minValue, maxValue, and stepSize for the spinner model to use.

It has implementations for Integers, Shorts, Longs, Floats, and Doubles.

##### Date Form Field
Date Form Field is a form field that uses the new Date Form to display a Date. It takes in minYear and maxYear for the Date Form to use.

### Bug Fixes
Gradients actually work now (previously building them caused a NullPointerException).

### JUnit Testing
New JUnit tests for FontFamily and FontFamilies

New JUnit tests for LinearGradient and RadialGradient

New JUnit tests for Orientation

### Technical/Other
Updated JUnit dependencies to the latest

Leckerli One font is now using the TTF constant instead of hard-coding "ttf"

Updated to Java 15 and no longer use preview features
