---
layout: post
title: "Infrastructure | Connect a Router to a LAN"
lab_title: "Connect a Router to a LAN"

lesson: "11.0"
lesson_id: "11.08"

categories: [portfolio, labs]

category: infrastructure
category_display: Infrastructure

subcategory: routing
subcategory_display: Routing

content_type: lab
content_type_display: Lab

topics: [routing, lan-connectivity, network-infrastructure]

tools: [Router, Ethernet-Cabling, cisco-packet-tracer]

sort_order: "110800"

tags:
  - packet-tracer
  - cabling
  - topology
  - networking-basics

permalink: /portfolio/labs/module-11-0/connect-router-to-lan/
status: complete

date: 2026-04-03 08:34:11 -0700
video: ""
pdf: ""
diagram: ""

protocols: []

---

In this lab, I configured multiple router interfaces across several LANs and a WAN connection. I used verification commands to inspect interfaces, review routing tables, and test end-to-end connectivity across the network.

This lab helped reinforce how routers connect multiple networks and how routing tables help determine packet paths.
<!--more-->

---

# Network Topology

<img src="{{ '/assets/images/packet-tracer/Connect-Router-To-LAN-table-image.jpg' | relative_url }}" sizes="medium">

---

<img src="{{ '/assets/images/packet-tracer/Connect-Router-To-LAN-topology-image.jpg' | relative_url }}" sizes="medium">

---

# Part 1: Display Router Information

Access R1:

```bash
Router> enable
Password: class
Router#
```

---

## View All Interface Statistics

```bash
R1# show interfaces
```

Displays all router interfaces.

---

## View Serial Interface Information

```bash
R1# show interfaces serial 0/0/0
```

Use this to verify:

- IP address  
- bandwidth  
- interface status  

---

## View Gigabit Interface Information

```bash
R1# show interfaces gigabitEthernet 0/0
```

Use this to verify:

- IP address  
- MAC address  
- bandwidth  

---

# View Interface Summary

```bash
R1# show ip interface brief
```

This displays:

- interface names  
- IP addresses  
- status  
- protocol status  

---

# View Routing Table

```bash
R1# show ip route
```

Look for:

```text
C
```

Connected routes

```text
O
```

OSPF learned routes

---

# Part 2: Configure Router Interfaces

---

# Configure R1 G0/0

```bash
R1# configure terminal
R1(config)# interface gigabitEthernet 0/0
R1(config-if)# ip address 192.168.10.1 255.255.255.0
R1(config-if)# no shutdown
R1(config-if)# description LAN connection to S1
R1(config-if)# exit
```

---

# Configure R1 G0/1

```bash
R1(config)# interface gigabitEthernet 0/1
R1(config-if)# ip address 192.168.11.1 255.255.255.0
R1(config-if)# no shutdown
R1(config-if)# description LAN connection to PC2 network
R1(config-if)# exit
```

---

# Configure R2 G0/0

```bash
R2# configure terminal
R2(config)# interface gigabitEthernet 0/0
R2(config-if)# ip address 10.1.1.1 255.255.255.0
R2(config-if)# no shutdown
R2(config-if)# description LAN connection to PC3 network
R2(config-if)# exit
```

---

# Configure R2 G0/1

```bash
R2(config)# interface gigabitEthernet 0/1
R2(config-if)# ip address 10.1.2.1 255.255.255.0
R2(config-if)# no shutdown
R2(config-if)# description LAN connection to PC4 network
R2(config-if)# exit
```

---

# Save Configurations

R1:

```bash
R1# copy running-config startup-config
```

R2:

```bash
R2# copy running-config startup-config
```

---

# Part 3: Verify Configuration

---

## Verify Interface Status

```bash
R1# show ip interface brief
R2# show ip interface brief
```

Confirm interfaces show:

```text
up/up
```

---

## Verify Routing Tables

```bash
R1# show ip route
R2# show ip route
```

Verify:

- Connected routes  
- OSPF routes  
- WAN routes  
- LAN routes  

---

# Test Connectivity

From PC1:

```bash
C:\> ping 10.1.2.10
```

---

From R2:

```bash
R2# ping 192.168.11.10
```

---

All devices should successfully communicate.

---

# Troubleshooting

If interfaces show:

```text
administratively down
```

Fix:

```bash
R1(config-if)# no shutdown
```

---

If pings fail:

Check:

- IP addresses  
- subnet masks  
- default gateways  
- interface status  
- routing table entries  

---

If routes are missing:

```bash
R1# show ip route
```

Verify OSPF learned routes exist.

---

# Commands Used (In Order)

```bash
enable
show interfaces
show interfaces serial 0/0/0
show interfaces gigabitEthernet 0/0
show ip interface brief
show ip route

configure terminal

interface gigabitEthernet 0/0
ip address
no shutdown
description
exit

interface gigabitEthernet 0/1
ip address
no shutdown
description
exit

copy running-config startup-config

ping
```

---

# Key Takeaways

This lab reinforced:

- LAN routing  
- WAN connectivity  
- interface configuration  
- routing table analysis  
- OSPF verification  
- end-to-end troubleshooting  

This felt like one of my first true multi-network routing labs where everything began working together.

---
---
---

## 🔗 Navigation

* **[HOME](/)**
* [Network+ Portfolio](/portfolio/)
  * [Formative Lessons](/portfolio/formative-lessons/)
  * [Lab Walkthroughs](/portfolio/labs/)
  * [Video Walkthroughs](/portfolio/videos/)
  * [Study Diagrams](/portfolio/study-diagrams/)
* [zBible Study](/zBible-Study/)
* [About Me](/about/)

---
---
---