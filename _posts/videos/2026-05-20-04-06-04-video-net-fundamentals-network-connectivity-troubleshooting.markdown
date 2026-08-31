---
layout: post
title: "Networking Fundamentals | Troubleshooting Network Connectivity with Ping and Tracert"
lab_title: "Troubleshooting Network Connectivity with Ping and Tracert"

lesson: "4.0"
lesson_id: "04.06.04"
sort_order: "040604"

categories: [portfolio, videos]

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: network-troubleshooting
subcategory_display: Network Troubleshooting

content_type: video
content_type_display: Video

tags:

- ping
- tracert
- ipconfig
- troubleshooting
- tcp-ip
- windows-networking

topics:

- network-troubleshooting
- connectivity-testing
- gateway-troubleshooting
- route-analysis
- tcp-ip-configuration

tools:

- Windows
- PowerShell
- Ping
- Tracert
- Ipconfig

protocols:

- IPv4
- ICMP
- TCP-IP

permalink: /network-portfolio/videos/network-connectivity-troubleshooting/

status: complete

video_id: "whVVTtXdvUw"
video_url: "https://youtu.be/whVVTtXdvUw"
thumbnail: "https://img.youtube.com/vi/whVVTtXdvUw/hqdefault.jpg"
---

## Overview

This walkthrough demonstrates the process used to identify a network connectivity issue using IP configuration review, connectivity testing, and route tracing.

<!--more-->

The objective is to determine where communication is failing and identify the network setting that requires correction.

---

## Video Walkthrough

Watch the complete walkthrough:

<a href="{{ page.video_url }}" target="_blank" rel="noopener noreferrer">
  <img src="{{ page.thumbnail }}"
       alt="{{ page.title }}"
       style="width:420px; border-radius:8px;">
</a>

---

## Network Reference

The following devices were available for connectivity testing during this exercise.

![Network Device Reference](/assets/images/labs/464-ping-tracert-commands-image.png)

---

## Step 1: Review the Current Configuration

Open PowerShell and review the workstation's TCP/IP settings.

```powershell
ipconfig
```

Record:

* IPv4 Address
* Subnet Mask
* Default Gateway
* DNS Server Information

---

## Step 2: Test Local Network Connectivity

Verify communication with local network resources.

```powershell
ping 192.168.0.10
```

```powershell
ping 192.168.0.30
```

```powershell
ping 192.168.0.31
```

Document which devices respond successfully.

---

## Step 3: Test Additional Devices

Continue testing communication with the remaining hosts.

```powershell
ping 192.168.0.32
```

```powershell
ping 192.168.0.33
```

```powershell
ping 192.168.0.34
```

Compare successful and failed responses against the network reference table.

---

## Step 4: Analyze Connectivity Results

Review the results from the ping tests.

Determine:

* Which devices are reachable
* Which devices are unreachable
* Whether the issue affects a single host or multiple hosts
* Whether communication remains inside the local network

---

## Step 5: Trace the Communication Path

Use Tracert to determine where communication stops.

```powershell
tracert <destination-ip>
```

Record:

* Successful hops
* Failed hops
* The point where communication is interrupted

---

## Step 6: Identify the Cause

Review:

* IP configuration
* Ping results
* Tracert results

Use the collected evidence to determine the configuration issue responsible for the connectivity failure.

---

## Step 7: Apply the Corrective Action

Update the incorrect network configuration setting identified during troubleshooting.

After making the change, save and apply the configuration.

---

## Step 8: Verify Connectivity

Repeat the previous tests.

```powershell
ipconfig
```

```powershell
ping <destination-ip>
```

```powershell
tracert <destination-ip>
```

Confirm that communication succeeds and the issue has been resolved.

---

## Skills Practiced

* TCP/IP Configuration Review
* Connectivity Testing
* Network Diagnostics
* Ping Analysis
* Route Tracing
* Root Cause Identification
* Troubleshooting Methodology
* Problem Resolution

---

## Key Takeaways

This exercise follows a structured troubleshooting workflow: review the configuration, test connectivity, trace the communication path, identify the cause, apply the fix, and verify successful operation.

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