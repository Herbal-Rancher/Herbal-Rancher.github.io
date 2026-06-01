---
layout: page
permalink: /portfolio/formative-lessons/
nav_exclude: true
---


---
---
---

# Formative Lessons

This section captures the **core concepts, theories, and foundational knowledge** I am developing throughout my IT coursework.

Each module represents a key learning milestone and is supported by related hands-on labs.

---

## Purpose

* Reinforce conceptual understanding
* Connect theory to practical application
* Track learning progression over time

---
{% assign it532_lessons = "1.0,2.0,3.0,4.0,5.0,6.0,7.0,8.0,9.0" | split: "," %}
{% assign it533_lessons = "10.0,11.0,12.0,13.0,14.0,15.0,16.0,17.0,18.0" | split: "," %}

___
___
---
### IT532 — Intro to Networking Concepts: Lessons 1 – 9
___
___
---

{% for lesson_number in it532_lessons %}
{% assign lesson_posts = site.posts | where: "lesson", lesson_number %}

{% assign has_content = false %}
{% for post in lesson_posts %}
{% if post.categories contains "assessment" or post.categories contains "milestone" or post.categories contains "summative" or post.categories contains "discussion" or post.categories contains "labs" or post.categories contains "walkthroughs" %}
{% assign has_content = true %}
{% endif %}
{% endfor %}

{% if has_content %}

<hr style="border: 1px solid #ddd;">

### Lesson {{ lesson_number }}

#### Discussions, Milestones, and Summative Assessments

<ul style="margin-top: 0; margin-bottom: 12px;">
{% assign has_assessments = false %}
{% for post in lesson_posts %}
{% if post.categories contains "assessment" or post.categories contains "milestone" or post.categories contains "summative" or post.categories contains "discussion" %}
{% assign has_assessments = true %}
<li style="margin-bottom: 6px;">
  <a href="{{ post.url | relative_url }}">{{ post.title }}</a><br>
</li>
{% endif %}
{% endfor %}
{% if has_assessments == false %}
<li style="margin-bottom: 4px;"><span style="color: #666;"><em>Discussions and assessments will continue to expand as additional lessons are completed.</em></span></li>
{% endif %}
</ul>

#### Labs and Walkthroughs

<ul style="margin-top: 0; margin-bottom: 12px;">
{% assign has_labs = false %}
{% for post in lesson_posts %}
{% if post.categories contains "labs" or post.categories contains "walkthroughs" %}
{% assign has_labs = true %}
<li style="margin-bottom: 6px;">
  <a href="{{ post.url | relative_url }}">{{ post.title }}</a><br>
</li>
{% endif %}
{% endfor %}
{% if has_labs == false %}
<li style="margin-bottom: 4px;"><span style="color: #666;"><em>Labs and walkthroughs will continue to expand as additional lessons are completed.</em></span></li>
{% endif %}
</ul>

{% endif %}
{% endfor %}
___
___
---
### IT533 — Intro to Networking Virtual Labs: Lessons 10 – 18
___
___
---

{% for lesson_number in it533_lessons %}
{% assign lesson_posts = site.posts | where: "lesson", lesson_number %}

{% assign has_content = false %}
{% for post in lesson_posts %}
{% if post.categories contains "assessment" or post.categories contains "milestone" or post.categories contains "summative" or post.categories contains "discussion" or post.categories contains "labs" or post.categories contains "walkthroughs" %}
{% assign has_content = true %}
{% endif %}
{% endfor %}

{% if has_content %}

<hr style="border: 1px solid #ddd;">

### Lesson {{ lesson_number }}

#### Discussions, Milestones, and Summative Assessments

<ul style="margin-top: 0; margin-bottom: 12px;">
{% assign has_assessments = false %}
{% for post in lesson_posts %}
{% if post.categories contains "assessment" or post.categories contains "milestone" or post.categories contains "summative" or post.categories contains "discussion" %}
{% assign has_assessments = true %}
<li style="margin-bottom: 6px;">
  <a href="{{ post.url | relative_url }}">{{ post.title }}</a><br>
 </li>
{% endif %}
{% endfor %}
{% if has_assessments == false %}
<li style="margin-bottom: 4px;"><span style="color: #666;"><em>Discussions and assessments will continue to expand as additional lessons are completed.</em></span></li>
{% endif %}
</ul>

#### Labs and Walkthroughs

<ul style="margin-top: 0; margin-bottom: 12px;">
{% assign has_labs = false %}
{% for post in lesson_posts %}
{% if post.categories contains "labs" or post.categories contains "walkthroughs" %}
{% assign has_labs = true %}
<li style="margin-bottom: 6px;">
  <a href="{{ post.url | relative_url }}">{{ post.title }}</a><br>
 </li>
{% endif %}
{% endfor %}
{% if has_labs == false %}
<li style="margin-bottom: 4px;"><span style="color: #666;"><em>Labs and walkthroughs will continue to expand as additional lessons are completed.</em></span></li>
{% endif %}
</ul>

{% endif %}
{% endfor %}

<hr style="border: 2px solid #ccc;">

---
---
---
## 🔗 Navigation

* [Home](/)
* [Network+ Portfolio](/portfolio/)
  * **[FORMATIVE LESSONS](/portfolio/formative-lessons/)**
  * [Lab Walkthroughs](/portfolio/labs/)
  * [Video Walkthroughs](/portfolio/videos/)
  * [Study Diagrams](/portfolio/study-diagrams/)
* [zBible Study](/zBible-Study/)
* [About Me](/about/)

---
---
---