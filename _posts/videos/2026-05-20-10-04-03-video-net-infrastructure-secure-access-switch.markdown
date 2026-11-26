---
layout: post
title: "Infrastructure | Secure Access to a Switch 2"
lab_title: "Secure Access to a Switch 2"

lesson: "03.0"
lesson_id: "10.04.03"
sort_order: "100403"	

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
  - switch-hardening
  - cisco

permalink: /network-portfolio/videos/lab-10-4-3-secure-access-switch/
status: complete

video_id: "exIfSvgadh0"
video_url: "https://youtu.be/exIfSvgadh0"
thumbnail: "https://img.youtube.com/vi/exIfSvgadh0/hqdefault.jpg"

topics:
  - switch-security
  - secure-management
  - cli-configuration

protocols:
  - SSH

tools:
  - Cisco-IOS
  - terminal
---

## Overview

This no-narration video walkthrough demonstrates secure access configuration techniques for Cisco switch administration and management.
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

# Lab 10.4.3 — Secure Access to Switch2

> Companion study guide for my TestOut lab walkthrough. This is an independently written learning resource, **not** a reproduction of TestOut's proprietary lab instructions. Exact screens, options and required settings depend on the lab version.

## Learning objectives

- Explain the purpose of secure access to switch2 in network operations.
- Apply the relevant configuration or analysis workflow in an authorized lab.
- Verify results using observable evidence rather than assumptions.
- Troubleshoot a failed or incomplete configuration safely.

## Core concepts

**Focus:** Switch administration. Connect this lab to least privilege, change control, documentation, and repeatable verification where applicable.

## Suggested hands-on workflow

1. **Record the baseline.** Note the device, interfaces, addressing, current configuration, and intended outcome.
2. **Plan the change.** Identify dependencies, permissions, and a rollback approach.
3. **Perform the lab task.** Apply administrative protections to Switch2; verify management reachability, user authentication and permitted remote protocols.
4. **Verify.** Check the resulting configuration or packet evidence and test the expected behavior.
5. **Document.** Capture redacted screenshots/output, observations, issues, and resolution.
6. **Restore or save.** Save only approved changes; otherwise revert the lab environment.

## Example commands or filters

The following are **reference examples**, not guaranteed exact commands for this TestOut simulation. Run only those supported by your lab platform and replace placeholders with authorized values.

```text
username admin privilege 15 secret <strong-secret>
ip domain-name lab.example
crypto key generate rsa
ip ssh version 2
line vty 0 15
 login local
 transport input ssh
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

Use unique secrets per device and restrict SSH to management hosts.

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