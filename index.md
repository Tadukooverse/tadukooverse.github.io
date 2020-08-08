---
layout: default
title: Home
---

Welcome to the official website for the [Tadukooverse organization](https://github.com/Tadukooverse) on GitHub!

> **Note**: Please bear with us as this website is under construction.

Current sitemap (Temporary, will add navigation soon):
- About
  {% for about in site.about %}
  - [{{about.title}}]({{about.url}}) - {{about.blurb}}
  {% endfor %}
- Community
  {% for community in site.community %}
  - [{{community.title}}]({{community.url}})
  {% endfor %}
- Projects
  {% for project in site.projects %}
  - [{{project.title}}]({{project.url}}) - {{project.blurb}}
  {% endfor %}
