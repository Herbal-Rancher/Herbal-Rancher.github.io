---
layout: post
title: "Lab 38 | Cisco Networking Labs - IPv6 Neighbor Discovery"
lab_title: "IPv6 Neighbor Discovery"

lesson: "17.0"
lesson_id: "17.38.00"
sort_order: "173800"

categories:
  - portfolio
  - labs

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: ip-addressing
subcategory_display: IP Addressing

content_type: lab
content_type_display: Lab Documentation

tags:
  - packet-tracer
  - ipv6
  - ndp
  - icmpv6
  - multicast
  - neighbor-cache

topics:
  - neighbor-solicitation-and-advertisement
  - local-versus-remote-ipv6
  - packet-analysis

tools:
  - cisco-packet-tracer
  - simulation-mode
  - show-ipv6-neighbors

protocols:
  - IPv6
  - ICMPv6
  - NDP

status: complete

video_id: ""
video_url: ""
thumbnail: ""

completed_lab: "/assets/pdfs/module-17-lab-38-Packet-Tracer-IPV6-Neighgor-Discovery.pdf"
lab_pdf: "/assets/pdfs/module-17-lab-38-Packet-Tracer-IPV6-Neighgor-Discovery.pdf"
permalink: /network-portfolio/videos/17-38-ipv6-neighbor-discovery/
diagram: ""
---

## Overview

Use Packet Tracer Simulation Mode to investigate how IPv6 Neighbor Discovery resolves next-hop link-layer addresses. Compare communication between hosts on the same LAN with communication routed to a remote IPv6 subnet.

<!--more-->

---

## Preconditions

![Packet Tracer Lab 38 - IPv6 Neighbor Discovery - Preconditions](/assets/images/packet-tracer/cisco-lab-topology-Module-17-Lab-38.png)

---

## Skills Practiced

- Identify Neighbor Solicitation and Neighbor Advertisement messages
- Interpret Ethernet and IPv6 addressing in PDU details
- Inspect and refresh the IPv6 neighbor cache

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

For local communication, a host resolves the destination neighbor directly. For remote communication, the Ethernet frame is addressed to the local router while the IPv6 packet remains addressed to the remote host.

### Activity Focus

1. Filter simulation events to ICMPv6 and NDP and inspect local-LAN communication.
2. Compare incoming and outgoing PDU details, including multicast addresses and ICMPv6 message types.
3. Observe next-hop discovery during remote-network communication and inspect router neighbor entries.

### Notes

Packet Tracer event fields should be recorded as displayed. The lab explores ICMPv6 Types 135 and 136 and the relationship between IPv6 addresses and Ethernet MAC addresses.

---

## Validation

Identify the intended next hop, the relevant Layer 2 destination, and learned neighbor entries for local and remote scenarios.


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
