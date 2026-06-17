---
layout: page
permalink: /network-portfolio/videos/
nav_exclude: true
---

---
---
---

# Video Walkthroughs

This page contains no-narration video walkthroughs documenting networking labs, troubleshooting processes, Wireshark analysis, DHCP implementation, switch hardening, PowerShell management, and other hands-on activities completed throughout my Network Technology learning journey.

The videos are grouped by topic to make the collection easier to review, navigate, and revisit over time. Each entry includes a thumbnail preview, a direct YouTube link, and metadata connected to the related lab or networking concept.

Creating these walkthroughs is also part of my learning process. Preparing to record each video requires me to review the lab objectives, configure the environment, troubleshoot issues, and complete the activities multiple times before recording the final walkthrough. Repeating the process helps reinforce commands, procedures, troubleshooting methods, and overall networking concepts while improving long-term retention and practical understanding.

These walkthroughs are intended to document both the technical implementation of networking tasks and the progression of my hands-on learning experience.


This project is part of my lifelong learning portfolio. My goal is to document my study process, share what I learn, and create resources that may help others on similar paths.
To learn more about my background, learning philosophy, use of AI tools, and creative projects, visit my [Behind the Portfolio](/network-portfolio/behind-the-portfolio/) page.

[View the full Network+ Learning Journey](/network-portfolio/learning-journey/)

---
---
---

<div style="height: 3px; background: #f4b400; margin: 30px 0;"></div>

{% assign all_posts = site.posts %}
{% assign videos = site.posts | where: "content_type", "video" | where: "status", "complete" %}

{% assign category_order = "networking-fundamentals|infrastructure|security|systems-administration|technical-communication" | split: "|" %}

{% for category_key in category_order %}
{% assign category_posts = videos | where: "category", category_key %}

{% if category_posts.size > 0 %}
{% assign category_display = category_posts | map: "category_display" | compact | first %}

# {{ category_display | default: category_key }}

**Total Posts: {{ category_posts.size }}**

{% assign subcategory_keys = category_posts | map: "subcategory" | uniq | compact %}

{% for subcategory_key in subcategory_keys %}
{% assign subcategory_posts = category_posts | where: "subcategory", subcategory_key %}
{% assign subcategory_display = subcategory_posts | map: "subcategory_display" | compact | first %}

## {{ subcategory_display | default: subcategory_key }}

<div style="display: grid; grid-template-columns: repeat(auto-fill, minmax(220px, 1fr)); gap: 16px; margin: 18px 0 30px;">

{% for post in subcategory_posts %}

<div style="border: 1px solid #ddd; border-radius: 10px; padding: 10px; background: #fff;">

{% if post.thumbnail %} <a href="{{ post.video_url }}" target="_blank" rel="noopener noreferrer"> <img src="{{ post.thumbnail }}"
    alt="{{ post.title }}"
    style="width: 100%; border-radius: 7px; border: 1px solid #eee;"> </a>
{% else %}

<p><strong>Missing thumbnail.</strong></p>
{% endif %}

<p style="font-size: .9rem; line-height: 1.25; margin: 8px 0 4px;">
  <strong>{{ post.lesson_id }} | {{ post.lab_title | default: post.title }}</strong>
</p>

<p style="font-size: .78rem; line-height: 1.25; margin: 0 0 8px;">
  {{ post.category_display }}{% if post.subcategory_display %} | {{ post.subcategory_display }}{% endif %}
</p>

<p style="font-size: .8rem; margin: 0;">
{% if post.video_url %}
<a href="{{ post.video_url }}" target="_blank" rel="noopener noreferrer">Watch on YouTube</a>
{% else %}
Missing video URL
{% endif %}
|
<a href="{{ post.url | relative_url }}">View Notes</a>
</p>

</div>

{% endfor %}

</div>

{% endfor %}

---

{% endif %}
{% endfor %}


---
---
---

## 🔗 Navigation

* [Home](/)
* [Network+ Portfolio](/network-portfolio/)
  * [Formative Lessons](/network-portfolio/formative-lessons/)
  * [Lab Walkthroughs](/network-portfolio/labs/)
  * **[VIDEO WALKTHROUGHS](/network-portfolio/videos/)**
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* [Bible Study](/Bible-Study/)
* [Behind the Portfolio](/network-portfolio/behind-the-portfolio/)

---
---
---