---
layout: page
permalink: /portfolio/videos/
---

---
## Video Walkthroughs

This page contains no-narration video walkthroughs documenting networking labs, troubleshooting processes, Wireshark analysis, DHCP implementation, switch hardening, PowerShell management, and other hands-on activities completed throughout my Network Technology learning journey.

The videos are grouped by topic to make the page easier to scan and review. Each video includes a thumbnail, a direct YouTube link, and metadata pulled from the related video post.

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

---
---
---