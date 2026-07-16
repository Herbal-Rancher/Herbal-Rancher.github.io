---
layout: post
title: "Networking Fundamentals | CIDR Prefix Notation Study Diagram"
lab_title: "CIDR Prefix Notation Study Diagram"

lesson: "2.0"
lesson_id: "13.11.00"
sort_order: "131100"

categories: [portfolio, diagrams]

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: subnetting
subcategory_display: IPv4 Subnetting

content_type: diagram
content_type_display: Diagram

topics:
  - cidr
  - subnetting
  - ipv4
  - prefix-notation
  - subnet-masks
  - network-bits
  - host-bits

tools:
  - IPv4
  - CIDR
  - Network+

permalink: /network-portfolio/study-diagrams/cidr-prefix-notation/

tags:
  - cidr
  - subnetting
  - ipv4
  - subnet-mask
  - prefix-length
  - networking

diagram_topic: "CIDR prefix notation, subnet masks, prefix lengths, and IPv4 subnetting."

diagram_reason: "I created this diagram to better understand CIDR notation and how prefix lengths define the network and host portions of an IPv4 address."

status: complete

image: "/assets/images/study-diagrams/cidr-prefix-notation-diagram-chatgpt-rendered-image.png"

image_alt: "Study diagram explaining CIDR prefix notation, subnet masks, prefix lengths, and IPv4 subnetting."

---

## Overview

This study diagram explains CIDR (Classless Inter-Domain Routing) prefix notation and how prefix lengths replace traditional classful subnet masks to create flexible IPv4 networks.

<!--more-->

Understanding CIDR notation is essential for subnetting, route summarization, address planning, and modern enterprise network design.

---

## Study Diagram

<a href="{{ page.image | relative_url }}" target="_blank" rel="noopener noreferrer">
  <img src="{{ page.image | relative_url }}"
       alt="{{ page.image_alt }}"
       style="width:100%; max-width:420px; border-radius:8px;">
</a>

---

## Topics Covered

- What CIDR is
- Prefix notation (/24, /27, /30, etc.)
- Network bits vs. host bits
- Common CIDR prefixes
- Binary subnet masks
- Dotted-decimal subnet masks
- Host calculations
- CIDR examples
- Route summarization
- CIDR advantages

---

## Key Takeaways

- CIDR replaces traditional classful addressing with flexible prefix lengths.
- The number after the slash (/) represents the number of **network bits**.
- More network bits create **more subnets with fewer hosts**.
- Fewer network bits create **fewer networks with more hosts**.
- CIDR enables efficient IP address allocation and route summarization.
- Modern routing protocols rely on CIDR for scalable network design.

---

## Why I Created This Diagram

CIDR notation was initially difficult for me because it required thinking in terms of bits rather than dotted-decimal subnet masks. This diagram helped me connect binary subnet masks, prefix lengths, host counts, and real-world subnetting examples into a single visual reference that I can quickly review while designing or troubleshooting IPv4 networks.

---

## Related Study Diagrams

- Subnet Masks
- Network vs Host Bits
- IPv4 Addressing
- IPv4 Network Design
- Default Gateway & OSI Model
- Packet Flow Through a Router
- IPv4 vs IPv6
- Network Troubleshooting Flowchart


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
* [About the Portfolio](/zabout-the-portfolio/)

---
---
---