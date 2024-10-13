---
layout: archive
permalink: categories/projects
title: "Projects"

author_profile: true
sidebar:
  nav: "docs"
---

{% assign posts = site.categories.Projects %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}

<div class="grid__wrapper">
    {% for post in paginator.posts %}
    {% include archive-single3.html type="list" %}
    {% endfor %}
</div>
{% include paginator.html %} 