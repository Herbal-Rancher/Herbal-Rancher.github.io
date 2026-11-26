---
layout: post
title: "Networking Fundamentals | Use nslookup"
lab_title: "Use nslookup"

lesson: "04.0"
lesson_id: "06.06.06"
sort_order: "040606"

categories: [portfolio, labs]

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: dhcp-dns
subcategory_display: DHCP & DNS

content_type: lab
content_type_display: Lab

topics: [dns, nslookup, mx-records, name-resolution, dns-troubleshooting]

tools: [Nslookup, DNS, Windows-Terminal, ip, ping]

tags: 
  - switch-security
  - linux
  - windows
  - dns
  - nslookup
  - terminal
  - networking
  - network-plus

permalink: /network-portfolio/labs/module-6-0/lab-6-6-6-use-nslookup/
status: complete

video: ""
video_id: "fio2pcSi2SY"
video_url: "https://youtu.be/fio2pcSi2SY"
thumbnail: "https://img.youtube.com/vi/fio2pcSi2SY/hqdefault.jpg"

pdf: ""
diagram: ""

protocols: [DNS]
---

In this lab, I used `nslookup` from the Linux terminal to query DNS records and verify mail server information for a domain.

This lab reinforced the relationship between domain names, DNS servers, and MX records while also helping bridge common Windows networking commands into their Linux equivalents.

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

# Lab 6.6.6 — Use nslookup

> Companion study guide for my TestOut lab walkthrough. This is an independently written learning resource, **not** a reproduction of TestOut's proprietary lab instructions. Exact screens, options and required settings depend on the lab version.

## Learning objectives

- Explain the purpose of use nslookup in network operations.
- Apply the relevant configuration or analysis workflow in an authorized lab.
- Verify results using observable evidence rather than assumptions.
- Troubleshoot a failed or incomplete configuration safely.

## Core concepts

**Focus:** DNS troubleshooting. Connect this lab to least privilege, change control, documentation, and repeatable verification where applicable.

## Suggested hands-on workflow

1. **Record the baseline.** Note the device, interfaces, addressing, current configuration, and intended outcome.
2. **Plan the change.** Identify dependencies, permissions, and a rollback approach.
3. **Perform the lab task.** Test forward and reverse lookups; identify which DNS server answered.
4. **Verify.** Check the resulting configuration or packet evidence and test the expected behavior.
5. **Document.** Capture redacted screenshots/output, observations, issues, and resolution.
6. **Restore or save.** Save only approved changes; otherwise revert the lab environment.

## Example commands or filters

The following are **reference examples**, not guaranteed exact commands for this TestOut simulation. Run only those supported by your lab platform and replace placeholders with authorized values.

```text
nslookup example.com
nslookup 8.8.8.8
nslookup -type=MX example.com
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

Reverse lookup requires a PTR record and may not be configured.

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