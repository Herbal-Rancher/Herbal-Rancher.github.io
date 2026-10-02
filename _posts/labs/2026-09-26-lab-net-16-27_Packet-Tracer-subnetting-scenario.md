---
layout: post
title: "Lab 27| Cisco Networking Labs - Subnetting Scenario"
lab_title: "Subnetting Scenario"

lesson: "16.0"
lesson_id: "16.27.00"
sort_order: "162700"

categories:
  - portfolio
  - labs

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: ip-addressing
subcategory_display: IP Addressing

content_type: lab
content_type_display: Lab

tags:
  - packet-tracer
  - subnetting
  - ipv4
  - routing
  - switching
  - vlan
  - eigrp
  - connectivity-testing

topics:
  - fixed-length-subnetting
  - ipv4-addressing
  - connectivity-testing
  - subnet-assignment
  - router-interface-configuration
  - switch-management-interface
  - default-gateway
  - connectivity-verification

tools:
  - cisco-packet-tracer
  - ping
  - switch
  - command-line-interface

protocols:
  - IPv4
  - ICMP

status: complete


completed_lab: "/assets/pdfs/Module-16-Lab-27-Packet-Tracer-Subnetting-Scenario.pdf"
lab_pdf: "/assets/pdfs/Module-16-Lab-27-Packet-Tracer-Subnetting-Scenario.pdf"

permalink: /network-portfolio/videos/16-27-subnetting-scenario/
diagram: ""

---

## Overview

This Packet Tracer lab applies an IPv4 addressing plan to a routed
network containing two routers, four LANs, four switches, and four PCs.
The `192.168.100.0/24` network is divided into `/27` subnets to provide
sufficient host addresses for each LAN.

The configuration portion of the lab focuses on assigning IPv4 addresses
to router interfaces and a switch management interface, configuring
default gateways, enabling router interfaces, configuring an end device,
and verifying end-to-end connectivity. EIGRP routing between R1 and R2
is preconfigured.


---

## Preconditions

![ Preconditions - Packet Tracer Lab 27 - Subnetting Scenario](/assets/images/packet-tracer/cisco-lab-topology-module-16-lab-27.png)

---

## Skills Practiced

-   Applying a completed IPv4 subnetting plan
-   Configuring IPv4 addresses on router interfaces
-   Enabling router interfaces with `no shutdown`
-   Configuring a switch VLAN 1 management interface
-   Configuring a switch default gateway
-   Configuring host IP addressing and a default gateway
-   Verifying interface status
-   Testing local and remote connectivity with `ping`

---

## Addressing Reference

| Device | Interface | IP Address | Subnet Mask | Default Gateway |
|---|---|---|---|---|
| R1 | G0/0 | 192.168.100.1 | 255.255.255.224 | — |
| R1 | G0/1 | 192.168.100.33 | 255.255.255.224 | — |
| R1 | S0/0/0 | 192.168.100.129 | 255.255.255.224 | — |
| R2 | G0/0 | 192.168.100.65 | 255.255.255.224 | — |
| R2 | G0/1 | 192.168.100.97 | 255.255.255.224 | — |
| R2 | S0/0/0 | 192.168.100.158 | 255.255.255.224 | — |
| S1 | VLAN 1 | 192.168.100.2 | 255.255.255.224 | 192.168.100.1 |
| S2 | VLAN 1 | 192.168.100.34 | 255.255.255.224 | 192.168.100.33 |
| S3 | VLAN 1 | 192.168.100.66 | 255.255.255.224 | 192.168.100.65 |
| S4 | VLAN 1 | 192.168.100.98 | 255.255.255.224 | 192.168.100.97 |
| PC1 | NIC | 192.168.100.30 | 255.255.255.224 | 192.168.100.1 |
| PC2 | NIC | 192.168.100.62 | 255.255.255.224 | 192.168.100.33 |
| PC3 | NIC | 192.168.100.94 | 255.255.255.224 | 192.168.100.65 |
| PC4 | NIC | 192.168.100.126 | 255.255.255.224 | 192.168.100.97 |

---


## Configuration

### R1 LAN Interfaces

Configure the two R1 interfaces that serve as the default gateways for
the LANs connected to R1.

``` text
enable
configure terminal

interface gigabitEthernet 0/0
 ip address 192.168.100.1 255.255.255.224
 no shutdown
 exit

interface gigabitEthernet 0/1
 ip address 192.168.100.33 255.255.255.224
 no shutdown
 exit

end
```

The `no shutdown` command administratively enables each router interface
so connected hosts can reach their default gateway.

### S3 Management Interface

Configure VLAN 1 with the switch management address and configure R2
G0/0 as the switch's default gateway.

``` text
enable
configure terminal

interface vlan 1
 ip address 192.168.100.66 255.255.255.224
 no shutdown
 exit

ip default-gateway 192.168.100.65

end
```

The VLAN 1 address provides IP management connectivity to S3. The
`ip default-gateway` command tells the Layer 2 switch where to send
management traffic destined for networks outside its local subnet.

### PC4

Configure PC4 through **Desktop \> IP Configuration**:

``` text
IP Address:      192.168.100.126
Subnet Mask:     255.255.255.224
Default Gateway: 192.168.100.97
```

PC4's default gateway is R2 G0/1 because both addresses belong to the
`192.168.100.96/27` subnet.

---

## Validation

### Verify R1 Interfaces

``` text
show ip interface brief
```

Confirm that G0/0 and G0/1 have the expected addresses and show an
operational state of `up/up`.

### Verify S3

``` text
show ip interface brief
show running-config
```

Confirm that VLAN 1 is configured as `192.168.100.66/27` and that the
switch default gateway is `192.168.100.65`.

### Test Connectivity

Use `ping` from the devices available for testing. Begin with the local
default gateway, then test progressively farther destinations.

From PC4:

``` text
ping 192.168.100.97
ping 192.168.100.65
ping 192.168.100.1
ping 192.168.100.30
```

Successful replies confirm that PC4 can reach its local gateway and
communicate across the routed network.

---

## Troubleshooting / Notes

If connectivity fails, verify the configuration in a logical order:

1.  Confirm the device has the correct IP address and `/27` subnet mask.
2.  Confirm the default gateway is the router interface in the device's
    local subnet.
3.  On routers, verify the required interfaces have been enabled with
    `no shutdown`.
4.  Use `show ip interface brief` to check interface addresses and
    `Status/Protocol`.
5.  Test the nearest device first with `ping`, then move progressively
    across the network.
6.  If local communication works but remote communication fails, check
    routing and the remote network configuration.

A key distinction in this lab is that the **subnet address is not the
default gateway**. The default gateway for a LAN host or Layer 2 switch
is the IP address assigned to the router interface on that same subnet.

---

## Lab Result

The completed network uses four `/27` LAN subnets and one `/27` WAN
subnet from the original `192.168.100.0/24` network. Router interfaces
provide the default gateways for each LAN, the switches use VLAN 1 for
management addressing, and EIGRP provides routing between R1 and R2.

Successful pings between local and remote addresses verify the
addressing, interface configuration, default gateways, and routed
connectivity across the topology.

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
