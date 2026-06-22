---
layout: post
title: "Networking Fundamentals | Configuring IPv4 Addresses on Multiple Network Interfaces"
lab_title: "Configuring IPv4 Addresses on Multiple Network Interfaces"

lesson: "4.0"
lesson_id: "04.02.09"
sort_order: "040209"

categories: [portfolio, videos]

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: ip-addressing-and-subnetting
subcategory_display: IP Addressing & Subnetting

content_type: video
content_type_display: Video

tags:
- ipv4
- tcp-ip
- subnetting
- dns
- default-gateway
- network-configuration

topics:
- ipv4-addressing
- subnet-masks
- default-gateways
- dns-configuration
- network-interfaces
- connectivity-testing

tools:
- Windows
- TCP-IP
- Ping
- Network-Adapter

protocols:
- IPv4
- ICMP
- DNS
- TCP-IP

permalink: /portfolio/videos/ipv4-address-configuration/

status: complete

video_id: "JuGv2zod9ow"
video_url: "https://youtu.be/JuGv2zod9ow"
thumbnail: "https://img.youtube.com/vi/JuGv2zod9ow/hqdefault.jpg"

date: 2026-06-19 20:00:00 -0700
last_updated: 2026-06-19 20:00:00 -0700

---

## Overview

This walkthrough demonstrates how to manually configure IPv4 addressing information on multiple network interfaces and verify successful network communication.

<!--more-->

Understanding how to assign IP addresses, subnet masks, default gateways, and DNS servers is one of the most fundamental skills in networking and systems administration.

---

## Concepts Explored

* IPv4 Addressing
* TCP/IP Configuration
* Network Interfaces
* DNS Resolution
* Default Gateways
* Network Communication

---

## Understanding Multi-Homed Systems

A multi-homed system contains more than one network interface.

Organizations may deploy multiple interfaces to:

* Access multiple networks
* Separate traffic types
* Improve security
* Support network segmentation
* Provide redundancy

Each interface can have its own unique addressing configuration.

---

## Core TCP/IP Components

### IP Address

An IP address uniquely identifies a device on a network.

Example:

```text
192.168.0.254
```

---

### Subnet Mask

The subnet mask determines which portion of the address identifies:

* The network
* The host

Examples:

```text
255.255.255.0
```

```text
255.255.0.0
```

---

### Default Gateway

The default gateway provides access to networks outside the local subnet.

Without a gateway, devices typically cannot reach:

* Remote networks
* Internet resources
* External services

---

### DNS Servers

Domain Name System (DNS) servers translate hostnames into IP addresses.

Example:

```text
www.example.com
```

becomes:

```text
192.0.2.1
```

Without DNS, users must communicate using IP addresses instead of names.

---

## Connectivity Testing

After configuration, connectivity should be verified.

Common tests include:

### Local Gateway Testing

Verifies communication with the local network.

### DNS Server Testing

Verifies external connectivity.

### Name Resolution Testing

Confirms DNS functionality by resolving hostnames into IP addresses.

---

## Skills Practiced

* IPv4 Address Configuration
* Network Administration
* DNS Configuration
* Connectivity Verification
* Interface Management
* Troubleshooting

---

## Why This Matters

Every networked device relies on proper IP configuration.

Understanding how addressing, gateways, and DNS work together enables administrators to:

* Troubleshoot connectivity issues
* Deploy new devices
* Configure network infrastructure
* Support enterprise environments

These skills form the foundation for nearly every networking and cybersecurity role.

---

## Common Troubleshooting Questions

When connectivity fails, ask:

* Is the IP address valid?
* Is the subnet mask correct?
* Is the gateway reachable?
* Are DNS servers configured properly?
* Can the device communicate locally?
* Can the device resolve names?

A systematic approach often identifies the root cause quickly.

---

## Video Walkthrough

<a href="{{ page.video_url }}" target="_blank" rel="noopener noreferrer">
  <img src="{{ page.thumbnail }}"
       alt="{{ page.title }}"
       style="width:420px; border-radius:8px;">
</a>

---

## Key Takeaway

Successful network communication depends on proper IP addressing, subnetting, gateway selection, and DNS configuration. Mastering these foundational concepts is essential for networking, cybersecurity, and systems administration careers.


---
---
---

## 🔗 Navigation

* [Home](/)
* [Network+ Portfolio](/network-portfolio/)
  * [Formative Modules](/network-portfolio/formative-modules/)
  * **[VIDEO WALKTHROUGHS](/network-portfolio/videos/)**
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* [Bible Study](/network-portfolio/bible-study/)
* [Behind the Portfolio](/network-portfolio/behind-the-portfolio/)

---
---
---