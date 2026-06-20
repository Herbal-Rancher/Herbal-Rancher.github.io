---

layout: post
title: "Networking Fundamentals | Linux Static IP Configuration and Connectivity Testing"
lab_title: "Linux Static IP Configuration and Connectivity Testing"

lesson: "4.0"
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
- Nano
- NetworkManager

protocols:

- IPv4
- ICMP
- DNS

---

## Overview

This walkthrough demonstrates how to manually configure IPv4 networking on a Linux workstation and verify communication with local and external network resources.

<!--more-->

The activity focuses on assigning a static IP address, configuring DNS servers, defining a default gateway, removing automatic address assignment, and validating connectivity using common Linux networking commands.

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

| Setting       | Value         |
| ------------- | ------------- |
| Primary DNS   | 163.128.78.93 |
| Secondary DNS | 163.128.80.93 |

---

## Linux Static IPv4 Configuration Example

The network interface can be configured by editing the interface configuration file for the `enp2s0` adapter.

### Open the Network Configuration File

```bash
sudo nano /etc/sysconfig/network-scripts/ifcfg-enp2s0
```

---

## Example Static Configuration

The configuration should remove automatic DHCP assignment and define the static TCP/IP settings manually.

```bash
TYPE=Ethernet
BOOTPROTO=none
NAME=enp2s0
DEVICE=enp2s0
ONBOOT=yes

IPADDR=192.168.0.254
NETMASK=255.255.255.0
BROADCAST=192.168.0.255
GATEWAY=192.168.0.5

DNS1=163.128.78.93
DNS2=163.128.80.93
```

---

## Restart Networking

After saving the file, restart the network service or reload NetworkManager.

```bash
sudo systemctl restart NetworkManager
```

---

## Verify Interface Configuration

Use the following command to confirm that the interface has the correct IPv4 settings.

```bash
ip addr show enp2s0
```

---

## Verify Routing

Use the routing table to confirm that the default gateway is configured correctly.

```bash
ip route
```

The default route should point toward:

```text
192.168.0.5
```

---

## Connectivity Validation

After applying the configuration, verify local connectivity, external connectivity, and DNS name resolution.

### Verify Local Network Connectivity

Test communication with the default gateway.

```bash
ping 192.168.0.5
```

Expected result:

* Successful replies confirm communication with the local network gateway.

---

### Verify Internet Connectivity

Test communication with an external DNS server.

```bash
ping 163.128.78.93
```

Expected result:

* Successful replies confirm external network access.

---

### Verify DNS Resolution

Test name resolution using an external website.

```bash
ping www.corpnet.xyz
```

Expected result:

* The hostname should resolve to an IP address and return successful replies.

---

## Commands Demonstrated

* `nano`
* `systemctl restart NetworkManager`
* `ip addr show`
* `ip route`
* `ping`

---

## Skills Practiced

* Linux Network Configuration
* Static IPv4 Addressing
* DNS Configuration
* Default Gateway Configuration
* Connectivity Testing
* Network Troubleshooting
* TCP/IP Fundamentals
* Command-Line Administration

---

## Video Walkthrough

<a href="{{ page.video_url }}" target="_blank" rel="noopener noreferrer">
  <img src="{{ page.thumbnail }}"
       alt="{{ page.title }}"
       style="width: 420px; border-radius: 8px;">
</a>

---

## Key Takeaways

Static addressing requires accurate configuration of the IP address, subnet mask, broadcast address, default gateway, and DNS servers.

Successful communication with the gateway confirms local network connectivity. Successful communication with an external DNS server confirms routed network access. Successful communication with a hostname confirms that DNS resolution is functioning correctly.

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