---
layout: post
title: "Security Fundamentals | Scan for Unsecure Protocols and Services with WHOIS, NSLookup & Zenmap"
lab_title: "Scan for Unsecure Protocols and Services with WHOIS, NSLookup & Zenmap"

lesson: "4.0"
lesson_id: "10.03.05"

sort_order: "100305"

categories: [portfolio, videos, walkthroughs]

category: security
category_display: Security

subcategory: reconnaissance
subcategory_display: Reconnaissance

content_type: video
content_type_display: Video

tags:
- network-reconnaissance
- dns-lookup
- nslookup
- whois
- zenmap
- port-scanning
- service-enumeration
- network-security

topics:
- reconnaissance
- dns-analysis
- port-discovery
- service-enumeration
- security-assessment
- attack-surface-awareness

tools:
- WHOIS
- NSLookup
- Zenmap
- Terminal

protocols:
- DNS
- TCP
- IP

permalink: /portfolio/videos/scan-for-unsecure-protocols-and-services/

status: complete

video_id: "-fv2BTjw5pA"
video_url: "https://www.youtube.com/watch?v=-fv2BTjw5pA"
thumbnail: "https://img.youtube.com/vi/-fv2BTjw5pA/hqdefault.jpg"

---

## Overview

This walkthrough documents a network reconnaissance exercise focused on gathering publicly available domain information, resolving a web server address, and identifying potentially insecure services through port scanning.

<!--more-->

The purpose of this exercise is to practice safe, authorized reconnaissance techniques used by network administrators and security analysts when reviewing exposed services and external infrastructure.

---
---

## Video Walkthrough

<a href="{{ page.video_url }}" target="_blank" rel="noopener noreferrer">
  <img src="{{ page.thumbnail }}"
       alt="{{ page.title }}"
       style="width: 420px; border-radius: 8px;">
</a>

---

## Scenario Summary

A security review is being performed against an authorized external web server target.

Target domain:

* [www.partnercorp.xyz](http://www.partnercorp.xyz)

The objective is to identify DNS information, determine the primary web server address, and scan for commonly exposed ports that may require further security review.

---

## Steps Performed

### 1. Identify Domain Name Server Information

Use a WHOIS lookup service to review public registration and DNS information for the target domain.

Information to collect:

* Domain name server records
* Public DNS registration details
* External infrastructure clues

Tool used:

* WHOIS

---

### 2. Resolve the Primary Web Server Address

Use `nslookup` to identify the IP address associated with the target web server.

Target:

* [www.partnercorp.xyz](http://www.partnercorp.xyz)

Tool used:

* NSLookup

Purpose:

* Confirm DNS resolution
* Identify the web server address
* Prepare the target network information for scanning

---

### 3. Scan for Commonly Exposed Ports

Use Zenmap to scan the network associated with the resolved web server address.

Scan focus:

* Top 50 commonly used ports
* Open services
* Potentially insecure protocols
* Exposed network services

Tool used:

* Zenmap

Purpose:

* Identify accessible services
* Review exposed ports
* Support security assessment and attack surface awareness

---

## Skills Practiced

* WHOIS Research
* DNS Investigation
* NSLookup Usage
* Port Scanning
* Service Enumeration
* Reconnaissance Methodology
* Security Assessment
* Network Documentation

---

## Key Takeaways

Reconnaissance helps security professionals understand what information and services are publicly visible.

By combining WHOIS research, DNS lookups, and port scanning, a technician can identify exposed services, validate DNS information, and recognize systems that may need additional hardening or review.

This exercise reinforces the importance of understanding an organization's external attack surface before deeper security analysis begins.

---

## Related Study Areas

* DNS Resolution
* Network Reconnaissance
* Port Scanning
* Service Enumeration
* Network Security
* Zenmap
* Nmap
* Attack Surface Awareness


---
---
---

## 🔗 Navigation

* [Home](/)
* [Network+ Portfolio](/network-portfolio/)
  * [Formative Lessons](/network-portfolio/formative-lessons/)
  * **[VIDEO WALKTHROUGHS](/network-portfolio/videos/)**
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* [Bible Study](/network-portfolio/Bible-Study/)
* [Behind the Portfolio](/network-portfolio/behind-the-portfolio/)

---
---
---