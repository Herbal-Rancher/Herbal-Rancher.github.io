---
layout: post
title: "Lab 23| Cisco Networking Labs - Troubleshoot Connectivity Issues"
lab_title: "Troubleshoot Connectivity Issues"

lesson: "15.0"
lesson_id: "15.23.00"
sort_order: "152300"

categories: [portfolio, videos]

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: network-troubleshooting
subcategory_display: Network Troubleshooting

content_type: video
content_type_display: Video

tags:
  - packet-tracer
  - connectivity
  - troubleshooting
  - ipv4
  - default-gateway
  - dns
  - web-server
  - network-services
  - end-to-end-connectivity

topics:
  - connectivity-troubleshooting
  - ipv4-addressing
  - default-gateway
  - dns-resolution
  - web-connectivity
  - local-connectivity
  - remote-connectivity
  - end-to-end-connectivity
  - issue-documentation
  - problem-escalation

tools:
  - cisco-packet-tracer
  - command-prompt
  - ipconfig
  - ping
  - web-browser
  - ssh

protocols:
  - IPv4
  - ICMP
  - DNS
  - HTTP
  - SSH

status: complete


video_id: "zwGWxiwK79o"
video_url: "https://youtu.be/zwGWxiwK79o"
thumbnail: "https://img.youtube.com/vi/zwGWxiwK79o/hqdefault.jpg"

completed_lab: "/assets/pdfs/Module-15-Lab-23-Packet-Tracer-Troubleshoot-Connectivity-Issues.pdf"
lab_pdf: "/assets/pdfs/Module-15-Lab-23-Packet-Tracer-Troubleshoot-Connectivity-Issues.pdf"

permalink: /network-portfolio/videos/15-23-troubleshoot-connectivity-issues/

diagram: ""
---

## Overview

This Packet Tracer lab demonstrates a systematic approach to
troubleshooting network connectivity after a network change involving
DNS services. I verified IPv4 addressing and default gateway
configuration, tested local and remote connectivity, compared web access
by hostname and IP address, corrected client-side issues when possible,
and documented problems requiring escalation.

<!--more-->

------------------------------------------------------------------------

## Preconditions

![Packet Tracer Lab 23 - Troubleshoot Connectivity Issues -
Preconditions](/assets/images/packet-tracer/cisco-lab-topology-module-15-lab-23.png)

------------------------------------------------------------------------

## Skills Practiced

-   Troubleshoot Connectivity Issues (Packet Tracer Lab 23)
-   Verify IPv4 addressing and default gateway configuration
-   Use `ipconfig` to identify client configuration problems
-   Use `ping` to test local and remote connectivity
-   Test web-server access by hostname and IPv4 address
-   Differentiate IP connectivity from DNS name-resolution problems
-   Correct client-side network configuration issues
-   Verify connectivity across multiple networks
-   Document troubleshooting results and solutions
-   Identify issues that require escalation

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

Connectivity troubleshooting requires testing network functions
individually to determine where communication fails.

-   **IP configuration:** `ipconfig` verifies the host address and
    default gateway against documented network settings.
-   **Local connectivity:** Ping tests between local devices help
    identify addressing or local-network problems.
-   **Remote connectivity:** Pinging the web server and devices on other
    networks helps verify routed communication.
-   **DNS troubleshooting:** Comparing web access by hostname with
    access by IP address helps distinguish DNS resolution problems from
    general IP connectivity problems.
-   **Escalation:** Problems outside the administrator's access or
    control should be clearly documented and escalated when they cannot
    be corrected locally.

------------------------------------------------------------------------

## Validation

I verified connectivity from each PC to its default gateway, other
network hosts, and the web server. I also compared access to the web
server using `www.cisco.pka` and its IPv4 address to isolate DNS-related
issues.

Final validation confirmed that the client configurations matched the
documented addressing plan and that required web-server connectivity was
restored where the available configuration permitted correction.

------------------------------------------------------------------------

## Related Exercises

-   IPv4 Addressing and Default Gateways
-   DNS Name Resolution
-   Local and Remote Connectivity Testing
-   Web Connectivity Troubleshooting
-   Systematic Network Troubleshooting
-   Issue Documentation and Escalation


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