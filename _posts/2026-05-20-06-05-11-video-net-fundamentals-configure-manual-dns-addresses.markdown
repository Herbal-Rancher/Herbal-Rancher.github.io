---
layout: post
title: "Windows Networking | Configure Manual DNS Server Addresses"
lab_title: "Configure Manual DNS Server Addresses"

lesson: "4.0"
lesson_id: "06.05.11"
sort_order: "060511"

categories: [portfolio, videos]

category: windows-networking
category_display: Windows Networking

subcategory: dns
subcategory_display: Domain Name System (DNS)

content_type: video
content_type_display: Guided Technical Walkthrough

tags:

- dns
- windows
- ipv4
- dhcp
- networking
- name-resolution

topics:

- dns-configuration
- windows-networking
- ipv4
- dhcp-client
- network-adapters

tools:

- Windows
- Network Connections
- Ethernet Adapter
- IPv4 Properties

protocols:

- IPv4
- DNS
- DHCP
- TCP-IP

permalink: /network-portfolio/videos/06-05-11-configure-manual-dns-addresses/

status: complete

video_id: "REPLACE_WITH_YOUTUBE_ID"
video_url: "REPLACE_WITH_YOUTUBE_URL"
thumbnail: "https://img.youtube.com/vi/REPLACE_WITH_YOUTUBE_ID/hqdefault.jpg"
---

## Overview

This walkthrough demonstrates how to manually configure DNS server addresses on a Windows computer while continuing to receive its IP address automatically from a DHCP server.

<!--more-->

---

> **Portfolio Note**
>
> This page documents my personal learning journey through networking, systems administration, and cybersecurity. The accompanying walkthrough demonstrates concepts and techniques using a hands-on lab environment for educational purposes.

---

## Preconditions

The computer is already connected to a functioning Ethernet network.

Use the lab instructions or environment image to reference the required DNS server addresses before beginning.

![Configure DNS Addresses](/assets/images/labs/060511-Configure-DNS-Addresses.png)

---

## Before You Begin

DNS (Domain Name System) translates domain names into IP addresses.

Although most computers receive DNS server addresses automatically from DHCP, administrators sometimes configure manual DNS servers for troubleshooting, testing, filtering, or performance improvements.

---

## Objectives

In this walkthrough you will:

- Open the Ethernet adapter properties.
- Configure manual IPv4 DNS server addresses.
- Save the new configuration.
- Verify the updated settings.

---

## Step-by-Step Walkthrough

1. Open **Network Connections**.
2. Open the **Ethernet Adapter Properties**.
3. Select **Internet Protocol Version 4 (TCP/IPv4)**.
4. Open **Properties**.
5. Select **Use the following DNS server addresses**.
6. Enter the preferred DNS server.
7. Enter the alternate DNS server.
8. Save the configuration.
9. Verify the updated DNS settings.

---

## Verification

Verify that:

- The preferred DNS server is configured correctly.
- The alternate DNS server is configured correctly.
- Network connectivity remains operational.
- DNS name resolution functions as expected.

---

## Skills Practiced

- Windows Networking
- DNS Configuration
- IPv4 Configuration
- DHCP Client Configuration
- Network Adapter Configuration
- Configuration Verification
- Technical Documentation

---

## Related Exercise

Course Module

- 4.0

Original Exercise

- Configure DNS Addresses (Lab: 6.5.11)

---

## Why This Matters

Manual DNS configuration is commonly used when troubleshooting name resolution issues, testing alternate DNS providers, implementing content filtering, or configuring enterprise networks.

Understanding how to override DHCP-provided DNS settings is an essential networking skill.

---

## Video Walkthrough

<a href="{{ page.video_url }}" target="_blank" rel="noopener noreferrer">

<img src="{{ page.thumbnail }}"
alt="{{ page.title }}"
style="width:420px; border-radius:8px;">

</a>

---

## Key Takeaways

Windows allows DNS servers to be configured independently from DHCP-assigned IP addresses. Knowing when and how to configure manual DNS settings is a valuable skill for troubleshooting and network administration.

---

## Related Resources

Study Diagrams

- DNS Resolution Process
- IPv4 Addressing

Reference Commands

- ipconfig /all
- ipconfig /flushdns
- nslookup
- ping


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
* [About the Portfolio](/zabout-the-portfolio/)

---
---
---