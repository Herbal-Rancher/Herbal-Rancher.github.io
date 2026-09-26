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

Practice VLSM with 192.168.72.0/24 for four room LANs and the Branch1–Branch2 link. Calculate each subnet, document the addressing plan, finish the required device configurations, and test end-to-end reachability.

<!--more-->

---

## Preconditions

<!-- Add the starting Packet Tracer topology screenshot here after recording. -->

---

## Skills Practiced

- VLSM Design and Implementation Practice (Packet Tracer Lab 29)
- Vlsm planning
- Device addressing
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

The largest LAN receives the first block, followed by progressively smaller LANs and the router link. Choosing a mask based only on the number of addresses in a block can leave too few usable host addresses.

### Activity Focus

1. Determine subnet sizes for Room-407 (58), Room-312 (29), Room-279 (15), and Room-114 (7) host addresses, plus the router link.
2. Allocate five subnets in descending LAN size and document each network/CIDR, first usable address, and broadcast address.
3. Apply the activity’s first usable router, second usable switch, and last usable PC address rules.
4. Configure the Branch1 LAN interfaces, Room-312 switch management and gateway, and PC-D addressing.
5. Ping all documented IP addresses from Branch1, Room-312, and PC-D.

### Notes

The activity can present one of three topologies. Match room names to the interfaces in your assigned Packet Tracer file. A 15-host LAN needs /27; /28 provides only 14 usable addresses.

---

## Validation

Verify the address plan has no overlap and pings work from the three devices where testing is permitted.

---

## Related Exercises

- VLSM Design
- Host Address Planning
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
