---
title: Essays
layout: base
header-title: Essays
---

# Essays

This template includes three sample essays on Southwest food history — nachos, chiles, and tamales — written with AI assistance as placeholder content. They're here to demonstrate what student essays can look like: how to use images, pull quotes, scrolling backgrounds, and other Xanthan components in a longer piece of writing.

Browse them to get a feel for the format. When you're ready to build your own project, you'll replace these with your students' essays — same structure, your topic.

{% assign all_pages = site.pages %}
{% assign cards = all_pages | where_exp: "p", "p.path contains 'essays/'" | where_exp: "p", "p.path != 'essays/index.md'" %}

{% include nav/card-grid.html cards=cards %}
