---
layout: default
title: Network Portfolio
permalink: /Network-Portfolio/
---

<h2>Network+ Posts</h2>

{% for post in site.categories.network %}
  <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
  <p>{{ post.date | date: "%B %d, %Y" }}</p>
  <p>{{ post.excerpt }}</p>
  <p>{{ post.categories }}</p>
{% endfor %}