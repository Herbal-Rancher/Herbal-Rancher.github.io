---
layout: page
title: "Home"
permalink: /
---

___
___
___

Welcome to my technical portfolio. I'm an IT student at Calbright College focused on building practical networking skills through Network+ studies and hands-on coursework.

Explore my **[NETWORK+ PORTFOLIO](/network-portfolio/)**, where I share my networking development journey through structured modules, projects, lab labs, and applied problem-solving.

Here I share my Artificial Intelligence (AI) driven, specifically ChatGPT and Visual Studio, network content deep dive diagrams in my **[STUDY DIAGRAMS](/network-portfolio/study-diagrams/)** page, which visually break down complex concepts and workflows.

Alongside my technical journey, I am also engaged in a personal study of the Bible (the Torah - 1st Testament and the New Testament - 2nd Testament). You can follow that progress in my **[BIBLE STUDY](/bible-study/)** posts, beginning with Genesis and continuing book by book.


This project is part of my lifelong learning portfolio. My goal is to document my study process, share what I learn, and create resources that may help others on similar paths.
To learn more about my background, learning philosophy, use of AI tools, and creative projects, visit my [Behind the Portfolio](/network-portfolio/behind-the-portfolio/) page.

***Shall we journey together?***

---
---
---
<div style="height: 3px; background: #f4b400; margin: 30px 0;"></div>

# Network+ Learning Journey

This section organizes my hands-on CompTIA Network+ studies into topic areas and skill paths. Labs include TestOut exercises, Cisco networking concepts, troubleshooting scenarios, security analysis, packet captures, remote administration, and technical documentation.

[View the full video gallery](/network-portfolio/videos/)

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

<p><strong>Labs Completed:</strong> {{ category_posts.size }}</p>

{% assign subcategory_keys = category_posts | map: "subcategory" | uniq | compact %}

{% for subcategory_key in subcategory_keys %}
{% assign subcategory_posts = category_posts | where: "subcategory", subcategory_key %}
{% assign subcategory_display = subcategory_posts | map: "subcategory_display" | compact | first %}


<div style="margin-left: 1.75rem; margin-top: 1.5rem; padding-left: 1rem; border-left: 3px solid #e5e5e5;">

<h2 style="margin-bottom: .25rem;">
  {{ subcategory_display | default: subcategory_key }}
</h2>

<p><strong>Labs Completed:</strong> {{ subcategory_posts.size }}</p>

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


---
---
---
## 🔗 Navigation

* **[HOME](/)**
* [Network+ Portfolio](/network-portfolio/)
  * [Formative Lessons](/network-portfolio/formative-lessons/)
  * [Lab Walkthroughs](/network-portfolio/labs/)
  * [Video Walkthroughs](/network-portfolio/videos/)
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* [Bible Study](/network-portfolio/Bible-Study/)
* [Behind the Portfolio](/network-portfolio/behind-the-portfolio/)

---
---
---