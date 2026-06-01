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

<div style="height: 3px; background: #f4b400; margin: 30px 0;"></div>

{% assign diagram_categories = "switching-infrastructure|Network Switching & Infrastructure,fiber-physical-media|Fiber Optics & Physical Media,routing-network-communication|Routing & Network Communication" | split: "," %}

{% for category_pair in diagram_categories %}
{% assign category_parts = category_pair | split: "|" %}
{% assign category_key = category_parts[0] %}
{% assign category_title = category_parts[1] %}

{% assign diagrams = site.posts | where: "diagram_category", category_key | sort: "sort_order" %}

{% if diagrams.size > 0 %}

# {{ category_title }}

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 28px; margin: 25px 0;">

{% for post in diagrams %}
{% if post.categories contains "diagrams" %}

  <div style="text-align:center; margin-bottom: 25px;">
    <a href="{{ post.image | relative_url }}" target="_blank" rel="noopener noreferrer">
      <img src="{{ post.image | relative_url }}"
           alt="{{ post.image_alt }}"
           style="width: 100%; max-width: 420px; border-radius: 8px;">
    </a>

    <p style="margin-top: 10px; margin-bottom: 4px;">
      <strong>{{ post.title }}</strong>
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
      <a href="{{ post.image | relative_url }}" target="_blank" rel="noopener noreferrer">
        Open full image
      </a>
    </p>
  </div>

{% endif %}
{% endfor %}

</div>

---

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
