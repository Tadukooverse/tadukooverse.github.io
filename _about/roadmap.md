---
title: Roadmap
blurb: An overview of current plans for Tadukooverse and our projects
summary: An overview of current plans for Tadukooverse and our projects, along with links to more detailed plans
---

> **Note**: This page is under construction and likely to change

#### Table of Contents
* [Vision](#vision)
* [Roadmap](#roadmap)
	* [General Tadukooverse](#general-tadukooverse)
	* [Tadukooverse Master Plan](#tadukooverse-master-plan)
		* [Tadukoo Util](#tadukoo-util)
		* [Tadukoo Parsing](#tadukoo-parsing)
		* [Tadukoo Web Services](#tadukoo-web-services)
		* [Tadukoo GitHub](#tadukoo-github)
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

Most of this is done now, but the [Contributing Guidelines](/community/CONTRIBUTING.html) could use some changes yet:
* Add note about not committing to master and a link to a guide on how we use branches
  * Guide should exist on this website
* Add actual links to Tadukoo Engine/Launcher guide and Debugging Guide
  * Note: These guides should be made on this website

#### tadukooverse.github.io
[tadukooverse.github.io](https://github.com/Tadukooverse/tadukooverse.github.io) is the repository to hold the GitHub pages website for the Tadukooverse organization.

##### Guides Section
* Branching Guide - guide on how we use branches on GitHub and don't commit directly to master
* Debugging Guide - guide on how to debug issues in the software - may need to be multiple guides for specific programs in the future?
* Tadukoo Engine/Launcher Guide - guide on how to develop against the engine/launcher - and a guide on how to use it?

##### Projects Section
* **Note**: These projects need more information on them
* [Tadukoo Engine](/project/TadukooEngine.html)
* [Tadukoo Util](/project/TadukooUtil.html)

#### Projects to Transfer
Currently, the projects that will be present in Tadukooverse are under control of me (Tadukoo). I want to move them to the Tadukooverse organization so that others can more easily contribute and use what I'm working on, and as a means to have 
everything organized better via this website.

I currently plan to move the following projects to Tadukooverse over time (not all at once) (note that most of them are in early development):
* [Tadukoo Util](https://github.com/Tadukoo/TadukooUtil)
* [Tadukoo Engine](https://github.com/Tadukoo/TadukooEngine)
* Old Tadukoo Util - currently private, is to be used for deprecated old libraries that probably shouldn't be used (as there are better options)
* Tadukoo Parsing - currently private, will be used for parsing libraries, e.g. JSON
* Tadukoo Web Services - currently private, will be used as a library for communicating with web services, particularly REST services at first
* [Tadukoo Genealogy](https://github.com/Tadukoo/TadukooGenealogy) - meant to be a free genealogy program that allows for plugins
* My Minecraft/Bukkit plugin projects - multiple projects, these are likely far away from being moved as they're in a weird state and I'll probably focus on Tadukoo Util and Engine/Launcher along with their libraries and programs before 
going back to working on Minecraft stuff

### Tadukooverse Master Plan
> **Note**: [The Tadukooverse Master Plan (Blog Post)]({%post_url 2020-08-14-the-tadukooverse-master-plan %}) will be kept updated for the general overview and updates, and the individual project pages will have more specific details.

A new plan has been devised leading up to release v.1.0 of several projects. The following projects will all be tied together for their v.1.0 release (but no other releases leading up to that). 
The basic idea of the plan is that the Tadukoo Engine/Launcher v.1.0 release will dictate what gets included in the other projects for their v.1.0 release.

#### Tadukoo Util
> **Note**: Tadukoo Util is meant as a collection of utility libraries for very common use. For more information about Tadukoo Util, see the 
[Tadukoo Util](/project/TadukooUtil.html) page.

The current Tadukoo Util plan includes 5 major milestones along with the v.1.0 release:
- Alpha v.0.1 - Finish Up Tadukoo Annotation Processor, Tadukoo Lang, and Tadukoo Util (basically just Javadocing and testing)
- Alpha v.0.2 - Complete Tadukoo Look & Feel
- Alpha v.0.3 - Complete Tadukoo View
- Alpha v.0.4 - Complete Tadukoo Database
- Beta v.0.5 - Complete Tadukoo File Format
- Release v.1.0 - Beta v.0.5 + anything else to be added for the Tadukoo Engine/Launcher v.1.0 requirements

**Note**: [Tadukoo Util's project page](/projects/TadukooUtil.html#current-plans) includes more specifics about these plans.

#### Tadukoo Parsing
> **Note**: Tadukoo Parsing is meant as a collection of libraries for parsing different formats (e.g. JSON, XML, etc.).

More details (and project page) for Tadukoo Parsing coming soon.

#### Tadukoo Web Services
> **Note**: Tadukoo Web Services is meant as a collection of libraries for interfacing with different web services (e.g. REST services).

More details (and project page) for Tadukoo Web Services coming soon.

#### Tadukoo GitHub
> **Note**: Tadukoo GitHub is meant as a library (/libraries) for interfacing with the GitHub REST API.

More details (and project page) for Tadukoo GitHub coming soon.

#### Tadukoo Engine/Launcher
> **Note**: Tadukoo Engine and Tadukoo Launcher go hand-in-hand. Tadukoo Engine is used as a base for programs made to run in the Tadukoo Launcher. Having a common launcher 
makes it easier to handle common dependencies across projects. For more information about Tadukoo Engine and Tadukoo Launcher, see the 
[Tadukoo Engine](project/TadukooEngine.html) page.

Tadukoo Engine/Launcher isn't currently broken down in the Tadukooverse Master Plan (it needs more thought put into it), so here's the list of stuff to be done:
- Running and terminating programs
- Making the launcher able to auto-update
- Handling informational files
- Downloading files
- Handling dependencies
- Allow installation on Windows, Mac, and Linux

**Note**: [Tadukoo Engine/Launcher's project page](/projects/TadukooEngine.html#current-plans) includes more specifics about these plans.
