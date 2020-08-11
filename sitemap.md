---
title: Sitemap
---
# Sitemap

#### Table of Contents
* [About](#about)
* [Blog](#blog)
* [Community](#community)
* [Guides](#guides)
	* [Tadukooverse Project Guides](#tadukooverse-project-guides)
	* [Developer Guides](#developer-guides)
* [Projects](#projects)

## About
{% for about in site.about %}- [{{about.title}}]({{about.url}}) - {{about.blurb}} 
{% endfor %}

## Blog
There are many blog posts compared to the other types of pages.
- For the most recent posts, [go here](/blog.html)
- For an index by series/topic, [go here](/blog_guide.html)

## Community
{% for community in site.community %}- [{{community.title}}]({{community.url}}) - {{community.blurb}}
{% endfor %}

## Guides

### Tadukooverse Project Guides
Guides on how to use the various [Tadukooverse projects](/projects.html)

{% for project in site.projects %}
#### {{project.title}} Guides
{% assign project_user_guides = site.guides | where:"project", project.short_name | sort %}
{% for guide in project_user_guides %}
* [{{guide.title}}]({{guide.url}}) - {{guide.blurb}}
{% endfor %}
{% endfor %}

### Developer Guides
Guides on how to develop with Tadukooverse. There may be overlap between the Tadukooverse Project guides and developer guides, but in general the ones in this section are 
meant for how to help contribute to our projects, rather than how to use them.

{% assign developer_guides = site.guides | where:"developer", true | sort %}
{% for guide in developer_guides %}
* [{{guide.title}}]({{guide.url}}) - {{guide.blurb}}
{% endfor %}

## Projects
{% for project in site.projects %}- [{{project.title}}]({{project.url}}) - {{project.blurb}}
{% endfor %}
