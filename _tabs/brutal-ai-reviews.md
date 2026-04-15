---
layout: page
title: "Brutal AI Reviews"
order: 4
icon: fas fa-robot
---

No fluff. Candid, no-holds-barred critiques of AI tools, platforms, and implementations.

## Latest Brutal Reviews

{% assign section_posts = site.posts | where_exp: "post", "post.path contains 'brutal-ai-reviews/'" %}
{% for post in section_posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) ({{ post.date | date: "%Y-%m-%d" }})
{% endfor %}
