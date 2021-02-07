---
title:  "Tadukoo Parsing Alpha v.0.2.3 Release"
author: Tadukoo
date:   2021-02-06 18:07
series: "Releases"
index: 10
categories: blog
tags: 
- News
- Programming
comment_issue_id: 
---
Tadukoo Parsing Alpha v.0.2.3 was [released today](https://github.com/Tadukooverse/TadukooParsing/releases/tag/v.0.2.3-Alpha).

Tadukoo Parsing is a collection of useful utilities for parsing different formats. It's released under the MIT license so it's very free for anyone to use for their projects. For more information about 
Tadukoo Parsing, check out its [project page](/projects/TadukooParsing.html). For Javadocs for Tadukoo Parsing, visit [this page](/docs/TadukooParsing/current/index.html).

The following modules are in Tadukoo Parsing:
- Tadukoo Parsing - basic parsing utilities to be used in the other modules
- Tadukoo JSON - which has code for parsing JSON
- Tadukoo Java - which has code for generating Java code
- Tadukoo File Format - which is unfinished custom file parsing

## Changes
### Tadukoo Parsing
A new module that will contain basic parsing utilities for the other modules to use.

Currently just contains some common patterns used in Tadukoo JSON

### Tadukoo Java
The following changes were made to Tadukoo Java:
- JavaAnnotation now exists and can be used in the other types
- JavaClass can now have static imports
- JavaFields can now have values set

### Tadukoo JSON
- JSONArray now has a size method

### Updated Tadukoo Util Dependency
- Tadukoo Util updated to Alpha v.0.3.1

### Technical/Other
* Cleaned up the poms
