---
layout: page
permalink: /network-portfolio/formative-modules/
nav_exclude: true
date: 2026-04-01 10:00:00 -0700
---

# Formative Modules

This section captures the **core concepts, theories, and foundational knowledge** I am developing throughout my IT coursework.

Each module represents a key learning milestone supported by related discussions, assessments, labs, walkthroughs, diagrams, and technical documentation.

This project is part of my lifelong learning portfolio. My goal is to document my study process, share what I learn, and create resources that may help others on similar paths.

To learn more about my background, learning philosophy, use of AI tools, and creative projects, visit my [Behind the Portfolio](/network-portfolio/behind-the-portfolio/) page.

---

## Purpose

* Reinforce conceptual understanding
* Connect theory to practical application
* Track learning progression over time
* Organize coursework, labs, and technical documentation by Module

---

{% assign it532_lessons = "1.0,2.0,3.0,4.0,5.0,6.0,7.0,8.0,9.0" | split: "," %}
{% assign it533_lessons = "10.0,11.0,12.0,13.0,14.0,15.0,16.0,17.0,18.0" | split: "," %}

<h2 style="border-bottom: 2px solid #f4b400; padding-bottom: .35rem; margin-top: 2.5rem;">
  IT532 — Intro to Networking Concepts
</h2>

<p>
Modules 01 – 09 focus on foundational networking theory, protocols, models, terminology, and conceptual understanding.
</p>

<p style="margin-top: 0; color: #555;">
  Related discussions, assessments, labs, walkthroughs, diagrams, and study resources.
</p>

<div style="margin-left: 1.25rem; margin-top: 1rem; padding-left: 1rem; border-left: 3px solid #e5e5e5;">

{% for lesson_number in it532_lessons %}

{% assign module_posts = site.posts | where: "lesson", lesson_number | where: "status", "complete" %}

{% if module_posts.size > 0 %}

<div style="margin: 1.5rem 0; padding: 1rem; border: 1px solid #ddd; border-radius: 10px; background: #fafafa;">

<h3 style="margin-top: 0; margin-bottom: .35rem;">
  Module {{ lesson_number }}
  <span style="background: #f4b400; color: #000; padding: .15rem .5rem; border-radius: 12px; font-size: .75rem;">
    {{ module_posts.size }} Posts
  </span>
</h3>

<p style="font-weight: bold; margin-bottom: .25rem;">
  Discussions & Assessments
</p>

<ul style="margin-top: 0; margin-bottom: 1rem;">
{% assign has_assessments = false %}

{% for post in module_posts %}
  {% if post.categories contains "assessment" or post.categories contains "milestone" or post.categories contains "summative" or post.categories contains "discussion" %}
    {% assign has_assessments = true %}
    <li style="margin-bottom: .5rem;">
      ✓ <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      {% if post.content_type_display %}
      <span style="background: #eef3ff; padding: .1rem .45rem; border-radius: 10px; font-size: .72rem;">
        {{ post.content_type_display }}
      </span>
      {% endif %}
    </li>
  {% endif %}
{% endfor %}

{% if has_assessments == false %}
<li style="margin-bottom: .4rem;">
  <span style="color: #666;"><em>Discussions and assessments will continue to expand as additional Modules are completed.</em></span>
</li>
{% endif %}
</ul>

<p style="font-weight: bold; margin-bottom: .25rem;">
  Labs, Walkthroughs, Diagrams & Reference Resources
</p>

<ul style="margin-top: 0; margin-bottom: 0;">
{% assign has_resources = false %}

{% for post in module_posts %}
  {% if post.categories contains "labs" or post.categories contains "walkthroughs" or post.categories contains "videos" or post.categories contains "diagrams" or post.categories contains "reference-guides" or post.categories contains "guides" %}
    {% assign has_resources = true %}
    <li style="margin-bottom: .5rem;">
      ✓ <a href="{{ post.url | relative_url }}">
        {% if post.lesson_id %}
          {{ post.lesson_id }}:
        {% endif %}
        {{ post.lab_title | default: post.title }}
      </a>
      {% if post.content_type_display %}
      <span style="background: #eef3ff; padding: .1rem .45rem; border-radius: 10px; font-size: .72rem;">
        {{ post.content_type_display }}
      </span>
      {% endif %}
    </li>
  {% endif %}
{% endfor %}

{% if has_resources == false %}
<li style="margin-bottom: .4rem;">
  <span style="color: #666;"><em>Labs, walkthroughs, diagrams, and reference resources will continue to expand as additional Modules are completed.</em></span>
</li>
{% endif %}
</ul>

</div>

{% endif %}
{% endfor %}

</div>

<h2 style="border-bottom: 2px solid #f4b400; padding-bottom: .35rem; margin-top: 2.5rem;">
  IT533 — Intro to Networking Virtual Labs
</h2>

<p>
Modules 10 – 18 focus on hands-on implementation, troubleshooting, security analysis, virtual labs, remote administration, and applied networking skills.
</p>

<p style="margin-top: 0; color: #555;">
  Related discussions, assessments, labs, walkthroughs, diagrams, and study resources.
</p>

<div style="margin-left: 1.25rem; margin-top: 1rem; padding-left: 1rem; border-left: 3px solid #e5e5e5;">

{% for lesson_number in it533_lessons %}

{% assign module_posts = site.posts | where: "lesson", lesson_number | where: "status", "complete" %}
{% if module_posts.size > 0 %}

<div style="margin: 1.5rem 0; padding: 1rem; border: 1px solid #ddd; border-radius: 10px; background: #fafafa;">

<h3 style="margin-top: 0; margin-bottom: .35rem;">
  Module {{ lesson_number }}
  <span style="background: #f4b400; color: #000; padding: .15rem .5rem; border-radius: 12px; font-size: .75rem;">
    {{ module_posts.size }} Posts
  </span>
</h3>

<p style="font-weight: bold; margin-bottom: .25rem;">
  Discussions & Assessments
</p>

<ul style="margin-top: 0; margin-bottom: 1rem;">
{% assign has_assessments = false %}

{% for post in module_posts %}
  {% if post.categories contains "assessment" or post.categories contains "milestone" or post.categories contains "summative" or post.categories contains "discussion" %}
    {% assign has_assessments = true %}
    <li style="margin-bottom: .5rem;">
      ✓ <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      {% if post.content_type_display %}
      <span style="background: #eef3ff; padding: .1rem .45rem; border-radius: 10px; font-size: .72rem;">
        {{ post.content_type_display }}
      </span>
      {% endif %}
    </li>
  {% endif %}
{% endfor %}

{% if has_assessments == false %}
<li style="margin-bottom: .4rem;">
  <span style="color: #666;"><em>Discussions and assessments will continue to expand as additional Modules are completed.</em></span>
</li>
{% endif %}
</ul>

<p style="font-weight: bold; margin-bottom: .25rem;">
  Labs, Walkthroughs, Diagrams & Reference Resources
</p>

<ul style="margin-top: 0; margin-bottom: 0;">
{% assign has_resources = false %}

{% for post in module_posts %}
  {% if post.categories contains "labs" or post.categories contains "walkthroughs" or post.categories contains "videos" or post.categories contains "diagrams" or post.categories contains "reference-guides" or post.categories contains "guides" %}
    {% assign has_resources = true %}
    <li style="margin-bottom: .5rem;">
      ✓ <a href="{{ post.url | relative_url }}">
        {% if post.lesson_id %}
          {{ post.lesson_id }}:
        {% endif %}
        {{ post.lab_title | default: post.title }}
      </a>
      {% if post.content_type_display %}
      <span style="background: #eef3ff; padding: .1rem .45rem; border-radius: 10px; font-size: .72rem;">
        {{ post.content_type_display }}
      </span>
      {% endif %}
    </li>
  {% endif %}
{% endfor %}

{% if has_resources == false %}
<li style="margin-bottom: .4rem;">
  <span style="color: #666;"><em>Labs, walkthroughs, diagrams, and reference resources will continue to expand as additional Modules are completed.</em></span>
</li>
{% endif %}
</ul>

</div>

{% endif %}
{% endfor %}

</div>


---
---
---
## 🔗 Navigation

* [Home](/)
* [Network+ Portfolio](/network-portfolio/)
  * **[FORMATIVE MODULES](/network-portfolio/formative-modules/)**
  * [Video Walkthroughs](/network-portfolio/videos/)
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* [Bible Study](/bible-study/)
* [Behind the Portfolio](/network-portfolio/behind-the-portfolio/)

---
---
---