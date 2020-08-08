---
layout: default
title: Projects
---
# Projects

{% for project in site.projects %}
	##[{{project.name}}]({{project.url}})
	{{project.summary}}
{% endfor %}