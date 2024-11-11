---
layout: archive
permalink: categories/jekyll
title: "Jekyll"

author_profile: true
sidebar:
  nav: "sidebar-category"
---

<div class="grid__wrapper">
{% assign posts = site.categories.Jekyll %}
{% for post in posts %}
{% include archive-single3.html type="list" %}
{% endfor %}
</div>
{% include paginator.html %} 