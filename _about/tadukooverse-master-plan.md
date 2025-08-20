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
  TadukooParsing: Working on Alpha v.0.4
  TadukooWebServices: Working on Alpha v.0.2
  TadukooGitHub: Working on Alpha v.0.2
  TadukooView: Working on Alpha v.0.4
  TadukooForm: Working on Alpha v.0.4
  TadukooLookAndFeel: Working on Alpha v.0.4
  TadukooEngine: Working on Alpha v.0.1
upcoming_versions:
  TadukooMaven: 
  - Others TBA
  TadukooUtil:
  - Beta v.0.7 - Non-Throwing/Int/Long/Double Functions and Throwing Streams
  - Others TBA
  TadukooJava:
  - Beta v.0.6 - Type Parameters, Varargs, and Static Code Blocks
  - Beta v.0.7 - Interfaces, Enums, Records, and Annotation Classes
  - Beta v.0.8 - Pure Java Code
  - Others TBA
  TadukooParsing:
  - Others TBA
  TadukooWebServices:
  - Alpha v.0.2 - Complete Tadukoo SOAP
  - Others TBA
  TadukooGitHub:
  - Others TBA
  TadukooView:
  - Alpha v.0.4 - Complete Look & Feel Pieces Used in Form/Components
  - Others TBA
  TadukooEngine:
  - Alpha v.0.1 - Informational files
  - Alpha v.0.2 - Auto-Updating
  - Beta v.0.? - TBA
  - Release v.1.0 - Needs Planning
current_plans:
  TadukooMaven:
  - item: Parent POMs to be used by libraries and programs
    color: lime
  - item: Maven Archetypes to be used for libraries and programs
    color: lime
  TadukooUtil:
  - item: Tadukoo Lang in a good state
    color: lime
  - item: Tadukoo Functions in a good state
    color: lime
  - item: Tadukoo Util in a good state
    color: lime
  - item: Tadukoo JUnit in a good state
    color: lime
  - item: Non-Throwing Functions (Beta v.0.7)
  - item: Int/Long/Double Functions (Beta v.0.7)
  - item: Throwing Streams (Beta v.0.7)
  TadukooJava:
  - item: Java Type (to handle types better) (Beta v.0.6)
  - item: Type Parameters (Beta v.0.6)
  - item: Varargs (Beta v.0.6)
  - item: Static Code Blocks (Beta v.0.6)
  - item: Interface Support (Beta v.0.7)
  - item: Enum Support (Beta v.0.7)
  - item: Record Support (Beta v.0.7)
  - item: Annotation Class Support (Beta v.0.7)
  - item: Greater parsing of code itself (within methods and such) (Beta v.0.8)
  UltimatePower:
  - item: TBA
  TadukooParsing:
  - item: TBA
  TadukooWebServices:
  - item: TBA
  TadukooGitHub:
  - item: TBA
  TadukooView:
  - item: TBA
  TadukooForm:
  - item: TBA
  TadukooLookAndFeel:
  - item: TBA
  TadukooEngine:
  - item: Running and terminating programs
  - item: Making the launcher able to auto-update
  - item: Handling informational files
  - item: Downloading files
  - item: Handling dependencies
  - item: Allow installation on Windows, Mac, and Linux
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
{% assign master_projects = "TadukooMaven,TadukooUtil,TadukooJava,UltimatePower,TadukooParsing,TadukooWebServices,TadukooGitHub,TadukooView,TadukooForm,TadukooLookAndFeel,TadukooEngine" | split:"," %}
## Plans
### Overview
The current goal with the Tadukooverse Master Plan is to get to release v.1.0 of [{{TadukooEngine.title}}]({{TadukooEngine.url}}). To get there, we need to get to Java 17, make some changes to the engine, and 
reach release v.1.0 (or higher) of the following projects:
{% for master_project in master_projects -%}
{% assign project = site.projects | where:"short_name", master_project | first %}
{% assign latest_changelog = site.changelogs | where:"project", master_project | last -%}
{% assign latest_log = latest_changelog.changelog | first -%}
{% assign latest_version = latest_log.version -%}
* [{{project.title}}]({{project.url}}) - {{latest_version}}
{%- endfor %}

Java 17 is being required because it's an LTS (long-term support) release and we want to use features of Java 14+

Release v.1.0+ of the other projects is required because that means they'll include backwards compatibility moving forward, which will allow the engine to have backwards compatibility too.

{% for master_project in master_projects -%}
{% assign project = site.projects | where:"short_name", master_project | first %}
{% assign current_plans = page.current_plans[master_project] %}
### [{{project.title}}]({{project.url}})
{{project.summary}}

The current goals for {{project.title}} are the following:
{% for plan in current_plans -%}
{% if plan.color -%}
* {% include text-color.html color=plan.color text=plan.item %}
{%- else -%}
* {{plan.item}}
{%- endif %}
{% endfor %}
{% endfor %}

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

### Tadukoo Util and Java Goals - August 19, 2025
Currently [{{TadukooUtil.title}}]({{TadukooUtil.url}}) only has 1 planned version: Beta v.0.7, which is coming along with [{{TadukooJava.title}}]({{TadukooJava.url}}) Beta v.0.6.
Those goals for [{{TadukooUtil.title}}]({{TadukooUtil.url}}) are:
* Non-Throwing Functions
* Int/Long/Double Functions
* Throwing Streams
* Some StringUtil changes for use in Java

[{{TadukooJava.title}}]({{TadukooJava.url}}) currently has 3 versions planned:
* Beta v.0.6
  * Java Type (to handle types better)
  * Type Parameters
  * Varargs
  * Static Code Blocks
* Beta v.0.7
  * Interface support
  * Enum support
  * Record support
  * annotation class support
* Beta v.0.8
  * Greater parsing of code itself (within methods and such)
