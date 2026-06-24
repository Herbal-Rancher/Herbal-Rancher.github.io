---
layout: page
title: "Network+"
permalink: /network-portfolio/
---


---
---
---

This portfolio documents my learning, hands-on labs, and technical labs as I progress through my IT coursework.

## Purpose

This portfolio is designed to:

- Demonstrate technical skill development  
- Document real-world problem-solving  
- Provide structured, repeatable workflows  
- Support academic and professional growth  

This project is part of my lifelong learning portfolio. My goal is to document my study process, share what I learn, and create resources that may help others on similar paths.
To learn more about my background, learning philosophy, use of AI tools, and creative projects, visit my [Behind the Portfolio](/network-portfolio/behind-the-portfolio/) page.

---
---
---

## Learning Structure

This portfolio supports both conceptual learning and practical application by providing a structured framework to document, organize, review, and demonstrate networking technologies and related technical skills.

The portfolio is organized into three primary sections that connect theory, visualization, hands-on practice, troubleshooting, and technical reflection into a progressive learning system.

* **[FORMATIVE MODULES](/network-portfolio/formative-modules/)** — Coursework, learning activities, and competency-based exercises completed throughout my studies.
* **[STUDY DIAGRAMS](/network-portfolio/study-diagrams/)** — AI-assisted visual resources that simplify networking concepts, protocols, architectures, and troubleshooting workflows.
* **[VIDEO WALKTHROUGHS](/network-portfolio/videos/)** — Narration-free demonstrations of labs, Packet Tracer activities, troubleshooting exercises, and technical projects.

---
---
---
<div style="height: 3px; background: #f4b400; margin: 30px 0;"></div>

## Network+ Learning Journey

This section organizes my hands-on CompTIA Network+ studies into topic areas and skill paths. Labs include TestOut exercises, Cisco networking concepts, troubleshooting scenarios, security analysis, packet captures, remote administration, and technical documentation.

---
---
---

{% assign posts = site.posts %}
{% assign category_order = "networking-fundamentals|infrastructure|security|systems-administration|technical-communication" | split: "|" %}


{% for category_key in category_order %}
{% assign category_posts = posts | where: "category", category_key %}

{% if category_posts.size > 0 %}
{% assign category_display = category_posts | map: "category_display" | compact | first %}



<h1 style="border-bottom: 3px solid #ddd; padding-bottom: .35rem; margin-top: 2.5rem;">
  {{ category_display | default: category_key }}
</h1>

<p><strong>Deliverables Completed:</strong> {{ category_posts.size }}</p>

{% assign subcategory_keys = category_posts | map: "subcategory" | uniq | compact %}

{% for subcategory_key in subcategory_keys %}
{% assign subcategory_posts = category_posts | where: "subcategory", subcategory_key %}
{% assign subcategory_display = subcategory_posts | map: "subcategory_display" | compact | first %}


<div style="margin-left: 1.75rem; margin-top: 1.5rem; padding-left: 1rem; border-left: 3px solid #e5e5e5;">

<h2 style="margin-bottom: .25rem;">
  {{ subcategory_display | default: subcategory_key }}: </h2><strong>{{ subcategory_posts.size }}</strong> Deliverables Completed

<ul>
{% for post in subcategory_posts %}
  <li>
    ✓ <a href="{{ post.url | relative_url }}">
      {% if post.lesson_id %}
        {{ post.lesson_id }} {{post.content_type_display }}: {{ post.lab_title }}
      {% else %}
        {{ post.title }}
      {% endif %}
    </a>
  </li>
{% endfor %}
</ul>

{% assign all_topics = "" | split: "" %}

{% for post in subcategory_posts %}
{% if post.topics %}
{% assign all_topics = all_topics | concat: post.topics %}
{% endif %}
{% endfor %}

{% assign unique_topics = all_topics | uniq | sort %}

{% if unique_topics.size > 0 %}

<p><strong>Skills Practiced:</strong> [
{% for topic in unique_topics %}
  {{ topic | replace: "-", " " | capitalize }},
{% endfor %}
] </p>
{% endif %}

{% assign all_tools = "" | split: "" %}

{% for post in subcategory_posts %}
{% if post.tools %}
{% assign all_tools = all_tools | concat: post.tools %}
{% endif %}
{% endfor %}

{% assign unique_tools = all_tools | uniq | sort %}

{% if unique_tools.size > 0 %}

<p><strong>Tools Used:</strong> [
{% for tool in unique_tools %}
  {{ tool | replace: "-", " " }},
{% endfor %}
]</p>
{% endif %}

</div>

{% endfor %}

{% endif %}
{% endfor %}


## 🔗 Navigation

* [Home](/)
* **[NETWORK+ PORTFOLIO](/network-portfolio/)**
  * [Formative Modules](/network-portfolio/formative-modules/)
  * [Video Walkthroughs](/network-portfolio/videos/)
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* [Bible Study](/bible-study/)
* [Behind the Portfolio](/network-portfolio/behind-the-portfolio/)

---
---
---