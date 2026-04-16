---
title: "Project Delta: Logic behind the Automated Email Splitter"
date: 2026-04-01 00:00:00 +0530
categories: [Projects]
tags: [Productivity, Projects, Tools]
description: "Why I built a tool to force my own emails to be shorter and the NLP logic that makes it work."
---

## Solving my Own Friction

As a founder, I was sending 500-word emails that were getting zero replies. I needed a tool that wouldn't let me hit 'Send' until the email was chopped into actionable bits.

### The Algorithm:
1. **Sentence Parsing**: Every paragraph is broken down into its core components.
2. **Action-Item Detection**: We use a custom dictionary of 'Action Verbs' (Send, Buy, Fix, Call) to ensure every sentence has a purpose.
3. **Complexity Scoring**: If a sentence has more than 2 clauses, it's flagged as 'Too complex.'

### The Impact:
Since using Project Delta, my reply rate has increased by 35%. People don't read long emails; they scan for work.

**Status:** Open source component available on GitHub.
