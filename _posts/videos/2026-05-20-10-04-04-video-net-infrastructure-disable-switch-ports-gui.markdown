---
layout: post
title: "Infrastructure | Disable Switch Ports - GUI Management"
lab_title: "Disable Switch Ports - GUI Management"

lesson: "03.0"
lesson_id: "10.04.04"
sort_order: "100404"

categories: [portfolio, videos]

category: infrastructure
category_display: Infrastructure

subcategory: switching
subcategory_display: Switching

content_type: video
content_type_display: Assignment Video


tags:
  - switch-security
  - gui-management
  - port-security
  - switch-hardening
  - cisco

permalink: /network-portfolio/videos/lab-10-4-4-disable-switch-ports-gui/
status: complete

video_id: "o5JVqLaCmOc"
video_url: "https://youtu.be/o5JVqLaCmOc"
thumbnail: "https://img.youtube.com/vi/o5JVqLaCmOc/hqdefault.jpg"

topics:
  - switch-security
  - gui-administration
  - port-management
  - network-hardening

protocols:
  - HTTP
  - HTTPS

tools:
  - Cisco-GUI
  - web-management-interface
---

## Overview

This no-narration video walkthrough demonstrates how to disable unused switch ports using graphical management tools to improve network security and reduce unauthorized access risks.
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

# Lab 10.4.4 — Disable Unused Switch Ports Using GUI Management

> Companion study guide for my TestOut lab walkthrough. This is an independently written learning resource, **not** a reproduction of TestOut's proprietary lab instructions. Exact screens, options and required settings depend on the lab version.

## Learning objectives

- Explain the purpose of disable unused switch ports using gui management in network operations.
- Apply the relevant configuration or analysis workflow in an authorized lab.
- Verify results using observable evidence rather than assumptions.
- Troubleshoot a failed or incomplete configuration safely.

## Core concepts

**Focus:** Switch GUI. Connect this lab to least privilege, change control, documentation, and repeatable verification where applicable.

## Suggested hands-on workflow

1. **Record the baseline.** Note the device, interfaces, addressing, current configuration, and intended outcome.
2. **Plan the change.** Identify dependencies, permissions, and a rollback approach.
3. **Perform the lab task.** In the GUI identify unused interfaces, confirm no active endpoint or uplink, disable them, save changes and verify administrative state.
4. **Verify.** Check the resulting configuration or packet evidence and test the expected behavior.
5. **Document.** Capture redacted screenshots/output, observations, issues, and resolution.
6. **Restore or save.** Save only approved changes; otherwise revert the lab environment.

## Example commands or filters

The following are **reference examples**, not guaranteed exact commands for this TestOut simulation. Run only those supported by your lab platform and replace placeholders with authorized values.

```text
show interfaces status
show running-config
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

Do not disable uplinks, trunks, management paths or live endpoints.


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