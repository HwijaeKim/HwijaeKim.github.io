---
layout: archive
permalink: categories/code
title: "Code"

author_profile: true
sidebar:
  nav: "sidebar-category"
---

<div class="grid__wrapper">
{% assign posts = site.categories.Code %}
{% for post in posts %}
{% include archive-single3.html type="list" %}
{% endfor %}
</div>