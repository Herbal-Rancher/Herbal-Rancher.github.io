---
layout: page
title: ""
permalink: /portfolio/formative-lessons/
---

# Formative Lessons

This section captures the **core concepts, theories, and foundational knowledge** I am developing throughout my IT coursework.

Each lesson represents a key learning milestone and is supported by related hands-on walkthroughs.

---

## 🎯 Purpose

* Reinforce conceptual understanding
* Connect theory to practical application
* Track learning progression over time


---
## [Lesson 01]({{ '/portfolio/formative-lessons/lesson-1-0/' | relative_url }})

{% assign walkthroughs = site.posts
  | where: "lesson", "1.0"
  | where_exp: "post", "post.categories contains 'walkthroughs'"
  | sort: "order" %}

{% if walkthroughs.size > 0 %}
  <ul>
  {% for post in walkthroughs %}
    <li>
      <a href="{{ post.url | relative_url }}">
        {{ post.title }}
      </a>
    </li>
  {% endfor %}
  </ul>
{% else %}
  <p><b><em><a href="/tbd.html">2.1 TBD 2.1</a></em></b></p>
{% endif %}

---

## [Lesson 02]({{ '/portfolio/formative-lessons/lesson-2-0/' | relative_url }})

{% assign walkthroughs = site.posts
  | where: "lesson", "2.0"
  | where_exp: "post", "post.categories contains 'walkthroughs'"
  | sort: "order" %}

{% if walkthroughs.size > 0 %}
  <ul>
  {% for post in walkthroughs %}
    <li>
      <a href="{{ post.url | relative_url }}">
        {{ post.title }}
      </a>
    </li>
  {% endfor %}
  </ul>
{% else %}
  <ul>
    <li><p><b><em><a href="/tbd.html">2.1 TBD 2.1</a></em></b></p></li>
  </ul>
{% endif %}


---

## 🔗 Navigation

* **[Refresh Formative Lessons](/portfolio/formative-lessons/)**
* **[Walkthroughs](/portfolio/walkthroughs/)**
* **[Network+ Portfolio](/portfolio/)**
* **[zBible Study](/zBible-study/)**
* **[Home](/)**

---