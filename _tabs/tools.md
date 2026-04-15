---
layout: page
title: "Tools Library"
order: 6
icon: fas fa-tools
---

<p class="lead text-muted mb-5">Free calculators, templates, and frameworks designed specifically for Indian SaaS founders. No fluff, just tools that work.</p>

<div class="tools-grid">
  {% for tool in site.data.tools %}
  <div class="tool-card">
    {% if tool.badge != "" %}
    <span class="tool-badge">{{ tool.badge }}</span>
    {% endif %}
    
    <div class="tool-icon">
      <i class="{{ tool.icon }}"></i>
    </div>
    
    <h3 class="tool-title">{{ tool.name }}</h3>
    <p class="tool-desc">{{ tool.description }}</p>
    
    <ul class="tool-features">
      {% for feature in tool.features %}
      <li><i class="fas fa-check"></i> {{ feature }}</li>
      {% endfor %}
    </ul>
    
    <div class="tool-footer">
      <span class="small text-muted"><i class="far fa-clock mr-1"></i> {{ tool.minutes }} min</span>
      <a href="{{ tool.url | relative_url }}" class="tool-link">Launch Tool <i class="fas fa-arrow-right"></i></a>
    </div>
  </div>
  {% endfor %}
</div>

<hr class="my-5">

<div class="text-center p-5 rounded" style="background: rgba(var(--accent-color-rgb), 0.05); border: 1px dashed rgba(255,255,255,0.1);">
  <h4 class="mb-3">Need a custom audit?</h4>
  <p class="text-muted mb-4">All tools are open source. For deep-dive brutal audits of your specific product or pricing, get in touch.</p>
  <a href="mailto:{{ site.social.email }}" class="btn btn-outline-primary">Request Manual Audit</a>
</div>
