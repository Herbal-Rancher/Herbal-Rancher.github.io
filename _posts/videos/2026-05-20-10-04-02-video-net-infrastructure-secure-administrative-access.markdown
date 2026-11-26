---
layout: post
title: "Infrastructure | Secure Administrative Access to a Network Switch"
lab_title: "Secure Administrative Access to a Network Switch"

lesson: "03.0"
lesson_id: "10.04.02"
sort_order: "100402"

categories: [portfolio, videos]

category: infrastructure
category_display: Infrastructure

subcategory: switching
subcategory_display: Switching

content_type: video
content_type_display: Assignment Video

tags:
  - switch-security
  - administrative-access
  - switch-management
  - cisco

permalink: /network-portfolio/videos/lab-10-4-2-secure-administrative-access/
status: complete

video_id: "hQZvScmrmd0"
video_url: "https://youtu.be/hQZvScmrmd0"
thumbnail: "https://img.youtube.com/vi/hQZvScmrmd0/hqdefault.jpg"

topics:
  - secure-access
  - switch-hardening
  - management-security

protocols:
  - SSH
  - Telnet

tools:
  - Cisco-IOS
  - terminal
---

## Overview

This no-narration video walkthrough demonstrates methods used to secure administrative access to Cisco network switches.
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

# Lab 10.4.2 — Secure Access to a Switch

> Companion study guide for my TestOut lab walkthrough. This is an independently written learning resource, **not** a reproduction of TestOut's proprietary lab instructions. Exact screens, options and required settings depend on the lab version.

## Learning objectives

- Explain the purpose of secure access to a switch in network operations.
- Apply the relevant configuration or analysis workflow in an authorized lab.
- Verify results using observable evidence rather than assumptions.
- Troubleshoot a failed or incomplete configuration safely.

## Core concepts

**Focus:** Switch administration. Connect this lab to least privilege, change control, documentation, and repeatable verification where applicable.

## Suggested hands-on workflow

1. **Record the baseline.** Note the device, interfaces, addressing, current configuration, and intended outcome.
2. **Plan the change.** Identify dependencies, permissions, and a rollback approach.
3. **Perform the lab task.** Establish protected administrative credentials, limit management access and validate console/remote authentication.
4. **Verify.** Check the resulting configuration or packet evidence and test the expected behavior.
5. **Document.** Capture redacted screenshots/output, observations, issues, and resolution.
6. **Restore or save.** Save only approved changes; otherwise revert the lab environment.

## Example commands or filters

The following are **reference examples**, not guaranteed exact commands for this TestOut simulation. Run only those supported by your lab platform and replace placeholders with authorized values.

```text
enable secret <strong-secret>
service password-encryption
line console 0
 login local
line vty 0 15
 transport input ssh
 login local
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

Cisco IOS examples are illustrative; actual TestOut switch GUI/CLI may differ.

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