---
title: Blog
---
***Note**:If you're looking for a guide to the posts by series/topic instead of chronologically, [go here](/blog_guide.html)*

# Latest Posts

{% for post in site.posts %}
## [{{post.title}}]({{post.url}})
{% assign author = site.contributors | where: 'short_name', page.author | first %}
### by [{{author.short_name}}]({{author.url}}) - {{post.date | date_to_string}}
{{post.excerpt}}
{% assign old_tags = post.tags | sort %}
{% assign tags = '' | split: '' %}
{% for tag in old_tags %}
{% capture newTag %}[{{tag}}](/blog/tags.html#{{tag | slugify}}){% endcapture %}
{% assign tags = tags | push: newTag %}
{% endfor %}
Tags: {{tags | join:", "}}
{% endfor %}
