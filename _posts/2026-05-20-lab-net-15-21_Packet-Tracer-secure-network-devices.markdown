---
layout: post
title: "Lab 21| Cisco Networking Labs - Secure Network Devices"
lab_title: "Secure Network Devices"

lesson: "15.0"
lesson_id: "15.21.00"
sort_order: "152100"

categories: [portfolio, videos]

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: network-security
subcategory_display: Network Security

content_type: video
content_type_display: Video

tags:
  - packet-tracer
  - network-security
  - device-hardening
  - router-security
  - switch-security
  - ssh
  - secure-management
  - access-control
  - password-security

topics:
  - network-device-security
  - router-hardening
  - switch-hardening
  - secure-remote-access
  - ssh-configuration
  - password-encryption
  - login-security
  - management-interface
  - unused-port-security
  - connectivity-testing

tools:
  - cisco-packet-tracer
  - router
  - switch
  - command-line-interface
  - ping
  - ssh

protocols:
  - IPv4
  - ICMP
  - SSH

status: complete

video_id: ""
video_url: ""
thumbnail: ""

completed_lab: "/assets/pdfs/Module-15-Lab-21-Packet-Tracer-Secure-Network-Devices.pdf"
lab_pdf: "/assets/pdfs/Module-15-Lab-21-Packet-Tracer-Secure-Network-Devices.pdf"

permalink: /network-portfolio/videos/15-21-secure-network-devices/

diagram: ""
---

## Overview

This Packet Tracer lab demonstrates how I secured a router and switch
for network administration. I configured device access controls,
password protection, SSH remote management, login security, switch
management access, and disabled unused switch ports while maintaining
connectivity between the network devices.

```{=html}
<!--more-->
```

------------------------------------------------------------------------

## Preconditions

![Packet Tracer Lab 21 - Secure Network Devices -
Preconditions](/assets/images/packet-tracer/cisco-lab-topology-module-15-lab-21.png)

------------------------------------------------------------------------

## Skills Practiced

-   Secure Network Devices (Packet Tracer Lab 21)
-   Configure router and switch security settings
-   Configure encrypted privileged and local user credentials
-   Configure SSH for secure remote administration
-   Restrict VTY access to SSH
-   Configure login authentication and brute-force protection
-   Configure session timeouts and an MOTD security banner
-   Configure switch management addressing
-   Administratively disable unused switch ports
-   Verify management connectivity with ping

------------------------------------------------------------------------

## Video Walkthrough

```{=html}
<iframe width="560" height="315" src="https://www.youtube.com/embed/{{ page.video_id }}" title="{{ page.title }}" frameborder="0" allowfullscreen>
```
```{=html}
</iframe>
```

------------------------------------------------------------------------

## Completed Lab Documentation

-   [Completed Lab
    PDF](%7B%7B%20page.completed_lab%20%7C%20relative_url%20%7D%7D)

------------------------------------------------------------------------

## Key Observations

Securing network infrastructure requires protecting both local and
remote administrative access.

-   **SSH:** Provides encrypted remote management.
-   **Authentication:** Local administrator credentials control access
    to device management.
-   **Password protection:** Encrypted credentials and minimum password
    requirements strengthen device security.
-   **Login protection:** Session timeouts and failed-login blocking
    reduce unauthorized access attempts.
-   **Switch hardening:** Unused ports are administratively disabled to
    reduce unnecessary exposure.
-   **Management access:** The switch management interface must be
    correctly addressed and reachable from remote networks.

------------------------------------------------------------------------

## Validation

I verified secure SSH management access, VTY authentication with the
configured administrator account, and network connectivity.

Hosts on both LANs were able to reach the switch management interface,
confirming that the security configuration preserved required network
communication.

------------------------------------------------------------------------

## Related Exercises

-   Network Device Hardening
-   Secure Remote Administration with SSH
-   Router and Switch Management
-   Password and Login Security
-   Switch Port Security
-   Network Connectivity Testing
