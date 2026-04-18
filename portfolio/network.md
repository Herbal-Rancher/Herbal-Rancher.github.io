---
layout: default
permalink: portfolio/formative-lessons/Network-Portfolio/
---

<h1>Welcome to My Network+ Portfolio</h1>

{% for post in site.categories.network %}
  <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
  <p>{{ post.date | date: "%B %d, %Y" }}</p>
  <p>{{ post.excerpt }}</p>
  <a href="{{ post.url }}">Read More →</a>
  <div style="height:1px; background:#ddd; margin:30px 0;"></div>
{% endfor %}