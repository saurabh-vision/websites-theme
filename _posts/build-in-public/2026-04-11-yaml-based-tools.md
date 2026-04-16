---
title: "Build Log #2: Why I use YAML for my Tool Directory"
date: 2026-04-11 14:00:00 +0530
categories: [Build in Public]
tags: [Architecture, Jekyll, YAML]
description: "Why hardcoding HTML is a mistake for SaaS tools and how the Saurabh Audit YAML engine makes scaling easy."
---

## Data over Markup

When I started Saurabh Audit, I was writing raw HTML for every tool card. It was a maintenance nightmare. Changing a button color meant editing 10 different files.

### The YAML Solution:
By moving all tool data to `_data/tools.yml`, I separated the content from the design. 

**The Schema:**
```yaml
- name: ROI Calculator
  category: Finance
  url: /tools/roi-calculator.html
  icon: fas fa-chart-line
```

### The Benefits:
1. **Consistency**: All cards now look identical because they are generated from a single Liquid template.
2. **Speed**: Adding a new tool takes 60 seconds—just add a few lines to the YAML file.
3. **Filtering**: The JavaScript filter engine (Premium v2) depends on this data structure to hide/show categories instantly.

**Lessons Learned:** Plan your data structures before you plan your UI.
