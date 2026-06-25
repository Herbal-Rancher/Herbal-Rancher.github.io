---
layout: post
title: "Network Troubleshooting | Diagnosing and Resolving APIPA Addressing Issues"
lab_title: "Diagnosing and Resolving APIPA Addressing Issues"

lesson: "4.0"
lesson_id: "06.03.04"
sort_order: "060304"

categories: [portfolio, videos]

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: dhcp-troubleshooting
subcategory_display: DHCP Troubleshooting

content_type: video
content_type_display: Video

tags:
- dhcp
- apipa
- troubleshooting
- ipconfig
- ping
- ipv4

topics:
- dhcp-troubleshooting
- apipa-addressing
- connectivity-testing
- tcp-ip-analysis
- network-diagnostics

tools:
- Ipconfig
- Ping
- Windows Networking
- DHCP Console

protocols:
- IPv4
- DHCP
- ICMP
- TCP-IP

permalink: /network-portfolio/videos/apipa-dhcp-troubleshooting/

status: complete

video_id: "REPLACE_WITH_YOUTUBE_ID"
video_url: "REPLACE_WITH_YOUTUBE_URL"
thumbnail: "https://img.youtube.com/vi/REPLACE_WITH_YOUTUBE_ID/hqdefault.jpg"
---

## Overview

This walkthrough demonstrates how to identify and resolve a DHCP-related connectivity issue caused by Automatic Private IP Addressing (APIPA).

<!--more-->

The objective is to determine why a workstation cannot obtain a valid network address, restore DHCP functionality, and verify successful communication throughout the network.

---

## Network Reference

Add the topology diagram used during the exercise.

```markdown
![APIPA Troubleshooting Diagram](/assets/images/apipa-troubleshooting-diagram.png)
```

---

## Step 1: Review IP Configuration

On each workstation, examine the current TCP/IP settings.

```powershell
ipconfig
```

Record:

* IPv4 address
* Subnet mask
* Default gateway

Look for signs of invalid or self-assigned addressing.

---

## Step 2: Test Connectivity

Verify communication with network resources.

```powershell
ping <default-gateway>
```

```powershell
ping <workstation-ip>
```

Document:

* Successful communication
* Failed communication
* Reachable devices
* Unreachable devices

---

## Step 3: Compare Results Across Systems

Review configuration information from multiple workstations.

Compare:

* IPv4 addresses
* Gateway assignments
* Connectivity results

Identify any system that differs from the others.

---

## Step 4: Identify the Cause

Review the collected evidence.

Indicators of a DHCP-related issue may include:

* Self-assigned addresses
* Missing network configuration
* Inability to reach the gateway
* Inability to communicate with other devices

---

## Step 5: Restore Address Assignment Services

Verify that DHCP services are available and operational.

Activate or restore address assignment services as required.

---

## Step 6: Renew and Verify Configuration

Recheck the workstation configuration.

```powershell
ipconfig
```

Confirm:

* Valid IPv4 address
* Correct subnet
* Proper gateway assignment

---

## Step 7: Verify Connectivity

Repeat connectivity tests.

```powershell
ping <default-gateway>
```

```powershell
ping <workstation-ip>
```

Confirm successful communication.

---

## Skills Practiced

* DHCP Troubleshooting
* APIPA Identification
* IPv4 Address Analysis
* Connectivity Testing
* Root Cause Analysis
* Problem Resolution
* Network Diagnostics
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

When a workstation cannot obtain an address from a DHCP server, Windows may automatically assign an APIPA address. Identifying the symptoms, restoring DHCP services, and verifying proper address assignment are essential skills for diagnosing and resolving network connectivity issues.


---
---
---

## 🔗 Navigation

* [Home](/)
* [Network+ Portfolio](/network-portfolio/)
  * [Formative Modules](/network-portfolio/formative-modules/)
  * **[VIDEO WALKTHROUGHS](/network-portfolio/videos/)**
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* [Bible Study](/bible-study/)
* [Behind the Portfolio](/network-portfolio/behind-the-portfolio/)

---
---
---