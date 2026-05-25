---
layout: page
title: "z-Bible Study"
permalink: /zBible-Study/
---

---
---
---

This page serves as a dedicated space for my zBible study notes, reflections, and insights. It is designed to document my journey through 
the Bible, capturing key learnings, personal reflections, and applications of biblical principles in my life.

{% for post in site.categories.zbible %}

  <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
  <p>{{ post.date | date: "%B %d, %Y" }}</p>
  <p>{{ post.excerpt }}</p>  
  <a href="{{ post.url }}">Read More →</a>
  <div style="height:1px; background:#ddd; margin:30px 0;"></div>
{% endfor %}

---
---
---

## 🔗 Navigation

* [Home](/)
* [Network+ Portfolio](/portfolio/)
  * [Formative Lessons](/portfolio/formative-lessons/)
  * [Lab Walkthroughs](/portfolio/labs/)
  * [Video Walkthroughs](/portfolio/videos/)
  * [Study Diagrams](/portfolio/study-diagrams/)
* **[Z-BIBLE STUDY](/zBible-Study/)**

---
---
---