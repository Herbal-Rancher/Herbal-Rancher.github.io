---
layout: post
title: "Lab 27| Cisco Networking Labs - Subnetting Scenario"
lab_title: "Subnetting Scenario"

lesson: "16.0"
lesson_id: "16.27.00"
sort_order: "162700"

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
  - ipv4
  - subnetting
  - addressing
  - eigrp
  - connectivity

topics:
  - fixed-length-subnetting
  - ipv4-addressing
  - connectivity-testing

tools:
  - cisco-packet-tracer
  - ping
  - ping

protocols:
  - IPv4
  - ICMP

status: complete

video_id: "zwGWxiwK79o"
video_url: "https://www.youtube.com/watch?v=zwGWxiwK79o"
thumbnail: "https://img.youtube.com/vi/zwGWxiwK79o/hqdefault.jpg"

completed_lab: "/assets/pdfs/Module-16-Lab-27-Packet-Tracer-Subnetting-Scenario.pdf"
lab_pdf: "/assets/pdfs/Module-16-Lab-27-Packet-Tracer-Subnetting-Scenario.pdf"

permalink: /network-portfolio/videos/16-27-subnetting-scenario/
diagram: ""
---

## Overview

Design an addressing scheme for four LANs and an R1–R2 link using 192.168.100.0/24. Document the subnets, configure the remaining device addresses, and test connectivity across the routed network.

<!--more-->

---

## Preconditions

<!-- Add the starting Packet Tracer topology screenshot here after recording. -->

---

## Skills Practiced

- Subnetting Scenario (Packet Tracer Lab 27)
- Fixed-length subnetting
- Ipv4 addressing
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

A consistent subnet size must provide enough host addresses for every LAN. The addressing table connects each calculated subnet to its router interface, switch management address, and PC gateway.

### Activity Focus

1. Determine the subnet count and borrow enough bits while retaining at least 25 usable addresses per LAN.
2. Calculate the new mask and subnet ranges; assign subnets 0–3 to the LANs and subnet 4 to the router link.
3. Document router, switch VLAN 1, and PC addresses using the activity’s first, second, and last usable address rules.
4. Configure the R1 LAN interfaces, S3 management address and gateway, and PC4 address and gateway.
5. Ping the listed addresses from R1, S3, and PC4.

### Notes

If a ping fails, inspect the subnet mask, host gateway, interface state, switch management gateway, and the corresponding addressing-table entry.

---

## Validation

Verify the completed addressing table and successful pings from the permitted devices. EIGRP is already configured in the activity.

---

## Related Exercises

- IPv4 Subnetting
- Address Planning
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
