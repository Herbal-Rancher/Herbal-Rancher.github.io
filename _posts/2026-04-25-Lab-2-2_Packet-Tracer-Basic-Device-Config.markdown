---
layout: post
title: "12.2 Packet Tracer Lab 2: Basic Device Configuration"
lesson: 2.0
order: 2.2
categories: [portfolio, blog, walkthroughs, lab, network]
tags: [packet-tracer, cisco-ios, ipv4, ipv6, router, switch, troubleshooting]
permalink: /portfolio/walkthroughs/lesson-2-0/lab-2-configure-basic-device-config/
---

## Module 12 Packet Tracer Lab 2: Basic Device Configuration
In this Lab, we present a guide to the "Basic Device Configuration" lab, to document easily repeatable steps for the foundation of assessing any network. This is configuring a Cisco router, 2 switches, and 4 hosts (2 hosts in each switched subnet. This lab uses Cisco Packet Tracer to simulate establishing a full IPv4 and IPv6 connectivity between two LANs.

<!--more-->
---



This lab reinforced:

- Basic Cisco IOS navigation
- Router configuration
- Switch management configuration
- IPv4 addressing
- IPv6 addressing
- Password security
- Connectivity verification
- Troubleshooting

---

## Lab Objective

Configure the following devices:

- Router: **College**
- Switch: **Class-B**
- PC Hosts:
  - Student-1
  - Student-2
  - Student-3
  - Student-4

Goal: To establish full end-to-end connectivity across both networks using IPv4 and IPv6.

---

## Step 1: Review the Topology

Before touching anything:

- Identify which devices are already configured
- Identify missing IP addresses
- Identify inaccessible devices

### Important Note:
You **cannot access Class-A switch**

This means:

- Do not waste time trying to configure it
- Only configure:
  - College router
  - Class-B switch
  - Student PCs

<img src="{{ '/assets/images/Packet-Tracer-Basic-Device-Config-imgage.jpg' | relative_url }}" sizes="medium">

---

##  Step 2: Complete Missing Addressing Table Information

Look for blanks in:

- Default gateway fields
- Missing host IPv4 addresses
- Missing IPv6 addresses

### Router Interface Addressing

| Interface | IPv4 Address | IPv6 Address | Link-Local Address |
|------------|--------------|---------------|-------------------|
| G0/0 | `128.107.20.1/24` | `2001:DB8:A::1/64` | `FE80::1` |
| G0/1 | `128.107.30.1/24` | `2001:DB8:B::1/64` | `FE80::1` |


### Default Gateways

| Network | Default Gateway |
|----------|------------------|
| Network A Devices | `128.107.20.1` |
| Network B Devices | `128.107.30.1` |

<img src="{{ '/assets/images/Packet-Tracer-Basic-Device-Config-router-addressing-table-imgage.jpg' | relative_url }}" sizes="small">

---

##  Step 3: Access the College Router CLI

Click router → CLI

When prompted: Click ```Enter``` to access the CLI.

The following prompt is presented:
```bash
Router>
```
--- 

##  Step 4: Configure Router Hostname
```bash
Router>enable
Router#configure terminal
Configuring from terminal, memory, or network [terminal]? Enter configuration commands, one per line.  End with CNTL/Z.
Router(config)#
Router(config)#hostname College
College(config)#
```
--- 

##  Step 5: Configure Password Security

Privileged EXEC Password
```bash
College(config)#enable secret class
```
College Router Console Password
```bash
College(config)#line console 0
College(config-line)#password cisco
College(config-line)#login
College(config-line)#exit
College(config)#
```
College VTY Password
```bash
College(config)#line vty 0 4
College(config-line)#password cisco
College(config-line)#login
College(config-line)#exit
College(config)#
```
Encrypt College Plain Text Passwords
```bash
College(config)#service password-encryption
```
--- 

##  Step 6: Configure Default Gateway Banner
```bash
College(config)#banner motd # Unauthorized College access prohibited #
```
--- 
Feel free to customize wording as needed.

##  Step 7: Configure Router Interfaces
G0/0 Configuration
```bash
College(config-if)#ip address 128.107.20.1 255.255.255.0
College(config-if)#ipv6 address 2001:DB8:A::1/64
College(config-if)#ipv6 address FE80::1 link-local
College(config-if)#no shutdown
College(config-if)#exit
College(config)#
```
G0/1 Configuration
```bash
College(config)#interface g0/1
College(config-if)#description Connection to Class-B LAN
College(config-if)#ip address 128.107.30.1 255.255.255.0
College(config-if)#ipv6 address 2001:DB8:B::1/64
College(config-if)#ipv6 address FE80::1 link-local
College(config-if)#no shutdown 
College(config-if)#exit
```
--- 
##  Step 8: Enable IPv6 Routing

This step is commonly forgotten.
```bash
College(config)#ipv6 unicast-routing 
```
Without this, IPv6 communication may fail.

--- 

##  Step 9: Configure Class-B Switch

Click: Class-B → CLI

Set Hostname
```bash
Router>
Router>enable
Router#configure terminal
Configuring from terminal, memory, or network [terminal]? Enter configuration commands, one per line.  End with CNTL/Z.
Router(config)#hostname Class-B
Class-B(config)#
```
Privileged EXEC Password
```bash
Class-B(config)#enable secret class
```
Class-B Console Password
```bash
Class-B(config)#line console 0
Class-B(config-line)#password cisco
Class-B(config-line)#login
Class-B(config-line)#exit
Class-B(config)#
```
VTY Password
```bash
Class-B(config)#line vty 0 4
Class-B(config-line)#password cisco
Class-B(config-line)#login
Class-B(config-line)#exit
Class-B(config)#
```
Encrypt Plain Text Passwords
```bash
Class-B(config)#service password-encryption
```
Configure Class-B Banner
```bash
Class-B(config)#banner motd # Authorized Class-B users only #
```
--- 

##  Step 10: Configure Class B Switch VLAN 1 Management Interface
```bash
Class-B(config)#interface vlan 1
Class-B(config-if)#description Management Interface
Class-B(config-if)#ip address 128.107.30.15 255.255.255.0
Class-B(config-if)#ipv6 address 2001:DB8:B::15/64
Class-B(config-if)#no shutdown
Class-B(config-if)#exit
Class-B(config)#
```
--- 

##  Step 11: Configure Switch Default Gateway
```bash
Class-B(config)#ip default-gateway 128.107.30.1
```
--- 
##  Step 12: Save Configurations

Router:

```bash
copy running-config startup-config
```
Switch:

```bash
Class-B#copy running-config startup-config
```
--- 

##  Step 13: Configure Student PCs

Click each PC:

Desktop → IP Configuration

### Student PC Addressing Configuration

| Device | **IPv4 Address** | **Subnet Mask** | **Default Gateway** | **IPv6 Address** | **IPv6 Gateway** |
|----------|------------------|------------------|----------------------|-------------------|-------------------|
| Student-1 | `128.107.20.25` | `255.255.255.0` | `128.107.20.1` | `2001:DB8:A::25/64` | `FE80::1` |
| Student-2 | `128.107.20.30` | `255.255.255.0` | `128.107.20.1` | `2001:DB8:A::30/64` | `FE80::1` |
| Student-3 | `128.107.30.25` | `255.255.255.0` | `128.107.30.1` | `2001:DB8:B::25/64` | `FE80::1` |
| Student-4 | `128.107.30.30` | `255.255.255.0` | `128.107.30.1` | `2001:DB8:B::30/64` | `FE80::1` |

--- 

##  Step 14: Verify Connectivity

Test from Router:

```bash
College#ping 128.107.30.30
```
Test IPv6:

```bash
College#ping 2001:DB8:B::30
```

Repeat from multiple devices.


--- 

##  Step 15: Troubleshooting

If pings fail, check:

Interface Status
```bash
College#show ip interface brief
```
Look for:

- administratively down
- incorrect IP addresses

IPv6 Verification:
```bash
College#show ipv6 interface brief
```
Routing Verification:
```bash
College#show running-config
```
Confirm:

```bash
College#configure terminal
College(config)#ipv6 unicast-routing
```
exists.

--- 

## 🔗 Navigation

* **[Formative Lessons](/portfolio/formative-lessons/)**
* **[Walkthroughs](/portfolio/walkthroughs/)**
* **[Network+ Portfolio](/portfolio/)**
* **[Home](/)**

---
