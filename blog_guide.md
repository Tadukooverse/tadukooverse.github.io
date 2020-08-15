---
title: Blog Guide
---
# Blog Guide

#### Table of Contents
* [Java API Tutorials](#java-api-tutorials)
	* [Java Components & Layouts](#java-components--layouts)
* [Tadukooverse Development](#tadukooverse-development)
	* [General](#general)
	* [Tadukoo Look & Feel Journey](#tadukoo-look--feel-journey)
* [Blog Updates](#blog-updates)

## Java API Tutorials
Tutorials on how to use the Java API.

### Java Components & Layouts
This tutorial goes over how to use the various components and layouts provided by Java. The goal Tadukoo has in writing it is to create a program that shows off all the components 
in order to show what the Tadukoo Look & Feel can do.

{% assign componentsAndLayoutsPosts = site.posts | where:"series", "Java Components & Layouts" | sort:"index" %}
{% for componentsAndLayoutsPost in componentsAndLayoutsPosts %}{{componentsAndLayoutsPost.index}}. [{{componentsAndLayoutsPost.title | remove:"Java Components & Layouts: "}}]({{componentsAndLayoutsPost.url}}) - 
{{componentsAndLayoutsPost.date | date_to_string}}
{% endfor %}

## Tadukooverse Development
Posts about how development is progressing on Tadukooverse projects.

### General
General Tadukooverse Development posts that don't fall under other categories.

{% assign generalDevPosts = site.posts | where:"series", "General Tadukooverse Development" | sort:"index" %}
{% for generalDevPost in generalDevPosts %}{{generalDevPost.index}}. [{{generalDevPost.title}}]({{generalDevPost.url}}) - 
{{generalDevPost.date | date_to_string}}
{% endfor %}

### Tadukoo Look & Feel Journey
{% assign TadukooUtil = site.projects | where:"short_name", "TadukooUtil" | first %}
Tadukoo is on a journey to create a customizable look & feel called "Tadukoo Look & Feel" (part of [Tadukoo Util]({{TadukooUtil.url}})).

This journey started with a special post about what the full plan was: [Java Look & Feel Journey]({% post_url 2020-05-03-java-look-and-feel-journey %})

{% assign lookAndFeelPosts = site.posts | where:"series", "Tadukoo Look & Feel Journey" | sort:"index" %}
{% for lookAndFeelPost in lookAndFeelPosts %}{{lookAndFeelPost.index}}. [{{lookAndFeelPost.title | remove:"Java Look and Feel: " | remove:"Java Look & Feel: "}}]({{lookAndFeelPost.url}}) - 
{{lookAndFeelPost.date | date_to_string}}
{% endfor %}

## Blog Updates
Updates about the blog in general.

{% assign blogUpdates = site.posts | where:"series", "Blog Updates" | sort:"index" %}
{% for blogUpdate in blogUpdates %}{{blogUpdate.index}}. [{{blogUpdate.title}}]({{blogUpdate.url}}) - {{blogUpdate.date | date_to_string}}
{% endfor %}
