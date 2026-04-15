---
layout: page
title: "Case Studies"
order: 2
icon: fas fa-file-contract
---

Deep dives into real audits, post-mortems, and conversion wins.

## Latest Case Studies

{% assign section_posts = site.posts | where_exp: "post", "post.path contains 'case-studies/'" %}
{% for post in section_posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) ({{ post.date | date: "%Y-%m-%d" }})
{% endfor %}
