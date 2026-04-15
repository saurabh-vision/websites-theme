---
layout: page
title: "Tools Library"
order: 6
icon: fas fa-tools
---

<link rel="stylesheet" href="{{ '/assets/css/design-system.css' | relative_url }}">

<div class="tools-header">
  <h1>Tools Built for India's Friction</h1>
  <p>Free calculators, templates, and frameworks designed specifically for Indian SaaS founders. No fluff, just tools that work.</p>
  <div class="header-badges">
    <div class="header-badge"><i class="fas fa-lock-open"></i> Open Source</div>
    <div class="header-badge"><i class="fas fa-user-shield"></i> No Auth Required</div>
    <div class="header-badge"><i class="fas fa-bolt"></i> Instant Result</div>
  </div>
</div>

<div class="filter-container">
  <div class="filter-bar" id="filter-bar">
    <button class="filter-btn active" data-filter="all">All Tools</button>
    <button class="filter-btn" data-filter="Finance">Finance</button>
    <button class="filter-btn" data-filter="Product">Product</button>
    <button class="filter-btn" data-filter="Strategy">Strategy</button>
    <button class="filter-btn" data-filter="Productivity">Productivity</button>
  </div>
</div>

<div class="audit-grid">
{% for tool in site.data.tools %}
  {% include card-item.html 
    title=tool.name 
    url=tool.url 
    description=tool.description 
    category=tool.category 
    icon=tool.icon 
    tags=tool.tags 
    badge=tool.badge 
    minutes=tool.minutes
  %}
{% endfor %}
</div>

<style>
  /* Page-specific overrides for Filter Bar */
  .filter-bar {
    display: flex;
    gap: 0.75rem;
    overflow-x: auto;
    padding-bottom: 0.75rem;
    scrollbar-width: none;
    margin-bottom: 2rem;
  }
  .filter-btn {
    padding: 0.6rem 1.4rem;
    border-radius: 50px;
    background: var(--audit-card-bg);
    border: 1px solid var(--audit-border);
    color: var(--audit-text-main);
    font-weight: 600;
    cursor: pointer;
    white-space: nowrap;
    transition: all 0.2s ease;
  }
  .filter-btn.active {
    background: var(--audit-accent);
    color: white;
    border-color: var(--audit-accent);
  }
  .tool-card.hidden { display: none; }
  
  /* Filtering Logic */
  .audit-card.hidden { display: none; }
</style>

<script>
  document.addEventListener('DOMContentLoaded', () => {
    const filterBtns = document.querySelectorAll('.filter-btn');
    const toolCards = document.querySelectorAll('.audit-card');

    filterBtns.forEach(btn => {
      btn.addEventListener('click', () => {
        filterBtns.forEach(b => b.classList.remove('active'));
        btn.classList.add('active');

        const filter = btn.getAttribute('data-filter');

        toolCards.forEach(card => {
          if (filter === 'all' || card.getAttribute('data-category') === filter) {
            card.style.display = 'flex';
          } else {
            card.style.display = 'none';
          }
        });
      });
    });
  });
</script>
