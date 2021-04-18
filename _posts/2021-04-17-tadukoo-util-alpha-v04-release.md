---
title:  "Tadukoo Util Alpha v.0.4 Release"
author: Tadukoo
date:   2021-04-17 21:16
series: "Releases"
index: 11
categories: blog
tags: 
- News
- Programming
comment_issue_id: 57
---
Tadukoo Util Alpha v.0.4 was [released today](https://github.com/Tadukooverse/TadukooUtil/releases/tag/v.0.4-Alpha).

Tadukoo Util is a collection of useful utilities for any project. It's released under the MIT license so it's very free for anyone to use for their projects. For more information about 
Tadukoo Util, check out its [project page](/projects/TadukooUtil.html). For Javadocs for Tadukoo Util, visit [this page](/docs/TadukooUtil/current/index.html).

Tadukoo Util contains the following modules:
- Tadukoo Lang - provides common basic utilities such as StringUtil and Tuples
- Tadukoo Functions - provides ThrowingFunctions, ThrowingPredicates, etc. for better use than Java's non-throwing versions
- Tadukoo Util - provides common utilities that are more advanced, such as MultiMap, ManyToManyMap, and pojo classes

## Changes
### Tadukoo Util
#### Dictionary
Created Dictionary, an interface used for storing and retrieving valid words.

Also created AbstractDictionary and several implementations for the Standard Charsets.

### Technical/Other
Updated to Java 16
