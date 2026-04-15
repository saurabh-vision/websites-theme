---
layout: page
title: "Case Studies"
order: 2
icon: fas fa-file-contract
---

<link rel="stylesheet" href="{{ '/assets/css/design-system.css' | relative_url }}">

<div class="tools-header">
  <h1>Case Studies</h1>
  <p>Deep dives into real audits, post-mortems, and conversion wins from the SaaS front lines.</p>
</div>

<div class="audit-grid">
  {% assign section_posts = site.posts | where_exp: "post", "post.path contains 'case-studies/'" %}
  {% for post in section_posts %}
    {% include card-item.html 
      title=post.title 
      url=post.url 
      description=post.description 
      date=post.date 
      category="Case Study" 
      tags=post.tags
      icon="📄"
    %}
  {% endfor %}
</div>
