---
layout: default
title: zBible Study
permalink: /zBible-Study/
---

<h1>zBible Study Posts</h1>

{% for post in site.categories.zbible %}
  <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
  <p>{{ post.date | date: "%B %d, %Y" }}</p>
  <p>{{ post.excerpt }}</p>  
{% endfor %}