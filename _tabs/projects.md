---
layout: page
title: "Projects Portfolio"
order: 5
icon: fas fa-folder-open
---

<link rel="stylesheet" href="{{ '/assets/css/design-system.css' | relative_url }}">

<div class="tools-header">
  <h1>Projects Portfolio</h1>
  <p>A showcase of the tools, automation platforms, and experiments we've built and scaled.</p>
</div>

<div class="audit-grid">
  {% assign section_posts = site.posts | where_exp: "post", "post.path contains 'projects/'" %}
  {% for post in section_posts %}
    {% include card-item.html title=post.title url=post.url description=post.description date=post.date category="Project" tags=post.tags icon="🚀" %}
  {% endfor %}
</div>
