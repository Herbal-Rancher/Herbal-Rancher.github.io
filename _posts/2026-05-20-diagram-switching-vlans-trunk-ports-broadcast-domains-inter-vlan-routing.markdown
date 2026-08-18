---
layout: post
title: "Networking Fundamentals | VLANs, Trunk Ports, Broadcast Domains, and Inter-VLAN Routing Study Diagram"
lab_title: "VLANs, Trunk Ports, Broadcast Domains, and Inter-VLAN Routing Study Diagram"

lesson: "5.0"
lesson_id: "05.03.00"
sort_order: "050300"

categories: [portfolio, diagrams]

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: switching
subcategory_display: Switching

content_type: diagram
content_type_display: Diagram

topics: [vlans, trunk-ports, broadcast-domains, inter-vlan-routing, switching, logical-segmentation, network-plus]

tools: [VLANs, IEEE-802.1Q, CompTIA-Network-Plus]

permalink: /network-portfolio/study-diagrams/vlans-trunk-ports-broadcast-domains-inter-vlan-routing/

tags:

- vlans
- switching
- trunking
- broadcast-domains
- inter-vlan-routing
- networking

diagram_topic: "VLAN segmentation, access ports, trunk ports, broadcast domains, inter-VLAN routing, and packet flow"
diagram_reason: "I wanted to better understand how VLANs logically segment a physical network, how trunk links carry multiple VLANs between switches, why each VLAN forms a separate broadcast domain, and how Layer 3 routing allows devices in different VLANs to communicate."

status: complete

image: "/assets/images/study-diagrams/vlans-trunk-ports-broadcast-domains-inter-vlan-routing.png"
image_alt: "Teaching diagram explaining VLAN segmentation, access ports, trunk ports, broadcast domains, inter-VLAN routing, and packet flow."
---

# Overview

This study diagram explains how VLANs, access ports, trunk ports, broadcast domains, and inter-VLAN routing work together within a switched network.

<!--more-->

The diagram helped me separate the physical network from the logical network. Devices can connect to the same switching infrastructure while VLANs logically divide them into separate broadcast domains. Access ports connect end devices to a single VLAN, trunk links carry traffic for multiple VLANs between switches, and a Layer 3 device routes traffic when communication is required between different VLANs.

## Study Diagram

<a href="{{ page.image | relative_url }}" target="_blank" rel="noopener noreferrer">
  <img src="{{ page.image | relative_url }}"
       alt="{{ page.image_alt }}"
       style="width:100%; max-width:900px; border-radius:8px;">
</a>

## Topic

VLAN segmentation, access ports, trunk ports, broadcast domains, inter-VLAN routing, and packet flow.

## Reason for Diagram

I wanted to clearly understand the difference between the physical network and its logical segmentation. This diagram shows how VLANs create separate broadcast domains across shared switching infrastructure, how IEEE 802.1Q trunk links carry multiple VLANs between switches, and why communication between VLANs requires a Layer 3 router or multilayer switch.

The packet-flow example also helped me connect these concepts by showing how traffic moves from a device in one VLAN to its default gateway, through Layer 3 routing, and into a different VLAN.

---
---
---

## 🔗 Navigation
* [Home](/)
* [Network+ Portfolio](/network-portfolio/)
  * [Formative Modules](/network-portfolio/formative-modules/)
  * [Video Walkthroughs](/network-portfolio/videos/)
  * **[STUDY DIAGRAMS](/network-portfolio/study-diagrams/)**
* [Trading+](/trading/)
* [Bible Study](/bible-study/)
* [About the Portfolio](/about/)

---
---
---