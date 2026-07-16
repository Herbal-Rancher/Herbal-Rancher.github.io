---
layout: post
title: "Windows Server DNS | Troubleshoot Missing DNS Host Records"
lab_title: "Troubleshoot Missing DNS Host Records"

lesson: "4.0"
lesson_id: "06.05.15"
sort_order: "060515"

categories: [portfolio, videos]

category: windows-server
category_display: Windows Server

subcategory: dns
subcategory_display: Domain Name System (DNS)

content_type: video
content_type_display: Guided Technical Walkthrough

tags:

- dns
- windows-server
- troubleshooting
- host-records
- name-resolution
- ping

topics:

- dns-troubleshooting
- host-records
- forward-lookup-zone
- name-resolution
- windows-server-dns

tools:

- Windows Server
- DNS Manager
- Command Prompt
- Ping

protocols:

- DNS
- ICMP
- IPv4
- TCP-IP

permalink: /network-portfolio/videos/06-05-15-troubleshoot-dns-host-records/

status: complete

video_id: "KDy6Z1iQFBs"
video_url: "https://youtu.be/KDy6Z1iQFBs"
thumbnail: "https://img.youtube.com/vi/KDy6Z1iQFBs/hqdefault.jpg"
---

## Overview

This guided walkthrough demonstrates how to troubleshoot a DNS name resolution problem by comparing hostname connectivity with direct IP connectivity.

<!--more-->

The exercise illustrates how missing DNS records can prevent users from accessing network resources even when the destination server is online.

---

> **Portfolio Note**
>
> This page documents my personal learning journey through networking, systems administration, and cybersecurity. The accompanying walkthrough demonstrates concepts and techniques using a hands-on lab environment for educational purposes.

---

## Preconditions

The DNS infrastructure is already operational.

A server is reachable on the network, but users are unable to access it using its DNS host name.

Use the lab environment or reference image for:

- Host name
- IPv4 address
- DNS zone

![Troubleshoot DNS Host Records image](/assets/images/labs/060515-troubleshoot-dns-host-records.png)

---

## Before You Begin

When troubleshooting DNS, comparing a hostname with its IP address is a simple way to determine whether the issue is related to name resolution or basic network connectivity.

If communication succeeds using the IP address but fails using the hostname, DNS should be tradeigated.

---

## Objectives

In this walkthrough you will:

- Test connectivity using a host name.
- Test connectivity using an IPv4 address.
- Identify a DNS name resolution issue.
- Create the required Host (A) record.
- Verify successful name resolution.

---

## Guided Walkthrough

### Test Connectivity

1. Open a command prompt.
2. Ping the server using its host name.
3. Ping the server using its IPv4 address.
4. Compare the results.

---

### Resolve the DNS Issue

1. Open **DNS Manager**.
2. Navigate to the appropriate forward lookup zone.
3. Create the required Host (A) record.
4. Save the new DNS record.

---

### Verify the Solution

1. Ping the server using its host name.
2. Confirm successful name resolution.
3. Verify connectivity.

---

## Troubleshooting Verification

Verify that:

- The Host (A) record exists.
- The hostname resolves correctly.
- The server responds to ping using both its hostname and IP address.
- Name resolution has been restored.

---

## Skills Practiced

- Windows Server Administration
- DNS Troubleshooting
- Host (A) Records
- Name Resolution
- Ping Testing
- Root Cause Analysis
- Configuration Verification
- Technical Documentation

---

## Related Exercise

Course Module

- 4.0

Original Exercise

- Troubleshoot DNS Records (Lab: 6.5.15)

---

## Why This Matters

One of the fastest ways to diagnose a DNS issue is to compare communication by hostname and by IP address.

If an IP address responds but the hostname does not, the problem often lies within DNS rather than the underlying network.

This troubleshooting technique is frequently used by help desk technicians, systems administrators, and network engineers.

---

## Video Walkthrough

<a href="{{ page.video_url }}" target="_blank" rel="noopener noreferrer">

<img src="{{ page.thumbnail }}"
alt="{{ page.title }}"
style="width:420px; border-radius:8px;">

</a>

---

## Key Takeaways

Successful IP connectivity does not always indicate successful DNS resolution. By comparing hostname and IP communication, administrators can quickly determine whether a problem originates with DNS records or general network connectivity.

---

## DNS Concepts Reinforced

- DNS translates host names into IP addresses.
- Host (A) records provide forward name resolution.
- Ping can help distinguish DNS issues from connectivity issues.
- Successful IP communication with failed hostname resolution often indicates a missing or incorrect DNS record.

---

## Related Resources

Study Diagrams

- DNS Resolution Process
- Host (A) Records
- DNS Troubleshooting Flowchart

Reference Tools

- DNS Manager
- ping
- nslookup
- ipconfig /flushdns

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