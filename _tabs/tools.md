---
layout: page
title: "Tools Library"
order: 6
icon: fas fa-tools
---

<style>
  :root {
    --tool-primary: #FF5722; /* High-impact orange from reference */
    --tool-primary-light: #FFF3E0;
    --tool-card-shadow: 0 4px 20px rgba(0,0,0,0.08);
    --tool-card-hover-shadow: 0 12px 30px rgba(0,0,0,0.12);
  }

  /* Hero Section */
  .tools-hero {
    background: var(--tool-primary);
    color: white;
    padding: 3rem 2rem;
    border-radius: 16px;
    margin-bottom: 3rem;
    text-align: left;
    position: relative;
    overflow: hidden;
  }
  .tools-hero h1 {
    color: white !important;
    font-size: 2.5rem !important;
    font-weight: 800 !important;
    margin-bottom: 1rem !important;
    border: none !important;
  }
  .tools-hero p {
    font-size: 1.1rem;
    opacity: 0.95;
    max-width: 600px;
    margin-bottom: 1.5rem;
  }
  .hero-badges {
    display: flex;
    flex-wrap: wrap;
    gap: 1.5rem;
    font-size: 0.9rem;
    font-weight: 500;
  }
  .hero-badge {
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }
  .hero-badge i {
    font-size: 1.1rem;
  }

  /* Filter Bar */
  .filter-bar {
    display: flex;
    gap: 0.75rem;
    margin-bottom: 2.5rem;
    overflow-x: auto;
    padding-bottom: 0.5rem;
    scrollbar-width: none;
  }
  .filter-btn {
    padding: 0.6rem 1.2rem;
    border-radius: 50px;
    background: var(--card-bg);
    border: 1px solid var(--main-border-color);
    color: var(--text-color);
    font-weight: 600;
    cursor: pointer;
    white-space: nowrap;
    transition: all 0.2s;
  }
  .filter-btn.active {
    background: #007bff; /* Active color from image */
    color: white;
    border-color: #007bff;
  }
  .filter-btn:hover:not(.active) {
    background: var(--tool-primary-light);
    border-color: var(--tool-primary);
  }

  /* Card Grid */
  .tool-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(400px, 1fr));
    gap: 2rem;
  }
  @media (max-width: 768px) {
    .tool-grid {
      grid-template-columns: 1fr;
    }
  }

  .tool-card {
    background: var(--card-bg);
    border: 1px solid var(--main-border-color);
    border-radius: 20px;
    padding: 2rem;
    display: flex;
    flex-direction: column;
    transition: all 0.3s ease;
    box-shadow: var(--tool-card-shadow);
  }
  .tool-card:hover {
    transform: translateY(-8px);
    box-shadow: var(--tool-card-hover-shadow);
    border-color: var(--tool-primary);
  }

  .card-top {
    display: flex;
    align-items: flex-start;
    gap: 1.5rem;
    margin-bottom: 1.5rem;
  }
  .tool-icon-box {
    width: 60px;
    height: 60px;
    background: var(--tool-primary);
    border-radius: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.8rem;
    flex-shrink: 0;
    box-shadow: 0 4px 10px rgba(255, 87, 34, 0.3);
  }
  .card-header-info {
    flex-grow: 1;
  }
  .card-header-info h2 {
    margin: 0 !important;
    font-size: 1.4rem !important;
    font-weight: 700 !important;
    border: none !important;
  }
  .card-labels {
    display: flex;
    gap: 0.5rem;
    margin-top: 0.4rem;
  }
  .label-pill {
    font-size: 0.75rem;
    padding: 2px 10px;
    border-radius: 20px;
    font-weight: 600;
  }
  .label-cat { background: var(--nav-cursor-color); color: var(--text-color); }
  .label-badge { background: #FF9800; color: white; } /* Popular/New color */

  .card-desc {
    font-size: 0.95rem;
    line-height: 1.6;
    color: var(--text-color);
    margin-bottom: 1.5rem;
    opacity: 0.85;
  }

  .card-features {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 0.8rem;
    margin-bottom: 2rem;
    padding: 0;
    list-style: none !important;
  }
  .card-features li {
    font-size: 0.85rem;
    display: flex;
    align-items: center;
    gap: 0.5rem;
    color: var(--text-muted-color);
  }
  .card-features li::before {
    content: "✓";
    color: #4CAF50;
    font-weight: 900;
  }

  .card-footer {
    border-top: 1px solid var(--main-border-color);
    padding-top: 1.5rem;
    margin-top: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .tool-time {
    font-size: 0.85rem;
    color: var(--text-muted-color);
    display: flex;
    align-items: center;
    gap: 0.4rem;
  }
  .open-btn {
    color: var(--tool-primary);
    font-weight: 700;
    text-decoration: none;
    font-size: 0.95rem;
    transition: color 0.2s;
  }
  .open-btn:hover {
    color: #E64A19;
    text-decoration: underline;
  }
</style>

<div class="tools-hero">
  <h1>Tools Built for India's Friction</h1>
  <p>Free calculators, templates, and frameworks designed specifically for Indian SaaS founders. No fluff, just tools that work.</p>
  <div class="hero-badges">
    <div class="hero-badge"><i class="fas fa-check-circle"></i> 100% Free Forever</div>
    <div class="hero-badge"><i class="fas fa-check-circle"></i> No Signup Required</div>
    <div class="hero-badge"><i class="fas fa-check-circle"></i> India-Optimized</div>
  </div>
</div>

<div class="filter-bar">
  <button class="filter-btn active">All</button>
  <button class="filter-btn">Finance</button>
  <button class="filter-btn">Product</button>
  <button class="filter-btn">Strategy</button>
  <button class="filter-btn">Analytics</button>
  <button class="filter-btn">Marketing</button>
  <button class="filter-btn">Templates</button>
</div>

<div class="tool-grid">
{% for tool in site.data.tools %}
  <div class="tool-card">
    <div class="card-top">
      <div class="tool-icon-box">{{ tool.icon }}</div>
      <div class="card-header-info">
        <h2>{{ tool.name }}</h2>
        <div class="card-labels">
          <span class="label-pill label-cat">{{ tool.category }}</span>
          {% if tool.badge != "" %}<span class="label-pill label-badge">{{ tool.badge }}</span>{% endif %}
        </div>
      </div>
    </div>
    
    <div class="card-desc">{{ tool.description }}</div>
    
    <ul class="card-features">
      {% for feature in tool.features %}
        <li>{{ feature }}</li>
      {% endfor %}
    </ul>
    
    <div class="card-footer">
      <div class="tool-time">🕒 {{ tool.minutes }} min</div>
      <a href="{{ tool.url | relative_url }}" class="open-btn">Open Tool →</a>
    </div>
  </div>
{% endfor %}
</div>
