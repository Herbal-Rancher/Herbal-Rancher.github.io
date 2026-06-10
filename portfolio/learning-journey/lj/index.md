---
layout: page
permalink: /portfolio/learning-journey/lj/
nav_exclude: true
---

---
---
---

# Network+ Learning Journey

This page organizes my hands-on CompTIA Network+ studies into topic areas and skill paths. Labs include TestOut exercises, Cisco networking concepts, troubleshooting scenarios, security analysis, packet captures, remote administration, and technical documentation.

[View the full video gallery](/portfolio/videos/)

---
---
---

{% assign posts = site.posts | where: "status", "complete" %}
{% assign category_order = "networking-fundamentals|infrastructure|security|systems-administration|technical-communication" | split: "|" %}

{% for category_key in category_order %}
{% assign category_posts = posts | where: "category_key", category_key %}

{% if category_posts.size > 0 %}
{% assign category_display = category_posts | map: "category_display" | compact | first %}

<hr>

<h1 style="border-bottom: 3px solid #ddd; padding-bottom: .35rem; margin-top: 2.5rem;">
  {{ category_display | default: category_key }}
</h1>

<p><strong>Items Completed:</strong> {{ category_posts.size }}</p>

{% assign subcategory_keys = category_posts | map: "subcategory_key" | uniq | compact %}

{% for subcategory_key in subcategory_keys %}
{% assign subcategory_posts = category_posts | where: "subcategory_key", subcategory_key %}
{% assign subcategory_display = subcategory_posts | map: "subcategory_display" | compact | first %}

<div style="margin-left: 1.75rem; margin-top: 1.5rem; padding-left: 1rem; border-left: 3px solid #e5e5e5;">

<h2 style="margin-bottom: .25rem;">
  {{ subcategory_display | default: subcategory_key }}
</h2>

<p><strong>Items Completed:</strong> {{ subcategory_posts.size }}</p>

<ul>
{% for post in subcategory_posts %}
  <li>
    ✓ <a href="{{ post.url | relative_url }}">
      {% if post.lesson_id %}
        {{ post.lesson_id }}: {{ post.lesson_title | default: post.title }}
      {% else %}
        {{ post.lesson_title | default: post.title }}
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

<p><strong>Skills Practiced:</strong></p>

<ul>
{% for topic in unique_topics %}
  <li>{{ topic | replace: "-", " " | capitalize }}</li>
{% endfor %}
</ul>
{% endif %}

{% assign all_tools = "" | split: "" %}

{% for post in subcategory_posts %}
{% if post.tools %}
{% assign all_tools = all_tools | concat: post.tools %}
{% endif %}
{% endfor %}

{% assign unique_tools = all_tools | uniq | sort %}

{% if unique_tools.size > 0 %}

<p><strong>Tools Used:</strong></p>

<ul>
{% for tool in unique_tools %}
  <li>{{ tool }}</li>
{% endfor %}
</ul>
{% endif %}

</div>

{% endfor %}

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