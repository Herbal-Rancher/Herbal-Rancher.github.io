---
layout: post
title: "Lab 35 | Cisco Networking Labs - Use Telnet and SSH"
lab_title: "Use Telnet and SSH"

lesson: "17.0"
lesson_id: "17.35.00"
sort_order: "173500"

categories:
  - portfolio
  - labs

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: network-security
subcategory_display: Network Security

content_type: lab
content_type_display: Lab Documentation

tags:
  - packet-tracer
  - telnet
  - ssh
  - remote-access
  - security

topics:
  - dhcp-address-verification
  - remote-management
  - secure-cli-access

tools:
  - cisco-packet-tracer
  - ipconfig
  - ping
  - ssh-client

protocols:
  - DHCP
  - ICMP
  - Telnet
  - SSH

status: complete

video_id: ""
video_url: ""
thumbnail: ""

completed_lab: "/assets/pdfs/module-17-lab-35-Packet-Tracer-Use-Telnet-SSH.pdf"
lab_pdf: "/assets/pdfs/module-17-lab-35-Packet-Tracer-Use-Telnet-SSH.pdf"
permalink: /network-portfolio/videos/17-35-use-telnet-and-ssh/
diagram: ""
---

## Overview

Verify DHCP addressing and connectivity to router HQ at `64.100.1.1`, then compare the results of Telnet and SSH connection attempts. Observe how a router can reject insecure remote access while permitting SSH.

<!--more-->

---

## Preconditions

![Packet Tracer Lab 35 - Use Telnet and SSH - Preconditions](/assets/images/packet-tracer/cisco-lab-topology-module-17-lab-35.png)

---

## Skills Practiced

- Inspect DHCP-assigned host settings
- Test IP connectivity before remote access
- Compare Telnet with encrypted SSH management

---

## Video Walkthrough

This lab is documented as a written exercise; no video walkthrough is planned.

{% if page.video_id != "" %}
<iframe width="560" height="315" src="https://www.youtube.com/embed/{{ page.video_id }}" title="{{ page.title }}" frameborder="0" allowfullscreen></iframe>
{% endif %}

---

## Completed Lab Documentation

- Note: [Completed Lab PDF may be available upon request]

---

## Key Observations

The completed lab records a closed Telnet connection and successful SSH access to the `HQ#` prompt. Network reachability and management-service authorization are separate checks.

### Activity Focus

1. Verify the PC address with `ipconfig /all` and ping the HQ router.
2. Attempt a Telnet connection and observe its result.
3. Use the Packet Tracer SSH client to connect to the router.

### Notes

SSH is preferred to Telnet for remote CLI administration because SSH encrypts the session.

---

## Validation

Confirm the router is reachable, Telnet access is refused, and the SSH session reaches the expected prompt.



---
---
---

## 🔗 Navigation

* [Home](/)
* [Network+ Portfolio](/network-portfolio/)
  * **[FORMATIVE MODULES](/network-portfolio/formative-modules/)**
  * [Video Walkthroughs](/network-portfolio/videos/)
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* [Trading+](/trading/)
* [Bible Study](/bible-study/)
* [About the Portfolio](/about/)

---
---
---
