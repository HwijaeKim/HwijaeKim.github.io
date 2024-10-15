---
layout: archive
permalink: categories/education
title: "Education"

author_profile: true
sidebar:
  nav: "sidebar-category"
---

{% assign posts = site.categories.education %}
{% for post in posts %} {% include archive-single3.html type=page.entries_layout %} {% endfor %}