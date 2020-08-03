---
layout: default
title: Roadmap
---

> **Note**: This page is under construction and likely to change

#### Table of Contents
[Vision](#vision)

[Roadmap](#roadmap)
* [Tadukoo Util](#tadukoo-util)
* [Tadukoo Engine/Launcher](#tadukoo-enginelauncher)

## Vision
Our vision is to create efficient free and open source software.

In terms of efficiency, we mean both via code efficiency (/speed) as well as memory efficiency, at least as best we can manage with a garbage collected language such as Java.

In terms of it being free and open source, we mean that anyone can do pretty much whatever they want with it (including producing proprietary software) and can make 
extensions or modifications based on their needs using the open source code.

## Roadmap

### Tadukoo Util
> **Note**: Tadukoo Util is meant as a collection of utility libraries for very common use. For more information about Tadukoo Util, see the 
[Tadukoo Util](project/TadukooUtil.html) page.

#### First Release: Alpha v.0.1
The current plan for Alpha v.0.1 is to complete the following:
- Finish Tadukoo Look & Feel
- Write Unit Tests for all of Tadukoo Lang and some of the other modules
- Write a few more utilities
> **Note**: This list will be updated in the near future to be more detailed

### Tadukoo Engine/Launcher
> **Note**: Tadukoo Engine and Tadukoo Launcher go hand-in-hand. Tadukoo Engine is used as a base for programs made to run in the Tadukoo Launcher. Having a common launcher 
makes it easier to handle common dependencies across projects. For more information about Tadukoo Engine and Tadukoo Launcher, see the 
[Tadukoo Engine](project/TadukooEngine.html) page.

#### First Release: Alpha v.0.1
The current plan for Alpha v.0.1 is to complete the following:
- Create files for programs to tell the launcher what dependencies they need
- Create library files (for a list of officially supported libraries for easy dependency lookup)
- Create program library files (in order to populate the launcher dynamically with lists of programs rather than hard-code it)
> **Note**: This list will be updated in the near future to be more detailed
