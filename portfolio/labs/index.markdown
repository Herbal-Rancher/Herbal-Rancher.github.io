---
layout: page
permalink: /portfolio/labs/
---

---
---
---

# Lab Walkthroughs

This section documents hands-on labs, configurations, troubleshooting processes, and technical implementation activities completed throughout my Network Technology coursework.

Each walkthrough captures commands, workflows, configuration steps, troubleshooting methods, and practical networking concepts reinforced through lab-based learning.

---

## 🎯 Purpose

* Demonstrate applied technical skills
* Document repeatable workflows
* Capture troubleshooting and debugging processes

---
---
---
---

## IT532 — Introduction to Networking Concepts
#### Lessons 1 – 9
---
---
---
---

{% assign it532_lessons = "1.0,2.0,3.0,4.0,5.0,6.0,7.0,8.0,9.0" | split: "," %}

{% for lesson_number in it532_lessons %}
{% assign lesson_labs = site.categories.labs | where: "lesson", lesson_number  %}

{% for post in lesson_labs %}

<h3>
  Lesson {{ post.lesson }}: <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
</h3>

<div style="margin-top: 6px; margin-bottom: 10px;">
  {{ post.excerpt | strip_html | truncatewords: 45 }}
</div>

<a href="{{ post.url | relative_url }}">Read More →</a>

<div style="height:1px; background:#ddd; margin:30px 0;"></div>
{% endfor %}
{% endfor %}

---
---
---
---

## IT533 - Introduction to Networking Virtual Labs
#### Lessons 10 – 18

---
---
---
---

{% assign it533_lessons = "10.0,11.0,12.0,13.0,14.0,15.0,16.0,17.0,18.0" | split: "," %}

{% for lesson_number in it533_lessons %}
{% assign lesson_labs = site.categories.labs | where: "lesson", lesson_number %}

{% for post in lesson_labs %}
<h3>
  Lesson {{ post.lesson }}: <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
</h3>

<div style="margin-top: 6px; margin-bottom: 10px;">
  {{ post.excerpt | strip_html | truncatewords: 45 }}
</div>

<a href="{{ post.url | relative_url }}">Read More →</a>

<div style="height:1px; background:#ddd; margin:30px 0;"></div>
{% endfor %}
{% endfor %}


---
---
---

## 🔗 Navigation

* [Home](/)
* [Network+ Portfolio](/portfolio/)
  * [Formative Lessons](/portfolio/formative-lessons/)
  * **[LAB WALKTHROUGHS](/portfolio/labs/)**
  * [Video Walkthroughs](/portfolio/videos/)
  * [Study Diagrams](/portfolio/study-diagrams/)
* [zBible Study](/zBible-Study/)

---
---
---