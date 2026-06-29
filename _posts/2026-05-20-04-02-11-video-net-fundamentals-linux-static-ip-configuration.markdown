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

video_id: "LZi_qs4KWSo"
video_url: "https://www.youtube.com/watch?v=LZi_qs4KWSo"
thumbnail: "https://img.youtube.com/vi/LZi_qs4KWSo/hqdefault.jpg"

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

To modify Linux IPv4 configuration, open and edit file "/etc/sysconfig/network-scripts/ifcfg-enp2s0"

| Setting           | Value         |
| ----------------- | ------------- |
| IP Address        | 192.168.0.254 |
| Subnet Mask       | 255.255.255.0 |
| Broadcast Address | 192.168.0.255 |
| Default Gateway   | 192.168.0.5   |

### DNS Configuration

To modify Linux DNS configuration, open and edit file "/etc/resolv.conf"

| Setting       | Value         |
| ------------- | ------------- |
| Primary DNS   | 163.128.78.93 |
| Secondary DNS | 163.128.80.93 |

---

## Linux Static IPv4 Configuration Example

The network interface can be configured by editing the interface configuration file for the `enp2s0` adapter.

### Open the Network Configuration File

Show the current IP address configuration, change to "/etc/sysconfig/network-scripts/" directory, list files, then open the file to edit the configuration.
```bash
root@IT-Laptop:~# ip addr show
root@IT-Laptop:~# cd /etc/sysconfig/network-scripts/
root@IT-Laptop:/etc/sysconfig/network-scripts/# ls
root@IT-Laptop:/etc/sysconfig/network-scripts/# nano ifcfg-enp2s0
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
Change to "/etc/" directory, list files, then open and edit the DNS configuration file.
```bash
root@IT-Laptop:~# cd /etc/
root@IT-Laptop:/etc# ls
root@IT-Laptop:/etc# nano resolv.conf
```
Modify the DNS configuration file to include the following DNS server addresses.
```bash
nameserver=163.128.78.93
nameserver=163.128.80.93
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

After applying the configuration, (1)verify interface configuration and connectivity, (2) default gateway, (3) external internet connectivity, and (4) DNS name resolution.

Expected result:

* Successful replies confirm communication.
* The hostname should resolve to an IP address and return successful replies.
* Failure to communicate may indicate misconfiguration, network issues, or connectivity problems that require troubleshooting.


1). Show the current IP address configuration.

```bash
root@IT-Laptop:~# ip addr show
```

2). Test communication with the default gateway.

```bash
root@IT-Laptop:~# ping -c4 192.168.0.5
```

3). Test communication with an external DNS server.

```bash
root@IT-Laptop:~# ping -c4163.128.78.93
```

4). Test name resolution using an external website.

```bash
root@IT-Laptop:~# ping -c4 www.corpnet.xyz
```

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
  * [Formative Modules](/network-portfolio/formative-modules/)
  * **[VIDEO WALKTHROUGHS](/network-portfolio/videos/)**
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* [Bible Study](/bible-study/)
* [About the Portfolio](/zabout-the-portfolio/)

---
---
---