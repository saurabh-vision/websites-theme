---
layout: page
title: "Build in Public"
order: 3
icon: fas fa-hammer
---

<link rel="stylesheet" href="{{ '/assets/css/design-system.css' | relative_url }}">

<div class="tools-header">
  <h1>Build in Public</h1>
  <p>Real-time updates, shipping logs, and behind-the-scenes of bootstrapping automation and products.</p>
</div>

<div class="audit-grid">
  {% assign section_posts = site.posts | where_exp: "post", "post.path contains 'build-in-public/'" %}
  {% for post in section_posts %}
    {% include card-item.html title=post.title url=post.url description=post.description date=post.date category="Log" tags=post.tags icon="🛠️" %}
  {% endfor %}
</div>
