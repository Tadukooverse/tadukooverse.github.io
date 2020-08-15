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
As part of [The Tadukooverse Master Plan]({% post_url 2020-08-14-the-tadukooverse-master-plan %}), Tadukoo Util has 5 milestones leading up to its v.1.0 release:
- Alpha v.0.1 - Finish Up Tadukoo Annotation Processor, Tadukoo Lang, and Tadukoo Util (basically just Javadocing and testing)
- Alpha v.0.2 - Complete Tadukoo Look & Feel
- Alpha v.0.3 - Complete Tadukoo View
- Alpha v.0.4 - Complete Tadukoo Database
- Beta v.0.5 - Complete Tadukoo File Format
- Release v.1.0 - Beta v.0.5 + anything else to be added for the Tadukoo Engine/Launcher v.1.0 requirements

### Alpha v.0.1 - Finish Up Tadukoo Annotation Processor, Tadukoo Lang, and Tadukoo Util
Tadukoo Annotation Processor, Tadukoo Lang, and Tadukoo Util are acceptable in their current code state, but are not fully Javadoc'd and tested yet.

### Alpha v.0.2 - Complete Tadukoo Look & Feel
Tadukoo Look & Feel has two major packages - the components package and the actual look and feel package.

The Look & Feel package needs to be able to completely replace the Metal Look & Feel, mimicking its functionality with much more customizability.

The Components package is being created to allow for UI components to specify their own colors/shapes/etc. beyond the defaults provided by the Tadukoo Look & Feel's theme. 
Ideally this should be done through a combination of interfaces and component extensions. The interfaces would allow other users to create their own custom components that 
use these customizations if they desire.

### Alpha v.0.3 - Complete Tadukoo View
To complete Tadukoo View, the following should be done:
- Create Forms (panel/frame used to store information for a pojo/piece of data to be easily converted to database or file format)
- Move some more utils from OldTadukooView to the new version

### Alpha v.0.4 - Complete Tadukoo Database
Tadukoo Database seems to be in a weird state at the moment and needs some planning done on it. The general plan is to make it simple to setup queries that are sanitized.

### Beta v.0.5 - Complete Tadukoo File Format
Tadukoo File Format is in a similar boat with Tadukoo Database, in the sense that it needs some planning done.

### Release v.1.0
Right now there are no plans to add anything after Beta v.0.5, but dependning on Tadukoo Engine/Launcher's v.1.0 requirements, more could be added here.
