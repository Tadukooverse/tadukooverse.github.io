---
title:  "Tadukoo Util Alpha v.0.3.1 Release"
author: Tadukoo
date:   2021-02-06 17:33
series: "Releases"
index: 8
categories: blog
tags: 
- News
- Programming
comment_issue_id: 52
---
Tadukoo Util Alpha v.0.3.1 was [released today](https://github.com/Tadukooverse/TadukooUtil/releases/tag/v.0.3.1-Alpha).

Tadukoo Util is a collection of useful utilities for any project. It's released under the MIT license so it's very free for anyone to use for their projects. For more information about 
Tadukoo Util, check out its [project page](/projects/TadukooUtil.html). For Javadocs for Tadukoo Util, visit [this page](/docs/TadukooUtil/current/index.html).

Tadukoo Util contains the following modules:
- Tadukoo Lang - provides common basic utilities such as StringUtil and Tuples
- Tadukoo Functions - provides ThrowingFunctions, ThrowingPredicates, etc. for better use than Java's non-throwing versions
- Tadukoo Util - provides common utilities that are more advanced, such as MultiMap, ManyToManyMap, and pojo classes

## Changes
### Tadukoo Lang
#### Character Util
Created Character Util, a class with utility methods for dealing with characters.

It includes the following methods:
- isUpperCase
- isLowerCase
- isLetter
- isNumber
- toUpperCase
- toLowerCase

### More String Util methods
Methods were added to String Util to deal with different cases.

The following methods were added:
- isPascalCase
- toPascalCase
- isCamelCase
- toCamelCase
- isSnakeCase
- toSnakeCase

### Technical/Other
Removed Tadukoo View from dependency management
