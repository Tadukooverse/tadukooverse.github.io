---
layout: default
title: Tags
---
# Tags

{% assign tags = site.tags | sort %}

#### Table of Contents
{% for tag in tags %}* [{{tag[0]}}](#{{tag[0] | slugify}}) - {{tag[1].size}} posts
{% endfor %}

{% for tag in tags %}## {{tag[0]}}
{% for post in tag[1] 
  %}{% assign author = site.contributors | where:'short_name', post.author | first 
  %}* [{{post.title}}]({{post.url}}) by [{{author.short_name}}]({{author.url}}) - {{post.date | date_to_string}}
{% endfor %}
{% endfor %}
