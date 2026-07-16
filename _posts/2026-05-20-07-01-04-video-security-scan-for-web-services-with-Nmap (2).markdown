---
layout: post
title: "Linux Administration | Install and Verify the Network Time Protocol (NTP)"
lab_title: "Install and Verify the Network Time Protocol (NTP)"

lesson: "4.0"
lesson_id: "07.01.04"
sort_order: "070104"

categories: [portfolio, videos]

category: linux-administration
category_display: Linux Administration

subcategory: network-services
subcategory_display: Network Services

content_type: video
content_type_display: Guided Technical Walkthrough

tags:

- linux
- ntp
- dnf
- systemctl
- time-synchronization
- network-services

topics:

- network-time-protocol
- linux-services
- package-management
- systemd
- enterprise-linux

tools:

- Linux
- Terminal
- dnf
- systemctl

protocols:

- NTP
- UDP
- IPv4

permalink: /network-portfolio/videos/07-01-04-install-verify-ntp-linux/

status: complete

video_id: "REPLACE_WITH_YOUTUBE_ID"
video_url: "REPLACE_WITH_YOUTUBE_URL"
thumbnail: "https://img.youtube.com/vi/REPLACE_WITH_YOUTUBE_ID/hqdefault.jpg"
---

## Overview

This guided walkthrough demonstrates how to install and verify the Network Time Protocol (NTP) service on a Linux system.

<!--more-->

Accurate system time is essential for authentication, logging, security auditing, scheduling, and communication across enterprise networks.

---

> **Portfolio Note**
>
> This page documents my personal learning journey through networking, Linux administration, and cybersecurity. The accompanying walkthrough demonstrates concepts and techniques using a hands-on lab environment for educational purposes.

---

## Preconditions

The Linux system is already installed and accessible.

You are logged in with administrative privileges.

Use the lab environment or reference image for:

- NTP server information
- Required package
- Verification results

![Configure NTP on Linux env image](/assets/images/labs/070104-configure-ntp-on-linux.png)

---

## Before You Begin

Network Time Protocol (NTP) synchronizes system clocks across networked devices.

Consistent time is critical for:

- Authentication
- Security logs
- Kerberos
- Active Directory
- Scheduled tasks
- Event correlation
- Troubleshooting

---

## Objectives

In this walkthrough you will:

- Install the NTP service.
- Verify the service is running.
- Identify the configured NTP server.
- Confirm successful synchronization.

---

## Guided Walkthrough

### Install the NTP Service

1. Open a terminal.
2. Install the NTP package using the Linux package manager.
3. Allow the installation to complete.

---

### Verify the Service

1. Check the service status.
2. Confirm the service is active.
3. Verify that NTP starts successfully.

---

### Identify the NTP Server

1. Display the configured NTP source.
2. Record the server information.
3. Confirm synchronization.

---

## Verification

Verify that:

- The NTP package installed successfully.
- The NTP service is running.
- The configured NTP server is displayed.
- Time synchronization is operational.

---

## Skills Practiced

- Linux Administration
- Package Management
- Linux Services
- Systemd
- Network Time Protocol (NTP)
- Service Verification
- Enterprise Linux
- Technical Documentation

---

## Related Exercise

Course Module

- 04.0

Original Exercise

- Configure NTP on Linux (Lab: 7.1.4)

---

## Why This Matters

Accurate system time is fundamental to nearly every enterprise network.

Authentication systems, log analysis, certificate validation, scheduled tasks, monitoring platforms, and cybersecurity tradeigations all rely on synchronized clocks.

Understanding NTP is an essential skill for Linux administrators, network engineers, and cybersecurity professionals.

---

## Video Walkthrough

<a href="{{ page.video_url }}" target="_blank" rel="noopener noreferrer">

<img src="{{ page.thumbnail }}"
alt="{{ page.title }}"
style="width:420px; border-radius:8px;">

</a>

---

## Key Takeaways

Network Time Protocol keeps systems synchronized by obtaining time from trusted sources. Maintaining accurate time improves reliability, simplifies troubleshooting, and supports secure enterprise environments.

---

## NTP Concepts Reinforced

- NTP synchronizes clocks across network devices.
- Accurate time is essential for authentication and logging.
- Linux services are commonly managed using systemctl.
- Package managers simplify software installation.

---

## Related Resources

Study Diagrams

- NTP Architecture
- Linux Service Management
- Client-Server Communication

Reference Commands

- dnf
- systemctl
- timedatectl
- chronyc


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