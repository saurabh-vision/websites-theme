---
layout: page
title: "Brutal AI Reviews"
order: 4
icon: fas fa-robot
---

<p class="lead text-muted mb-5">No fluff. Candid, no-holds-barred critiques of AI tools, platforms, and implementations. We test until they break.</p>

<div class="post-feed">
  {% assign section_posts = site.posts | where_exp: "post", "post.path contains 'brutal-ai-reviews/'" %}
  {% for post in section_posts %}
  <div class="feed-item mb-5 pb-4 border-bottom border-secondary" style="border-color: rgba(255,255,255,0.05) !important;">
    <div class="d-flex justify-content-between align-items-center mb-2">
      <span class="badge badge-outline-accent px-3 py-1 uppercase" style="font-size: 0.7rem; border: 1px solid var(--accent-color); color: var(--accent-color); border-radius: 20px;">AI Review</span>
      <time class="text-muted small"><i class="fas fa-microchip mr-1"></i> Technical Analysis</time>
    </div>
    <h2 class="h4 font-weight-bold mb-3 mt-1"><a href="{{ post.url | relative_url }}" class="text-white hover-accent">{{ post.title }}</a></h2>
    
    {% if post.description %}
      <span class="post-description">{{ post.description }}</span>
    {% endif %}

    <div class="post-meta-wrapper mb-4">
      {% if post.categories.size > 0 %}
        <span class="meta-chip category">
          <i class="fas fa-folder-open"></i> {{ post.categories | first }}
        </span>
      {% endif %}
      
      {% for tag in post.tags %}
        <span class="meta-chip tag">
          <i class="fas fa-tag"></i> {{ tag }}
        </span>
      {% endfor %}
    </div>

    <a href="{{ post.url | relative_url }}" class="btn btn-sm btn-outline-primary px-4">Read Brutal Review</a>
  </div>
  {% endfor %}
</div>

{% if section_posts.size == 0 %}
<div class="text-center p-5 rounded" style="background: rgba(255,255,255,0.02);">
  <p class="text-muted">Currently stress-testing new models. Updates coming soon.</p>
</div>
{% endif %}

<style>
  .hover-accent:hover { color: var(--accent-color) !important; text-decoration: none; }
  .uppercase { text-transform: uppercase; letter-spacing: 1px; }
</style>
