---
title: Tadukooverse Master Plan
note: "Note: If you don't see a project on this page, it should be in the [Other Project Plans](/about/other-project-plans.html)"
blurb: The current master plan for Tadukooverse
summary: The current master plan for Tadukooverse. This contains the main plans for Tadukooverse projects.
current_work:
  TadukooMaven: Not currently working on it - everything done?
  TadukooUtil: Working on Beta v.0.7
  TadukooJava: Working on Beta v.0.6
  UltimatePower: Working on Alpha v.0.3
  TadukooView: Working on Alpha v.0.4
  TadukooForm: Working on Alpha v.0.4
  TadukooLookAndFeel: Working on Alpha v.0.4
  TadukooParsing: Working on Alpha v.0.4
  TadukooWebServices: Working on Alpha v.0.2
  TadukooGitHub: Working on Alpha v.0.2
  TadukooEngine: Working on Alpha v.0.1
upcoming_versions:
  TadukooMaven: 
  - Beta v.0.6+ - TBA?
  TadukooUtil:
  - Others TBA
  - Release v.1.0 - Prepare for Tadukoo Engine/Launcher v.1.0
  TadukooView:
  - Alpha v.0.4 - Complete Look & Feel Pieces Used in Form/Components
  - Others TBA
  - Release v.1.0 - Prepare for Tadukoo Engine/Launcher v.1.0
  TadukooParsing:
  - Others TBA
  - Release v.1.0 - Prepare for Tadukoo Engine/Launcher v.1.0
  TadukooWebServices:
  - Alpha v.0.2 - Complete Tadukoo SOAP
  - Others TBA
  - Release v.1.0 - Prepare for Tadukoo Engine/Launcher v.1.0
  TadukooGitHub:
  - Others TBA
  - Release v.1.0 - Prepare for Tadukoo Engine/Launcher v.1.0
  TadukooEngine:
  - Alpha v.0.1 - Informational files
  - Alpha v.0.2 - Auto-Updating
  - Beta v.0.? - TBA
  - Release v.1.0 - Needs Planning
---
{% assign TadukooAnnotations = site.projects | where:"short_name", "TadukooAnnotations" | first %}
{% assign TadukooCodeParsing = site.projects | where:"short_name", "TadukooCodeParsing" | first %}
{% assign TadukooDatabase = site.projects | where:"short_name", "TadukooDatabase" | first %}
{% assign TadukooEngine = site.projects | where:"short_name", "TadukooEngine" | first %}
{% assign TadukooForm = site.projects | where:"short_name", "TadukooForm" | first %}
{% assign TadukooGitHub = site.projects | where:"short_name", "TadukooGitHub" | first %}
{% assign TadukooJava = site.projects | where:"short_name", "TadukooJava" | first %}
{% assign TadukooLookAndFeel = site.projects | where:"short_name", "TadukooLookAndFeel" | first %}
{% assign TadukooMaven = site.projects | where:"short_name", "TadukooMaven" | first %}
{% assign TadukooParsing = site.projects | where:"short_name", "TadukooParsing" | first %}
{% assign TadukooUtil = site.projects | where:"short_name", "TadukooUtil" | first %}
{% assign TadukooView = site.projects | where:"short_name", "TadukooView" | first %}
{% assign TadukooWebServices = site.projects | where:"short_name", "TadukooWebServices" | first %}
{% assign UltimatePower = site.projects | where:"short_name", "UltimatePower" | first %}
{% assign master_projects = "TadukooMaven,TadukooUtil,TadukooJava,UltimatePower,TadukooView,TadukooForm,TadukooLookAndFeel,TadukooParsing,TadukooWebServices,TadukooGitHub,TadukooEngine" | split:"," %}
## Plans
### Overview
The current goal with the Tadukooverse Master Plan is to get to release v.1.0 of [{{TadukooEngine.title}}]({{TadukooEngine.url}}). To get there, we need to get to Java 17, make some changes to the engine, and 
reach release v.1.0 (or higher) of the following projects:
{% for master_project in master_projects -%}
{% assign project = site.projects | where:"short_name", master_project | first %}
* [{{project.title}}]({{project.url}})
{%- endfor %}

Java 17 is being required because it's an LTS (long-term support) release and we want to use features of Java 14+

Release v.1.0+ of the other projects is required because that means they'll include backwards compatibility moving forward, which will allow the engine to have backwards compatibility too.

### [{{TadukooMaven.title}}]({{TadukooMaven.url}})
{{TadukooMaven.summary}}

The current goals for Tadukoo Maven are the following:
* Parent POMs to be used by libraries and programs
  * Tadukoo Maven Base POM - base POM for all projects, to provide Maven, JaCoCo, and Central Repo plugins as well as JUnit dependencies
  * Tadukoo Maven Library POM - base POM for library projects that directly use [{{TadukooUtil.title}}]({{TadukooUtil.url}})
  * Tadukoo Maven Parsing POM - base POM for parsing projects that directly use [{{TadukooParsing.title}}]({{TadukooParsing.url}})
  * Tadukoo Maven Web Service POM - base POM for web service projects that directly use [{{TadukooWebServices.title}}]({{TadukooWebServices.url}})
  * Tadukoo Maven View POM - base POM for view projects that directly use [{{TadukooView.title}}]({{TadukooView.url}})
  * Tadukoo Maven Program POM - base POM for program projects that directly use [{{TadukooEngine.title}}]({{TadukooEngine.url}})
* Maven Archetypes to be used for libraries and programs
  * TBA

### [{{TadukooUtil.title}}]({{TadukooUtil.url}})
{{TadukooUtil.summary}}

The current goals for Tadukoo Util are the following:
* TBA

### [{{TadukooJava.title}}]({{TadukooJava.url}})
{{TadukooJava.summary}}

The current goals for Tadukoo Java are the following:
* TBA

### [{{UltimatePower.title}}]({{UltimatePower.url}})
{{UltimatePower.summary}}

The current goals for Ultimate Power are the following:
* TBA

### [{{TadukooView.title}}]({{TadukooView.url}})
{{TadukooView.summary}}

The current goals for Tadukoo View are the following:
* TBA

### [{{TadukooParsing.title}}]({{TadukooParsing.url}})
{{TadukooParsing.summary}}

The current plans for Tadukoo Parsing are the following:
* TBA

### [{{TadukooWebServices.title}}]({{TadukooWebServices.url}})
{{TadukooWebServices.summary}}

The current goals for Tadukoo Web Services are the following:
* TBA

### [{{TadukooGitHub.title}}]({{TadukooGitHub.url}})
{{TadukooGitHub.summary}}

The current goals for Tadukoo GitHub are the following:
* TBA

### [{{TadukooAnnotations.title}}]({{TadukooAnnotations.url}})
{{TadukooAnnotations.summary}}

The current goals for Tadukoo Annotations are the following:
* TBA

### [{{TadukooEngine.title}}]({{TadukooEngine.url}})
{{TadukooEngine.summary}}

The current goals for Tadukoo Engine/Launcher are the following:
* Running and terminating programs
* Making the launcher able to auto-update
* Handling informational files
* Downloading files
* Handling dependencies
* Allow installation on Windows, Mac, and Linux

## Progress
> Last Updated: August 16, 2025 8:44 PM

{% for master_project in master_projects %}
{% assign current_work = page.current_work[master_project] %}
{% assign project = site.projects | where:"short_name", master_project | first %}
### [{{project.title}}]({{project.url}})
> {% include text-color.html color="yellow" text=current_work %}
{%- assign changelogs = site.changelogs | where:"project", master_project | sort -%}
{% for changelog in changelogs -%}
{% assign logs = changelog.changelog | reverse -%}
{% for log in logs -%}
{% assign log_text = log.version | append: " - " | append: log.blurb | append: " - Released " | append: log.released %}
* {% include text-color.html color="lime" text=log_text %}
{%- endfor %}
{%- endfor %}
{%- assign upcoming_versions = page.upcoming_versions[master_project] -%}
{% for upcoming_version in upcoming_versions %}
* {% include text-color.html color="red" text=upcoming_version %}
{%- endfor %}
{% endfor %}

## History
### Prior to the Master Plan
Prior to the Tadukooverse Master Plan, the plan was just to make a new jar called Tadukoo Util with a few utilities for use in projects. Eventually, that project got loaded with more jars 
for various small libraries I was working on (namely the annotation processor, MySQL, file format, view, and look & feel libraries). After that, the idea for the engine came about to 
provide the libraries for programs to use and to make a launcher for those programs.

### The Original Plan - August 14, 2020
In the original Tadukooverse Master Plan, the plan was just to split the current plans for [{{TadukooUtil.title}}]({{TadukooUtil.url}}) and [{{TadukooEngine.title}}]({{TadukooEngine.url}}) into 
multiple releases leading up to their respective release v.1.0 releases, as well as adding the plans for [{{TadukooParsing.title}}]({{TadukooParsing.url}}), 
[{{TadukooWebServices.title}}]({{TadukooWebServices.url}}), and [{{TadukooGitHub.title}}]({{TadukooGitHub.url}}). The idea for these other libraries was to provide support for releasing programs 
via GitHub, using the GitHub REST API (hence needing REST in the Web Services), and that API uses JSON (hence JSON parsing in the Parsing project).

### Release v.1.0 Tying - September 2, 2020
At this point, [{{TadukooUtil.title}}]({{TadukooUtil.url}}) and [{{TadukooEngine.title}}]({{TadukooEngine.url}}) had their release v.1.0 versions tied together (for them to be released at the same 
time, but other projects would not have their v.1.0 releases at the same time (and likely would have them sometime after this).

### Splitting Tadukoo Util - December 16, 2020
[{{TadukooUtil.title}}]({{TadukooUtil.url}}) had its libraries split into multiple projects.

[{{TadukooUtil.title}}]({{TadukooUtil.url}}) itself was changed to include 3 libraries:
* Tadukoo Lang - which includes the most basic utilities for working with common Java types like Booleans, Strings, Files, etc. and for having tuples
* Tadukoo Functions - which includes functional interfaces that can throw different Throwables
* Tadukoo Util - which includes other utilities

[{{TadukooView.title}}]({{TadukooView.url}}) was newly created, and includes 4 libraries (which came from Tadukoo View and Tadukoo Look & Feel from Tadukoo Util):
* Tadukoo View - for the most basic View utilities
* Tadukoo Components - for custom components for using custom paints, borders, etc.
* Tadukoo Form - for creating forms for users to input data
* Tadukoo Look & Feel - for a look & feel for custom paints, borders, etc.

[{{TadukooAnnotations.title}}]({{TadukooAnnotations.url}}) was newly created, and includes 2 libraries (which came from Tadukoo Annotation Processor and annotations from Tadukoo Util):
* Tadukoo Annotation Processor - which provides utilities for making annotations
* Tadukoo Annotations - which contains annotations

[{{TadukooDatabase.title}}]({{TadukooDatabase.url}}) was newly created, and includes 1 library (which came from Tadukoo Database from Tadukoo Util):
* Tadukoo MySQL - which is used to interact with a MySQL database

[{{TadukooParsing.title}}]({{TadukooParsing.url}}) was changed to include Tadukoo File Format from Tadukoo Util.

### More Projects - May 30, 2021
[{{TadukooMaven.title}}]({{TadukooMaven.url}}) was created, in order to make it easier to maintain Maven/Java/JUnit versions and such, and to make it easier to create new projects in the future.

[{{TadukooAnnotations.title}}]({{TadukooAnnotations.url}}) was re-added to this plan (it was removed because of thinking it wouldn't be used for the release of the engine). Once the engine and 
other projects reach release v.1.0+, they'll use annotations for noting backwards-compatibility-related changes.

[{{TadukooDatabase.title}}]({{TadukooDatabase.url}}) was removed from this plan (at least for now), because the engine itself doesn't require it.

[{{TadukooCodeParsing.title}}]({{TadukooCodeParsing.url}}) was created for Tadukoo Java to be moved to (out of Tadukoo Parsing).

[{{TadukooDatabase.title}}]({{TadukooDatabse.url}}) and [{{TadukooCodeParsing.title}}]({{TadukooCodeParsing.url}}) can be found on the [Other Project Plans page](/about/other-project-plans.html).

### 4 Years Changes/Releases Catchup - August 16, 2025
Now [{{TadukooCodeParsing.title}}]({{TadukooCodeParsing.url}}) is [{{TadukooJava.title}}]({{TadukooJava.url}}), and it's relevant for the plan again, because of [{{UltimatePower.title}}]({{UltimatePower.url}}) using it.

[{{UltimatePower.title}}]({{UltimatePower.url}}) is a new project that will be used to make custom annotations for generating simple code, similar to Lombok.
[{{UltimatePower.title}}]({{UltimatePower.url}}) requires Java parsing/generation to work, and it will be used by all projects other than [{{TadukooJava.title}}]({{TadukooJava.url}}) and 
[{{TadukooUtil.title}}]({{TadukooUtil.url}}). [{{UltimatePower.title}}]({{UltimatePower.url}}) is also effectively the replacement of [{{TadukooAnnotations.title}}]({{TadukooAnnotations.url}}).

Also in the past few years, [{{TadukooView.title}}]({{TadukooView.url}}) was split into 3 projects. [{{TadukooView.title}}]({{TadukooView.url}}) now just contains the basic utilities 
in View and Components modules. [{{TadukooForm.title}}]({{TadukooForm.url}}) is the form content, now split into 3 modules, Form Fields, Form, and Form Components. 
[{{TadukooLookAndFeel.title}}]({{TadukooLookAndFeel.url}}) is now its own project.
