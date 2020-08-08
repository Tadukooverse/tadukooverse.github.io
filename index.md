---
layout: default
title: Home
---

Welcome to the official website for the [Tadukooverse organization](https://github.com/Tadukooverse) on GitHub!

> **Note**: Please bear with us as this website is under construction.

Current sitemap (Temporary, will add navigation soon):
- About
	- [FAQ](about/faq.html)
	- [Roadmap](about/roadmap.html)
- Community
	- [Code of Conduct](community/CODE_OF_CONDUCT.html)
	- [Contributing Guidelines](community/CONTRIBUTING.html)
- Projects
  <ul>
  {% for project in site.projects %}
    <li>
	  <h2><a href="{{project.url}}">{{project.name}}</a></h2>
	  <p>{{project.summary}}</p>
	</li>
  {% endfor %}
