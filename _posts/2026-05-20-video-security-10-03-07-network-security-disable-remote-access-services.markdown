---
layout: post
title: "Security | Identifying and Disabling Remote Access Services"
lab_title: "Identifying and Disabling Remote Access Services"

lesson: "4.0"
lesson_id: "10.03.07"

sort_order: "100307"

categories: [portfolio, videos]

category: security
category_display: Security

subcategory: attack-surface-reduction
subcategory_display: Attack Surface Reduction

content_type: video
content_type_display: Video

tags:

- security-hardening
- remote-desktop
- vnc
- service-discovery
- zenmap
- network-security

topics:

- attack-surface-reduction
- service-enumeration
- network-reconnaissance
- remote-access-security
- security-hardening
- network-security

tools:

- Zenmap
- Nmap
- Windows-Services
- Windows

protocols:

- RDP
- VNC
- TCP

permalink: /portfolio/videos/network-security-disable-remote-access-services/

status: complete

video_id: "UzRt0Xdv8vE"
video_url: "https://youtu.be/UzRt0Xdv8vE"
thumbnail: "https://img.youtube.com/vi/UzRt0Xdv8vE/hqdefault.jpg"

date: 2026-06-19 13:00:00 -0700
last_updated: 2026-06-19 13:00:00 -0700

---

## Overview

This walkthrough demonstrates how network administrators and security professionals can identify remote access services running on networked systems and reduce unnecessary exposure by disabling services that are no longer required.

<!--more-->

Understanding how to discover and manage remote access services is an important part of network security and attack surface management.

---

## Concepts Explored

* Network Reconnaissance
* Service Enumeration
* Remote Access Technologies
* Attack Surface Reduction
* Security Hardening
* Network Administration

---

## Technologies Discussed

### Remote Desktop Protocol (RDP)

RDP provides remote graphical access to Windows systems and commonly uses:

* TCP Port 3389

### Virtual Network Computing (VNC)

VNC provides remote desktop access across multiple operating systems and commonly uses:

* TCP Port 5900

---

## Tools Used

### Zenmap

Zenmap provides a graphical interface for Nmap and can be used to:

* Discover devices
* Identify open ports
* Enumerate services
* Perform network reconnaissance

### Nmap

Nmap is widely used for:

* Host discovery
* Port scanning
* Service identification
* Security assessments

---

## Skills Practiced

* Service Discovery
* Network Enumeration
* Security Assessment
* Security Hardening
* Attack Surface Analysis
* Systems Administration

---

## Why This Matters

Unused remote access services increase the attack surface of a network. Regularly reviewing active services helps administrators:

* Reduce unnecessary exposure
* Improve system security
* Meet security compliance requirements
* Identify unauthorized software
* Strengthen network defenses

Security is often improved not by adding more software, but by removing unnecessary services that are not actively required.

---

## Video Walkthrough

<a href="{{ page.video_url }}" target="_blank" rel="noopener noreferrer">
  <img src="{{ page.thumbnail }}"
       alt="{{ page.title }}"
       style="width:420px; border-radius:8px;">
</a>

---

## Key Takeaway

Effective security begins with visibility. Understanding which services are running, which ports are exposed, and which remote access technologies are active helps administrators reduce risk and maintain a stronger security posture.

---
---
---

## 🔗 Navigation

* [Home](/)
* [Network+ Portfolio](/network-portfolio/)
  * [Formative Modules](/network-portfolio/formative-modules/)
  * **[VIDEO WALKTHROUGHS](/network-portfolio/videos/)**
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* [Bible Study](/network-portfolio/Bible-Study/)
* [Behind the Portfolio](/network-portfolio/behind-the-portfolio/)

---
---
---