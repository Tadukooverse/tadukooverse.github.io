---
layout: default
title: Projects
---
# Projects

{% for project in site.projects %}
## [{{project.title}}]({{project.url}})
{{project.summary}}
{% endfor %}
