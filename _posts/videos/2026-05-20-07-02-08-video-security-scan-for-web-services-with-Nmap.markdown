---
layout: post
title: "Security | Scan for Web Services with Nmap"
lab_title: "Scan for Web Services with Nmap"

lesson: "04.0"
lesson_id: "07.02.08"
sort_order: "070208"

categories: [portfolio, videos]

category: security
category_display: Security

subcategory: reconnaissance  
subcategory_display: Reconnaissance

content_type: video
content_type_display: Assignment Video

tags:

- nmap
- port-scanning
- web-services
- vulnerability-assessment
- network-security

permalink: /network-portfolio/videos/lab-7-2-8-scan-for-web-services-with-Nmap/
status: complete

video_id: "EIXQGfch_ms"
video_url: "https://youtu.be/EIXQGfch_ms"
thumbnail: "https://img.youtube.com/vi/EIXQGfch_ms/hqdefault.jpg"

topics:

- port-scanning
- service-discovery
- reconnaissance
- security-analysis

protocols:

- TCP
- IP

tools:

- Nmap
- Terminal
---

## Overview

This no-narration video walkthrough demonstrates how to use Nmap to identify open ports and discover active services on a network host.

The lab focuses on network reconnaissance, service discovery, and understanding how security analysts assess exposed services during security reviews and vulnerability assessments.

<!--more-->

---

## Video Walkthrough

Watch the complete walkthrough:

<a href="{{ page.video_url }}" target="_blank" rel="noopener noreferrer">
  <img src="{{ page.thumbnail }}"
       alt="{{ page.title }}"
       style="width:420px; border-radius:8px;">
</a>

---

# Lab 7.2.8 — Scan for Web Services with Nmap

> Companion study guide for my TestOut lab walkthrough. This is an independently written learning resource, **not** a reproduction of TestOut's proprietary lab instructions. Exact screens, options and required settings depend on the lab version.

## Learning objectives

- Explain the purpose of scan for web services with nmap in network operations.
- Apply the relevant configuration or analysis workflow in an authorized lab.
- Verify results using observable evidence rather than assumptions.
- Troubleshoot a failed or incomplete configuration safely.

## Core concepts

**Focus:** Nmap. Connect this lab to least privilege, change control, documentation, and repeatable verification where applicable.

## Suggested hands-on workflow

1. **Record the baseline.** Note the device, interfaces, addressing, current configuration, and intended outcome.
2. **Plan the change.** Identify dependencies, permissions, and a rollback approach.
3. **Perform the lab task.** With authorization, scan the lab database server at 192.168.0.22 for HTTP/HTTPS service ports; interpret open/closed/filtered.
4. **Verify.** Check the resulting configuration or packet evidence and test the expected behavior.
5. **Document.** Capture redacted screenshots/output, observations, issues, and resolution.
6. **Restore or save.** Save only approved changes; otherwise revert the lab environment.

## Example commands or filters

The following are **reference examples**, not guaranteed exact commands for this TestOut simulation. Run only those supported by your lab platform and replace placeholders with authorized values.

```text
nmap -sV -p 80,443 192.168.0.22
nmap -Pn -p 80,443 192.168.0.22
```

## Verification checklist

- [ ] Initial state and desired result documented
- [ ] Configuration or capture completed without unintended side effects
- [ ] Expected behavior confirmed with an independent check
- [ ] Unexpected results investigated and explained
- [ ] Screenshots or output sanitized before publication
- [ ] Final state and lessons learned recorded

## Troubleshooting prompts

- Is the correct device, adapter, scope, interface, zone, or traffic stream selected?
- Are permissions, connectivity, and prerequisite services available?
- Is a policy override, firewall, VLAN, or upstream dependency affecting results?
- What single observation would distinguish a configuration issue from a connectivity issue?

## Security and operational notes

Scan only owned or explicitly authorized targets; service fingerprints are estimates.

---
---
---

## 🔗 Navigation

* [Home](/)
* [Network+ Portfolio](/network-portfolio/)
  * [Formative Modules](/network-portfolio/formative-modules/)
  * **[VIDEOS](/network-portfolio/videos/)**
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* [Trading+](/trading/)
* [Bible Study](/bible-study/)
* [About the Portfolio](/about/)

---
---
---