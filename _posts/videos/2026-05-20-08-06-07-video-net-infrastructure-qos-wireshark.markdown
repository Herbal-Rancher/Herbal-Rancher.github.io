---
layout: post
title: "Infrastructure | Configure QoS and Analyze Traffic with Wireshark"
lab_title: "Configure QoS and Analyze Traffic with Wireshark"

lesson: "03.0"
lesson_id: "08.06.07"
sort_order: "080607"

categories: [portfolio, videos]

category: infrastructure
category_display: Infrastructure

subcategory: switching
subcategory_display: Switching

content_type: video
content_type_display: Assignment Video


tags:
  - qos
  - wireshark
  - traffic-analysis
  - routing
  - packet-analysis

permalink: /network-portfolio/videos/lab-8-6-7-qos-wireshark/
status: complete

video_id: "WukW4e4zapY"
video_url: "https://youtu.be/WukW4e4zapY"
thumbnail: "https://img.youtube.com/vi/WukW4e4zapY/hqdefault.jpg"

topics:
  - qos
  - packet-analysis
  - traffic-prioritization
  - network-performance

protocols:
  - TCP
  - UDP
  - QoS

tools:
  - Wireshark
  - Cisco-IOS
  - Packet-Tracer
---

## Overview

This no-narration video walkthrough demonstrates Quality of Service (QoS) configuration and network traffic analysis using Wireshark.
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

# Lab 8.6.7 — Configure QoS and Analyze Traffic with Wireshark

> Companion study guide for my TestOut lab walkthrough. This is an independently written learning resource, **not** a reproduction of TestOut's proprietary lab instructions. Exact screens, options and required settings depend on the lab version.

## Learning objectives

- Explain the purpose of configure qos and analyze traffic with wireshark in network operations.
- Apply the relevant configuration or analysis workflow in an authorized lab.
- Verify results using observable evidence rather than assumptions.
- Troubleshoot a failed or incomplete configuration safely.

## Core concepts

**Focus:** QoS and Wireshark. Connect this lab to least privilege, change control, documentation, and repeatable verification where applicable.

## Suggested hands-on workflow

1. **Record the baseline.** Note the device, interfaces, addressing, current configuration, and intended outcome.
2. **Plan the change.** Identify dependencies, permissions, and a rollback approach.
3. **Perform the lab task.** Identify traffic classes, apply marking/priority policies as lab permits, capture packets and compare DSCP and observed behavior.
4. **Verify.** Check the resulting configuration or packet evidence and test the expected behavior.
5. **Document.** Capture redacted screenshots/output, observations, issues, and resolution.
6. **Restore or save.** Save only approved changes; otherwise revert the lab environment.

## Example commands or filters

The following are **reference examples**, not guaranteed exact commands for this TestOut simulation. Run only those supported by your lab platform and replace placeholders with authorized values.

```text
ip.dsfield.dscp
rtp
udp
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

Marking alone does not guarantee end-to-end QoS; congestion and policy matter.

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