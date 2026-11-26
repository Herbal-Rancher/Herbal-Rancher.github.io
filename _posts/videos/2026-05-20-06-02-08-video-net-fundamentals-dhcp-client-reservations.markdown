---
layout: post
title: "Networking Fundamentals | Create DHCP Client Reservations"
lab_title: "Create DHCP Client Reservations"

lesson: "03.0"
lesson_id: "06.02.08"
sort_order: "060208"

categories: [portfolio, videos]

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: dhcp-dns
subcategory_display: DHCP & DNS

content_type: video
content_type_display: Assignment Video


tags:
  - dhcp
  - reservations
  - ip-addressing
  - network-management

permalink: /network-portfolio/videos/lab-6-2-8-dhcp-client-reservations/
status: complete

video_id: "_exNJXEFSM0"
video_url: "https://youtu.be/_exNJXEFSM0"
thumbnail: "https://img.youtube.com/vi/_exNJXEFSM0/hqdefault.jpg"

topics:
  - dhcp-reservations
  - static-addressing
  - client-management

protocols:
  - DHCP
  - IPv4

tools:
  - DHCP-console
  - Windows-Server
---

## Overview

This no-narration video walkthrough demonstrates creating DHCP client reservations within a Windows DHCP environment.

<!--more-->

The video walkthrough focuses on assigning reserved IP addresses to specific network devices using MAC address associations.

---

## Video Walkthrough

Watch the complete walkthrough:

<a href="{{ page.video_url }}" target="_blank" rel="noopener noreferrer">
  <img src="{{ page.thumbnail }}"
       alt="{{ page.title }}"
       style="width:420px; border-radius:8px;">
</a>

# Lab 6.2.8 — Create DHCP Client Reservations

> Companion study guide for my TestOut lab walkthrough. This is an independently written learning resource, **not** a reproduction of TestOut's proprietary lab instructions. Exact screens, options and required settings depend on the lab version.

## Learning objectives

- Explain the purpose of create dhcp client reservations in network operations.
- Apply the relevant configuration or analysis workflow in an authorized lab.
- Verify results using observable evidence rather than assumptions.
- Troubleshoot a failed or incomplete configuration safely.

## Core concepts

**Focus:** DHCP. Connect this lab to least privilege, change control, documentation, and repeatable verification where applicable.

## Suggested hands-on workflow

1. **Record the baseline.** Note the device, interfaces, addressing, current configuration, and intended outcome.
2. **Plan the change.** Identify dependencies, permissions, and a rollback approach.
3. **Perform the lab task.** Identify client MAC address; create reservation in the correct scope; renew and confirm assigned address.
4. **Verify.** Check the resulting configuration or packet evidence and test the expected behavior.
5. **Document.** Capture redacted screenshots/output, observations, issues, and resolution.
6. **Restore or save.** Save only approved changes; otherwise revert the lab environment.

## Example commands or filters

The following are **reference examples**, not guaranteed exact commands for this TestOut simulation. Run only those supported by your lab platform and replace placeholders with authorized values.

```text
ipconfig /all
ipconfig /renew
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

Reservations map client identity to an address; verify MAC and scope.

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