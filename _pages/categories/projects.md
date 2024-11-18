---
layout: archive
permalink: categories/projects
title: "Projects"

author_profile: true
sidebar:
  nav: "sidebar-category"
---

<div class="grid__wrapper">
{% assign posts = site.categories.Projects %}
{% for post in posts %}
{% include archive-single3.html type="list" %}
{% endfor %}
</div>