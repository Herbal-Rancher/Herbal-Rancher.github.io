---
layout: default
title: zBible Study
permalink: /zBible-Study/
---

<h1>Howdy and Welcome to zBible Study Posts</h1>

{% for post in site.categories.zbible %}

  <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
  <p>{{ post.date | date: "%B %d, %Y" }}</p>
  <p>{{ post.excerpt }}</p>  
  <a href="{{ post.url }}">Read More →</a>
  <div style="height:1px; background:#ddd; margin:30px 0;"></div>
{% endfor %}

## 🔗 Navigation

* **[Refresh zBible Study](/zBible-study/)**
* **[Home](/)**
* **[Network+ Portfolio](/portfolio/)**

---