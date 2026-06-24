---
layout: page
title: "Bible Study"
permalink: /bible-study/
date: 2026-04-01 10:00:00 -0700
---

---
---
---

This page serves as a dedicated space for my Bible study notes, reflections, and insights. It is designed to document my journey through 
the Bible, discovering and documenting key lessons, personal reflections, and applications of biblical principles in my life. 

This project is part of my lifelong learning portfolio. My goal is to document my study process, share what I learn, and create resources that may help others on similar paths.

To learn more about my background, learning philosophy, use of AI tools, and creative projects, visit my [Behind the Portfolio](/network-portfolio/behind-the-portfolio/) page.

---
---
---
<div style="height: 3px; background: #f4b400; margin: 30px 0;"></div>


{% assign bible_posts = site.categories.bible | where: "status", "complete" | sort: "sort_order" %}
{% assign testament_keys = bible_posts | map: "subcategory" | uniq | compact %}

{% for testament_key in testament_keys %}
{% assign testament_posts = bible_posts | where: "subcategory", testament_key %}
{% assign testament_display = testament_posts | map: "subcategory_display" | compact | first %}

<h2 style="border-bottom: 3px solid #ddd; padding-bottom: .35rem; margin-top: 2.5rem;">
  {{ testament_display | default: testament_key }}
</h2>

{% assign book_group_keys = testament_posts | map: "book_group" | uniq | compact %}

{% for book_group_key in book_group_keys %}
{% assign book_group_posts = testament_posts | where: "book_group", book_group_key %}
{% assign book_group_display = book_group_posts | map: "book_group_display" | compact | first %}

<div style="margin-left: 1.5rem; margin-top: 1.5rem; padding-left: 1rem; border-left: 3px solid #e5e5e5;">

<h3 style="margin-bottom: .25rem;">
  {{ book_group_display | default: book_group_key }}
</h3>
<p><strong>Studies Completed:</strong> {{ book_group_posts.size }}</p>

{% assign book_keys = book_group_posts | map: "book" | uniq | compact %}

{% for book_key in book_keys %}
{% assign book_posts = book_group_posts | where: "book", book_key %}
{% assign book_display = book_posts | map: "book_display" | compact | first %}

<div style="margin-left: 1.25rem; margin-top: 1rem; padding-left: 1rem; border-left: 2px solid #eee;">
<ul>
{% for post in book_posts %}
  <li>

    <a href="{{ post.url | relative_url }}">
      {% if post.lesson_id %}
        {{ post.lesson_id }}: {{ post.lab_title | default: post.title }}
      {% else %}
        {{ post.lab_title | default: post.title }}
      {% endif %}
    </a>
    <br>
  </li>
{% endfor %}
</ul>

</div>

{% endfor %}

</div>

{% endfor %}

{% endfor %}


---
---
---

## 🔗 Navigation

* [Home](/)
* [Network+ Portfolio](/network-portfolio/)
  * [Formative Modules](/network-portfolio/formative-modules/)
  * [Video Walkthroughs](/network-portfolio/videos/)
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* **[BIBLE STUDY](/bible-study/)**
* [Behind the Portfolio](/network-portfolio/behind-the-portfolio/)

---
---
---