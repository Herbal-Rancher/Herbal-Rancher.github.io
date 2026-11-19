---
layout: post
title: "Lab 44| Cisco Networking Labs - The Client Interaction"
lab_title: "The Client Interaction"

lesson: "18.0"
lesson_id: "18.44.00"
sort_order: "184400"

categories:
  - portfolio
  - labs

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: ip-addressing
subcategory_display: IP Addressing

content_type: lab
content_type_display: Lab Documentation

tags:
  - packet-tracer
  - client-server
  - dns
  - http
  - pdu
  - osi-model

topics:
  - dns-name-resolution
  - http-request-response
  - client-server-workflow

tools:
  - cisco-packet-tracer
  - web-browser
  - simulation-mode

protocols:
  - DNS
  - HTTP
  - TCP
  - IPv4

status: documentation-in-progress

video_id: ""
video_url: ""
thumbnail: ""

completed_lab: ""
lab_pdf: ""
permalink: /network-portfolio/videos/18-44-the-client-interaction/
diagram: ""
---

## Overview

Follow a web request from a simulated PC to a server that provides DNS and HTTP services. Observe how the client resolves a hostname, requests a web page, receives the response, and acknowledges the transferred data.

<!--more-->

---

## Preconditions

![Packet Tracer Lab 44 topology](/assets/images/packet-tracer/cisco-lab-topology-module-18-lab-44.png)

---

## Skills Practiced

- Trace the sequence of DNS and HTTP events
- Interpret client/server interactions in Simulation Mode
- Use PDU Information to inspect OSI-layer processing
- Relate hostname resolution to subsequent web traffic

---

## Completed Lab Documentation

{% if page.completed_lab != "" %}
- Note: [Completed Lab PDF may be available upon request]
{% endif %}

---

## Key Observations

A web request by hostname depends on name resolution before the client can communicate with the server by IP address. Simulation Mode makes these separate application steps visible.

### Activity Focus

1. Enable Simulation Mode and filter DNS and HTTP events.
2. Request `www.example.com` from the simulated client browser.
3. Follow the name-resolution and page-delivery event sequence.
4. Inspect individual PDU information windows and their OSI-layer descriptions.

### Notes

This lab is currently in progress. Observations above describe the concepts and intended investigation, not verified completion results. Add screenshots, your own findings, and any corrections after finishing the activity.

---

## Validation

Confirm the requested web page appears and inspect the DNS and HTTP events that lead to the response.

---

## Related Exercises

- DNS fundamentals
- HTTP client/server model
- OSI encapsulation

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
