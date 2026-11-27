---
layout: page
title: Security+
permalink: /security-portfolio/
hr_theme: security
---

Welcome to my Security+ portfolio! This is where I document my cybersecurity education at Calbright College, practical skills, and preparation for CompTIA Security+.

## Purpose

- Demonstrate cybersecurity skill development
- Document practical security solutions
- Develop repeatable threat detection and response workflows
- Strengthen security architecture and risk management knowledge
- Support Security+ certification and professional growth
- Explore emerging cybersecurity and AI technologies

This project is part of my lifelong learning portfolio, expanding my professional technology journey from networking and systems administration into cybersecurity.

My goal is to document my learning, strengthen my skills through hands-on practice, and share educational resources that may benefit others pursuing similar paths.

[About the Portfolio](/about/)

## Learning Structure

This portfolio supports conceptual learning and practical application through a structured framework for cybersecurity concepts, technologies, and technical skills.

- [**SECURITY+ CERTIFICATION STUDY CENTER — TBD**](/security-portfolio/security-plus/) — Objective reviews and structured learning paths.
- [**FORMATIVE SECURITY MODULES — TBD**](/security-portfolio/formative-modules/) — Coursework and assessments.
- [**SECURITY VIDEO WALKTHROUGHS — TBD**](/security-portfolio/videos/) — Hands-on demonstrations.
- [**STUDY DIAGRAMS — TBD**](/security-portfolio/study-diagrams/) — Interactive visual resources.
- [**TEST READINESS LAB**](/test-readiness-lab/) — Centralized examination preparation.
- [**SECURITY TROUBLESHOOTING CHECKLIST — TBD**](/security-portfolio/security-troubleshooting-checklist/) — Structured security diagnostics.
- [**CYBERSECURITY PROJECTS & SECURITY OPERATIONS — TBD**](/security-portfolio/cybersecurity-projects/) — Defensive projects and practical implementations.

## Security+ Learning Journey

This section organizes my hands-on cybersecurity studies into topic areas and skill paths as my studies progress.

{% assign posts = site.posts | where: "portfolio", "security-plus" %}
{% assign category_order = "security-fundamentals|threats-vulnerabilities-mitigations|security-architecture|security-operations|security-program-management|emerging-security-technologies" | split: "|" %}
{% for key in category_order %}
{% assign group = posts | where: "category", key %}
{% if group.size > 0 %}
{% assign display = group | map: "category_display" | compact | first %}
<h2>{{ display | default: key }}</h2>
<p><strong>Deliverables Completed:</strong> {{ group.size }}</p>
{% assign subs = group | map: "subcategory" | compact | uniq %}
{% for sub in subs %}
{% assign items = group | where: "subcategory", sub %}
{% assign label = items | map: "subcategory_display" | compact | first %}
<h3>{{ label | default: sub }}</h3>
<ul>{% for post in items %}<li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>{% endfor %}</ul>
{% endfor %}
{% endif %}
{% endfor %}
{% if posts.size == 0 %}
# Security Fundamentals

Deliverables will be added as my studies progress.
{% endif %}

## 🔗 Navigation

* [Home](/)
* [Network+ Portfolio](/network-portfolio/)
  * [Formative Modules](/network-portfolio/formative-modules/)
  * [Videos](/network-portfolio/videos/)
  * [Study Diagrams](/network-portfolio/study-diagrams/)
  * [Test Readiness Lab](/test-readiness-lab/)
  * [Network Troubleshooting Checklist](/network-portfolio/network-troubleshooting-checklist/)
* **[SECURITY+ PORTFOLIO](/security-portfolio/)**
  * [Formative Modules](/security-portfolio/formative-modules/)
  * [Videos](/security-portfolio/videos/)
  * [Study Diagrams](/security-portfolio/study-diagrams/)
  * [Test Readiness Lab](/test-readiness-lab/)
  * [Security Troubleshooting Checklist](/security-portfolio/security-troubleshooting-checklist/)
* [Trading+](/trading/)
* [Bible Study](/bible-study/)
* [About the Portfolio](/about/)

---
---
---
