---
layout: post
title: "Lab 42 | Cisco Networking Labs - Examine the ARP Table"
lab_title: "Examine the ARP Table"

lesson: "18.0"
lesson_id: "18.42.00"
sort_order: "184200"

categories:
  - portfolio
  - labs

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: ip-addressing
subcategory_display: IP Addressing

content_type: lab
content_type_display: Lab

tags:
  - packet-tracer
  - arp
  - mac-address-table
  - broadcast
  - routing
  - simulation-mode

topics:
  - arp-request-reply
  - switch-mac-learning
  - remote-destination-next-hop

tools:
  - cisco-packet-tracer
  - arp
  - ping
  - show-mac-address-table
  - show-arp

protocols:
  - ARP
  - Ethernet
  - IPv4
  - ICMP

status: complete

video_id: ""
video_url: ""
thumbnail: ""

completed_lab: ""
lab_pdf: ""
permalink: /network-portfolio/videos/18-42-examine-the-arp-table/
diagram: ""
---

## Overview

Investigate how ARP resolves IPv4 next-hop addresses and how switches learn source MAC addresses. Compare local-LAN communication with traffic destined for a remote network, using Packet Tracer PDU inspection and device tables.

<!--more-->

---

## Preconditions

![Packet Tracer Lab 42 topology](/assets/images/packet-tracer/cisco-lab-topology-module-18-lab-42.png)

---

## Skills Practiced

- Trace an ARP request and reply in Simulation Mode
- Compare host ARP caches with switch MAC address tables
- Recognize the Ethernet broadcast destination used by ARP requests
- Explain why remote traffic resolves the default gateway rather than the remote host

---

## Completed Lab Documentation

{% if page.completed_lab != "" %}
**Completed Lab:** [View PDF]({{ page.completed_lab| relative_url }})
{% endif %}

---

## Key Observations

ARP maps a local next-hop IPv4 address to a MAC address; a switch MAC table maps observed MAC addresses to switch ports. These tables answer different questions and are learned in different ways.

### Activity Focus

1. Clear a host ARP cache and generate a local ping to observe the initial broadcast.
2. Inspect the switch forwarding behavior and learned MAC addresses.
3. Generate traffic on both LANs to examine MAC address table entries.
4. Trace an ARP request when a host communicates with a remote IPv4 network.

### Notes

This lab is currently in progress. Observations above describe the concepts and intended investigation, not verified completion results. Add screenshots, your own findings, and any corrections after finishing the activity.

---

## Validation

Use `arp -a`, `show mac-address-table`, and `show arp` to compare learned entries with the addressing table and selected PDUs.

---

## Related Exercises

- Layer 2 switching
- Default gateway operation
- IPv4 routing

---
---
---

## 🔗 Navigation

* [Home](/)
* [Network+ Portfolio](/network-portfolio/)
  * **[FORMATIVE MODULES](/network-portfolio/formative-modules/)**
  * [Videos](/network-portfolio/videos/)
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* [Trading+](/trading/)
* [Bible Study](/bible-study/)
* [About the Portfolio](/about/)

---
---
---
