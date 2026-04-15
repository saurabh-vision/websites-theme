---
layout: page
title: "Case Studies"
order: 2
icon: fas fa-file-contract
---

<p class="lead text-muted mb-5">Deep dives into real audits, post-mortems, and conversion wins. Real data from real startups to help you avoid common SaaS pitfalls.</p>

<div class="post-feed">
  {% assign section_posts = site.posts | where_exp: "post", "post.path contains 'case-studies/'" %}
  {% for post in section_posts %}
  <div class="feed-item mb-5 pb-4 border-bottom border-secondary" style="border-color: rgba(255,255,255,0.05) !important;">
    <div class="d-flex justify-content-between align-items-center mb-2">
      <span class="badge badge-outline-accent px-3 py-1 uppercase" style="font-size: 0.7rem; border: 1px solid var(--accent-color); color: var(--accent-color); border-radius: 20px;">Case Study</span>
      <time class="text-muted small"><i class="far fa-clock mr-1"></i> {{ post.content | number_of_words | divided_by: 200 | plus: 1 }} min read</time>
    </div>
    <h2 class="h4 font-weight-bold mb-3 mt-1"><a href="{{ post.url | relative_url }}" class="text-white hover-accent">{{ post.title }}</a></h2>
    <p class="text-muted mb-4">{{ post.excerpt | strip_html | truncate: 200 }}</p>
    <a href="{{ post.url | relative_url }}" class="btn btn-sm btn-outline-primary px-4">View Case Study →</a>
  </div>
  {% endfor %}
</div>

{% if section_posts.size == 0 %}
<div class="text-center p-5 rounded" style="background: rgba(255,255,255,0.02);">
  <p class="text-muted">Analyzing the next big win. New case studies coming soon.</p>
</div>
{% endif %}

<style>
  .hover-accent:hover { color: var(--accent-color) !important; text-decoration: none; }
  .uppercase { text-transform: uppercase; letter-spacing: 1px; }
</style>
