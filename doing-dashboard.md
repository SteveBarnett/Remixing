---
layout: theme-now
title: Doing
class: dashboard
---

{% assign currentMonth = site.time | date: "%B" %}

{% include themes/2026/{{ currentMonth | downcase }}.md %}
