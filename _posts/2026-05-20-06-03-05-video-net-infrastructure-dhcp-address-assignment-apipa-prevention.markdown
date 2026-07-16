---
layout: post
title: "Network Fundamentals | DHCP Address Assignment and APIPA Prevention"
lab_title: "DHCP Address Assignment and APIPA Prevention"

lesson: "4.0"
lesson_id: "06.03.05"
sort_order: "060305"

categories: [portfolio, videos]

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: dhcp-networking
subcategory_display: DHCP Networking

content_type: video
content_type_display: Video

tags:
- dhcp
- apipa
- ipv4
- switch
- router
- connectivity

topics:
- dhcp-addressing
- apipa-prevention
- soho-networking
- connectivity-testing
- network-modeling

tools:
- Network Modeler
- Router
- Switch
- Ipconfig
- Ping

protocols:
- IPv4
- DHCP
- ICMP
- TCP-IP

permalink: /network-portfolio/videos/dhcp-address-assignment-apipa-prevention/

status: complete

video_id: "uIPwr-4YvH4"
video_url: "https://youtu.be/uIPwr-4YvH4"
thumbnail: "https://img.youtube.com/vi/uIPwr-4YvH4/hqdefault.jpg"
---

## Overview

This walkthrough demonstrates how DHCP automatically assigns IP addresses within a small office network and prevents devices from relying on APIPA self-assigned addressing.

<!--more-->

The exercise focuses on building network connectivity, validating address assignments, renewing DHCP leases, and verifying communication between devices.

---

## Network Reference

Lab precondition and network topology image used during the exercise.

![Lab Precondition](/assets/images/labs/explore-apipa-addressing-in-network-modeler-2.png)

![APIPA Lab Network Modeler](/assets/images/labs/explore-apipa-addressing-in-network-modeler.png)

---

## Step 1: Build the Local Network

Add the required network devices:

* Workstations
* Switch
* Router

Establish the necessary physical connections between devices.

---

## Step 2: Verify Initial Addressing

On a workstation, review the current IP configuration.

```powershell
ipconfig /all
```

Record:

* IPv4 address
* Subnet mask
* Default gateway
* DHCP status

---

## Step 3: Test Local Connectivity

Verify communication between workstations.

```powershell
ping <workstation-ip>
```

Document successful and failed connectivity attempts.

---

## Step 4: Connect the Router

Connect the switch to the router and verify physical connectivity.

The router will provide gateway services and DHCP address assignment for the network.

---

## Step 5: Renew the DHCP Lease

Request a new IP configuration.

```powershell
ipconfig /renew
```

Review the updated network settings.

```powershell
ipconfig /all
```

Confirm:

* Valid IPv4 address
* DHCP-assigned configuration
* Default gateway assignment

---

## Step 6: Verify Network Connectivity

Test communication with:

```powershell
ping <workstation-ip>
```

```powershell
ping <gateway-ip>
```

Confirm successful communication between hosts and the gateway.

---

## Step 7: Validate DHCP Operation

Verify that all connected devices receive valid network configurations and can communicate successfully across the network.

---

## Skills Practiced

* DHCP Address Assignment
* APIPA Recognition
* Network Modeling
* Switch Connectivity
* Router Deployment
* Connectivity Testing
* IPv4 Configuration Analysis
* Technical Documentation

---

## Video Walkthrough

<a href="{{ page.video_url }}" target="_blank" rel="noopener noreferrer">
  <img src="{{ page.thumbnail }}"
       alt="{{ page.title }}"
       style="width:420px; border-radius:8px;">
</a>

---

## Key Takeaways

DHCP simplifies network administration by automatically providing valid IP configurations to connected devices. When DHCP services are available, devices receive proper network settings and can communicate successfully with other hosts and network resources.

---
---
---

## 🔗 Navigation

* [Home](/)
* [Network+ Portfolio](/network-portfolio/)
  * [Formative Modules](/network-portfolio/formative-modules/)
  * **[VIDEO WALKTHROUGHS](/network-portfolio/videos/)**
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* [Trading+](/trading/)
* [Bible Study](/bible-study/)
* [About the Portfolio](/about/)

---
---
---