---
title: Tadukoo Parsing Alpha Changelog
project: TadukooParsing
version_range: Alpha
blurb: Tadukoo Parsing's Alpha changelog
changelog:
- version: Alpha v.0.3.2
  blurb: Java 17
  released: November 19, 2021 10:33 PM
  github: https://github.com/Tadukooverse/TadukooParsing/releases/tag/0.3.2-Alpha
  details: | 
    ### Technical/Other
    * Tadukoo Util updated to Beta v.0.5.1
    * Tadukoo Maven Library POM updated to Alpha v.0.3.1 (Java 17 + updated dependencies)
- version: Alpha v.0.3.1
  blurb: Update to Tadukoo Util Beta v.0.5 + Other Minor Changes
  released: July 10, 2021 7:54 PM
  github: https://github.com/Tadukooverse/TadukooParsing/releases/tag/v.0.3.1-Alpha
  details: | 
    ### Tadukoo JSON
    * JSONArray is now a List and has JSONArrayList as a default implementation
    * JSONConverter now includes parseFileFromJSON methods to make it easier to parse files
    * getJSONArrayItem methods in JSONClass, similar to getListItem methods in MappedPojo
    
    ### Tadukoo Java
    * Moved to [Tadukoo Code Parsing](/projects/TadukooCodeParsing)
    
    ### Technical/Other
    * Tadukoo Util updated to Beta v.0.5
    * Now using Tadukoo Maven (Alpha v.0.3)
- version: Alpha v.0.3
  blurb: Complete Tadukoo File Format
  released: April 24, 2021 11:00 PM
  github: https://github.com/Tadukooverse/TadukooParsing/releases/tag/v.0.3-Alpha
  details: | 
    ### Tadukoo Parsing
    * Moved TadFormatRegexConverter here (from Tadukoo File Format)
    
    ### Tadukoo File Format
    * Made various improvements and added JUnit testing
    
    ### Technical/Other
    * Tadukoo Util updated to Alpha v.0.4
    * Updated to Java 16
- version: Alpha v.0.2.3
  blurb: Updated Tadukoo Util to Alpha v.0.3.1 + Other Minor Changes
  released: February 6, 2021 6:43 PM
  github: https://github.com/Tadukooverse/TadukooParsing/releases/tag/v.0.2.3-Alpha
  details: | 
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
- version: Alpha v.0.2.2
  blurb: Moved Tadukoo File Format Over + Other Minor Changes
  released: December 13, 2020 9:18 PM
  github: https://github.com/Tadukooverse/TadukooParsing/releases/tag/v.0.2.2-Alpha
  details: | 
    This is an official release of the following module:
    - Tadukoo JSON - which has code for parsing JSON
    
    It is an unofficial release for the following modules:
    - Tadukoo Java - which has code for generating Java code
    - Tadukoo File Format - which is unfinished custom file parsing
    
    Basically Tadukoo File Format is moved over from Tadukoo Util and is currently the same as the Alpha v.0.2.1 release from over there. 
    Tadukoo Java is thrown in due to being in progress when this whole reorganization happened. Future releases will complete Tadukoo Java and Tadukoo File Format at some point.
- version: Alpha v.0.1
  blurb: Complete Tadukoo JSON
  released: November 10, 2020 6:11 PM
  github: https://github.com/Tadukooverse/TadukooParsing/releases/tag/v.0.1-Alpha
  details: | 
    Alpha v.0.1 of Tadukoo Parsing - Tadukoo JSON
    
    - This release includes Tadukoo JSON, a library for parsing JSON into/from pojos and lists
    
    This release is part of [the Tadukooverse Master Plan](/about/tadukooverse-master-plan.html) for making Tadukoo Engine/Launcher.
    
    This release is available on Maven Central.
---