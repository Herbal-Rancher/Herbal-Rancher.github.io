---
layout: post
title: "11.7 Packet Tracer Lab 7: Network Cabling and Physical Topology Reference"
module: 11.0
order: 11.7
categories: [portfolio, blog, labs, lab, network]
tags: [packet-tracer, cabling, topology, networking-basics]
permalink: /portfolio/labs/module-11-0/cabling-topology-reference/
---

## Module 11 Packet Tracer Lab 7:  Network Cabling and Physical Topology Reference

This lab was more exploratory than configuration-focused, but it helped reinforce foundational networking concepts related to cable selection, physical topology, and device connectivity.

Rather than creating a full walkthrough, I documented the key concepts learned for future reference.

<!--more-->
---

# Cable Types

## Copper Straight-Through

Used for connecting **unlike devices**

Examples:

- PC → Switch  
- Router → Switch  
- Wireless Router → PC  
- Cable Modem → Router  

---

## Copper Cross-Over

Used for connecting **like devices**

Examples:

- Router → PC  
- Switch → Switch  
- Router → Router (Ethernet)

In this lab:

- Router0 → Netacad.pka

Modern devices often support auto-MDIX, but older devices may still require crossover cables.

---

## Serial Cable

Used for:

- Router → Router WAN connections

In this lab:

- Router0 → Router1

This simulated WAN connectivity between routers.

---

## Console Cable

Used for:

- Local administrative configuration

In this lab:

- Configuration Terminal → Router0

This allows direct CLI access without requiring network connectivity.

---

## Coaxial Cable

Used for:

- ISP/Cable internet connections

In this lab:

- Cloud → Cable Modem

This simulated an internet service provider connection.

---

# Logical vs Physical Topology

---

## Logical Topology

Shows:

- How devices communicate
- IP addressing
- Network relationships
- Traffic flow

This is the default Packet Tracer view.

---

## Physical Topology

Shows:

- Device placement
- Rooms/buildings
- Racks
- Physical cable paths

This was explored using:

```text
Shift + P
Shift + L
```

---

# Network Layout Observations

---

## Enterprise Networks

Used:

- Server racks
- Structured cabling
- Dedicated networking rooms

Examples:

- Primary Network
- Secondary Network

---

## Home Networks

Used:

- Smaller consumer devices
- No dedicated rack
- Simplified physical layout

Example:

- Home Network

---

# Connectivity Testing

From Family PC:

```bash
C:\> ping netacad.pka
```

---

Test switch connectivity:

```bash
C:\> ping 172.16.0.2
```

---

View router interfaces:

```bash
Router> enable
Router# show ip interface brief
```

---

# Key Takeaways

This lab reinforced that networking is not only about IP addresses and configurations.

Physical infrastructure matters:

- Proper cable selection  
- Device placement  
- Physical accessibility  
- Network design  

Even perfect configurations fail if devices are connected incorrectly.



---

## 🔗 Navigation

* **[HOME](/)**
* [Network+ Portfolio](/portfolio/)
  * [Formative Modules](/portfolio/formative-modules/)
  * [Lab Walkthroughs](/portfolio/labs/)
  * [Video Walkthroughs](/portfolio/videos/)
  * [Study Diagrams](/portfolio/study-diagrams/)
* [zBible Study](/zBible-Study/)

---
