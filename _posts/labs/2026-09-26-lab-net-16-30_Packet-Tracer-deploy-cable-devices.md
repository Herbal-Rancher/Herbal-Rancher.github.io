---
layout: post
title: "Lab 30| Cisco Networking Labs - Deploy and Cable Devices"
lab_title: "Deploy and Cable Devices"

lesson: "16.0"
lesson_id: "16.30.00"
sort_order: "163000"

categories:
  - portfolio
  - videos

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: network-infrastructure
subcategory_display: Network Infrastructure

content_type: video
content_type_display: Video

tags:
  - packet-tracer
  - cabling
  - switches
  - physical-topology

topics:
  - device-deployment
  - copper-cabling
  - interface-selection

tools:
  - cisco-packet-tracer
  - copper-straight-through
  - copper-crossover

status: complete

video_id: "zwGWxiwK79o"
video_url: "https://www.youtube.com/watch?v=zwGWxiwK79o"
thumbnail: "https://img.youtube.com/vi/zwGWxiwK79o/hqdefault.jpg"

completed_lab: "/assets/pdfs/Module-16-Lab-30-Packet-Tracer-Deployment-Cable-Devices.pdf"
lab_pdf: "/assets/pdfs/Module-16-Lab-30-Packet-Tracer-Deployment-Cable-Devices.pdf"
permalink: /network-portfolio/videos/16-30-deploy-cable-devices/
diagram: ""
---

## Overview

Build the supplied Packet Tracer topology by placing two 2960 switches and six PCs, then connect each device using the specified Ethernet interfaces and cable types.

<!--more-->

---

## Preconditions

<!-- Add the starting Packet Tracer topology screenshot here after recording. -->

---

## Skills Practiced

- Deploy and Cable Devices (Packet Tracer Lab 30)
- Device deployment
- Copper cabling
- Interface selection

---

## Video Walkthrough

<!-- Add video_id, video_url, and thumbnail when the recording is ready. -->

{% if page.video_id != "" %}
<iframe width="560" height="315" src="https://www.youtube.com/embed/{{ page.video_id }}" title="{{ page.title }}" frameborder="0" allowfullscreen></iframe>
{% endif %}

---

## Completed Lab Documentation

{% if page.completed_lab != "" %}
- [Completed Lab PDF]({{ page.completed_lab | relative_url }})
{% endif %}

---

## Key Observations

PC-to-switch connections use straight-through cable in this activity; the switch-to-switch connection uses a crossover cable. Link indicators may be amber temporarily while the ports initialize.

### Activity Focus

1. Place Switch0 and Switch1 and deploy PC0 through PC5 in the logical workspace.
2. Use copper straight-through cables: PC0–PC2 to Switch0 Fa0/1–Fa0/3, and PC3–PC5 to Switch1 Fa0/1–Fa0/3. Use each PC’s FastEthernet0 port.
3. Connect Switch0 Gi0/1 to Switch1 Gi0/1 with a copper crossover cable.
4. Wait for the links to come up, inspect the port choices, and save the Packet Tracer file.

### Notes

An amber link light can be temporary while the switch port transitions. Recheck the cable type and both interface selections if a link does not come up.

---

## Validation

Confirm all six PC links and the switch-to-switch link are present and their link lights settle to green.

---

## Related Exercises

- Ethernet Cabling
- Switch Interfaces
- Packet Tracer Topology

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
