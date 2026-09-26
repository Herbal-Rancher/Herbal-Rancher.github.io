---
layout: post
title: "Lab 31| Cisco Networking Labs - Implement a Subnetted IPv6 Addressing Scheme"
lab_title: "Implement a Subnetted IPv6 Addressing Scheme"

lesson: "16.0"
lesson_id: "16.31.00"
sort_order: "163100"

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
  - ipv6
  - subnetting
  - slaac
  - routing
  - connectivity

topics:
  - ipv6-subnet-planning
  - router-ipv6-configuration
  - automatic-host-addressing

tools:
  - cisco-packet-tracer
  - ping

protocols:
  - IPv6
  - ICMPv6

status: complete

video_id: "zwGWxiwK79o"
video_url: "https://www.youtube.com/watch?v=zwGWxiwK79o"
thumbnail: "https://img.youtube.com/vi/zwGWxiwK79o/hqdefault.jpg"

completed_lab: "/assets/pdfs/Module-16-Lab-31-Packet-Tracer-IPv6-Subnet-Addressing.pdf"
lab_pdf: "/assets/pdfs/Module-16-Lab-31-Packet-Tracer-IPv6-Subnet-Addressing.pdf"
permalink: /network-portfolio/videos/16-31-implement-subnetted-ipv6-addressing-scheme/
diagram: ""
---

## Overview

Assign consecutive IPv6 /64 networks to four LANs and the R1–R2 link, starting with 2001:db8:acad:00c8::/64. Configure the router interfaces and host autoconfiguration, then verify connectivity between PCs.

<!--more-->

---

## Preconditions

<!-- Add the starting Packet Tracer topology screenshot here after recording. -->

---

## Skills Practiced

- Implement a Subnetted IPv6 Addressing Scheme (Packet Tracer Lab 31)
- Ipv6 subnet planning
- Router ipv6 configuration
- Automatic host addressing

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

Each network segment needs its own /64 prefix. Link-local addresses can be reused on different links, while routing and host autoconfiguration are needed for communication between LANs.

### Activity Focus

1. Use consecutive /64 prefixes for R1 G0/0, R1 G0/1, R2 G0/0, R2 G0/1, and the R1–R2 link.
2. Complete the address table: first usable address on LAN router interfaces, first address on R1’s router link, and second on R2’s link.
3. Set the specified link-local addresses (fe80::1 on R1 and fe80::2 on R2), enable IPv6 routing, and configure the necessary routes.
4. Set PC1–PC4 to IPv6 Auto Config and test pings between PCs.

### Notes

The source worksheet shows /32 in several unfinished subnet-table cells, despite requiring consecutive /64 subnets. Use /64 for each LAN and the router link; check that the link-local addresses are applied on the intended interfaces.

---

## Validation

Check router interface prefixes, host IPv6 addresses and gateways, routes, and successful cross-LAN pings.

---

## Related Exercises

- IPv6 Subnetting
- Router Configuration
- IPv6 Autoconfiguration

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
