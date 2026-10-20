---
layout: post
title: "Lab 29| Cisco Networking Labs - VLSM Design and Implementation Practice"
lab_title: "VLSM Design and Implementation Practice"

lesson: "16.0"
lesson_id: "16.29.00"
sort_order: "162900"

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
  - vlsm-planning
  - device-addressing
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

completed_lab: "/assets/pdfs/Module-16-Lab-29-Packet-Tracer-VLSM-VLSM-Design-Implementation.pdf"
lab_pdf: "/assets/pdfs/Module-16-Lab-29-Packet-Tracer-VLSM-VLSM-Design-Implementation.pdf"
permalink: /network-portfolio/videos/16-29-vlsm-design-implementation-practice/
diagram: ""

---

## Overview

This Cisco Packet Tracer lab explores how **Variable Length Subnet Masking (VLSM)** supports efficient IPv4 address allocation across networks with different host requirements. Starting with `172.31.103.0/24`, I designed five subnets for four LANs and a point-to-point WAN connection, documented the addressing scheme, and completed the required device-addressing tasks.

The accompanying video walks through the implementation and connectivity checks.
<!--more-->
---

## Preconditions

- Cisco Packet Tracer activity with two branch routers, four LANs, and a WAN connection
- Starting IPv4 network: `172.31.103.0/24`
- Host requirements: 27, 25, 14, and 8 for the four LANs; 2 for the WAN


![Preconditions - Packet Tracer Lab 29 - VLSM Design and Implementation Practice](/assets/images/packet-tracer/cisco-lab-topology-module-16-lab-29.png)

---

## Skills Practiced

- Selecting appropriate subnet masks based on host requirements
- Allocating nonoverlapping VLSM subnets from largest to smallest
- Documenting network, usable host, and broadcast addresses
- Assigning IPv4 addresses, subnet masks, and default gateways
- Verifying network connectivity with ICMP ping tests

---

## Watch the Video Walkthrough

<!-- Add video_id, video_url, and thumbnail when the recording is ready. -->

{% if page.video_id != "" %}
<iframe width="560" height="315" src="https://www.youtube.com/embed/{{ page.video_id }}" title="{{ page.title }}" frameborder="0" allowfullscreen></iframe>
{% endif %}

---

## Completed Lab Documentation

{% if page.completed_lab != "" %}
- Note: *[Completed Lab PDF may be available upon request]*
{% endif %}

---
## Lab Steps

1. **Examine requirements:** Identify the five required subnets and their host capacities.
2. **Design the addressing scheme:** Allocate two `/27` LANs, two `/28` LANs, and one `/30` WAN from the original `/24` network.
3. **Implement addressing:** Complete the required configuration on Branch1, the Room-312 switch, and PC-D.
4. **Verify connectivity:** Run the specified ping tests from Branch1, Room-312, and PC-D.

---

## Validation

The lab documentation identifies ping destinations across the LAN and WAN subnets. The video demonstrates the connectivity checks and their results.

---

## Troubleshooting / Notes

The addressing plan uses different subnet sizes to meet host requirements without overlapping networks. Correct subnet masks and default gateways are essential for communication between subnets.


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