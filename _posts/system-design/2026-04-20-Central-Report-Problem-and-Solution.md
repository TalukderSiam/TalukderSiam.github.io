---
layout: post
title: "Building a Unified Reporting System from Multiple Microservice Databases"
date: 2026-04-20
categories: [system-design]
tags: [ai, architecture, voice-agent]
---

## Problem-Description

There are three Voice AI agents running on separate servers. Although they follow the same workflow, each agent operates in a different context and stores its conversation data in its own isolated database.
The challenge is to view and filter reports from all three systems in a single place.

OR 

How can we collect, filter, and analyze data from multiple independent microservices and databases in one centralized location without breaking the decoupled nature of the system?


## 

1. How frequently will reports be used?
2. Do you need real-time data?
3. Do you need aggregated or independent reports?
