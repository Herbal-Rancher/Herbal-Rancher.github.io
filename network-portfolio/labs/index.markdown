---
layout: page
permalink: /network-portfolio/labs/
nav_exclude: true
---

---
---
---

# Lab Walkthroughs

This section documents hands-on labs, configurations, troubleshooting processes, and technical implementation activities completed throughout my Network Technology coursework.

Each walkthrough captures commands, workflows, configuration steps, troubleshooting methods, and practical networking concepts reinforced through lab-based learning.


This project is part of my lifelong learning portfolio. My goal is to document my study process, share what I learn, and create resources that may help others on similar paths.
To learn more about my background, learning philosophy, use of AI tools, and creative projects, visit my [About the Portfolio](/about/) page.

---
---
---

<div style="height: 3px; background: #f4b400; margin: 30px 0;"></div>

## 🎯 Purpose

* Demonstrate applied technical skills
* Document repeatable workflows
* Capture troubleshooting and debugging processes

---
---
---

## IT532 — Introduction to Networking Concepts
#### Lessons 1 – 9
---
---
---

{% assign it532_lessons = "1.0,2.0,3.0,4.0,5.0,6.0,7.0,8.0,9.0" | split: "," %}

{% for lesson_number in it532_lessons %}

  {% assign lesson_labs = site.categories.labs | where: "lesson", lesson_number %}

  {% if lesson_labs.size > 0 %}

<!-- RESET POINT: each lesson starts fresh here -->
<div style="margin-top: 30px; margin-left: 0;">

<!-- ALL content indented ONLY once -->
<div style="margin-left: 25px;">
<h2 style="margin: 0 0 10px 0;">
    Lesson {{ lesson_number }}
</h2>

{% for post in lesson_labs %}

<!-- Each post block is NOT additionally indented -->
<div style="margin-bottom: 25px;">

<h3 style="margin-bottom: 5px;">
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
</h3>

<div style="margin-bottom: 8px;">
    {{ post.excerpt | strip_html | truncatewords: 45 }}
</div>

<a href="{{ post.url | relative_url }}">Read More →</a>

</div>

{% endfor %}

</div>
</div>
<div style="height:1px; background:#ddd; margin:30px 0;"></div>

  {% endif %}

{% endfor %}


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

  {% if lesson_labs.size > 0 %}

<!-- RESET POINT: each lesson starts fresh here -->
<div style="margin-top: 30px; margin-left: 0;">



<!-- ALL content indented ONLY once -->
<div style="margin-left: 25px;">
<h2 style="margin: 0 0 10px 0;">
    Lesson {{ lesson_number }}
</h2>

{% for post in lesson_labs %}

<!-- Each post block is NOT additionally indented -->
<div style="margin-bottom: 25px;">

<h3 style="margin-bottom: 5px;">
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
</h3>

<div style="margin-bottom: 8px;">
    {{ post.excerpt | strip_html | truncatewords: 45 }}
</div>

<a href="{{ post.url | relative_url }}">Read More →</a>

</div>

{% endfor %}

</div>
</div>
<div style="height:1px; background:#ddd; margin:30px 0;"></div>

  {% endif %}

{% endfor %}


---
---
---

## 🔗 Navigation

* [Home](/)
* [Network+ Portfolio](/network-portfolio/)
  * [Formative Modules](/network-portfolio/formative-modules/)
  * **[LAB WALKTHROUGHS](/network-portfolio/labs/)**
  * [Video Walkthroughs](/network-portfolio/videos/)
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* [Trading+](/trading/)
* [Bible Study](/bible-study/)
* [About the Portfolio](/about/)

---
---
---