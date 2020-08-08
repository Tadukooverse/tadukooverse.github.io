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
	- [Code of Conduct](community/CODE_OF_CONDUCT.html)
	- [Contributing Guidelines](community/CONTRIBUTING.html)
- Projects
  {% for project in site.projects %}
  - [{{project.title}}]({{project.url}}) - {{project.blurb}}
  {% endfor %}
