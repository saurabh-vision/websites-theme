---
layout: page
title: "Tools Library"
order: 6
icon: fas fa-tools
---

<p class="lead text-muted mb-5">Free calculators, templates, and frameworks designed specifically for Indian SaaS founders. No fluff, just tools that work.</p>

<div class="filter-bar mb-5">
  <button class="filter-btn active" data-category="all">All</button>
  <button class="filter-btn" data-category="Finance">Finance</button>
  <button class="filter-btn" data-category="Product">Product</button>
  <button class="filter-btn" data-category="Strategy">Strategy</button>
  <button class="filter-btn" data-category="Productivity">Productivity</button>
</div>

<div class="tools-grid">
  {% for tool in site.data.tools %}
  <div class="tool-card" data-category="{{ tool.category }}">
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
    
    <div class="tool-footer mt-4">
      <a href="{{ tool.url | relative_url }}" class="btn-v2-launch">Launch Tool <i class="fas fa-rocket ml-2"></i></a>
    </div>
  </div>
  {% endfor %}
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const filterBtns = document.querySelectorAll('.filter-btn');
  const toolCards = document.querySelectorAll('.tool-card');

  filterBtns.forEach(btn => {
    btn.addEventListener('click', () => {
      filterBtns.forEach(b => b.classList.remove('active'));
      btn.classList.add('active');

      const category = btn.getAttribute('data-category');

      toolCards.forEach(card => {
        if (category === 'all' || card.getAttribute('data-category') === category) {
          card.classList.remove('hidden');
        } else {
          card.classList.add('hidden');
        }
      });
    });
  });
});
</script>

<hr class="my-5">

<div class="text-center p-5 rounded" style="background: rgba(var(--accent-color-rgb), 0.05); border: 1px dashed rgba(255,255,255,0.1);">
  <h4 class="mb-3">Need a custom audit?</h4>
  <p class="text-muted mb-4">All tools are open source. For deep-dive brutal audits of your specific product or pricing, get in touch.</p>
  <a href="mailto:{{ site.social.email }}" class="btn btn-outline-primary">Request Manual Audit</a>
</div>
