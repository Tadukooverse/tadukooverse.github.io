---
title:  "Tadukoo Util Alpha v.0.1 Release"
author: Tadukoo
date:   2020-09-05 
series: "Releases"
index: 1
categories: blog
tags: 
- News
- Programming
comment_issue_id: 44
---
Tadukoo Util Alpha v.0.1 was released earlier today. It represents the first piece of software released by Tadukooverse, and the first piece of software I have personally released in 
over four years, so it's a major milestone for me.

Tadukoo Util is a collection of useful utilities for any project. It's released under the MIT license so it's very free for anyone to use for their projects. For more information about 
Tadukoo Util, check out its [project page](/projects/TadukooUtil.html). For Javadocs for Tadukoo Util, visit [this page](/docs/TadukooUtil/current/index.html).

This release represents the first release for Tadukoo Util of the following modules:
- Tadukoo Annotation Processor - provides @AnnotationProcessor and AnnotationUtil for making Annotations
- Tadukoo Lang - provides common basic utilities such as StringUtil and Tuples
- Tadukoo Util - provides common utilities that are more advanced, such as MultiMap, ManyToManyMap, and Throwing Functional Interfaces

While the following modules are included, they should not be considered officially released with this release, and will be completed in future Alpha releases leading up to Beta. Use 
them at your own risk, understanding they may change entirely.
- Tadukoo Database - utilities for communicating with a SQL database
- Tadukoo File Format - allows you to create your own file formats
- Tadukoo Look & Feel - a customizable Look & Feel
- Tadukoo View - common view utilities

The first set of modules will be fully supported, while the second set will not. Tadukoo Util (the project) is in kind of a weird state at the moment, See 
[the Tadukooverse Master Plan](% post_url 2020-08-14-the-tadukooverse-master-plan %}) for more details on what's going on.

Due to some weird things going on with the plan, this version has the version string 0.1-Alpha-SNAPSHOT for the purposes of Maven, and will only be available in the snapshots repository 
of Maven Central, and not in the official releases repository. Also, this is why the jars themselves have "-SNAPSHOT" in them.

Tadukoo Util is now officially transferred over to Tadukooverse [on GitHub](https://github.com/Tadukooverse/TadukooUtil) as the first actual software in the organization (other projects 
at this point are related to the website or community files).
