---
layout: archive
permalink: categories/education
title: "Education"

author_profile: true
sidebar:
  nav: "docs"
---

{% assign posts = site.categories.Education %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}