---
layout: page
title: "Case Studies"
order: 2
icon: fas fa-file-contract
---

<<<<<<< HEAD
Deep dives into real audits, post-mortems, and conversion wins.

## Latest Case Studies

{% assign section_posts = site.posts | where_exp: "post", "post.path contains 'case-studies/'" %}
{% for post in section_posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) ({{ post.date | date: "%Y-%m-%d" }})
{% endfor %}
<<<<<<< HEAD
=======
=======
<link rel="stylesheet" href="{{ '/assets/css/design-system.css' | relative_url }}">

<div class="tools-header">
  <h1>Case Studies</h1>
  <p>Deep dives into real audits, post-mortems, and conversion wins from the SaaS front lines.</p>
</div>

<div class="audit-grid">
  {% assign section_posts = site.posts | where_exp: "post", "post.path contains 'case-studies/'" %}
  {% for post in section_posts %}
    {% include card-item.html title=post.title url=post.url description=post.description date=post.date category="Case Study" tags=post.tags icon="📄" %}
  {% endfor %}
</div>
>>>>>>> e229eb9bcfb4f8c29e215d935c1ce5162e738051
>>>>>>> 5177466c0f506205f27ca28adaa21f10b37c364b
