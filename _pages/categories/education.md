---
layout: archive
permalink: categories/education
title: "Education"

author_profile: true
sidebar:
  nav: "sidebar-category"
---

<div class="grid__wrapper">
{% assign posts = site.categories.Education %}
{% for post in posts %}
{% include archive-single3.html type="list" %}
{% endfor %}
</div>