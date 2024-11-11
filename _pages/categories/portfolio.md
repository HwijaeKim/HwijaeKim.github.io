---
layout: archive
permalink: categories/portfolio
title: "Portfolio"

author_profile: true
sidebar:
  nav: "sidebar-category"
---

<div class="grid__wrapper">
{% assign posts = site.categories.Portfolio %}
{% for post in posts %}
{% include archive-single3.html type="list" %}
{% endfor %}
</div>