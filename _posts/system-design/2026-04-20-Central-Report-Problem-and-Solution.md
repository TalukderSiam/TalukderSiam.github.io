---
layout: post
title: "Central Reporting Problem in Multi Voice AI Agents"
date: 2026-04-20
categories: [system-design]
tags: [ai, architecture, voice-agent]
---

## Problem

I have 3 different Voice AI agents running on separate servers.

Each one stores its own conversations.

Now I need a central reporting system.

## Challenges

- No shared database
- Distributed architecture
- Same workflow, different contexts

## Key Questions

1. How frequently will reports be used?
2. Do you need real-time data?
3. Do you need aggregated or independent reports?
