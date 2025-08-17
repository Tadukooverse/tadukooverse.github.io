---
short_name: TadukooAnnotations
title: Tadukoo Annotations
blurb: Tadukoo Annotations is a collection of annotations and utilities for creating annotations easier.
summary: Tadukoo Annotations is a collection of annotations and utilities for creating annotations easier.
version: Alpha v.0.2.2
github: https://github.com/Tadukooverse/TadukooAnnotations
---
## Modules
### Tadukoo Annotation Processor
Tadukoo Annotation Processor makes it easier to create annotation processors.

It contains the @AnnotationProcessor annotation, which should be used in annotation processors so they're properly added
to the META_INF services file. This annotation is handled by AnnotationProcessorProcessor, which just adds the canonical
class name to the META_INF/services/javax.annotation.processing.Processor file.

AbstractAnnotationProcessor should be extended by annotation processors you create. It handles the standard methods and
provides an instance of AnnotationUtil to make common functionality easier for processing annotations.

For more information on creating annotation processors using Tadukoo Annotation Processor, check out the
[Tadukoo Annotation Processor Guide](https://tadukooverse.github.io/guides/tadukoo-annotation-processor.html)

### Tadukoo Annotations
Tadukoo Annotations is a collection of annotations.

## Current Plans
There are no current plans for Tadukoo Annotations (it may not be worked on until the engine/launcher is completed)
