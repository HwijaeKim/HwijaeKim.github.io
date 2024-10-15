---
layout: archive
permalink: categories/portfolio
title: "Portfolio"

author_profile: true
sidebar:
  nav: "sidebar-category"
---

{% assign posts = site.categories.portfolio %}
{% for post in posts %} {% include archive-single3.html type=page.entries_layout %} {% endfor %}