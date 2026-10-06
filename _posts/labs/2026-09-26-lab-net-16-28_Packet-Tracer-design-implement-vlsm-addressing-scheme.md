---
layout: post
title: "Lab 28| Cisco Networking Labs - Design and Implement a VLSM Addressing Scheme"
lab_title: "Design and Implement a VLSM Addressing Scheme"

lesson: "16.0"
lesson_id: "16.28.00"
sort_order: "162800"

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
  - vlsm-design
  - subnet-allocation
  - router-and-switch-addressing
  - connectivity-testing

tools:
  - cisco-packet-tracer
  - command-line-interface
  - ping

protocols:
  - IPv4
  - ICMP

status: complete

video_id: "zwGWxiwK79o"
video_url: "https://www.youtube.com/watch?v=zwGWxiwK79o"
thumbnail: "https://img.youtube.com/vi/zwGWxiwK79o/hqdefault.jpg"

completed_lab: "/assets/pdfs/Module-16-Lab-28-Packet-Tracer-VLSM-Addressing-Scheme.pdf"
lab_pdf: "/assets/pdfs/Module-16-Lab-28-Packet-Tracer-VLSM-Addressing-Scheme.pdf"

permalink: /network-portfolio/videos/16-28-design-implement-vlsm-addressing-scheme/
diagram: ""
---

## Overview

Design and implement a Variable Length Subnet Masking (VLSM) addressing scheme within the 10.1.1.0/24 network. This lab applies subnet sizing, contiguous address allocation, device addressing, and connectivity testing across multiple LANs and a point-to-point WAN link.

<!--more-->

---

## Preconditions

![Preconditions - Packet Tracer Lab 28 - VLSM Addressing Scheme](/assets/images/packet-tracer/cisco-lab-topology-module-16-lab-28.png)

---

## Skills Practiced

- Design a VLSM IPv4 addressing scheme based on host requirements
- Select appropriate subnet masks for different network sizes
- Allocate contiguous, nonoverlapping subnets
- Configure router interfaces and switch management interfaces
- Assign IPv4 addresses and default gateways to hosts
- Verify end-to-end IP connectivity
- Troubleshoot addressing and connectivity issues

---

## Video Walkthrough

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

VLSM allows each network segment to receive a subnet sized for its actual host requirements instead of using the same subnet mask throughout the network. In this design, the largest LAN was allocated first, followed by progressively smaller LANs and finally the point-to-point WAN link.

The resulting subnets are contiguous and nonoverlapping, allowing the 10.1.1.0/24 address space to be used efficiently.

### VLSM Addressing Design

| Network | Hosts Required | Network/CIDR | First Usable | Broadcast |
|---|---:|---|---|---|
| PS-115 LAN | 47 | 10.1.1.0/26 | 10.1.1.1 | 10.1.1.63 |
| PD-2 LAN | 28 | 10.1.1.64/27 | 10.1.1.65 | 10.1.1.95 |
| PD-1 LAN | 11 | 10.1.1.96/28 | 10.1.1.97 | 10.1.1.111 |
| PS-101 LAN | 5 | 10.1.1.112/29 | 10.1.1.113 | 10.1.1.119 |
| WAN | 2 | 10.1.1.120/30 | 10.1.1.121 | 10.1.1.123 |

### Address Assignment Strategy

- Assign the first usable address of each LAN subnet to the router interface.
- Assign the second usable address to the switch VLAN 1 management interface.
- Assign the last usable address to the LAN host.
- Use the first and last usable addresses of the /30 subnet for the point-to-point WAN connection.
- Configure the appropriate router interface as the default gateway for each switch and host.

---

## Validation

The completed addressing plan satisfies the host requirements while conserving IPv4 address space. The LANs use /26, /27, /28, and /29 networks, while the two-router WAN connection uses an efficient /30 subnet.

Validation includes confirming:

- Each device has the correct IPv4 address and subnet mask
- Hosts and switches use the correct default gateway
- Subnet ranges do not overlap
- The allocated subnets remain contiguous
- Switch management interfaces are reachable from hosts across the LANs
- Hosts and network devices can communicate across the network

---

## Troubleshooting / Notes

The subnet mask must provide enough **usable host addresses**, not simply enough total addresses. For example, a network requiring 28 hosts can use a /27 because it provides 30 usable addresses, while a network requiring 47 hosts requires a /26 because a /27 would be too small.

Working from the largest host requirement to the smallest also helps prevent fragmentation and makes the VLSM addressing plan easier to calculate and verify.

---

## Related Exercises

- VLSM Subnetting
- IPv4 Address Planning
- Router and Switch Addressing
- Default Gateway Configuration
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