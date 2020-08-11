---
title: Guides
---
# Guides

#### Table of Contents
* [Tadukooverse Project Guides](#tadukooverse-project-guides)
{% for project in site.projects %}	* [{{project.title}} Guides](#{{project.title | slugify}}-guides)
{% endfor %}
* [Developer Guides](#developer-guides)

## Tadukooverse Project Guides
Guides on how to use the various [Tadukooverse projects](/projects.html)

{% for project in site.projects %}
### {{project.title}} Guides
{% assign project_user_guides = site.guides | where:"project", project.short_name | sort %}
{% for guide in project_user_guides %}
* [{{guide.title}}]({{guide.url}}) - {{guide.blurb}}
{% endfor %}
{% endfor %}

## Developer Guides
Guides on how to develop with Tadukooverse. There may be overlap between the Tadukooverse Project guides and developer guides, but in general the ones in this section are 
meant for how to help contribute to our projects, rather than how to use them.

{% assign developer_guides = site.guides | where:"developer", true | sort %}
{% for guide in developer_guides %}
* [{{guide.title}}]({{guide.url}}) - {{guide.blurb}}
{% endfor %}
