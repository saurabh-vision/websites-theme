---
layout: page
title: "Projects Portfolio"
order: 5
icon: fas fa-folder-open
---

A showcase of the tools, automation, and platforms we've built.

## Latest Projects

{% assign section_posts = site.posts | where_exp: "post", "post.path contains 'projects/'" %}
{% for post in section_posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) ({{ post.date | date: "%Y-%m-%d" }})
{% endfor %}
