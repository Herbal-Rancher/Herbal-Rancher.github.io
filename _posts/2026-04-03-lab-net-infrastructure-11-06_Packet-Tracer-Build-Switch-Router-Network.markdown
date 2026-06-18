---
layout: post
title: "Infrastructure | Build a Switch and Router Network"
lab_title: "Build a Switch and Router Network"

lesson: "11.0"
lesson_id: "11.06.00"
sort_order: "110600"

categories: [portfolio, labs]

category: infrastructure
category_display: Infrastructure

subcategory: network-services-devices
subcategory_display: Network Services & Devices

content_type: lab
content_type_display: Lab

topics: [switching, routing, network-design, infrastructure]

tools: [Switch, Router]

tags: 
  - packet-tracer
  - cabling
  - topology
  - networking-basics

permalink: /network-portfolio/labs/module-11-0/build-switch-router-network/
status: complete

date: 2026-04-03 06:54:11 -0700
video: ""
pdf: ""
diagram: ""

protocols: []

---

In this lab, I built a small network by connecting a router, switch, and two PCs. I configured device security settings, assigned IP addresses, verified connectivity, reviewed device information, and implemented secure remote SSH access.

<!--more-->
---

# Network Topology

<img src="{{ '/assets/images/packet-tracer/Build-Switch-Router-Network-table-image.jpg' | relative_url }}" sizes="medium">

---

# Part 1: Connect Devices

Connect:

- PC-A F0 → S1 F0/1  
- S1 G0/1 → R1 G0/0/1  
- R1 G0/0/0 → PC-B F0  

Use proper Ethernet cables.

---

# Part 2: Configure PC Addresses

Configure:

### PC-A
- IP Address: `192.168.1.3`
- Subnet Mask: `255.255.255.0`
- Default Gateway: `192.168.1.1`

### PC-B
- IP Address: `192.168.0.3`
- Subnet Mask: `255.255.255.0`
- Default Gateway: `192.168.0.1`

---

## Initial Connectivity Test

From PC-A:

```bash
ping 192.168.0.3
```

Initial ping fails because router interfaces are not configured yet.

---

# Part 3: Configure Router R1

Enter privileged mode:

```bash
enable
```

Enter configuration mode:

```bash
configure terminal
```

Configure hostname:

```bash
hostname R1
```

Configure enable secret:

```bash
enable secret class
```

Configure console password:

```bash
line console 0
password cisco
login
exit
```

Encrypt passwords:

```bash
service password-encryption
```

Configure MOTD banner:

```bash
banner motd "Unauthorized access is prohibited."
```

---

## Configure Router Interfaces

Configure G0/0/0:

```bash
interface g0/0/0
ip address 192.168.0.1 255.255.255.0
no shutdown
exit
```

Configure G0/0/1:

```bash
interface g0/0/1
ip address 192.168.1.1 255.255.255.0
no shutdown
exit
```

Save configuration:

```bash
copy running-config startup-config
```

---

# Verify Connectivity

From PC-A:

```bash
ping 192.168.0.3
```

Pings should now succeed because the router is routing traffic between both networks.

---

# Part 4: Configure Switch S1

Enter privileged mode:

```bash
enable
```

Enter configuration mode:

```bash
configure terminal
```

Configure hostname:

```bash
hostname S1
```

Configure enable secret:

```bash
enable secret class
```

Configure console password:

```bash
line console 0
password cisco
login
exit
```

Encrypt passwords:

```bash
service password-encryption
```

Configure MOTD banner:

```bash
banner motd "Unauthorized access is prohibited."
```

---

## Configure VLAN 1 Management Interface

```bash
interface vlan 1
ip address 192.168.1.2 255.255.255.0
no shutdown
exit
```

Configure default gateway:

```bash
ip default-gateway 192.168.1.1
```

Save configuration:

```bash
copy running-config startup-config
```

---

# Part 5: Display Device Information

View IOS version:

```bash
show version
```


View routing table:

```bash
show ip route
```

Directly connected networks will display a:

```bash
C
```


---

View detailed interface information:

```bash
show interfaces g0/0/1
```

---

View interface summary:

```bash
show ip interface brief
```

---

# Part 6: Configure SSH Remote Access

Configure domain name:

```bash
ip domain-name academy.net
```

Generate RSA keys:

```bash
crypto key generate rsa
```

Enter:

```bash
1024
```

Create local SSH user:

```bash
username SSHuser secret cisco
```

Configure VTY lines:

```bash
line vty 0 4
login local
transport input ssh
exit
```

Save configuration:

```bash
copy running-config startup-config
```

---

# Part 7: Verify SSH Access

From PC-A command prompt:

```bash
ssh -l SSHuser 192.168.1.1
```

Enter password:

```bash
cisco
```

Successful login should place you at the R1 CLI remotely.

---

# Troubleshooting

If interfaces show:

```bash
administratively down
```

Fix with:

```bash
no shutdown
```

---

If devices cannot ping:

Check:

- IP addresses  
- Subnet masks  
- Default gateways  
- Cabling  
- Interface status  

---

If SSH fails:

```bash
show ip ssh
```

Verify:

- RSA keys exist  
- Username exists  
- VTY lines allow SSH only  

---

# Commands Used (In Order)

```bash
enable
configure terminal
hostname R1
enable secret class

line console 0
password cisco
login
exit

service password-encryption
banner motd "Unauthorized access is prohibited."

interface g0/0/0
ip address 192.168.0.1 255.255.255.0
no shutdown
exit

interface g0/0/1
ip address 192.168.1.1 255.255.255.0
no shutdown
exit

copy running-config startup-config

hostname S1
enable secret class

line console 0
password cisco
login
exit

service password-encryption
banner motd "Unauthorized access is prohibited."

interface vlan 1
ip address 192.168.1.2 255.255.255.0
no shutdown
exit

ip default-gateway 192.168.1.1

copy running-config startup-config

show version
show ip route
show interfaces g0/0/1
show ip interface brief

ip domain-name academy.net
crypto key generate rsa
1024

username SSHuser secret cisco

line vty 0 4
login local
transport input ssh
exit

copy running-config startup-config

ssh -l SSHuser 192.168.1.1
```

---

# Key Takeaways

This lab combined:

- Routing  
- Switching  
- IP addressing  
- Network troubleshooting  
- Device verification  
- Secure remote access

This was one of my first full network builds that included both infrastructure configuration and SSH security implementation.


---
---
---

## 🔗 Navigation

* **[HOME](/)**
* [Network+ Portfolio](/network-portfolio/)
  * [Formative Lessons](/network-portfolio/formative-lessons/)
  * [Lab Walkthroughs](/network-portfolio/labs/)
  * [Video Walkthroughs](/network-portfolio/videos/)
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* [Bible Study](/network-portfolio/Bible-Study/)
* [Behind the Portfolio](/network-portfolio/behind-the-portfolio/)

---
---
---
