---
layout: page
title: "Projects"
order: 5
icon: fas fa-folder-open
---

<p class="lead text-muted mb-5">A showcase of the custom tools, automation frameworks, and specialized platforms we've built for the SaaS ecosystem.</p>

<div class="post-feed">
  {% assign section_posts = site.posts | where_exp: "post", "post.path contains 'projects/'" %}
  {% for post in section_posts %}
  <div class="feed-item mb-5 pb-4 border-bottom border-secondary" style="border-color: rgba(255,255,255,0.05) !important;">
    <div class="d-flex justify-content-between align-items-center mb-2">
      <span class="badge badge-outline-accent px-3 py-1 uppercase" style="font-size: 0.7rem; border: 1px solid var(--accent-color); color: var(--accent-color); border-radius: 20px;">Project</span>
      <time class="text-muted small"><i class="fas fa-external-link-alt mr-1"></i> Live Portfolio</time>
    </div>
    <h2 class="h4 font-weight-bold mb-3 mt-1"><a href="{{ post.url | relative_url }}" class="text-white hover-accent">{{ post.title }}</a></h2>
    <p class="text-muted mb-4">{{ post.excerpt | strip_html | truncate: 180 }}</p>
    <a href="{{ post.url | relative_url }}" class="btn btn-sm btn-outline-primary px-4">View Project Details</a>
  </div>
  {% endfor %}
</div>

{% if section_posts.size == 0 %}
<div class="text-center p-5 rounded" style="background: rgba(255,255,255,0.02);">
  <p class="text-muted">Currently shipping something big. New projects dropping soon.</p>
</div>
{% endif %}

<style>
  .hover-accent:hover { color: var(--accent-color) !important; text-decoration: none; }
  .uppercase { text-transform: uppercase; letter-spacing: 1px; }
</style>
