---
layout: page
title: ""
permalink: /portfolio/formative-lessons/
---

# Formative Lessons

This section captures the **core concepts, theories, and foundational knowledge** I am developing throughout my IT coursework.

Each lesson represents a key learning milestone and is supported by related hands-on walkthroughs.

---

## Purpose

* Reinforce conceptual understanding
* Connect theory to practical application
* Track learning progression over time

---
## Lesson 01

#### Milestone and Summative Assessments

<UL><li>
  <a href="/assets/docs/01-0-Milestone_Assessment_Network-OSI-model.pdf"
   target="_blank"
   rel="noopener noreferrer">
    1.0 Milestone Assessment - Network OSI Model (PDF)
  </a></li><li>
   <a href="/assets/docs/01-0-Summative-Assessment_Network-OSI-model.pdf"
   target="_blank"
   rel="noopener noreferrer">
    1.0 Summative Assessment - Network OSI Open Systems Interconnect Model (PDF)
  </a>
</li></UL>

#### Labs and Walkthroughs

{% assign walkthroughs = site.posts
  | where: "lesson", "1.0"
  | where_exp: "post", "post.categories contains 'walkthroughs'"
  | sort: "order" %}

{% if walkthroughs.size > 0 %}
  <ul>
  {% for post in walkthroughs %}
    <li>
      <a href="{{ post.url | relative_url }}" target="_blank" rel="noopener noreferrer">
        {{ post.title }}
      </a>
    </li>
  {% endfor %}
  </ul>
{% else %}
{% endif %}

---

## Lesson 02

#### Milestone and Summative Assessments
<UL><li>
  <a href="/assets/docs/02-0-Milestone-Assessment_Network-Systems.pdf"
   target="_blank"
   rel="noopener noreferrer">
    2.0 Milestone Assessment - Network Systems (PDF)
  </a></li><li>
   <a href="/assets/docs/02-0-Summative-Assessment_Network-Systems.pdf"
   target="_blank"
   rel="noopener noreferrer">
    2.0 Summative Assessment - Network Systems (PDF)
  </a>
</li></UL>

#### Labs and Walkthroughs

{% assign walkthroughs = site.posts
  | where: "lesson", "2.0"
  | where_exp: "post", "post.categories contains 'walkthroughs'"
  | sort: "order" %}

{% if walkthroughs.size > 0 %}
  <ul>
  {% for post in walkthroughs %}
    <li>
      <a href="{{ post.url | relative_url }}" target="_blank" rel="noopener noreferrer">
        {{ post.title }}
      </a>
    </li>
  {% endfor %}
   </ul>
{% else %}
{% endif %}

---

## Lesson 03

#### Milestone and Summative Assessments
<UL><li>
 <a href="/assets/docs/03-0-Discussion-IP-Address-Subclasses"
   target="_blank"
   rel="noopener noreferrer">
    3.0 Discussion: IP Address Subclasses (PDF)
  </a></li><li>
  <a href="/assets/docs/TBD.HTML"
   target="_blank"
   rel="noopener noreferrer">
    3.0 Milestone Assessment - TBD (PDF)
  </a></li><li>
   <a href="/assets/docs/TBD.HTML"
   target="_blank"
   rel="noopener noreferrer">
    3.0 Summative Assessment - TBD (PDF)
  </a>
</li></UL>

#### Labs and Walkthroughs

{% assign walkthroughs = site.posts
  | where: "lesson", "3.0"
  | where_exp: "post", "post.categories contains 'walkthroughs'"
  | sort: "order" %}

{% if walkthroughs.size > 0 %}
  <ul>
  {% for post in walkthroughs %}
    <li>
      <a href="{{ post.url | relative_url }}" target="_blank" rel="noopener noreferrer">
        {{ post.title }}
      </a>
    </li>
  {% endfor %}
   </ul>
{% else %}
{% endif %}

---

## Lesson 11

#### Milestone and Summative Assessments
<UL><li>
 
   <a href="/assets/docs/11-0-Milestone_Assessment_Network_Topologies.pdf"
   target="_blank"
   rel="noopener noreferrer">
    11.0 Milestone Assessment - Network Topologies (PDF)
  </a>
</li></UL>

#### Labs and Walkthroughs

{% assign walkthroughs = site.posts
  | where: "lesson", "11.0"
  | where_exp: "post", "post.categories contains 'walkthroughs'"
  | sort: "order" %}

{% if walkthroughs.size > 0 %}
 <ul>
  {% for post in walkthroughs %}
    <li>
      <a href="{{ post.url | relative_url }}" target="_blank" rel="noopener noreferrer">
        {{ post.title }}
      </a>
    </li>
  {% endfor %}
   </ul>
{% else %}
{% endif %}

---

## 🔗 Navigation

* **[Refresh Formative Lessons](/portfolio/formative-lessons/)**
* **[Walkthroughs](/portfolio/walkthroughs/)**
* **[Network+ Portfolio](/portfolio/)**
* **[zBible Study](/zBible-study/)**
* **[Home](/)**

---