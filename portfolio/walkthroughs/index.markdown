---
layout: page
title: ""
permalink: /portfolio/walkthroughs/
---

# Walkthroughs

This section documents **hands-on labs, configurations, and troubleshooting processes** completed throughout my IT coursework.

Each walkthrough provides step-by-step actions, commands, and real-world problem-solving insights.


## 🎯 Purpose

* Demonstrate applied technical skills
* Document repeatable workflows
* Capture troubleshooting and debugging processes


---

{% for post in site.categories.walkthroughs %}

  <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
  <p>{{ post.date | date: "%B %d, %Y" }}</p>
  <p>{{ post.excerpt }}</p>
  <a href="{{ post.url | relative_url }}">Read More →</a>
  <div style="height:1px; background:#ddd; margin:30px 0;"></div>

{% endfor %}

---

## 🔗 Navigation


* **[Refresh Walkthroughs](/portfolio/Walkthroughs/)**
* **[Formative Lessons](/portfolio/formative-lessons/)**
* **[Network+ Portfolio](/portfolio/)**
* **[zBible Study](/zBible-study/)**
* **[Home](/)**

---