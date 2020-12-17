---
title:  "Tadukoo Util (and others) Alpha v.0.2.2 Release"
author: Tadukoo
date:   2020-12-16 21:07
series: "Releases"
index: 5
categories: blog
tags: 
- News
- Programming
comment_issue_id: 49
---

#### Table of Contents
* [Tadukoo Util](#tadukoo-util)
* [Tadukoo Annotations](#tadukoo-annotations)
* [Tadukoo Database)(#tadukoo-database)
* [Tadukoo Parsing)(#tadukoo-parsing)
* [Tadukoo View](#tadukoo-view)

## Tadukoo Util
Tadukoo Util Alpha v.0.2.2 was [released a few days ago](https://github.com/Tadukooverse/TadukooUtil/releases/tag/v.0.2.2-Alpha).

Tadukoo Util is a collection of useful utilities for any project. It's released under the MIT license so it's very free for anyone to use for their projects. For more information about 
Tadukoo Util, check out its [project page](/projects/TadukooUtil.html). For Javadocs for Tadukoo Util, visit [this page](/docs/TadukooUtil/current/index.html).

This release doesn't really have any code changes compared to Alpha v.0.2.1, it's just a reorganization of the modules involved. So now Tadukoo Util contains the following modules only:
- Tadukoo Lang - provides common basic utilities such as StringUtil and Tuples
- Tadukoo Functions - provides ThrowingFunctions, ThrowingPredicates, etc. for better use than Java's non-throwing versions
- Tadukoo Util - provides common utilities that are more advanced, such as MultiMap, ManyToManyMap, and pojo classes

Tadukoo Functions was moved out of Tadukoo Util, so it's not really new code, just moved code. Also the annotations stuff present in Tadukoo Util moved to the new Tadukoo Annotations project (see below).

For a summary of the moved modules:
- Tadukoo Annotation Processor is now in Tadukoo Annotations
- Tadukoo Database is now Tadukoo MySQL and is in Tadukoo Database
- Tadukoo File Format is now in Tadukoo Parsing
- Tadukoo Look & Feel is now in Tadukoo View
- Tadukoo View is now Tadukoo View, Tadukoo Components, and Tadukoo Form and is in Tadukoo View

## Tadukoo Annotations
Tadukoo Annotations Alpha v.0.2.2 was [released a few days ago](https://github.com/Tadukooverse/TadukooAnnotations/releases/tag/0.2.2-Alpha)

Tadukoo Annotations is a collection of annotations and utilities for creating annotations easier. For more information about Tadukoo Annotations, check out its [project page](/projects/TadukooAnnotations.html). 
For Javadocs for Tadukoo Annotations, visit [this page](/docs/TadukooAnnotations/current/index.html).

The code present in this release is the same as was in Tadukoo Util in Alpha v.0.2.1, and is just a reorganization of the code. The following modules are present in Tadukoo Annotations:
- Tadukoo Annotation Processor - makes it easier to create annotation processors
- Tadukoo Annotations - a collection of annotations

Tadukoo Annotations contains @ShouldBeFinal, which came from Tadukoo Util.

## Tadukoo Database
Tadukoo Database Alpha v.0.2.2 was [released a few days ago](https://github.com/Tadukooverse/TadukooDatabase/releases/tag/0.2.2-Alpha)

Tadukoo Database is a collection of utilities used for interacting with databases. For more information about Tadukoo Database, check out its [project page](/projects/TadukooDatabase.html). For 
Javadocs for Tadukoo Database, visit [this page](/docs/TadukooDatabase/current/index.html).

This release is just the Tadukoo Database module from Tadukoo Util Alpha v.0.2.1, moved here and renamed. It's just the following module:
- Tadukoo MySQL - used for interacting with a MySQL database

## Tadukoo Parsing
Tadukoo Parsing Alpha v.0.2.2 was [released a few days ago](https://github.com/Tadukooverse/TadukooParsing/releases/tag/0.2.2-Alpha)

Tadukoo Parsing is a collection of useful utilities for parsing different formats. It's released under the MIT license so it's very free for anyone to use for their projects. For more information about 
Tadukoo Parsing, check out its [project page](/projects/TadukooParsing.html). For Javadocs for Tadukoo Parsing, visit [this page](/docs/TadukooParsing/current/index.html).

The following modules are in Tadukoo Parsing:
- Tadukoo JSON - which has code for parsing JSON
- Tadukoo Java - which has code for generating Java code
- Tadukoo File Format - which is unfinished custom file parsing

This release is an official release for Tadukoo JSON, but not for Tadukoo Java and Tadukoo File Format.

Tadukoo File Format is the same code as was present in Alpha v.0.2.1 of Tadukoo Util.

Tadukoo Java is new code, but was not really complete yet and was just released due to releasing Tadukoo File Format here.

## Tadukoo View
Tadukoo View Alpha v.0.2.2 was [released a few days ago](https://github.com/Tadukooverse/TadukooView/releases/tag/0.2.2-Alpha)

Tadukoo View is a collection of view utilities. It's released under the MIT license so it's very free for anyone to use for their projects. For more information about 
Tadukoo View, check out its [project page](/projects/TadukooView.html). For Javadocs for Tadukoo View, visit [this page](/docs/TadukooView/current/index.html).

Tadukoo View has the following modules:
- Tadukoo View - A collection of utilities for basic View stuff, and contains code to make it easier to customize fonts, paints, etc.
- Tadukoo Components - A collection of components that are more customizable than Java's default versions
- Tadukoo Form - Makes it easy to setup Forms with various fields
- Tadukoo Look & Feel - allows you to customize the look & feel of view components more easily than the default Java look & feels allow for

This release is an official release for all the modules except for Tadukoo Look & Feel.

Tadukoo Look & Feel is the same code as was present in Alpha v.0.2.1 of Tadukoo Util.

All the code in this project was present in Alpha v.0.2.1, just in different locations. Tadukoo View, Tadukoo Components, and Tadukoo Form all used to be in the Tadukoo View module in 
Alpha v.0.2.1 of Tadukoo Util.
