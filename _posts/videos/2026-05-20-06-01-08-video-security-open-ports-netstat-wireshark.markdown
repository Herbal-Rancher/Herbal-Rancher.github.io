---
layout: post
title: "Security | View Open Ports with Netstat and Wireshark"
lab_title: "View Open Ports with Netstat and Wireshark"

lesson: "04.0"
lesson_id: "06.01.08"
sort_order: "060108"

categories: [portfolio, videos]

category: security
category_display: Security

subcategory: reconnaissance
subcategory_display: Reconnaissance

content_type: video
content_type_display: Assignment Video


tags:
  - netstat
  - wireshark
  - open-ports
  - packet-analysis
  - network-security

permalink: /network-portfolio/videos/lab-6-1-8-open-ports-netstat-wireshark/
status: complete

video_id: "9C_G1ZVLWCI"
video_url: "https://youtu.be/9C_G1ZVLWCI"
thumbnail: "https://img.youtube.com/vi/9C_G1ZVLWCI/hqdefault.jpg"

topics:
  - port-analysis
  - packet-capture
  - network-monitoring
  - troubleshooting

protocols:
  - TCP
  - UDP

tools:
  - Wireshark
  - Netstat
  - Windows-Terminal
---

## Overview

This no-narration video walkthrough demonstrates how to identify open ports and analyze network communication using Netstat and Wireshark.
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

# Lab 6.1.8 — View Open Ports with Netstat and Wireshark

> Companion study guide for my TestOut lab walkthrough. This is an independently written learning resource, **not** a reproduction of TestOut's proprietary lab instructions. Exact screens, options and required settings depend on the lab version.

## Learning objectives

- Explain the purpose of view open ports with netstat and wireshark in network operations.
- Apply the relevant configuration or analysis workflow in an authorized lab.
- Verify results using observable evidence rather than assumptions.
- Troubleshoot a failed or incomplete configuration safely.

## Core concepts

**Focus:** Windows and Wireshark. Connect this lab to least privilege, change control, documentation, and repeatable verification where applicable.

## Suggested hands-on workflow

1. **Record the baseline.** Note the device, interfaces, addressing, current configuration, and intended outcome.
2. **Plan the change.** Identify dependencies, permissions, and a rollback approach.
3. **Perform the lab task.** Map listening ports to process IDs; compare socket state to observed packets.
4. **Verify.** Check the resulting configuration or packet evidence and test the expected behavior.
5. **Document.** Capture redacted screenshots/output, observations, issues, and resolution.
6. **Restore or save.** Save only approved changes; otherwise revert the lab environment.

## Example commands or filters

The following are **reference examples**, not guaranteed exact commands for this TestOut simulation. Run only those supported by your lab platform and replace placeholders with authorized values.

```text
netstat -ano
netstat -ab
tcp.port == 443
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

Run elevated only when authorized; listening does not imply publicly reachable.

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