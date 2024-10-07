---
layout: archive
permalink: categories/solve
title: "문제해결"

author_profile: true
sidebar:
  nav: "docs"
---

{% assign posts = site.categories.solve %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}
