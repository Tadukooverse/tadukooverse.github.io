---
title: Projects
---
{% assign active_projects = site.projects | where:"replaced", false %}
{% for project in active_projects %}
## [{{project.title}}]({{project.url}})
{{project.summary}}
{% endfor %}
