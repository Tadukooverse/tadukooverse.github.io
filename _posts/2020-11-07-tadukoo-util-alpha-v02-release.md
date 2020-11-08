---
title:  "Tadukoo Util Alpha v.0.2 Release"
author: Tadukoo
date:   2020-11-07 21:16
series: "Releases"
index: 2
categories: blog
tags: 
- News
- Programming
comment_issue_id: 46
---
Tadukoo Util Alpha v.0.2 was [released today](https://github.com/Tadukooverse/TadukooUtil/releases/tag/v.0.2-alpha). It represents the second release of software by Tadukooverse.

Tadukoo Util is a collection of useful utilities for any project. It's released under the MIT license so it's very free for anyone to use for their projects. For more information about 
Tadukoo Util, check out its [project page](/projects/TadukooUtil.html). For Javadocs for Tadukoo Util, visit [this page](/docs/TadukooUtil/current/index.html).

This release is mainly for the first release of Tadukoo View, but there were change sto Tadukoo Lang and Tadukoo Util as well.

This release represents the second release for Tadukoo Util, and is an official release of the following modules:
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

Due to some weird things going on with the plan, this version has the version string 0.2-Alpha-SNAPSHOT for the purposes of Maven, and will only be available in the snapshots repository 
of Maven Central, and not in the official releases repository. Also, this is why the jars themselves have "-SNAPSHOT" in them.
