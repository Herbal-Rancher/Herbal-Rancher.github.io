---
layout: post
title: "Lab 45| Cisco Networking Labs - Observe Web Request"
lab_title: "Observe Web Request"

lesson: "18.0"
lesson_id: "18.45.00"
sort_order: "184500"

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
  - web-traffic
  - http
  - tcp
  - dns
  - html
  - simulation-mode

topics:
  - web-request-traffic
  - http-over-tcp
  - html-server-content

tools:
  - cisco-packet-tracer
  - ping
  - web-browser
  - complex-pdu

protocols:
  - DNS
  - HTTP
  - TCP
  - ICMP
  - IPv4

status: documentation-in-progress

video_id: ""
video_url: ""
thumbnail: ""

completed_lab: ""
lab_pdf: ""
permalink: /network-portfolio/videos/18-45-observe-web-request/
diagram: ""
---

## Overview

Explore the network exchanges behind a web page request. Verify hostname resolution and connectivity, compare server-side HTML with the client browser display, and use a Complex PDU to observe HTTP traffic over TCP.

<!--more-->

---

## Preconditions

![Packet Tracer Lab 45 topology](/assets/images/packet-tracer/cisco-lab-topology-module-18-lab-45.png)

---

## Skills Practiced

- Check DNS resolution and reachability using ping
- Compare an HTTP server HTML file with the browser rendering
- Create a Complex PDU for HTTP traffic
- Observe TCP connection setup and acknowledgements during web communication

---

## Completed Lab Documentation

{% if page.completed_lab != "" %}
- Note: [Completed Lab PDF may be available upon request]
{% endif %}

---

## Key Observations

The browser display comes from content hosted by the server, while TCP exchanges support the underlying HTTP transfer. PDU inspection reveals more network events than the single user action of opening a page.

### Activity Focus

1. Ping `ciscolearn.web.com` and note the resolved server address.
2. Open the site in the simulated client browser.
3. Compare the displayed page with the server’s `index.html`.
4. Create a periodic HTTP Complex PDU and inspect the TCP/HTTP event sequence.

### Notes

This lab is currently in progress. Observations above describe the concepts and intended investigation, not verified completion results. Add screenshots, your own findings, and any corrections after finishing the activity.

---

## Validation

Verify hostname resolution, browser access, HTML correspondence, and the HTTP/TCP events produced by the Complex PDU.

---

## Related Exercises

- HTTP over TCP
- DNS name resolution
- Web server fundamentals

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
