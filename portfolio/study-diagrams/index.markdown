---
layout: page
permalink: /portfolio/study-diagrams/
nav_exclude: true
---

---
---
---

# Study Diagrams

This page is a collection of study diagrams created during my Network Technology learning journey.

When I take practice exams, complete labs, or review networking concepts, I sometimes come across a question or topic that I only partially understand — or do not understand yet. When that happens, I use ChatGPT to help turn the knowledge gap into a visual study aid.

These diagrams are generated from my real learning process. Each image represents a concept I needed to slow down, review, and understand more clearly.

---
---
---

<div style="height: 3px; background: #f4b400; margin: 30px 0;"></div>

## Purpose of This Page

The purpose of this page is to:

- Learn from knowledge gaps
- Document areas where I needed additional study
- Turn difficult topics into visual explanations
- Create quick-reference study material for future review
- Support my preparation for Network+ and future cybersecurity learning
- Share helpful visuals with others who may be learning the same concepts

---

## How These Diagrams Are Created

Each diagram begins with a question, practice exam topic, or networking concept that I want to understand better.

I ask ChatGPT to create a clear visual explanation based on the topic. I then use the diagram as a study tool to reinforce the concept, review terminology, and connect the topic to real-world networking.

These images are not meant to replace official course material, vendor documentation, or certification objectives. They are study aids created to help me understand and remember important ideas.

---

## Study Diagram Collection

These diagrams were created to help reinforce difficult networking concepts, troubleshoot knowledge gaps, and improve long-term retention through visual learning.

Many of these diagrams were generated while studying for Network+ topics, reviewing practice exam questions, or working through labs and troubleshooting scenarios.


{% assign diagrams = site.posts | where: "content_type", "diagram" | where: "status", "complete" %}
{% assign category_order = "networking-fundamentals|infrastructure|security|systems-administration|technical-communication" | split: "|" %}

{% for category_key in category_order %}
{% assign category_posts = diagrams | where: "category", category_key %}

{% if category_posts.size > 0 %}
{% assign category_display = category_posts | map: "category_display" | compact | first %}

<h1 style="border-bottom: 3px solid #ddd; padding-bottom: .35rem; margin-top: 2.5rem;">
  {{ category_display | default: category_key }}
</h1>

<p><strong>Diagrams Completed:</strong> {{ category_posts.size }}</p>

{% assign subcategory_keys = category_posts | map: "subcategory" | uniq | compact %}

{% for subcategory_key in subcategory_keys %}
{% assign subcategory_posts = category_posts | where: "subcategory", subcategory_key %}
{% assign subcategory_display = subcategory_posts | map: "subcategory_display" | compact | first %}

<div style="margin-left: 1.75rem; margin-top: 1.5rem; padding-left: 1rem; border-left: 3px solid #e5e5e5;">

<h2 style="margin-bottom: .25rem;">
  {{ subcategory_display | default: subcategory_key }}
</h2>

<p><strong>Diagrams Completed:</strong> {{ subcategory_posts.size }}</p>

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 24px; margin: 20px 0;">

{% for post in subcategory_posts %}

<div style="text-align:center; border: 1px solid #ddd; border-radius: 10px; padding: 12px;">

{% if post.image %} <a href="{{ post.image | relative_url }}" target="_blank" rel="noopener noreferrer"> <img src="{{ post.image | relative_url }}"
    alt="{{ post.image_alt | default: post.title }}"
    style="width: 100%; max-width: 360px; border-radius: 8px;"> </a>
{% endif %}

<p style="margin-top: 10px; margin-bottom: 4px;">
  <strong>
    {% if post.lesson_id %}
      {{ post.lesson_id }} |
    {% endif %}
    {{ post.lab_title | default: post.title }}
  </strong>
</p>

{% if post.diagram_topic %}

<p style="margin-top: 0; margin-bottom: 6px;">
  <strong>Topic:</strong> {{ post.diagram_topic }}
</p>
{% endif %}

{% if post.diagram_reason %}

<p style="margin-top: 0; margin-bottom: 8px;">
  <em>{{ post.diagram_reason }}</em>
</p>
{% endif %}

<p style="margin-top: 0;">
  <a href="{{ post.url | relative_url }}">View Notes</a>
  |
  <a href="{{ post.image | relative_url }}" target="_blank" rel="noopener noreferrer">Open Image</a>
</p>

</div>

{% endfor %}

</div>

</div>

{% endfor %}

<hr>

{% endif %}
{% endfor %}


## Reflection

Using diagrams has helped me slow down and learn more intentionally. Instead of simply marking a question wrong or guessing through an unfamiliar topic, I use the confusion as a starting point for deeper study.

Each image on this page represents a moment where I identified a gap in my understanding and turned it into a learning resource.

This process helps me build stronger technical knowledge, prepare for certification exams, and create a portfolio that shows how I learn, troubleshoot, and grow.

---

## Ongoing Updates

This page will continue to grow as I study new topics, complete labs, and prepare for Network+ and cybersecurity concepts.

---
---
---

## 🔗 Navigation

* [Home](/)
* [Network+ Portfolio](/portfolio/)
  * [Formative Lessons](/portfolio/formative-lessons/)
  * [Lab Walkthroughs](/portfolio/labs/)
  * [Video Walkthroughs](/portfolio/videos/)
  * **[STUDY DIAGRAMS](/portfolio/study-diagrams/)**
* [zBible Study](/zBible-Study/)
* [About Me](/about/)

---
---
---
