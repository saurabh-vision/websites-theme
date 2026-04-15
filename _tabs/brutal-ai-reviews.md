---
layout: page
title: "Brutal AI Reviews"
order: 4
icon: fas fa-robot
---

<link rel="stylesheet" href="{{ '/assets/css/design-system.css' | relative_url }}">

<div class="tools-header">
  <h1>Brutal AI Reviews</h1>
  <p>Candid, no-holds-barred critiques of AI tools, platforms, and implementations. No fluff, just the truth.</p>
</div>

<div class="audit-grid">
  {% assign section_posts = site.posts | where_exp: "post", "post.path contains 'brutal-ai-reviews/'" %}
  {% for post in section_posts %}
    {% include card-item.html 
      title=post.title 
      url=post.url 
      description=post.description 
      date=post.date 
      category="AI Review" 
      tags=post.tags
      icon="🤖"
    %}
  {% endfor %}
</div>
