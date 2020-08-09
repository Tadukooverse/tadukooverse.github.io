---
title: Blog
---
***Note**:If you're looking for a guide to the posts by series/topic instead of chronologically, [go here](/blog_guide.html)*

# Latest Posts

{% for post in site.posts %}
## [{{post.title}}]({{post.url}})
### by {{post.author}} - {{post.date | date_to_string}}
{{post.excerpt}}
{% endfor %}