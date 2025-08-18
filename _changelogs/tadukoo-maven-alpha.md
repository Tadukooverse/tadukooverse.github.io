---
title: Tadukoo Maven Alpha Changelog
project: TadukooMaven
version_range: Alpha
blurb: Tadukoo Maven's Alpha changelog
changelog:
- version: Alpha v.0.4.2
  blurb: Tadukoo Maven Plugin POM, and Changed Settings
  released: August 31, 2023 7:20 PM
  github: https://github.com/Tadukooverse/TadukooMaven/releases/tag/0.4.2-Alpha
  details: | 
    * TadukooMavenPluginPOM created for Maven Plugins
    * Added Maven Compiler Release setting to TadukooMavenBasePOM - and this is now inherited
    * Updated JaCoCo to 0.8.10
    * Added Directory settings to TadukooMavenBasePOM, so you don't have to specify it for lower POMs
- version: Alpha v.0.4.1
  blurb: Fix for wrong Form GroupID
  released: March 25, 2023 6:25 PM
  github: https://github.com/Tadukooverse/TadukooMaven/releases/tag/0.4.1-Alpha
  details: | 
    * Fixes issue where TadukooMavenFormPOM had the wrong groupID (for the tadukoo.form.groupID property)
- version: Alpha v.0.4
  blurb: Tadukoo Maven JUnit, Form, EngineBase POMs and Test Jars
  released: March 25, 2023 5:45 PM
  github: https://github.com/Tadukooverse/TadukooMaven/releases/tag/0.4-Alpha
  details: |
    * Added TadukooMavenJUnitPOM and made it as the base of most of the other POMs
    * Added TadukooMavenFormPOM (since Tadukoo Form is now a separate project from Tadukoo View)
    * Added TadukooMavenEngineBasePOM as a base pom for Tadukoo Engine
    * Added maven-jar-plugin to TadukooMavenBasePOM to build test jars for projects by default in order to make it easier to reuse testing utils for specific projects 
    (this avoided duplicating code for Tadukoo Form between a JUnit jar and all the other modules)
- version: Alpha v.0.3.1
  blurb: Updated to Java 17, Updated Dependencies, and Tadukoo Maven Program pom
  released: November 19, 2021 9:42 PM
  github: https://github.com/Tadukooverse/TadukooMaven/releases/tag/0.3.1-Alpha
  details: | 
    * Updated to Java 17, updated various dependencies
    * Added Tadukoo Maven Program POM
- version: Alpha v.0.3
  blurb: Added Tadukoo JUnit Dependencies
  released: July 5, 2021 6:04 PM
  github: https://github.com/Tadukooverse/TadukooMaven/releases/tag/0.3-Alpha
  details: | 
    * Now includes Tadukoo JUnit dependencies
- version: Alpha v.0.2
  blurb: Tadukoo Maven Parsing, Web Service, and View poms
  released: May 29, 2021 7:47 PM
  github: https://github.com/Tadukooverse/TadukooMaven/releases/tag/0.2-Alpha
  details: | 
    Tadukoo Maven contains the following modules:
    - TadukooMavenBasePOM - the base pom for all projects
      - TadukooMavenLibraryPOM - a pom for use in Tadukooverse libraries that use Tadukoo Util
      - TadukooMavenParsingPOM - a pom for use in Tadukooverse libraries that use Tadukoo Parsing
      - TadukooMavenWebServicePOM - a pom for use in Tadukooverse libraries that use Tadukoo Web Services
      - TadukooMavenViewPOM - a pom for use in Tadukooverse projects that use Tadukoo View
- version: Alpha v.0.1
  blurb: Tadukoo Maven Base POM and Library POM
  released: May 28, 2021 6:56 PM
  github: https://github.com/Tadukooverse/TadukooMaven/releases/tag/0.1-Alpha
  details: | 
    Tadukoo Maven is a collection of Maven poms and archetypes for use in Tadukooverse projects. It's released under the MIT license so it's very free for anyone to use for their projects. 
    For more information about Tadukoo Maven, check out its [project page](/projects/TadukooMaven.html).
    
    Tadukoo Maven contains the following modules:
    - TadukooMavenBasePOM - the base pom for all projects
      - TadukooMavenLibraryPOM - a pom for use in Tadukooverse libraries that use Tadukoo Util
---