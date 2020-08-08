---
title: Blog
---
# Latest Posts

{% for post in site.posts %}
## [{{post.title}}]({{post.url}})
### by {{post.author}} - {{post.date | date_to_string}}
{{post.excerpt}}
{% endfor %}