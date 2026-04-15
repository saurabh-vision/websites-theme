---
layout: page
title: "Build in Public"
order: 3
icon: fas fa-hammer
---

Real-time updates, shipping logs, and behind-the-scenes of bootstrapping.

## Latest Build Logs

{% assign section_posts = site.posts | where_exp: "post", "post.path contains 'build-in-public/'" %}
{% for post in section_posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) ({{ post.date | date: "%Y-%m-%d" }})
{% endfor %}
