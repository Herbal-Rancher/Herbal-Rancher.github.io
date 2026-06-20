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

View the current IP address configuration before editing the file then open the file to edit the configuration.
```bash
root@IT-Laptop:~# ip addr show
root@IT-Laptop:~# cd /etc/sysconfig/network-scripts/
root@IT-Laptop:~# nano ifcfg-enp2s0
```

---

## Example Static IP Configuration
The current configuration may look similar to the following, which includes automatic DHCP assignment.

```bash
# Realtek 8169
DEVICE=enp2s0
BOOTPROTO=dhcp
HWADDR=00:60:98:7f:41:e3
ONBOOT=yes
```

The configuration should remove automatic DHCP assignment and define the static TCP/IP settings manually.

```bash
# Realtek 8169
DEVICE=enp2s0
HWADDR=00:60:98:7f:41:e3
ONBOOT=yes

IPADDR=192.168.0.254
NETMASK=255.255.255.0
BROADCAST=192.168.0.255
GATEWAY=192.168.0.5
BOOTPROTO=none
```
---

## Example Static DNS Configuration
Open the DNS configuration file and add the DNS server addresses.
```bash
root@IT-Laptop:~# cd /etc/
root@IT-Laptop:~# nano resolv.conf
```
Modify the file to include the following DNS server addresses.
```bash
DNS1=163.128.78.93
DNS2=163.128.80.93
```
---

## Restart Network Interface

After saving the file, restart the network service or reload NetworkManager.

```bash
root@IT-Laptop:~# ip link set enp2s0 down
root@IT-Laptop:~# ip link set enp2s0 up
```

---

## Connectivity Validation

After applying the configuration, verify configuration, local connectivity, external connectivity, and DNS name resolution.

### Verify Interface Configuration and Local Network Connectivity

```bash
root@IT-Laptop:~# ip addr show
```
Test communication with the default gateway.

```bash
root@IT-Laptop:~# ping -c4 192.168.0.5
```

Expected result:

* Successful replies confirm communication with the local network gateway.

---

### Verify Internet Connectivity

Test communication with an external DNS server.

```bash
root@IT-Laptop:~# ping -c4163.128.78.93
```

Expected result:

* Successful replies confirm external network access.

---

### Verify DNS Resolution

Test name resolution using an external website.

```bash
root@IT-Laptop:~# ping -c4 www.corpnet.xyz
```

Expected result:

* The hostname should resolve to an IP address and return successful replies.

---

## Commands Demonstrated

* `ip addr show`
* `cd /etc/sysconfig/network-scripts/`
* `nano`
* `ip link set enp2s0 down`
* `ip link set enp2s0 up`
* `ping -c4`

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
* Configuration IP Addresses on Linux

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