---
short_name: TadukooMaven
title: Tadukoo Maven
blurb: Tadukoo Maven is a collection of Maven poms and archetypes for Tadukooverse projects.
summary: Tadukoo View is a collection of Maven poms and archetypes for Tadukooverse projects.
version: Alpha v.0.2
github: https://github.com/Tadukooverse/TadukooMaven
---
{% assign TadukooUtil = site.projects | where:"short_name", "TadukooUtil" | first %}
{% assign TadukooView = site.projects | where:"short_name", "TadukooView" | first %}
{% assign TadukooParsing = site.projects | where:"short_name", "TadukooParsing" | first %}
{% assign TadukooWebServices = site.projects | where:"short_name", "TadukooWebServices" | first %}

#### Table of Contents
* [Modules](#modules)
    * [Tadukoo Maven Base POM](#tadukoo-maven-base-pom)
      * [Tadukoo Maven Library POM](#tadukoo-maven-library-pom)
      * [Tadukoo Maven Parsing POM](#tadukoo-maven-parsing-pom)
      * [Tadukoo Maven Web Service POM](#tadukoo-maven-web-service-pom)
      * [Tadukoo Maven View POM](#tadukoo-maven-view-pom)
* [Current Plans](#current-plans)

## Modules
### Tadukoo Maven Base POM
Tadukoo Maven Base POM is the base POM.xml for all Tadukooverse Maven projects.

#### Tadukoo Maven Library POM
Tadukoo Maven Library POM is the base POM to be used by libraries in Tadukooverse.
It extends Tadukoo Maven Base POM, providing the dependencies for 
[{{TadukooUtil.title}}]({{TadukooUtil.url}})

#### Tadukoo Maven Parsing POM
Tadukoo Maven Parsing POM is the base POM to be used by parsing libraries in 
Tadukooverse. It extends Tadukoo Maven Base POM, providing the dependencies 
for [{{TadukooParsing.title}}]({{TadukooParsing.url}})

#### Tadukoo Maven Web Service POM
Tadukoo Maven Web Service POM is the base POM to be used by web services 
libraries in Tadukooverse. It extends Tadukoo Maven Base POM, providing the 
dependencies for [{{TadukooWebServices.title}}]({{TadukooWebServices.url}})

#### Tadukoo Maven View POM
Tadukoo Maven View POM is the base POM to be used by libraries or programs using 
view components in Tadukooverse. It extends Tadukoo Maven Base POM, providing 
the dependencies for [{{TadukooView.title}}]({{TadukooView.url}})

## Current Plans
TBA
