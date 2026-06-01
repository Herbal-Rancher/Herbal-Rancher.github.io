---
layout: page
permalink: /portfolio/videos/
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

---

{% assign video_categories = "security|Security,routing-switching|Routing and Switching,troubleshooting-analysis|Network Troubleshooting and Analysis,dhcp|DHCP" | split: "," %}

{% for category_pair in video_categories %}
{% assign category_parts = category_pair | split: "|" %}
{% assign category_key = category_parts[0] %}
{% assign category_title = category_parts[1] %}

{% assign videos = site.posts | where: "video_category", category_key | sort: "date" | reverse %}

{% if videos.size > 0 %}

## {{ category_title }}

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 28px; margin: 25px 0;">

{% for post in videos %}
{% if post.categories contains "videos" %}

  <div style="text-align:center; margin-bottom: 20px;">
    <a href="{{ post.video_url }}" target="_blank" rel="noopener noreferrer">
      <img src="{{ post.thumbnail }}"
           alt="{{ post.title }}"
           style="width: 100%; max-width: 420px; border-radius: 8px;">
    </a>

    <p style="margin-top: 10px; margin-bottom: 4px;">
      <strong>{{ post.lab }}</strong>
    </p>

    <p style="margin-top: 0; margin-bottom: 6px;">
      {{ post.title }}
    </p>

    <p style="margin-top: 0;">
      <a href="{{ post.video_url }}" target="_blank" rel="noopener noreferrer">
        Open video directly in YouTube
      </a>
    </p>
  </div>

{% endif %}
{% endfor %}

</div>

---

{% endif %}
{% endfor %}



---
---
---

## 🔗 Navigation

* [Home](/)
* [Network+ Portfolio](/portfolio/)
  * [Formative Lessons](/portfolio/formative-lessons/)
  * [Lab Walkthroughs](/portfolio/labs/)
  * **[VIDEO WALKTHROUGHS](/portfolio/videos/)**
  * [Study Diagrams](/portfolio/study-diagrams/)
* [zBible Study](/zBible-Study/)
* [About Me](/about/)

---
---
---