---
short_name: TadukooUtil
title: Tadukoo Util
blurb: Tadukoo Util is meant as a collection of utility libraries for very common use.
summary: >
  Tadukoo Util is meant as a collection of utility libraries for very common use. They can be used in conjunction with Tadukoo Engine/Launcher, or can be used separately in other programs if desired. 
  This collection is not meant as a full smorgasbord of all libraries, but is just meant to include the most common libraries to be reused in most projects 
  (e.g. common null-safe string/boolean checks, multimaps, throwing functional interfaces, etc.)
version: Alpha v.0.2.2
github: https://github.com/Tadukooverse/TadukooUtil
changelog:
- alpha: 
  - version: Alpha v.0.1
    blurb: Finish Up Tadukoo Annotation Processor, Tadukoo Lang, and Tadukoo Util
    released: September 5, 2020 8:01 PM
    details: 'Alpha v.0.1 of Tadukoo Util - Tadukoo Annotation Processor, Tadukoo Lang, and Tadukoo Util
- This release represents the first release for Tadukoo Util of the following modules:
  - Tadukoo Annotation Processor - provides @AnnotationProcessor and AnnotationUtil for making Annotations
  - Tadukoo Lang - provides common basic utilities such as StringUtil and Tuples
  - Tadukoo Util - provides common utilities that are more advanced, such as MultiMap, ManyToManyMap, and Throwing Functional Interfaces
- While the following modules are included, they should not be considered officially released with this release, and will be completed in future Alpha releases leading up to Beta. 
Use them at your own risk, understanding they may change entirely.
  - Tadukoo Database - utilities for communicating with a SQL database
  - Tadukoo File Format - allows you to create your own file formats
  - Tadukoo Look & Feel - a customizable Look & Feel
  - Tadukoo View - common view utilities

The first set of modules will be fully supported, while the second set will not. Tadukoo Util (the project) is in kind of a weird state at the moment, See 
[the Tadukooverse Master Plan](http://tadukooverse.github.io/blog/2020/08/14/the-tadukooverse-master-plan.html) for more details on what''s going on.

Due to some weird things going on with the plan, this version has the version string 0.1-Alpha-SNAPSHOT for the purposes of Maven, and will only be available in the snapshots 
repository of Maven Central, and not in the official releases repository. Also, this is why the jars themselves have "-SNAPSHOT" in them.'
---
## Modules
### Tadukoo Functions
Tadukoo Functions provides throwing functional interfaces.

### Tadukoo Lang
Tadukoo Lang provides common utility functions along with tuples.

### Tadukoo Util
Tadukoo Util provides a collection of useful utilities.

## Current Plans
As part of [The Tadukooverse Master Plan](/about/Tadukooverse-Master-Plan.html), Tadukoo Util has 5 milestones leading up to its v.1.0 release:
- Alpha v.0.1 - Finish Up Tadukoo Annotation Processor, Tadukoo Lang, and Tadukoo Util (basically just Javadocing and testing)
- Alpha v.0.2 - Complete Tadukoo Look & Feel
- Alpha v.0.3 - Complete Tadukoo View
- Alpha v.0.4 - Complete Tadukoo Database
- Beta v.0.5 - Complete Tadukoo File Format
- Release v.1.0 - Beta v.0.5 + anything else to be added for the Tadukoo Engine/Launcher v.1.0 requirements

### Alpha v.0.1 - Finish Up Tadukoo Annotation Processor, Tadukoo Lang, and Tadukoo Util
> [GitHub Milestone]({{page.github}}/milestone/1)

Tadukoo Annotation Processor, Tadukoo Lang, and Tadukoo Util are acceptable in their current code state, but are not fully Javadoc'd and tested yet.

### Alpha v.0.2 - Complete Tadukoo View
> [GitHub Milestone]({{page.github}}/milestone/2)

To complete Tadukoo View, the following should be done:
- Make it possible for customizations in Tadukoo Look & Feel
  - Gradient builders to support custom painting
  - Font package to support custom fonts
- Create Forms (panel/frame used to store information for a pojo/piece of data to be easily converted to database or file format)
- Move some more utils from OldTadukooView to the new version

#### Other (More Minor) Changes
- Some Tadukoo Lang changes
  - Fix LoggerUtil.createFileLogger to append instead of recreating the file
  - Create zip and unzip functions in FileUtil
- Some Tadukoo Util changes
  - Create EasyLogger to make logging easier
- Remove .github folder (should've been done in Alpha v.0.1)

### Alpha v.0.3 - Complete Tadukoo Look & Feel
> [GitHub Milestone]({{page.github}}/milestone/3)

Tadukoo Look & Feel has two major packages - the components package and the actual look and feel package.

The Look & Feel package needs to be able to completely replace the Metal Look & Feel, mimicking its functionality with much more customizability.

The Components package is being created to allow for UI components to specify their own colors/shapes/etc. beyond the defaults provided by the Tadukoo Look & Feel's theme. 
Ideally this should be done through a combination of interfaces and component extensions. The interfaces would allow other users to create their own custom components that 
use these customizations if they desire.


### Alpha v.0.4 - Complete Tadukoo Database
> [GitHub Milestone]({{page.github}}/milestone/4)

Tadukoo Database seems to be in a weird state at the moment and needs some planning done on it. The general plan is to make it simple to setup queries that are sanitized.

### Beta v.0.5 - Complete Tadukoo File Format
> [GitHub Milestone]({{page.github}}/milestone/5)

Tadukoo File Format is in a similar boat with Tadukoo Database, in the sense that it needs some planning done.

### Release v.1.0
Right now there are no plans to add anything after Beta v.0.5, but depending on Tadukoo Engine/Launcher's v.1.0 requirements, more could be added here.
