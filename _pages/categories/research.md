---
layout: archive
permalink: categories/research
title: "Research"

author_profile: true
sidebar:
  nav: "docs"
---

<div class="grid__wrapper">
{% assign posts = site.categories.Research %}
{% for post in posts %}
{% include archive-single3.html type="list" %}
{% endfor %}
</div>
{% include paginator.html %} 