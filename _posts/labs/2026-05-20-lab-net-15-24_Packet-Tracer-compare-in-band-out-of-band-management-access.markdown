---
layout: post
title: "Lab 24| Cisco Networking Labs - Compare In-Band and Out-of-Band Management Access"
lab_title: "Compare In-Band and Out-of-Band Management Access"

lesson: "15.0"
lesson_id: "15.24.00"
sort_order: "152400"

categories: [portfolio, videos]

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: network-management
subcategory_display: Network Management

content_type: video
content_type_display: Video

tags:
  - packet-tracer
  - network-management
  - in-band-management
  - out-of-band-management
  - console-access
  - usb-console
  - ssh
  - remote-management
  - device-access

topics:
  - in-band-management
  - out-of-band-management
  - console-connection
  - usb-console-connection
  - terminal-access
  - command-line-interface
  - ssh-remote-access
  - ip-based-management
  - router-management
  - switch-management

tools:
  - cisco-packet-tracer
  - console-cable
  - usb-cable
  - terminal
  - command-prompt
  - router
  - switch

protocols:
  - IPv4
  - SSH

status: complete

video_id: "zwGWxiwK79o"
video_url: "https://youtu.be/zwGWxiwK79o"
thumbnail: "https://img.youtube.com/vi/zwGWxiwK79o/hqdefault.jpg"

completed_lab: "/assets/pdfs/Module-15-Lab-24-Packet-Tracer-InBand-OutOfBand-Access.pdf"
lab_pdf: "/assets/pdfs/Module-15-Lab-24-Packet-Tracer-InBand-OutOfBand-Access.pdf"

permalink: /network-portfolio/videos/15-24-in-band-out-of-band-management-access/

diagram: ""
---

## Overview

This Packet Tracer lab compares **out-of-band and in-band management
access** for network devices. I established local management connections
using console and USB console interfaces, then used SSH over an IP
network to remotely access routers and compare the requirements and use
cases of each management method.

<!--more-->

------------------------------------------------------------------------

## Preconditions

![Packet Tracer Lab 24 - Compare In-Band and Out-of-Band Management Access - Preconditions](/assets/images/packet-tracer/cisco-lab-topology-module-15-lab-24.png)

------------------------------------------------------------------------

## Skills Practiced

-   Compare In-Band and Out-of-Band Management Access (Packet Tracer Lab
    24)
-   Establish an out-of-band console connection
-   Access router and switch command-line interfaces through a terminal
-   Establish a USB console connection
-   Identify management methods that do not require IP connectivity
-   Establish in-band management access over an IP network
-   Use SSH for secure remote device management
-   Access routers from another network device and from a PC
-   Compare local and remote network-management methods

------------------------------------------------------------------------

## Video Walkthrough

<iframe
width="560"
height="315"
src="https://www.youtube.com/embed/{{ page.video_id }}"
title="{{ page.title }}"
frameborder="0"
allowfullscreen>
</iframe>

---
## Completed Lab Documentation

- [Completed Lab PDF]({{ page.completed_lab | relative_url }})

---

## Key Observations

In-band and out-of-band management provide different methods for
accessing and administering network infrastructure.

-   **Out-of-band management:** Uses a direct physical management
    connection such as a console or USB console connection and does not
    require IP addressing.
-   **Console access:** Provides local CLI access through terminal
    emulation software.
-   **In-band management:** Uses the operational IP network to reach a
    remote device and therefore requires working IP connectivity.
-   **SSH:** Provides secure remote command-line access for in-band
    device management.
-   **Management availability:** Out-of-band access can be especially
    useful when normal network connectivity is unavailable or has not
    yet been configured.

------------------------------------------------------------------------

## Validation

I verified out-of-band access by connecting to router and switch
command-line interfaces through console and USB console connections.

I then established in-band SSH sessions to remotely access the East and
West routers over the IP network, confirming the operational differences
between physical management access and IP-based remote management.

------------------------------------------------------------------------

## Related Exercises

-   Network Device Management
-   Console and USB Console Access
-   Secure Remote Administration with SSH
-   Router and Switch Management
-   In-Band Network Management
-   Out-of-Band Network Management


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