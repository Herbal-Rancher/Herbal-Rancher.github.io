---
layout: post
title: "Lab 40| Cisco Networking Labs - Configure Secure Passwords and SSH"
lab_title: "Configure Secure Passwords and SSH"

lesson: "17.0"
lesson_id: "17.40.00"
sort_order: "174000"

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
  - ssh
  - device-hardening
  - passwords
  - router
  - switch

topics:
  - router-hardening
  - switch-hardening
  - ssh-management

tools:
  - cisco-packet-tracer
  - cisco-ios-cli
  - ssh-client

protocols:
  - IPv4
  - SSH

status: complete

video_id: ""
video_url: ""
thumbnail: ""

completed_lab: ""
lab_pdf: ""
permalink: /network-portfolio/videos/17-40-configure-secure-passwords-and-ssh/
diagram: ""
---

## Overview

Prepare a Cisco router and switch for secure management in a Packet Tracer deployment scenario. Configure management addressing, local authentication, password controls, SSH access, and restrictions on unused switch ports.

<!--more-->

---

## Preconditions

![Packet Tracer Lab 40 - Configure Secure Passwords and SSH - Preconditions](/assets/images/packet-tracer/cisco-lab-topology-module-17-Lab-40.png)

---

## Skills Practiced

- Configure router and switch management addressing
- Apply password and login controls
- Generate keys and enable SSH-only remote management
- Disable unused switch ports and verify remote access

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

Device hardening combines multiple protections: local credentials, controlled management access, login restrictions, session timeouts, and reducing unused access points. A secure configuration must also be saved and tested.

### Activity Focus

1. Configure RTA and PCA addressing and apply basic router security controls.
2. Enable SSH management with local authentication and verify connectivity.
3. Configure SW1 management settings and secure unused interfaces.

### Notes

The educational activity specifies 1024-bit RSA keys for Packet Tracer scoring. This is a lab requirement, not a recommended production key size. The supplied completed source is DOCX; export it to PDF before populating the PDF link.

---

## Validation

Confirm SSH access to RTA and SW1 as appropriate, saved configurations, and disabled unused ports.

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
