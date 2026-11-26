---
layout: post
title: "Systems Administration | Manage Account Policies in Windows"
lab_title: "Manage Account Policies in Windows"

lesson: "03.0"
lesson_id: "10.02.05"
sort_order: "100205"

categories: [portfolio, videos]

category: systems-administration
category_display: Systems Administration

subcategory: remote-administration
subcategory_display: Remote Administration

content_type: video
content_type_display: Assignment Video

tags:
  - windows-security
  - account-policies
  - password-policy
  - user-management

permalink: /network-portfolio/videos/lab-10-2-5-windows-account-policies/
status: complete

topics:
  - router-configuration
  - routing-tables
  - connectivity-testing

tools: 
  - cisco-packet-tracer
  
video_id: "lhCbgWjY4nM"
video_url: "https://youtu.be/lhCbgWjY4nM"
thumbnail: "https://img.youtube.com/vi/lhCbgWjY4nM/hqdefault.jpg"

protocols: []

---

## Overview

This no-narration video walkthrough demonstrates Windows account policy management and security configuration techniques.
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

# Lab 10.2.5 — Manage Windows Account Policies

> Companion study guide for my TestOut lab walkthrough. This is an independently written learning resource, **not** a reproduction of TestOut's proprietary lab instructions. Exact screens, options and required settings depend on the lab version.

## Learning objectives

- Explain the purpose of manage windows account policies in network operations.
- Apply the relevant configuration or analysis workflow in an authorized lab.
- Verify results using observable evidence rather than assumptions.
- Troubleshoot a failed or incomplete configuration safely.

## Core concepts

**Focus:** Windows Local Security Policy. Connect this lab to least privilege, change control, documentation, and repeatable verification where applicable.

## Suggested hands-on workflow

1. **Record the baseline.** Note the device, interfaces, addressing, current configuration, and intended outcome.
2. **Plan the change.** Identify dependencies, permissions, and a rollback approach.
3. **Perform the lab task.** Review password length/complexity/age and account lockout threshold, duration and reset settings; test in an isolated lab.
4. **Verify.** Check the resulting configuration or packet evidence and test the expected behavior.
5. **Document.** Capture redacted screenshots/output, observations, issues, and resolution.
6. **Restore or save.** Save only approved changes; otherwise revert the lab environment.

## Example commands or filters

The following are **reference examples**, not guaranteed exact commands for this TestOut simulation. Run only those supported by your lab platform and replace placeholders with authorized values.

```text
secpol.msc
net accounts
gpresult /r
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

Domain Group Policy may override local settings; use current organizational guidance.

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