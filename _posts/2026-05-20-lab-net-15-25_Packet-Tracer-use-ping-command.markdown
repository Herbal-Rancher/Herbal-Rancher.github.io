---
layout: post
title: "Lab 25| Cisco Networking Labs - Use the Ping Command"
lab_title: "Use the Ping Command"

lesson: "15.0"
lesson_id: "15.25.00"
sort_order: "152500"

categories: [portfolio, videos]

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: network-troubleshooting
subcategory_display: Network Troubleshooting

content_type: video
content_type_display: Video

tags:
  - packet-tracer
  - ping
  - dns
  - ipv4
  - connectivity
  - troubleshooting
  - static-ip
  - web-connectivity

topics:
  - ping-command
  - connectivity-testing
  - dns-troubleshooting
  - name-resolution
  - ipv4-connectivity
  - static-ip-addressing
  - client-configuration
  - web-connectivity
  - network-troubleshooting

tools:
  - cisco-packet-tracer
  - command-prompt
  - ping
  - ipconfig
  - ip-configuration
  - web-browser

protocols:
  - IPv4
  - ICMP
  - DNS
  - HTTP

status: complete

video_id: ""
video_url: ""
thumbnail: ""

completed_lab: "/assets/pdfs/Module-15-Lab-25-Packet-Tracer-Use-Ping-Command.pdf"
lab_pdf: "/assets/pdfs/Module-15-Lab-25-Packet-Tracer-Use-Ping-Command.pdf"

permalink: /network-portfolio/videos/15-25-use-ping-command/

diagram: ""
---

## Overview

This Packet Tracer lab demonstrates how I used the `ping` command to
identify a client configuration problem affecting website access. I
compared hostname and IP-address connectivity, examined DNS
configuration with `ipconfig /all`, corrected the affected PC
configuration, and verified restored access to the web server.

```{=html}
<!--more-->
```

------------------------------------------------------------------------

## Preconditions

![Packet Tracer Lab 25 - Use the Ping Command -
Preconditions](/assets/images/packet-tracer/cisco-lab-topology-module-15-lab-25.png)

------------------------------------------------------------------------

## Skills Practiced

-   Use the Ping Command (Packet Tracer Lab 25)
-   Identify PCs experiencing web connectivity problems
-   Use `ping` to test hostname connectivity
-   Use `ping` to test direct IPv4 connectivity
-   Distinguish IP connectivity from DNS name-resolution problems
-   Use `ipconfig /all` to examine DNS server configuration
-   Compare working and misconfigured client settings
-   Correct client IP configuration
-   Verify restored website connectivity

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

The `ping` command can help isolate whether a connectivity problem is
related to basic IP communication or hostname resolution.

-   **Hostname test:** Pinging `www.cisco.pka` tests whether the client
    can resolve the hostname and reach the destination.
-   **IP address test:** Successfully pinging the web server by IP
    address confirms that IP connectivity exists even when hostname
    access fails.
-   **DNS configuration:** If IP communication succeeds but hostname
    communication fails, the client's DNS server configuration should be
    investigated.
-   **Configuration comparison:** `ipconfig /all` allows DNS settings on
    affected PCs to be compared with correctly configured clients.

------------------------------------------------------------------------

## Validation

After correcting the affected PC configuration, I used the web browser
to access `www.cisco.pka`.

Successful website access confirmed that the client configuration
problem was resolved and DNS name resolution was functioning correctly.

------------------------------------------------------------------------

## Related Exercises

-   ICMP and Ping Testing
-   DNS Name Resolution
-   IPv4 Connectivity Testing
-   Static IP Configuration
-   Client Network Troubleshooting
-   Web Connectivity Troubleshooting

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