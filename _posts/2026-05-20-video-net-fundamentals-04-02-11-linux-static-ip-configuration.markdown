---
layout: post
title: "Networking Fundamentals | Linux Static IP Configuration and Connectivity Testing"
lab_title: "Linux Static IP Configuration and Connectivity Testing"

lesson: "4c.0"
lesson_id: "04.02.11"
sort_order: "040211"

categories: [portfolio, videos]

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: tcpip
subcategory_display: TCP/IP

content_type: video
content_type_display: Video

tags:
  - linux
  - static-ip
  - tcp-ip
  - dns
  - gateway
  - network-configuration

permalink: /network-portfolio/videos/linux-static-ip-configuration/
status: complete

video_id: "zwGWxiwK79o"
video_url: "https://www.youtube.com/watch?v=zwGWxiwK79o"
thumbnail: "https://img.youtube.com/vi/zwGWxiwK79o/hqdefault.jpg"

topics:
  - static-ip-addressing
  - dns-configuration
  - gateway-configuration
  - connectivity-testing
  - linux-networking

tools:
  - Linux
  - Terminal
  - Ping

protocols:
  - IPv4
  - ICMP
  - DNS

---

## Overview

The activity focuses on assigning a static IP address, configuring DNS servers, defining a default gateway, and validating connectivity using common network troubleshooting tools.

<!--more-->

The linked, no-narration video walkthrough, visuallydemonstrates how to manually configure IPv4 networking on a Linux workstation and verify communication with local and external resources.

---

## Video Walkthrough

<a href="{{ page.video_url }}" target="_blank" rel="noopener noreferrer">
  <img src="{{ page.thumbnail }}"
       alt="{{ page.title }}"
       style="width: 420px; border-radius: 8px;">
</a>

---

## Configuration Requirements

### IPv4 Configuration

| Setting           | Value         |
| ----------------- | ------------- |
| IP Address        | 192.168.0.254 |
| Subnet Mask       | 255.255.255.0 |
| Broadcast Address | 192.168.0.255 |
| Default Gateway   | 192.168.0.5   |

### DNS Configuration

Primary DNS:

163.128.78.93

Secondary DNS:

163.128.80.93

---

## Configuration Process

1. Open the network interface configuration for the `enp2s0` adapter.
2. Remove any automatic address assignment settings.
3. Configure a static IPv4 address.
4. Configure the subnet mask and broadcast address.
5. Configure the default gateway.
6. Configure primary and secondary DNS servers.
7. Save the configuration.
8. Restart or reload the network interface.

---

## Connectivity Validation

After applying the configuration, verify network communication.

### Verify Local Network Connectivity

Test communication with the default gateway:

```bash
ping 192.168.0.5
```

Expected Result:

The workstation should successfully communicate with the local network gateway.

---

### Verify Internet Connectivity

Test communication with an external DNS server:

```bash
ping 163.128.78.93
```

Expected Result:

The workstation should successfully communicate with an external internet host.

---

### Verify DNS Resolution

Test name resolution using an external website:

```bash
ping www.corpnet.xyz
```

Expected Result:

The hostname should successfully resolve to an IP address and return responses.

---

## Skills Practiced

* Linux Network Configuration
* Static IPv4 Addressing
* DNS Configuration
* Default Gateway Configuration
* Connectivity Testing
* Network Troubleshooting
* TCP/IP Fundamentals

---

## Key Takeaways

Static addressing requires accurate configuration of the IP address, subnet mask, gateway, and DNS servers. Successful communication with the gateway, external hosts, and domain names confirms that local networking, routing, and DNS services are functioning correctly.


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