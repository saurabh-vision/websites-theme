---
title: "Build Log #3: Modernizing the Chirpy Theme"
date: 2026-04-10 15:00:00 +0530
categories: [Build in Public]
tags: [Design, CSS, Glassmorphism]
description: "How we transformed the minimalist Chirpy theme into a high-authority, glassmorphism-inspired SaaS platform."
---

## Minimal but Premium

Chirpy is a fantastic theme for developers, but for founders, it was a bit too 'plain.' We needed something that screamed 'Premium SaaS Audits' from the first scroll.

### Key Changes:
1. **Glassmorphism 2.0**: Added `backdrop-filter: blur(10px)` and subtle borders to all cards.
2. **Neon Accents**: Defined `#00ff88` as our core accent color to give it a 'Terminal/Brutal' feel.
3. **Interactive Timelines**: Moved away from simple lists to a detailed, metadata-rich chronological timeline.
4. **Custom Filter Engine**: Implemented a pure JS engine for the Tools Library to avoid page reloads.

### The Challenge:
Balancing these heavy visual effects with fast load times. We accomplished this by using CSS variables and minimizing external libraries.

**Design Philosophy:** If it doesn't move or glow, it should be invisible.
