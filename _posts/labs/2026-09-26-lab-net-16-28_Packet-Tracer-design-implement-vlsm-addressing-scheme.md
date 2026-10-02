---
layout: post
title: "Lab 28| Cisco Networking Labs - Design and Implement a VLSM Addressing Scheme"
lab_title: "Design and Implement a VLSM Addressing Scheme"

lesson: "16.0"
lesson_id: "16.28.00"
sort_order: "162800"

categories:
  - portfolio
  - videos

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: ip-addressing
subcategory_display: IP Addressing

content_type: video
content_type_display: Video

tags:
  - packet-tracer
  - vlsm
  - ipv4
  - subnetting
  - addressing
  - connectivity

topics:
  - vlsm-design
  - router-and-switch-addressing
  - connectivity-testing

tools:
  - cisco-packet-tracer
  - ping

protocols:
  - IPv4
  - ICMP

status: complete

video_id: "zwGWxiwK79o"
video_url: "https://www.youtube.com/watch?v=zwGWxiwK79o"
thumbnail: "https://img.youtube.com/vi/zwGWxiwK79o/hqdefault.jpg"

completed_lab: "/assets/pdfs/Module-16-Lab-28-Packet-Tracer-VLSM-Addressing-Scheme.pdf"
lab_pdf: "/assets/pdfs/Module-16-Lab-28-Packet-Tracer-VLSM-Addressing-Scheme.pdf"

permalink: /network-portfolio/videos/16-28-design-implement-vlsm-addressing-scheme/
diagram: ""
---

## Overview

Plan and implement a contiguous VLSM scheme within 192.168.203.0/24 for four LANs and a point-to-point router link. The design must meet the stated host counts and allow devices on every LAN to communicate.

<!--more-->

---

## Preconditions

![ Preconditions - Packet Tracer Lab 28 - VLSM Addressing Scheme](/assets/images/packet-tracer/cisco-lab-topology-module-16-lab-28.png)

---

## Skills Practiced

- Design and Implement a VLSM Addressing Scheme (Packet Tracer Lab 28)
- Vlsm design
- Router and switch addressing
- Connectivity testing

---

## Video Walkthrough

<!-- Add video_id, video_url, and thumbnail when the recording is ready. -->

{% if page.video_id != "" %}
<iframe width="560" height="315" src="https://www.youtube.com/embed/{{ page.video_id }}" title="{{ page.title }}" frameborder="0" allowfullscreen></iframe>
{% endif %}

---

## Completed Lab Documentation

{% if page.completed_lab != "" %}
- [Completed Lab PDF]({{ page.completed_lab | relative_url }})
{% endif %}

---

## Key Observations

VLSM allocates larger address blocks to networks with more hosts and smaller blocks where fewer addresses are needed. Contiguous, nonoverlapping subnets make the plan easier to verify.

### Activity Focus

1. Size subnets for Remote-1 (32), HQ-1 (21), Remote-2 (19), and HQ-2 (14) addresses.
2. Allocate contiguous ranges from largest to smallest, then reserve an efficient subnet for the HQ–Remote link.
3. Record each network/CIDR, first usable address, and broadcast address.
4. Assign the first usable LAN addresses to router interfaces, second usable to switch management, and last usable to hosts; use first and last usable on the WAN link.
5. Configure the devices and test reachability across all LANs.

### Notes

A requirement of 14 addresses can fit /28, while 32 requires /26 because /27 has only 30 usable host addresses. Check the exact topology before assigning interface names.

---

## Validation

Confirm there are no overlapping ranges or gaps between assigned subnets and that hosts and switch management interfaces are reachable.

---

## Related Exercises

- VLSM Subnetting
- Router and Switch Addressing
- Connectivity Testing

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