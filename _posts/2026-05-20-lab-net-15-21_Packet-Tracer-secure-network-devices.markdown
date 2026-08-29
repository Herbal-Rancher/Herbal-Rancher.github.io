---

layout: post
title: "Lab 21| Cisco Networking Labs - Secure Network Devices"
lab_title: "Secure Network Devices"

lesson: "15.0"
lesson_id: "15.21.00"
sort_order: "152100"

categories:

- portfolio
- labs
- videos

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

topics:

- network-device-security
- ssh-configuration
- password-security
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

video_id: "zwGWxiwK79o"
video_url: "https://youtu.be/zwGWxiwK79o"
thumbnail: "https://img.youtube.com/vi/zwGWxiwK79o/hqdefault.jpg"

completed_lab: "/assets/pdfs/Module-15-Lab-21-Packet-Tracer-Secure-Network-Devices.pdf"
lab_pdf: "/assets/pdfs/Module-15-Lab-21-Packet-Tracer-Secure-Network-Devices.pdf"

permalink: /network-portfolio/videos/15-21-secure-network-devices/

---
## Overview

This Packet Tracer lab demonstrates how I secured a Cisco router and switch for network administration. I configured secure passwords, SSH remote access, local authentication, login protection, switch management access, disabled unused ports, and verified connectivity between both LANs.

<!--more-->

---

## Preconditions

![Packet Tracer Lab 21 - Secure Network Devices - Preconditions](/assets/images/packet-tracer/cisco-lab-topology-module-15-Lab-21.png)

### Addressing

| Device    | Interface | Address       | Mask          | Gateway     |
| --------- | --------- | ------------- | ------------- | ----------- |
| RTR-A     | G0/0/0    | 192.168.1.1   | 255.255.255.0 | N/A         |
| RTR-A     | G0/0/1    | 192.168.2.1   | 255.255.255.0 | N/A         |
| SW-1      | VLAN 1    | 192.168.1.254 | 255.255.255.0 | 192.168.1.1 |
| PC        | NIC       | 192.168.1.2   | 255.255.255.0 | 192.168.1.1 |
| Laptop    | NIC       | 192.168.1.10  | 255.255.255.0 | 192.168.1.1 |
| Remote PC | NIC       | 192.168.2.10  | 255.255.255.0 | 192.168.2.1 |

---

## Skills Practiced

* Secure Network Devices (Packet Tracer Lab 21)
* Configure Cisco router and switch security
* Configure encrypted credentials
* Configure SSH Version 2
* Restrict VTY access to SSH
* Configure local user authentication
* Configure session and login protection
* Configure switch management addressing
* Disable unused switch ports
* Verify network connectivity

---

## Steps

### Step 1 — Secure RTR-A

Configure the router identity and basic security settings:

```text
enable
configure terminal
hostname RTR-A
no ip domain-lookup
security passwords min-length 10
enable secret @Cons1234!
service password-encryption
banner motd #WARNING: Authorized access only.#
```

**Purpose:** Establishes the router identity, prevents unwanted DNS lookups, protects privileged access, and secures stored passwords.

Configure console access:

```text
line console 0
password @Cons1234!
login
exec-timeout 7 0
exit
```

**Purpose:** Requires console authentication and closes inactive sessions after seven minutes.

Create the administrator account:

```text
username NETadmin secret LogAdmin!9
```

Configure SSH:

```text
ip domain-name security.com
crypto key generate rsa
```

Enter:

```text
1024
```

Then:

```text
ip ssh version 2
```

Configure secure VTY access:

```text
line vty 0 15
transport input ssh
login local
exec-timeout 7 0
exit
```

Protect against repeated failed logins:

```text
login block-for 45 attempts 3 within 100
```

**Purpose:** SSH encrypts remote management traffic, while `login local` requires the configured administrator account.

---

### Step 2 — Configure SW-1 Security

Configure the switch identity and warning banner:

```text
enable
configure terminal
hostname SW-1
no ip domain-lookup
banner motd #WARNING: Authorized access only.#
```

Configure privileged access:

```text
enable secret @Cons1234!
```

Create the administrator account:

```text
username NETadmin secret LogAdmin!9
```

---

### Step 3 — Configure SW-1 Management Access

Configure the VLAN 1 management SVI:

```text
interface vlan 1
ip address 192.168.1.254 255.255.255.0
no shutdown
exit
```

Configure the switch default gateway:

```text
ip default-gateway 192.168.1.1
```

**Purpose:** Allows SW-1 to be managed from both the local and remote networks.

---

### Step 4 — Disable Unused Switch Ports

```text
interface range fa0/3-24
shutdown
exit

interface range gi0/1-2
shutdown
exit
```

**Purpose:** Reduces unnecessary exposure by disabling interfaces that are not used by the topology.

---

### Step 5 — Configure SSH on SW-1

```text
ip domain-name security.com
crypto key generate rsa
```

Enter:

```text
1024
```

Then:

```text
ip ssh version 2
```

Configure VTY access:

```text
line vty 0 15
transport input ssh
login local
exit
```

**Purpose:** Allows encrypted remote administration and requires authentication with the `NETadmin` account.

---

## Validation

Verify the switch management interface:

```text
show ip interface brief
```

Verify SSH:

```text
show ip ssh
```

Verify the configuration:

```text
show running-config
```

From a host on LAN 1:

```text
ping 192.168.1.254
```

From the Remote PC on LAN 2:

```text
ping 192.168.1.254
```

Both should successfully reach the SW-1 management interface.

---

## Security Notes

This activity demonstrates several common device-hardening practices:

* Use SSH instead of Telnet for remote management.
* Use encrypted secret credentials for administrative accounts.
* Limit inactive administrative sessions.
* Block repeated failed login attempts.
* Disable unused switch ports.
* Use a management IP and default gateway so authorized administrators can reach the switch remotely.

The lab requires a 1024-bit RSA key for Packet Tracer. Production environments should follow current organizational and platform security standards rather than relying on lab-specific cryptographic values.

---

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

* [Completed Lab PDF]({{ page.completed_lab | relative_url }})

---

## Key Observations

* SSH provides encrypted remote management.
* `login local` uses the configured administrator account for VTY authentication.
* The switch management SVI and default gateway provide remote management connectivity.
* Disabling unused ports reduces unnecessary network exposure.
* Security configuration should protect administrative access without disrupting required network communication.

---

## Related Exercises

* Network Device Hardening
* Secure Remote Administration with SSH
* Router and Switch Management
* Password and Login Security
* Network Connectivity Testing


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