---
title: "Build Log #1: Scaling Saurabh Audit to 1k Founders"
date: 2026-04-12 13:00:00 +0530
categories: [Build in Public]
tags: [Growth, SaaS, Metrics]
description: "The brutal truth about what broke when we hit 1,000 active users and how we refactored our data engine to handle the load."
---

## The 1k Milestone

Scaling from 100 to 1,000 users wasn't just '10x more traffic.' It was a fundamental stress test of our architecture. 

### What Broke:
1. **GitHub Action Limits**: We were running proofer checks on every push, and the concurrency was killing our build times.
2. **Liquid Overload**: Our categorical filters were originally too complex, causing Jekyll's build speed to drop significantly.
3. **Internal Links**: As the site grew, broken links became a daily nightmare until we standardized our `relative_url` logic.

### The Fix:
- **Optimized Workflows**: I deleted the redundant `jekyll.yml` and moved everything to a single, high-performance `pages-deploy.yml`.
- **CSS Variable Tokens**: Moved all hardcoded colors to `:root` variables, making the dark mode flip much smoother.
- **Lazy Loading**: We stopped loading all tool cards at once and moved to a client-side filter engine.

**Next Goal:** 5,000 users. The architecture is ready.
