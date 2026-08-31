---

layout: post
title: "Lab 21| Cisco Networking Labs - Secure Network Devices"
lab_title: "Secure Network Devices"

lesson: "15.0"
lesson_id: "15.21.00"
sort_order: "152100"

categories:

- portfolio
- labs
- videos

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: network-security
subcategory_display: Network Security

content_type: video
content_type_display: Video

tags:

- packet-tracer
- network-security
- device-hardening
- router-security
- switch-security
- ssh
- secure-management

topics:

- network-device-security
- ssh-configuration
- password-security
- login-security
- management-interface
- unused-port-security
- connectivity-testing

tools:

- cisco-packet-tracer
- router
- switch
- command-line-interface
- ping
- ssh

protocols:

- IPv4
- ICMP
- SSH

status: complete

video_id: "lmbg0J23ZPM"
video_url: "https://youtu.be/lmbg0J23ZPM"
thumbnail: "https://img.youtube.com/vi/lmbg0J23ZPM/hqdefault.jpg"

completed_lab: "/assets/pdfs/Module-15-Lab-21-Packet-Tracer-Secure-Network-Devices.pdf"
lab_pdf: "/assets/pdfs/Module-15-Lab-21-Packet-Tracer-Secure-Network-Devices.pdf"

permalink: /network-portfolio/videos/15-21-secure-network-devices/

---
## Overview

This Packet Tracer lab focuses on securing Cisco router and switch management while maintaining network connectivity. I configured device hardening, secure SSH administration, local authentication, login protection, switch management access, and unused-port security, then verified connectivity across both LANs.

<!--more-->

---

## Preconditions

![Packet Tracer Lab 21 - Secure Network Devices - Preconditions](/assets/images/packet-tracer/cisco-lab-topology-module-15-Lab-21.png)

---

### Addressing

| Device    | Interface | Address       | Mask          | Gateway     |
| --------- | --------- | ------------- | ------------- | ----------- |
| RTR-A     | G0/0/0    | 192.168.1.1   | 255.255.255.0 | N/A         |
| RTR-A     | G0/0/1    | 192.168.2.1   | 255.255.255.0 | N/A         |
| SW-1      | VLAN 1    | 192.168.1.254 | 255.255.255.0 | 192.168.1.1 |
| PC        | NIC       | 192.168.1.2   | 255.255.255.0 | 192.168.1.1 |
| Laptop    | NIC       | 192.168.1.10  | 255.255.255.0 | 192.168.1.1 |
| Remote PC | NIC       | 192.168.2.10  | 255.255.255.0 | 192.168.2.1 |

---

## Topics & Features Covered

- Cisco router and switch device hardening
- Secure passwords and encrypted credentials
- Console and VTY session security
- SSH Version 2 remote administration
- RSA key generation and domain configuration
- Local administrator authentication with `login local`
- Login blocking against repeated failed attempts
- Switch management through a VLAN 1 SVI
- Switch default-gateway configuration
- Administrative shutdown of unused switchports
- Configuration verification and persistence
- ICMP connectivity testing across both LANs

---

## Skills Practiced

- Secure Network Devices (Packet Tracer Lab 21)
- Configure Cisco router and switch security
- Configure secure administrative access
- Configure and verify SSH
- Configure local user authentication
- Secure console and VTY access
- Configure switch management addressing
- Disable unused switchports
- Save and verify device configurations
- Verify routed network connectivity

---

## Video Walkthrough

<iframe
width="560"
height="315"
src="https://www.youtube.com/embed/{{ page.video_id }}"
title="{{ page.title }}"
frameborder="0"
allowfullscreen>
</iframe>

---

## Completed Lab Documentation

- [Completed Lab PDF]({{ page.completed_lab | relative_url }})

---

## Related Exercises

- Network Device Hardening
- Secure Remote Administration with SSH
- Router and Switch Management
- Password and Login Security
- Switch Management Interfaces
- Network Connectivity Testing

---
---
---

## 🔗 Navigation

- [Home](/)
- [Network+ Portfolio](/network-portfolio/)
  - **[FORMATIVE MODULES](/network-portfolio/formative-modules/)**
  - [Video Walkthroughs](/network-portfolio/videos/)
  - [Study Diagrams](/network-portfolio/study-diagrams/)
- [Trading+](/trading/)
- [Bible Study](/bible-study/)
- [About the Portfolio](/about/)

---
---
---