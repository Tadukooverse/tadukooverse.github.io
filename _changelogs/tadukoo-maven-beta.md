---
title: Tadukoo Maven Beta Changelog
project: TadukooMaven
version_range: Beta
blurb: Tadukoo Maven's Beta changelog
changelog:
- version: Beta v.0.5.2
  blurb: Updated Plugin Settings
  released: January 9, 2025 8:41 PM
  github: https://github.com/Tadukooverse/TadukooMaven/releases/tag/0.5.2-Beta
  details: | 
    * Updated Maven Plugin Settings in TadukooBasePOM (plugin API was wrong and goalPrefix is now specified explicitly)
- version: Beta v.0.5.1
  blurb: Updated Dependencies and Plugins
  released: December 18, 2024 10:36 PM
  github: https://github.com/Tadukooverse/TadukooMaven/releases/tag/0.5.1-Beta
  details: | 
    * Updated a bunch of dependency and plugin versions
    * Removed junit platform dependency (it causes JUnit tests to not run with the latest surefire plugin)
- version: Beta v.0.5
  blurb: Archetypes Added and Maven dropped from module names, etc.
  released: August 30, 2024 7:04 PM
  github: https://github.com/Tadukooverse/TadukooMaven/releases/tag/0.5-Beta
  details: | 
    * Made archetypes for each pom
    * Removed "Maven" from namings of POMs/Archetypes
    * Removed Maven Plugin POM (it's covered by base POM now)
    * Removed EngineBase POM (engine now uses Form POM and provides Look & Feel and GitHub in its pom)
    * Library POM is now for Ultimate Power instead of Util
    * Created Util POM
    * Created Java POM
---
