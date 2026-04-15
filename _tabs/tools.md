---
layout: page
title: "Tools Library"
order: 6
icon: fas fa-tools
---

## 🛠 Tools Library

Free calculators, templates, and frameworks designed specifically for Indian SaaS founders. No fluff, just tools that work.

{% for tool in site.data.tools %}
- **[{{ tool.name }}]({{ tool.url | relative_url }})**  
  *{{ tool.description }}*  
  `{{ tool.category }}` {% if tool.badge %}`{{ tool.badge }}`{% endif %}
{% endfor %}

<hr>

Looking for something specific? All tools are open source and require no authentication.
