---
layout: default
title: Projects
---
# Projects

{% for project in site.projects %}
	<h2><a href="{{project.url}}">{{project.name}}</a></h2>
	{{project.summary}}
{% endfor %}