---
title: "Project Gamma: The SaaS Pricing Audit Engine"
date: 2026-04-02 23:00:00 +0530
categories: [Projects]
tags: [Pricing, Projects, SaaS]
description: "How we automated the 'Pricing Roast' with an engine that scans your tiers for decoy pricing and anchoring flaws."
---

## Automating the Roast

Pricing strategy is usually a human-led affair. But for most Micro-SaaS, the mistakes are standard. I built Project Gamma to detect these patterns automatically.

### What it Scans for:
1. **Decoy Pricing**: Absence of a 'middle tier' that makes the pro tier look attractive.
2. **Anchor Mismatch**: When your highest tier is too close to your lowest tier.
3. **Currency Conversion**: Checking if your prices make sense for the Indian market.

### Technical Detail:
Project Gamma uses a specific sentiment-analysis model trained on 1,000 successful SaaS pricing pages. It looks at every word—'Monthly,' 'Annual,' 'Enterprise'—to ensure the psychological flow is perfect.

**Status:** Free tool live on Saurabh Audit.
