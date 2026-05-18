---
layout: post
title: "11.0 Milestone Lab - Enterprise Network Redesign"
module: 11.0
order: 11.1
categories: [portfolio, blog, labs, lab, network]
tags: [network-design, vlan, switching, wireless, redundancy, troubleshooting, enterprise]
permalink: /portfolio/labs/module-11-0/milestone-network-topologies-redesign/
---

## Enterprise Network Redesign Lab

In this lab, I redesign a growing company’s network after expansion into a second building. The 
goal is to improve **performance, reliability, scalability, and security** using structured network 
engineering practices. In this lab, I will address VLANs, Redundancy, and Wireless Optimization.

<!--more-->
---

## Overview

The existing network had several issues:

- Network slowdowns due to poor VLAN configuration  
- No redundancy → outages when links fail  
- Inconsistent wireless coverage and dead zones  
- No separation between internal and guest wireless  


This walkthrough demonstrates how to **analyze, design, and improve** the network using industry-standard practices.

---

## Objectives

- Implement proper VLAN segmentation  
- Configure trunking between switches  
- Add redundancy and eliminate single points of failure  
- Prevent switching loops using STP  
- Deploy secure and reliable wireless infrastructure  
- Separate guest and internal network traffic  

---

## Step 1: Assess the Physical Network

Before configuring anything, evaluate the environment:

- Verify **fiber connectivity** between buildings  
- Confirm Ethernet distance limits (≤100m for copper)  
- Identify high-density areas (conference rooms, common spaces)  
- Count devices:
  - Workstations  
  - VoIP phones  
  - Wireless devices  
  - IoT  

*Why this matters:*  
Design decisions must match physical constraints and usage patterns.

---

## Step 2: Design VLAN Segmentation

The original network used a flat structure, causing congestion and security risks.

### VLAN Design

| Department | VLAN |
|------------|--------|
| HR | VLAN 10 |
| Finance | VLAN 20 |
| Sales | VLAN 30 |
| IT | VLAN 40 |
| Servers | VLAN 50 |
| Voice | VLAN 60 |
| Guest WiFi | VLAN 70 |
| Management | VLAN 99 |

### Benefits

- Reduces broadcast traffic  
- Improves performance  
- Limits lateral movement (security)  
- Simplifies troubleshooting  

**Critical Rule:**  
Guest VLAN must never access internal resources.

---

## Step 3: Configure Trunk Links

To allow VLAN communication across switches and buildings:

- Use **802.1Q trunking**  
- Carry multiple VLANs over one link  
- Use fiber uplinks between buildings  

This ensures all VLANs are available across the network.

---

## Step 4: Add Redundancy

The original design had no failover.

### Improvements

- Add **redundant uplinks** between switches  
- Provide multiple network paths  

### Link Aggregation

- Combine multiple links using:
  - LACP (Link Aggregation Control Protocol)  

### Benefits

- Increased bandwidth  
- Automatic failover  
- Higher reliability  

---

## Step 5: Prevent Switching Loops

Redundant links can create loops.

### Symptoms of loops:

- Broadcast storms  
- MAC address instability  
- Severe network slowdown  

### Solution

- Enable **RSTP (Rapid Spanning Tree Protocol)**  
- Set core switch as **root bridge**  

RSTP blocks unnecessary paths while keeping backups ready.

---

## Step 6: Implement Layer 3 Switching

Instead of relying on a router:

- Use Layer 3 switches for **inter-VLAN routing**

### Benefits:

- Faster internal traffic flow  
- Reduced latency  
- Scalable design  

---

## Step 7: Redesign Wireless Network

The original wireless setup caused dead zones and poor performance.


### Deploy Enterprise Access Points

Use enterprise-grade APs (not consumer routers), such as:

- [Cisco Systems](https://www.britannica.com/money/Cisco-Systems-Inc)
- [Ubiquiti Inc.](https://ui.com/) 
- [Aruba Networks](https://mobilesecurity.com.pa/aruba-networks/?utm_source=chatgpt.com)  

Install APs in:

- Conference rooms  
- Hallways  
- Common areas  

### Conduct a Wireless Site Survey

Identify:

- Dead zones  
- Interference  
- Coverage gaps  

### Use Modern Wireless Standards

Deploy:

- [Wi-Fi6](https://www.wlink-tech.com/art/wi-fi-6-introduction)

Benefits:

- Supports high device density  
- Better performance in crowded areas  
- Improved roaming  

---

## Step 8: Secure Wireless Networks

### Corporate Wi-Fi

- SSID: **Company-Internal**  
- Security:
  - [Wi-Fi Alliance WPA3 Overview](https://www.wi-fi.org/discover-wi-fi/security)
  - [WPA3 Enterprise Explained (Cisco)](https://www.cisco.com/c/en/us/products/wireless/what-is-wpa3.html)

- Authentication:
  - RADIUS server  
  - Unique credentials  

###  Guest Wi-Fi

- SSID: **Company-Guest**  
- VLAN: 70  
- Restrictions:
  - Internet-only access  
  - No internal network access  

Optional:

  - [What is a Captive Portal](https://www.cisco.com/c/en/us/products/wireless/what-is-a-captive-portal.html)
  - [Guest and Public Networks](https://www.wi-fi.org/discover-wi-fi/guest-and-public-networks)

###  Wireless Roaming

- Wireless LAN Controller (WLC)

  - [What is a Wireless LAN Controller](https://www.cisco.com/c/en/us/products/wireless/what-is-a-wireless-lan-controller.html)
  - [Aruba Networks FAQ: What is a Wireless LAN Controller](https://www.arubanetworks.com/faq/what-is-a-wireless-lan-controller/)

Benefits:

- Seamless roaming between buildings  
- Centralized configuration  
- Consistent security policies  

---

## Step 9: Security Hardening

To strengthen the network:

- Enable:
  - [Cisco Port Security](https://www.cisco.com/c/en/us/support/docs/lan-switching/port-security/10588-74.html)  
- Disable unused ports  
- Monitor network activity using:
  - [SNMP (Simple Network Management Protocol](https://www.cisco.com/c/en/us/products/ios-nx-os-software/simple-network-management-protocol-snmp/index.html)
  
---

## Step 10: Validation & Testing

After implementation:

- Test failover (disconnect links)  
- Verify VLAN isolation  
- Confirm guest network restrictions  
- Test wireless roaming between buildings  
- Measure performance improvements  

## Key Takeaways

This redesign demonstrates:

- Proper VLAN segmentation improves performance and security  
- Redundancy ensures high availability  
- RSTP prevents network loops  
- Layer 3 switching improves efficiency  
- Enterprise wireless design ensures reliability and coverage  

## Final Thoughts

This project reflects how real-world networks are designed:

- Structured  
- Scalable  
- Secure  
- Fault-tolerant  

These principles are foundational not only for networking, but also for **cybersecurity**, where segmentation, monitoring, and control are critical.


## Quick Reference

- VLANs → Network segmentation  
- Trunking → VLAN transport  
- RSTP → Loop prevention  
- LACP → Redundancy + bandwidth  
- WPA3 → Wireless security  
- SNMP → Monitoring  


---

## 🔗 Navigation

* **[HOME](/)**
* [Network+ Portfolio](/portfolio/)
  * [Formative Modules](/portfolio/formative-modules/)
  * [Lab Walkthroughs](/portfolio/labs/)
  * [Study Diagrams](/portfolio/study-diagrams/)
* [zBible Study](/zBible-Study/)

---