---
layout: post
title: "Lab 41 | Cisco Networking Labs - Observe Data Flow in a LAN"
lab_title: "Observe Data Flow in a LAN"

lesson: "18.0"
lesson_id: "18.41.00"
sort_order: "184100"

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
  - ethernet
  - arp
  - icmp
  - simulation-mode
  - switching

topics:
  - lan-topology
  - arp-broadcasts
  - icmp-echo
  - arp-cache

tools:
  - cisco-packet-tracer
  - ping
  - arp

protocols:
  - Ethernet
  - ARP
  - ICMP
  - IPv4

status: complete

video_id: ""
video_url: ""
thumbnail: ""

completed_lab: "/assets/pdfs/module-18-lab-41-Packet-Tracer-Observe-Data-Flow-in-a-LAN.pdf"
lab_pdf: ""
permalink: /network-portfolio/videos/18-41-observe-data-flow-in-a-lan/
diagram: ""
---

## Overview

Explore the movement of traffic through a small switched Ethernet LAN. Build a topology with three PCs and a Cisco 2960 switch, generate ARP and ICMP traffic, and use Simulation Mode to observe how address resolution affects subsequent pings.

<!--more-->

---

## Preconditions

![Packet Tracer Lab 41 topology](/assets/images/packet-tracer/cisco-lab-topology-module-18-lab-41.png)

---

## Skills Practiced

- Construct and cable a three-host switched LAN
- Assign IPv4 addresses within a common /24 network
- Distinguish ARP broadcast traffic from ICMP echo traffic
- Inspect ARP caches and compare simulation reset with device power cycling

---

## Completed Lab Documentation

{% if page.completed_lab != "" %}
> * **Completed Lab:** [View LAB PDF]({{ page.completed_lab | relative_url }})
{% endif %}

---

## Key Observations

An initial ping may require ARP to resolve the destination MAC address. Simulation resets do not necessarily clear learned dynamic tables, so later traffic can look different from the first exchange.

### Activity Focus

1. Build a 2960 switch topology with three hosts and observe link status.
2. Configure PC-A, PC-B, and PC-C on the 192.168.1.0/24 LAN.
3. Use a Simple PDU from PC-A to PC-C to examine ARP and ICMP events.
4. Inspect ARP tables using the Packet Tracer inspection tool and `arp -a`.

### Notes

This lab is currently in progress. Observations above describe the concepts and intended investigation, not verified completion results. Add screenshots, your own findings, and any corrections after finishing the activity.

---

## Validation

Confirm the three hosts share the intended subnet, the Ethernet links are active, and the ARP table contains the expected neighbor after traffic is generated.

---

## Related Exercises

- Ethernet switching
- ARP address resolution
- ICMP and network diagnostics

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
