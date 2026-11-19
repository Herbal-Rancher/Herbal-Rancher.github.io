---
layout: post
title: "Lab 36 | Cisco Networking Labs - Use ICMP to Test and Correct Network Connectivity"
lab_title: "Use ICMP to Test and Correct Network Connectivity"

lesson: "17.0"
lesson_id: "17.36.00"
sort_order: "173600"

categories:
  - portfolio
  - labs

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: troubleshooting
subcategory_display: Network Troubleshooting

content_type: lab
content_type_display: Lab Documentation

tags:
  - packet-tracer
  - icmp
  - troubleshooting
  - ipv4
  - ipv6
  - connectivity

topics:
  - connectivity-testing
  - fault-isolation
  - configuration-repair

tools:
  - cisco-packet-tracer
  - ping
  - traceroute

protocols:
  - IPv4
  - IPv6
  - ICMP
  - ICMPv6

status: complete

video_id: ""
video_url: ""
thumbnail: ""

completed_lab: "/assets/pdfs/module-17-lab-36-Packet-Tracer-Use-ICMP-to-Test-Connectivity.pdf"
lab_pdf: "/assets/pdfs/module-17-lab-36-Packet-Tracer-Use-ICMP-to-Test-Connectivity.pdf"
permalink: /network-portfolio/videos/17-36-use-icmp-to-test-and-correct-connectivity/
diagram: ""
---

## Overview

Investigate a multi-router network in which users cannot reach some resources. Use ICMP tests and route tracing to identify where communication fails, then correct configuration issues and retest IPv4 and IPv6 connectivity.

<!--more-->

---

## Preconditions

![Packet Tracer Lab 36 - Use ICMP to Test and Correct Connectivity - Preconditions](/assets/images/packet-tracer/cisco-lab-topology-Module-17-Lab-36.png)

---

## Skills Practiced

- Build a systematic connectivity test plan
- Use echo requests and trace results to isolate faults
- Verify communication among clients and the Corporate Server

---

## Video Walkthrough

This lab is documented as a written exercise; no video walkthrough is planned.

{% if page.video_id != "" %}
<iframe width="560" height="315" src="https://www.youtube.com/embed/{{ page.video_id }}" title="{{ page.title }}" frameborder="0" allowfullscreen></iframe>
{% endif %}

---

## Completed Lab Documentation

- Note: [Completed Lab PDF may be available upon request]

---

## Key Observations

A failed ping identifies a reachability symptom but not necessarily the root cause. Comparing results from multiple source devices and tracing the route helps narrow the fault domain.

### Activity Focus

1. Inspect the provided router, host, and server addressing information.
2. Test local and remote reachability using ICMP.
3. Use trace output to locate failing paths, correct faults, and repeat tests.

### Notes

The worksheet includes IPv4 and IPv6 addressing and specifies that hosts should reach other hosts and the Corporate Server.

---

## Validation

Retest affected hosts and confirm end-to-end communication after changes.


---
---
---

## 🔗 Navigation

* [Home](/)
* [Network+ Portfolio](/network-portfolio/)
  * **[FORMATIVE MODULES](/network-portfolio/formative-modules/)**
  * [Video Walkthroughs](/network-portfolio/videos/)
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* [Trading+](/trading/)
* [Bible Study](/bible-study/)
* [About the Portfolio](/about/)

---
---
---
