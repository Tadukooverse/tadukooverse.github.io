---
layout: default
title: Roadmap
---

> **Note**: This page is under construction and likely to change

#### Table of Contents
[Vision](#vision)

[Roadmap](#roadmap)
* [General Tadukooverse](#general-tadukooverse)
* [Tadukoo Util](#tadukoo-util)
* [Tadukoo Engine/Launcher](#tadukoo-enginelauncher)

## Vision
Our vision is to create efficient free and open source software.

In terms of efficiency, we mean both via code efficiency (/speed) as well as memory efficiency, at least as best we can manage with a garbage collected language such as Java.

In terms of it being free and open source, we mean that anyone can do pretty much whatever they want with it (including producing proprietary software) and can make 
extensions or modifications based on their needs using the open source code.

## Roadmap

### General Tadukooverse
> **Note**: This section is mainly to deal with how we get from nothing to the early stages of Tadukooverse

#### .github
[.github](https://github.com/Tadukooverse/.github) is the repository to hold the [Community Health Files](https://docs.github.com/en/github/building-a-strong-community/creating-a-default-community-health-file) for the Tadukooverse organization.

We plan to include the following files (note: some links may not work due to the files not existing yet):
* [Code of Conduct](/community/CODE_OF_CONDUCT.html)
* [Contributing Guidelines](/community/CONTRIBUTING.html)
* [Issue Templates](https://github.com/Tadukooverse/.github/.github/ISSUE_TEMPLATE)
* [Pull Request Templates](https://github.com/Tadukooverse/.github/.github/PULL_REQUEST_TEMPLATE)
* [Security Policy](/community/SECURITY.md)
* [Support Resources](/community/SUPPORT.md)

#### tadukooverse.github.io
[tadukooverse.github.io](https://github.com/Tadukooverse/tadukooverse.github.io) is the repository to hold the GitHub pages website for the Tadukooverse organization.

It'll have the following sections:
* [About](/about.html) - used for general pages about the Tadukooverse organization
* [Blog](/blog.html) - used for blogging/updates for the Tadukooverse organization
* [Community](/community.html) - used to link to the default community pages from the .github repo
* [Projects](/projects.html) - used for pages about the various projects on Tadukooverse

##### About Section
* [FAQ](/about/faq.html) - For frequently asked questions
* **Roadmap** - this page, for current major goals

##### Blog Section
* TBD (don't have a solid plan on this yet, but I do want to have an updates/history/information section on the website)

##### Community Section
* Updated via the .github repo

##### Projects Section
* [Tadukoo Engine](/project/TadukooEngine.html)
* [Tadukoo Util](/project/TadukooUtil.html)

#### Projects to Transfer
Currently, the projects that will be present in Tadukooverse are under control of me (Tadukoo). I want to move them to the Tadukooverse organization so that others can more easily contribute and use what I'm working on, and as a means to have everything organized better via this website.

I currently plan to move the following projects to Tadukooverse over time (not all at once) (note that most of them are in early development):
* [Tadukoo Util](https://github.com/Tadukoo/TadukooUtil)
* [Tadukoo Engine](https://github.com/Tadukoo/TadukooEngine)
* Old Tadukoo Util - currently private, is to be used for deprecated old libraries that probably shouldn't be used (as there are better options)
* Tadukoo Parsing - currently private, will be used for parsing libraries, e.g. JSON
* Tadukoo Web Services - currently private, will be used as a library for communicating with web services, particularly REST services at first
* [Tadukoo Genealogy](https://github.com/Tadukoo/TadukooGenealogy) - meant to be a free genealogy program that allows for plugins
* My Minecraft/Bukkit plugin projects - multiple projects, these are likely far away from being moved as they're in a weird state and I'll probably focus on Tadukoo Util and Engine/Launcher along with their libraries and programs before going back to working on Minecraft stuff

### Tadukoo Util
> **Note**: Tadukoo Util is meant as a collection of utility libraries for very common use. For more information about Tadukoo Util, see the 
[Tadukoo Util](/project/TadukooUtil.html) page.

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
> **[Main Page/Progress](https://github.com/Tadukoo/TadukooEngine/milestone/1)**
The current plan for Alpha v.0.1 is to complete the following:
- Allow the launcher to successfully launch and terminate programs
- Allow the launcher to download programs and libraries (using GitHub releases for now)
- Create files for programs to tell the launcher what dependencies they need (program description files)
- Create library description files (for information the launcher needs about the libraries, how to get them, and their dependencies)
- Create program library files (in order to populate the launcher dynamically with lists of programs rather than hard-code it)
- The downloader should download and run the installer (currently just plans for Windows installer, since I don't have Mac or Linux)
	- There will be instructions to run it on Mac/Linux
- Allow the launcher to update itself using the GitHub releases
> **Note**: This list will be updated in the near future to be more detailed
