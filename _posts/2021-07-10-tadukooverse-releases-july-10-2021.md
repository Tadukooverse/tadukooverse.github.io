---
title:  "Tadukooverse Releases July 10, 2021"
author: Tadukoo
date:   2021-07-10 21:00
series: "Releases"
index: 18
categories: blog
tags: 
- News
- Programming
comment_issue_id: 62
---
Multiple releases happened for Tadukooverse recently.

## Tadukoo Maven
Tadukoo Maven Alpha v.0.3 was [released on July 5](https://github.com/Tadukooverse/TadukooMaven/releases/tag/0.3-Alpha).

Tadukoo Maven is a collection of Maven poms and archetypes for use in Tadukooverse projects. It's released under the MIT license so it's very free for anyone to use for their projects. For more information about Tadukoo Maven, 
check out its [project page](/projects/TadukooMaven.html).

Tadukoo Maven contains the following modules:
* TadukooMavenBasePOM - the base pom for all projects
  * TadukooMavenLibraryPOM - a pom for use in Tadukooverse libraries that use Tadukoo Util
  * TadukooMavenParsingPOM - a pom for use in Tadukooverse libraries that use Tadukoo Parsing
  * TadukooMavenWebServicePOM - a pom for use in Tadukooverse libraries that use Tadukoo Web Services
  * TadukooMavenViewPOM - a pom for use in Tadukooverse projects that use Tadukoo View

Changes:
* Now includes Tadukoo JUnit dependencies

## Tadukoo Util
Tadukoo Util Beta v.0.5 was [released on July 5](https://github.com/Tadukooverse/TadukooUtil/releases/tag/0.5-Beta)

Tadukoo Util is a collection of useful utilities for any project. It's released under the MIT license so it's very free for anyone to use for their projects. For more information about 
Tadukoo Util, check out its [project page](https://tadukooverse.github.io/projects/TadukooUtil.html). For Javadocs for Tadukoo Util, visit [this page](https://tadukooverse.github.io/docs/TadukooUtil/current/index.html).

Tadukoo Util contains the following modules:
- Tadukoo Lang - provides common basic utilities such as StringUtil and Tuples
- Tadukoo Functions - provides ThrowingFunctions, ThrowingPredicates, etc. for better use than Java's non-throwing versions
- Tadukoo Util - provides common utilities that are more advanced, such as MultiMap, ManyToManyMap, and pojo classes

### Changes
#### Tadukoo Lang
##### File Util
New methods:
* BufferedReader setupFileReader(String filepath)
* BufferedReader setupFileReader(File file)
* boolean exists(String filepath)
* boolean exists(File file)
* boolean notExists(String filepath)
* boolean notExists(File file)
* String readAsString(String filepath)
* String readAsString(File file)
* List<String> readLinesAsList(String filepath)
* List<String> readLinesAsList(File file)
* List<String> getLinesAsList renamed to readLinesAsList(Reader reader)
* byte[] readAsBytes(String filepath)
* byte[] readAsBytes(File file)

##### Byte Util
Completely new

#### Tadukoo Util
##### Added ProgressReadableByteChannel and ProgressRBCWrapper
Used to track progress on a download/file read

##### Removed Table
It was just a List anyway

##### Mapped Pojo
New methods:
* boolean isEmpty()
* void clear()
* <T extends MappedPojo> T getPojoItemNoThrow(String key, Class<T> clazz)
* <T extends MappedPojo> T getPojoItemNoThrow(EasyLogger logger, String key, Class<T> clazz)
* <T extends MappedPojo> List<T> getListItemNoThrow(String key, Class<T> clazz)
* <T extends MappedPojo> List<T> getListItemNoThrow(EasyLogger logger, String key, Class<T> clazz)

#### Other/Technical
* Now using Tadukoo Maven Library POM as a parent pom - Alpha v.0.3 of it

## Tadukoo JUnit
Tadukoo JUnit Alpha v.0.1 was [released on July 5](https://github.com/Tadukooverse/TadukooJUnit/releases/tag/0.1-Alpha)

Tadukoo JUnit is a collection of useful utilities for JUnit testing. It's released under the MIT license so it's very free for anyone to use for their projects. For more information about 
Tadukoo JUnit, check out its [project page](https://tadukooverse.github.io/projects/TadukooJUnit.html). For Javadocs for Tadukoo JUnit, visit [this page](https://tadukooverse.github.io/docs/TadukooJUnit/current/index.html).

Tadukoo JUnit contains the following modules:
- Tadukoo JUnit - provides common utilities for JUnit testing

## Tadukoo Parsing
Tadukoo Parsing Alpha v.0.3.1 was [released today](https://github.com/Tadukooverse/TadukooParsing/releases/tag/v.0.3.1-Alpha)

Tadukoo Parsing is a collection of useful utilities for parsing different formats. It's released under the MIT license so it's very free for anyone to use for their projects. For more information about 
Tadukoo Parsing, check out its [project page](https://tadukooverse.github.io/projects/TadukooParsing.html). For Javadocs for Tadukoo Parsing, visit [this page](https://tadukooverse.github.io/docs/TadukooParsing/current/index.html).

The following modules are in Tadukoo Parsing:
- Tadukoo Parsing - basic parsing utilities to be used in the other modules
- Tadukoo JSON - which has code for parsing JSON
- Tadukoo File Format - which is unfinished custom file parsing

### Changes
#### Tadukoo JSON
* JSONArray is now a List and has JSONArrayList as a default implementation
* JSONConverter now includes parseFileFromJSON methods to make it easier to parse files
* getJSONArrayItem methods in JSONClass, similar to getListItem methods in MappedPojo

#### Tadukoo Java
* Moved to [Tadukoo Code Parsing](https://github.com/Tadukooverse/TadukooCodeParsing)

#### Technical/Other
* Tadukoo Util updated to Beta v.0.5
* Now using Tadukoo Maven (Alpha v.0.3)

## Tadukoo Web Services
Tadukoo Web Services Alpha v.0.1.2 was [released today](https://github.com/Tadukooverse/TadukooWebServices/releases/tag/0.1.2-Alpha)

Tadukoo Web Services is a collection of libraries for interacting with web services. It's released under the MIT license so it's very free for anyone to use for their projects. For more information about 
Tadukoo Web Services, check out its [project page](https://tadukooverse.github.io/projects/TadukooWebServices.html). For Javadocs for Tadukoo Web Services, visit [this page](https://tadukooverse.github.io/docs/TadukooWebServices/current/index.html).

The following modules are in Tadukoo Web Services:
- Tadukoo REST - used to interact with REST APIs

### Changes
#### Tadukoo Web Services
* JSONArrayBodyHandler improved based on JSONArray improvements in Tadukoo Parsing

#### Technical/Other
* Updated to Tadukoo Parsing Alpha v.0.3.1
* Now using Tadukoo Maven (Alpha v.0.3)

## Tadukoo GitHub
Tadukoo GitHub Alpha v.0.1.2 was [released today](https://github.com/Tadukooverse/TadukooGitHub/releases/tag/0.1.2-Alpha)

Tadukoo GitHub is a collection of libraries for interacting with GitHub's web services. It's released under the MIT license so it's very free for anyone to use for their projects. For more information about 
Tadukoo GitHub, check out its [project page](https://tadukooverse.github.io/projects/TadukooGitHub.html). For Javadocs for Tadukoo GitHub, visit [this page](https://tadukooverse.github.io/docs/TadukooGitHub/current/index.html).

The following modules are in Tadukoo GitHub:
- Tadukoo GitHub - used to interact with GitHub's REST API

### Changes
#### Tadukoo GitHub
* Updated pojos for minor changes (mainly testing changes due to Tadukoo JUnit)
* Updated endpoints with changes to JSONArrayBodyHandler (due to improvements from Tadukoo Web Services/Tadukoo Parsing)

#### Technical/Other
* Updated to Tadukoo Web Services Alpha v.0.1.2
* Now using Tadukoo Maven (Alpha v.0.3)

## Tadukoo Code Parsing
Tadukoo Code Parsing Alpha v.0.3.1 was [released today](https://github.com/Tadukooverse/TadukooCodeParsing/releases/tag/0.3.1-Alpha)

Tadukoo Code Parsing is a collection of useful utilities for parsing code. It's released under the MIT license so it's very free for anyone to use for their projects. For more information about 
Tadukoo Code Parsing, check out its [project page](https://tadukooverse.github.io/projects/TadukooCodeParsing.html). For Javadocs for Tadukoo Code Parsing, visit [this page](https://tadukooverse.github.io/docs/TadukooCodeParsing/current/index.html).

The following modules are in Tadukoo Code Parsing:
- Tadukoo Java - which has code for generating Java code

The main change here is that Tadukoo Java was moved here from Tadukoo Parsing. There have been some changes to it as well for new features.
