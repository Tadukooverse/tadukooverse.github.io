---
short_name: TadukooUtil
title: Tadukoo Util
blurb: Tadukoo Util is meant as a collection of utility libraries for very common use.
summary: >
  Tadukoo Util is meant as a collection of utility libraries for very common use. They can be used in conjunction with Tadukoo Engine/Launcher, or can be used separately in other programs if desired. 
  This collection is not meant as a full smorgasbord of all libraries, but is just meant to include the most common libraries to be reused in most projects 
  (e.g. common null-safe string/boolean checks, multimaps, view utilities, etc.)
---

#### Table of Contents
* [Modules](#modules)
	* [Tadukoo Annotation Processor](#tadukoo-annotation-processor)
	* [Tadukoo Database](#tadukoo-database)
	* [Tadukoo File Format](#tadukoo-file-format)
	* [Tadukoo Lang](#tadukoo-lang)
	* [Tadukoo Look & Feel](#tadukoo-look--feel)
	* [Tadukoo Util](#tadukoo-util)
	* [Tadukoo View](#tadukoo-view)
* [Current Plans](#current-plans)

## Modules

### Tadukoo Annotation Processor
Tadukoo Annotation Processor makes it easier to create annotation processors.

It contains the @AnnotationProcessor annotation, which should be used in annotation processors so they're properly added to the META_INF services file.
This annotation is handled by AnnotationProcessorProcessor, which just adds the canonical class name to the META_INF/services/javax.annotation.processing.Processor file.

AbstractAnnotationProcessor should be extended by annotation processors you create. It handles the standard methods and provides an instance of AnnotationUtil to make common 
functionality easier for processing annotations.

For more information on creating annotation processors using Tadukoo Annotation Processor, check out the [Tadukoo Annotation Processor Guide](/guides/tadukoo-annotation-processor.html)

### Tadukoo Database
Tadukoo Database is used to make interfacing with a MySQL database easier.

### Tadukoo File Format
Tadukoo File Format is used to handle custom file formats.

### Tadukoo Lang
Tadukoo Lang provides common utility functions along with tuples.

### Tadukoo Look & Feel
Tadukoo Look & Feel allows you to customize the look & feel of view components more easily than the default Java look & feels allow for.

### Tadukoo Util
Tadukoo Util provides a collection of useful utilities that don't quite fit into other specific modules in this list.

### Tadukoo View
Tadukoo View provides utilities to make it easier to handle view functionality, such as drawing to the screen and handling images.

## Current Plans
> **[Main Page/Progress](https://github.com/Tadukoo/TadukooUtil/milestone/1)**

Currently, progress is moving forward on the first release of Tadukoo Util, Alpha v.0.1.

The overall goals are:
- Complete Tadukoo Database
- Complete Tadukoo File Format
- Complete Tadukoo Look & Feel
- Complete Tadukoo View
- Javadoc and test most (/all?) of the classes and packages

**Note**: Tadukoo Annotation Processor, Tadukoo Lang, and Tadukoo Util are acceptable in their current code state (but may need Javadoc'd and/or tested yet). It is 
acceptable to add more to them, as long as they are properly Javadoc'd and tested by release.

### Complete Tadukoo Database
Tadukoo Database seems to be in a weird state at the moment and needs some planning done on it. The general plan is to make it simple to setup queries that are sanitized.

### Complete Tadukoo File Format
Tadukoo File Format is in a similar boat with Tadukoo Database, in the sense that it needs some planning done.

### Complete Tadukoo Look & Feel
Tadukoo Look & Feel has two major packages - the components package and the actual look and feel package.

The Look & Feel package needs to be able to completely replace the Metal Look & Feel, mimicking its functionality with much more customizability.

The Components package is being created to allow for UI components to specify their own colors/shapes/etc. beyond the defaults provided by the Tadukoo Look & Feel's theme. 
Ideally this should be done through a combination of interfaces and component extensions. The interfaces would allow other users to create their own custom components that 
use these customizations if they desire.

### Complete Tadukoo View
To complete Tadukoo View, the following should be done:
- Create Forms (panel/frame used to store information for a pojo/piece of data to be easily converted to database or file format)
- Move some more utils from OldTadukooView to the new version

### Javadocing and Testing
Some of the classes and packages are already Javadoc'd, but ideally all of them would be.

In terms of testing, Tadukoo Lang has most of the tests at the moment, as testing has been neglected for a while in other areas.
