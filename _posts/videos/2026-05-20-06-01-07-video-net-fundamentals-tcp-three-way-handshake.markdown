---
layout: post
title: "Networking Fundamentals | Explore Three-Way Handshake in Wireshark"
lab_title: "Explore Three-Way Handshake in Wireshark"

lesson: "04.0"
lesson_id: "06.01.07"
sort_order: "061070"

categories: [portfolio, videos]

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: tcpip
subcategory_display: TCP/IP

content_type: video
content_type_display: Assignment Video

tags:
  - tcp
  - wireshark
  - packet-analysis
  - tcp-handshake
  - networking

permalink: /network-portfolio/videos/lab-6-1-7-tcp-three-way-handshake/
status: complete

video_id: "DWqHgWJlFu0"
video_url: "https://youtu.be/DWqHgWJlFu0"
thumbnail: "https://img.youtube.com/vi/DWqHgWJlFu0/hqdefault.jpg"

topics:
  - tcp-handshake
  - packet-analysis
  - session-establishment
  - tcp-ip

protocols:
  - TCP
  - IPv4

tools:
  - Wireshark
  - Packet-Tracer

---

## Overview

This no-narration video walkthrough demonstrates the TCP three-way handshake process using Wireshark packet analysis.

<!--more-->

The linked, no-narration video walkthrough, visually examines how TCP establishes reliable communication sessions between network devices through SYN, SYN-ACK, and ACK packet exchanges.

---

## Video Walkthrough

Watch the complete walkthrough:

<a href="{{ page.video_url }}" target="_blank" rel="noopener noreferrer">
  <img src="{{ page.thumbnail }}"
       alt="{{ page.title }}"
       style="width:420px; border-radius:8px;">
</a>

---
# Lab 6.1.7 — Explore the TCP Three-Way Handshake

> Companion study guide for my TestOut lab walkthrough. This is an independently written learning resource, **not** a reproduction of TestOut's proprietary lab instructions. Exact screens, options and required settings depend on the lab version.

## Learning objectives

- Explain the purpose of explore the tcp three-way handshake in network operations.
- Apply the relevant configuration or analysis workflow in an authorized lab.
- Verify results using observable evidence rather than assumptions.
- Troubleshoot a failed or incomplete configuration safely.

## Core concepts

**Focus:** Wireshark. Connect this lab to least privilege, change control, documentation, and repeatable verification where applicable.

## Suggested hands-on workflow

1. **Record the baseline.** Note the device, interfaces, addressing, current configuration, and intended outcome.
2. **Plan the change.** Identify dependencies, permissions, and a rollback approach.
3. **Perform the lab task.** Capture SYN, SYN-ACK and ACK; inspect source/destination ports, flags, sequence and acknowledgement numbers.
4. **Verify.** Check the resulting configuration or packet evidence and test the expected behavior.
5. **Document.** Capture redacted screenshots/output, observations, issues, and resolution.
6. **Restore or save.** Save only approved changes; otherwise revert the lab environment.

## Example commands or filters

The following are **reference examples**, not guaranteed exact commands for this TestOut simulation. Run only those supported by your lab platform and replace placeholders with authorized values.

```text
tcp.flags.syn == 1
tcp.stream eq 0
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

A completed handshake confirms transport establishment, not application health.


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