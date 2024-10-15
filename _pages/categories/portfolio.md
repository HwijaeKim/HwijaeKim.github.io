---
layout: archive
permalink: categories/portfolio
title: "Portfolio(포트폴리오)"

author_profile: true
sidebar:
  nav: "docs"
---


{% assign posts = site.categories.Portfolio %}
{% for post in posts %} {% include archive-single3.html type=page.entries_layout %} {% endfor %}

<!-- <ul>
  {% for post in site.posts %}
    {% if post.categories contains "포트폴리오" %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
        <span>{{ post.date | date: "%Y-%m-%d" }}</span>
      </li>
    {% endif %}
  {% endfor %}
</ul>

<div class="grid__wrapper">
    {% for post in paginator.posts %}
    {% include archive-single3.html type="list" %}
    {% endfor %}
</div>
{% include paginator.html %}  -->