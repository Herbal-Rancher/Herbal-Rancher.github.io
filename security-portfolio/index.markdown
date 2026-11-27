---
layout: page
title: Security+
permalink: /security-portfolio/
hr_theme: security
---

---
---
---


Welcome to my Security+ portfolio! This is where I document my cybersecurity education at Calbright College, practical skills, projects, and preparation for CompTIA Security+.

## Purpose

This portfolio is designed to:

- Develop practical cybersecurity skills
- Document security solutions and repeatable workflows
- Strengthen security architecture and risk management knowledge
- Support Security+ certification and professional growth
- Explore emerging cybersecurity and AI technologies

As part of my lifelong learning portfolio, this journey builds upon my networking and systems administration experience through hands-on practice, technical exploration, and shared educational resources.

Learn more about my background, learning philosophy, and use of AI on my [About the Portfolio](/about/) page.

---
---
---

## Certification Study Centers

* **[Security+ Certification Study Center - TBD](/security-portfolio/security-plus/)** — Objective review and interactive practice.
* **[Network+ Certification Study Center](/network-portfolio/network-plus/)** — Objective review and interactive practice.

## Learning structure

This portfolio supports both conceptual learning and practical application by providing a structured framework to document, organize, review, and demonstrate cybersecurity concepts, security technologies, and related technical skills.

The portfolio is organized into three primary sections that connect theory, visualization, hands-on practice, threat analysis, security troubleshooting, and technical reflection into a progressive learning system.

The following areas are planned for development as my studies progress:

- [**FORMATIVE MODULES — TBD**](/security-portfolio/formative-modules/) — Coursework, learning activities, technical assessments, and competency-based exercises.
- [**VIDEO WALKTHROUGHS — TBD**](/security-portfolio/videos/) — Narration-free demonstrations of hands-on cybersecurity labs, security configurations, troubleshooting exercises, and technical projects.
- [**STUDY DIAGRAMS — TBD**](/security-portfolio/study-diagrams/) — AI-assisted interactive diagrams and technical references that simplify cybersecurity concepts, protocols, architectures, and workflows.
- [**SECURITY TROUBLESHOOTING CHECKLIST — TBD**](/security-portfolio/security-troubleshooting-checklist/) — Interactive, structured workflows for identifying, diagnosing, mitigating, and resolving cybersecurity issues.
- [**SECURITY+ CERTIFICATION STUDY CENTER — TBD**](/security-portfolio/security-plus/) — Comprehensive certification study guides, exam objective reviews, and structured learning paths.
- [**CYBERSECURITY PROJECTS & SECURITY OPERATIONS — TBD**](/security-portfolio/cybersecurity-projects/) — Practical security implementations, threat analysis, vulnerability management, incident response, and defensive security projects.
- [**TEST READINESS LAB**](/test-readiness-lab/) — Interactive certification and career examination preparation, featuring Security+, security-focused examinations, scenario-based questions, and mastery tracking.

---
---
---
<div style="height: 3px; background: #f4b400; margin: 30px 0;"></div>

## Security+ Learning Journey

My [Security+ portfolio](/security-portfolio/) remains a separate learning journey. Its [Security+ Certification Study Center - TBD](/security-portfolio/security-plus/) includes foundational network security topics that support my cybersecurity studies.

This section organizes my hands-on CompTIA Security+ studies into topic areas and skill paths. Labs include TestOut exercises, Cisco security concepts, troubleshooting scenarios, security analysis, packet captures, remote administration, and technical documentation.

**Learn. Practice. Test. Retest. Master.**

---
---
---


{% assign posts = site.posts | where: "portfolio", "security-plus" %}

{% assign category_order = "security-fundamentals|threats-vulnerabilities-mitigations|security-architecture|security-operations|security-program-management|emerging-security-technologies" | split: "|" %}

{% for category_key in category_order %}

{% assign category_posts = posts | where: "category", category_key %}

{% if category_posts.size > 0 %}

{% assign category_display = category_posts | map: "category_display" | compact | first %}

<h1 style="border-bottom: 3px solid #27835C; padding-bottom: .35rem; margin-top: 2.5rem;">
  {{ category_display | default: category_key }}
</h1>

<p>
  <strong>Deliverables Completed:</strong> {{ category_posts.size }}
</p>

{% assign subcategory_keys = category_posts | map: "subcategory" | uniq | compact %}

{% for subcategory_key in subcategory_keys %}

{% assign subcategory_posts = category_posts | where: "subcategory", subcategory_key %}

{% assign subcategory_display = subcategory_posts | map: "subcategory_display" | compact | first %}

<div style="margin-left: 1.75rem; margin-top: 1.5rem; padding-left: 1rem; border-left: 3px solid #27835C;">

<h2 style="margin-bottom: .25rem;">
  {{ subcategory_display | default: subcategory_key }}:
</h2>

<strong>{{ subcategory_posts.size }}</strong> Deliverables Completed

<ul>
{% for post in subcategory_posts %}
  <li>
    ✓ <a href="{{ post.url | relative_url }}">
      {% if post.lesson_id and post.lab_title %}
        {{ post.lesson_id }} {{ post.content_type_display }}: {{ post.lab_title }}
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
<!--
<p><strong>Skills Practiced:</strong>
{% for topic in unique_topics %}
  {{ topic | replace: "-", " " | capitalize }}{% unless forloop.last %}, {% endunless %}
{% endfor %}
</p>
-->
{% endif %}

{% assign all_tools = "" | split: "" %}

{% for post in subcategory_posts %}
  {% if post.tools %}
    {% assign all_tools = all_tools | concat: post.tools %}
  {% endif %}
{% endfor %}

{% assign unique_tools = all_tools | uniq | sort %}

{% if unique_tools.size > 0 %}
<!--
<p><strong>Tools Used:</strong>
{% for tool in unique_tools %}
  {{ tool | replace: "-", " " }}{% unless forloop.last %}, {% endunless %}
{% endfor %}
</p>
-->
{% endif %}

</div>

{% endfor %}

{% endif %}

{% endfor %}

{% if posts.size == 0 %}

<p><em>My cybersecurity learning journey is underway. Educational resources, hands-on labs, assessments, and technical deliverables will be added as my studies progress.</em></p>

{% endif %}



---
---
---

## 🔗 Navigation

* [Home](/)
* [Network+ Portfolio](/network-portfolio/)
  * [Formative Modules](/network-portfolio/formative-modules/)
  * [Videos](/network-portfolio/videos/)
  * [Study Diagrams](/network-portfolio/study-diagrams/)
  * [Network Test Readiness Lab](/network-portfolio/network-test-readiness-lab/)
  * [Network Troubleshooting Checklist](/network-portfolio/network-troubleshooting-checklist/)
* **[SECURITY+ PORTFOLIO](/security-portfolio/)**
  * [Formative Modules](/security-portfolio/formative-modules/)
  * [Videos](/security-portfolio/videos/)
  * [Study Diagrams](/security-portfolio/study-diagrams/)
  * [Security Test Readiness Lab](/security-portfolio/security-test-readiness-lab/)
  * [Security Troubleshooting Checklist](/security-portfolio/security-troubleshooting-checklist/)
* [Trading+](/trading/)
* [Bible Study](/bible-study/)
* [About the Portfolio](/about/)

---
---
---
