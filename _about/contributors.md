---
title: Contributors
blurb: A list of the contributors to Tadukooverse
summary: Information about Tadukooverse's contributors along with links to pages with more details about them and their contributions.
---
<h1>Contributors</h1>

{% for contributor in site.contributors %}## [{{contributor.name}}]({{contributor.url}})
### {{contributor.position}}
{{contributor.blurb}}
{% endfor %}
