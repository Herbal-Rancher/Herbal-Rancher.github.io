---

layout: post
title: "Lab 19| Cisco Networking Labs - Examine NAT on a Wireless Router"
lab_title: "Examine NAT on a Wireless Router"

lesson: "14.0"
lesson_id: "14.19.00"
sort_order: "141900"

categories:
  - portfolio
  - labs
  - videos

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: network-services
subcategory_display: Network Services

content_type: video
content_type_display: Video

tags:
  - packet-tracer
  - nat
  - dhcp
  - wireless-router
  - private-ip
  - public-ip
  - packet-analysis
  - simulation-mode

topics:
  - network-address-translation
  - private-public-addressing
  - dhcp
  - nat-translation
  - packet-headers
  - traffic-analysis
  - connectivity-testing

tools:
  - cisco-packet-tracer
  - wireless-router
  - simulation-mode
  - complex-pdu
  - ipconfig

protocols:
  - NAT
  - DHCP
  - IPv4
  - TCP
  - HTTP

permalink: /network-portfolio/videos/13-19-examine-nat-on-wireless-router/

status: complete

video_id: "zwGWxiwK79o"
video_url: "https://youtu.be/zwGWxiwK79o"
thumbnail: "https://img.youtube.com/vi/zwGWxiwK79o/hqdefault.jpg"

completed_lab: "/assets/pdfs/Module-13-Lab-19-Packet-Tracer-Explore-NAT-on-wireless-router.pdf"
lab_pdf: "/assets/pdfs/Module-13-Lab-19-Packet-Tracer-Explore-NAT-on-wireless-router.pdf"

diagram: ""
---

## Overview

This Packet Tracer lab examines **Network Address Translation (NAT)** on a wireless router. I configured four PCs to receive private IPv4 addresses through DHCP, examined the router's internal and Internet addressing, and used Simulation mode to observe how NAT translates traffic as it crosses between the private network and an external web server.

<!--more-->

---

## Preconditions

![Packet Tracer Lab 19 - Examine NAT on a Wireless Router - Preconditions]({{ '/assets/images/packet-tracer/cisco-lab-topology-module-14-lab-19.png' | relative_url }})

---

## Skills Practiced

* Examine NAT on a Wireless Router (Packet Tracer Lab 19)
* Configure clients to obtain IPv4 addressing through DHCP
* Identify private and public IP addressing
* Examine internal and external router addressing
* Create and analyze a Complex PDU
* Filter and observe TCP and HTTP traffic
* Examine inbound and outbound packet headers
* Identify source IP address translation through NAT

---

## Key Observations

The wireless router connects two different addressing environments:

* **Internal network:** PCs receive private IPv4 addresses through DHCP.
* **External network:** The router uses its Internet-facing address to communicate outside the private network.
* **NAT:** Translates the private source address as traffic crosses the wireless router.

Using Packet Tracer Simulation mode, I compared the **Inbound PDU** and **Outbound PDU** header information and observed the change in the source IP address as NAT occurred.

---

## Validation

I verified client addressing with `ipconfig /all` and used a periodic HTTP Complex PDU to `ciscolearn.nat.com` to observe TCP/HTTP traffic crossing the wireless router.

Packet header inspection confirmed the NAT translation between the internal and external networks.

---

## Video

{% if page.video and page.video != "" %}

<div class="video-container">
  <iframe
    src="{{ page.video }}"
    title="{{ page.lab_title }}"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
  </iframe>
</div>
{% else %}
*Video coming soon.*
{% endif %}

---

## Related Exercises

* Packet Tracer Lab 17 — Configure DHCP on a Wireless Router
* Packet Tracer Lab 18 — Configure Basic Wireless Security
* DHCP Client Configuration
* IPv4 Private and Public Addressing
* Network Address Translation
* Packet and Traffic Analysis


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