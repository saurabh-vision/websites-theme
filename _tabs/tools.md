---
layout: tab
title: "Tools Library"
order: 6
icon: fas fa-tools
---

## 🛠 Tools Library

<style>
  .tool-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 1.5rem;
    margin-top: 2rem;
  }
  .tool-card {
    border: 1px solid var(--main-border-color);
    border-radius: 12px;
    padding: 1.5rem;
    background: var(--card-bg);
    transition: transform 0.2s, box-shadow 0.2s;
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  .tool-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(0,0,0,0.1);
    border-color: var(--link-color);
  }
  .tool-card.featured {
    border: 2px solid var(--link-color);
  }
  .tool-card h3 {
    margin-top: 0;
    margin-bottom: 0.5rem;
    font-size: 1.25rem;
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }
  .tool-card a {
    color: inherit;
    text-decoration: none;
  }
  .tool-card a:hover {
    color: var(--link-color);
  }
  .tool-featured {
    font-size: 0.7rem;
    background: var(--link-color);
    color: white;
    padding: 2px 8px;
    border-radius: 20px;
    text-transform: uppercase;
    font-weight: bold;
    margin-left: auto;
  }
  .tool-desc {
    font-size: 0.9rem;
    color: var(--text-muted-color);
    margin-bottom: 1rem;
    line-height: 1.4;
  }
  .tool-tags {
    font-size: 0.8rem;
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
  }
  .tool-tag {
    background: var(--nav-cursor-color);
    padding: 2px 10px;
    border-radius: 4px;
    color: var(--text-color);
  }
</style>

<div class="tool-grid">
{% for tool in site.data.tools %}
  <div class="tool-card{% if tool.featured %} featured{% endif %}">
    <div>
      <h3>
        <a href="/tools/{{ tool.slug }}.html">{{ tool.icon }} {{ tool.name }}</a>
        {% if tool.featured %}<span class="tool-featured">Featured</span>{% endif %}
      </h3>
      <div class="tool-desc">{{ tool.description }}</div>
    </div>
    <div class="tool-tags">
      {% for tag in tool.tags %}
        <span class="tool-tag">{{ tag }}</span>
      {% endfor %}
    </div>
  </div>
{% endfor %}
</div>
