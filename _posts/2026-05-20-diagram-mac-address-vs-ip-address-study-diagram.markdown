---
layout: post
title: "Networking Fundamentals | MAC Address vs IP Address Study Diagram"
lab_title: "MAC Address vs IP Address Study Diagram"

lesson: "2.0"
lesson_id: "13.08.00"
sort_order: "130800"

categories: [portfolio, diagrams]

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: tcpip
subcategory_display: TCP/IP

content_type: diagram
content_type_display: Diagram

topics:
  - mac-address
  - ip-address
  - ethernet
  - osi-model
  - layer-2
  - layer-3
  - arp
  - tcpip

tools:
  - Ethernet
  - IPv4
  - ARP
  - Network+

permalink: /network-portfolio/study-diagrams/mac-address-vs-ip-address/

tags:
  - mac-address
  - ip-address
  - ethernet
  - arp
  - osi-model
  - networking
  - tcpip

diagram_topic: "Comparing MAC addresses and IP addresses, their roles, communication scope, and how they work together."

diagram_reason: "I created this diagram to better understand the relationship between Layer 2 MAC addresses and Layer 3 IP addresses and how both are required for successful network communication."

status: complete

image: "/assets/images/study-diagrams/MAC-address-vs-ip-address-diagram-chatgpt-rendered-image.png"

image_alt: "Study diagram comparing MAC addresses and IP addresses, explaining their purposes, communication scope, OSI layers, and how they work together."

---

## Overview

This study diagram compares MAC addresses and IP addresses, explaining their roles within the OSI Model, how each is assigned, where each is used, and how they work together to deliver data across local and remote networks.

<!--more-->

Understanding the difference between physical addressing (MAC) and logical addressing (IP) is fundamental to learning Ethernet, routing, ARP, switching, and packet delivery.

---

## Study Diagram

<a href="{{ page.image | relative_url }}" target="_blank" rel="noopener noreferrer">
  <img src="{{ page.image | relative_url }}"
       alt="{{ page.image_alt }}"
       style="width:100%; max-width:420px; border-radius:8px;">
</a>

---

## Topics Covered

- MAC Address vs IP Address
- Physical vs Logical Addressing
- Layer 2 vs Layer 3
- Ethernet Communication
- Local vs Remote Communication
- Switches vs Routers
- ARP Resolution
- MAC Address Format
- IPv4 and IPv6 Address Examples
- Packet Delivery

---

## Key Takeaways

- A MAC address identifies a network interface on the local LAN.
- An IP address identifies a device across interconnected networks.
- Switches forward frames using MAC addresses.
- Routers forward packets using IP addresses.
- ARP maps an IP address to a MAC address before local communication begins.
- MAC and IP addresses work together to deliver data from source to destination.

---

## Why I Created This Diagram

Early in my networking studies, I understood what MAC and IP addresses were individually, but I struggled to understand how they worked together during communication. Creating this visual guide helped me connect switching, routing, ARP, and the OSI Model into one complete picture of how data travels across a network.

---

## Related Study Diagrams

- Ethernet Frame Structure
- ARP Overview
- Packet Flow Through a Router
- Default Gateway & OSI Model
- IPv4 Addressing
- IPv4 vs IPv6
- Dual-Stack Networking
- Network vs Host Bits
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