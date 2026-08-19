---
layout: post
title: "Lab 17 | Cisco Networking Labs - Configure DHCP on a Wireless Router"
lab_title: "Configure DHCP on a Wireless Router"

lesson: "14.0"
lesson_id: "14.17.00"
sort_order: "141700"

categories: [portfolio, videos]

category: cisco-networking-labs
category_display: Cisco Networking Labs

subcategory: dhcp
subcategory_display: DHCP

content_type: video
content_type_display: Video

tags:

- cisco
- packet-tracer
- dhcp
- ipv4
- wireless-router
- dynamic-addressing
- ip-configuration
- ping
- connectivity-testing

topics:

- dhcp
- ipv4-addressing
- wireless-router-configuration
- client-configuration
- dynamic-ip-addressing
- connectivity-testing

tools:

- Cisco Packet Tracer
- Wireless Router
- Web Browser
- IP Configuration
- Command Prompt
- Ping
- Ipconfig

protocols:

- DHCP
- IPv4
- ICMP
- TCP-IP

permalink: /network-portfolio/videos/14-17-configure-dhcp-wireless-router/

status: complete
completed_lab: "/assets/pdfs/Module-14-Lab-17-Packet-Tracer-Configure-DHCP-wireless-router.pdf"
lab_pdf: "/assets/pdfs/Module-14-Lab-17-Packet-Tracer-Configure-DHCP-wireless-router.pdf"

video_id: ""
video_url: ""
thumbnail: ""


---

## Overview

This guided technical walkthrough demonstrates how to configure DHCP on a wireless router, modify the router's IPv4 network and DHCP address pool, configure client devices to obtain addresses automatically, and verify network connectivity using Cisco Packet Tracer.

<!--more-->

---

> **Portfolio Note**
>
> This page documents my networking learning journey. The accompanying video demonstrates this exercise using Cisco Packet Tracer for educational purposes.

---

## Preconditions

Before beginning this exercise, have available:

- Cisco Packet Tracer
- Wireless router
- Three generic PCs
- Copper straight-through Ethernet cables
- Lab instructions


![Lab 17 Topology Screenshot](/assets/images/packet-tracer/cisco-lab-topology-module-14-lab-17-configure-dhcp-on-wireless.png)


---

## Learning Objectives

By completing this exercise you will learn how to:

- Connect multiple PCs to a wireless router
- Examine default DHCP settings
- Configure a wireless router's IPv4 address
- Modify a DHCP address pool
- Configure clients to obtain IPv4 addresses dynamically
- Verify DHCP-assigned addressing with `ipconfig`
- Test connectivity using `ping`
- Validate communication between network devices

---

## Lab Environment

This exercise uses a wireless router to provide network connectivity and DHCP services for three Ethernet-connected PCs.

The router initially uses the default gateway address:

`192.168.0.1`

During the exercise, the LAN is reconfigured to use:

`192.168.5.0/24`

The wireless router becomes the default gateway at:

`192.168.5.1`

The DHCP pool is then configured to begin at:

`192.168.5.126`

with a maximum of:

`75 clients`

---

## Part 1: Set Up the Network Topology

Add three generic PCs to the Packet Tracer workspace.

Connect each PC to an Ethernet port on the wireless router using copper straight-through cables.

Wait for the Ethernet link indicators to transition from amber to green before continuing.

---

## Part 2: Observe the Default DHCP Settings

On **PC0**:

1. Select **Desktop**.
2. Open **IP Configuration**.
3. Select **DHCP**.
4. Allow PC0 to obtain its IPv4 configuration automatically.

The initial default gateway is:

`192.168.0.1`

Close IP Configuration and open the **Web Browser**.

Navigate to:

`192.168.0.1`

Authenticate to the wireless router using the credentials provided by the lab.

Review the **Basic Setup** page and identify:

- Router IPv4 address
- DHCP server status
- Starting DHCP address
- Maximum number of DHCP clients

---

## Part 3: Change the Router IP Address

Within the router's **Router IP Settings**, change the router IPv4 address to:

`192.168.5.1`

Scroll to the bottom of the page and select **Save Settings**.

Because the router's management address has changed, the existing browser session can no longer communicate with the router at its previous address.

Close the browser.

On **PC0**, open **IP Configuration** and force the client to renew its network configuration:

1. Select **Static**.
2. Select **DHCP**.

PC0 should receive new IPv4 configuration information for the `192.168.5.0/24` network.

Open the browser again and navigate to:

`192.168.5.1`

Authenticate to the wireless router.

---

## Part 4: Configure the DHCP Address Range

Observe that the DHCP Server Start IP Address has automatically changed to match the router's new network.

Change the DHCP configuration to:

| Setting | Configuration |
|---|---|
| Router IP | `192.168.5.1` |
| Starting DHCP Address | `192.168.5.126` |
| Maximum Number of Users | `75` |

Select **Save Settings** and close the browser.

On **PC0**, renew the DHCP lease again:

1. Open **IP Configuration**.
2. Select **Static**.
3. Select **DHCP**.

Open **Command Prompt** and enter:

```text
ipconfig
````

PC0 should receive the first available address from the newly configured DHCP pool.

### PC0 Address

`192.168.5.126`

---

## Part 5: Enable DHCP on the Remaining PCs

### PC1

Select:

**PC1 → Desktop → IP Configuration → DHCP**

PC1 should receive the next available DHCP address.

### PC1 Address

`192.168.5.127`

### PC2

Repeat the DHCP configuration process:

**PC2 → Desktop → IP Configuration → DHCP**

PC2 should receive another available address from the configured DHCP pool.

The clients are now configured to obtain their IPv4 settings automatically from the wireless router.

---

## Part 6: Verify Connectivity

On **PC2**, select:

**Desktop → Command Prompt**

Display the DHCP-assigned configuration:

```text
ipconfig
```

Verify connectivity to the wireless router:

```text
ping 192.168.5.1
```

Verify connectivity to PC0:

```text
ping 192.168.5.126
```

Verify connectivity to PC1:

```text
ping 192.168.5.127
```

Successful replies confirm communication between the DHCP clients and their default gateway.

---

## Validation

The completed network should demonstrate:

* Wireless router configured as `192.168.5.1`
* DHCP server enabled
* DHCP pool beginning at `192.168.5.126`
* Maximum DHCP clients configured for `75`
* PC0 receiving `192.168.5.126`
* PC1 receiving `192.168.5.127`
* PC2 receiving an address dynamically
* Clients using `192.168.5.1` as their default gateway
* Successful ICMP communication between devices

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

## Concepts Reinforced

* DHCP
* Dynamic IPv4 Addressing
* DHCP Address Pools
* IPv4 Network Configuration
* Default Gateways
* Client Address Assignment
* DHCP Lease Renewal
* Wireless Router Configuration
* ICMP
* Network Connectivity

---

## Skills Practiced

* Cisco Packet Tracer
* DHCP Configuration
* Wireless Router Configuration
* IPv4 Addressing
* Client IP Configuration
* DHCP Lease Renewal
* `ipconfig`
* `ping`
* Connectivity Testing
* Technical Documentation

---

## Why This Matters

DHCP simplifies network administration by automatically assigning IPv4 configuration information to client devices. Instead of manually configuring an IP address, subnet mask, default gateway, and other network settings on every host, administrators can centrally define an address pool and allow DHCP to distribute valid configurations automatically.

Understanding how to configure DHCP scopes, renew client addressing, and verify connectivity is an important networking skill for supporting home, small-business, and enterprise networks.

---

## Related Resources

Study Diagrams

* DHCP Process
* IPv4 Address Structure
* IPv4 Subnet Masks
* Default Gateway & OSI Model
* MAC Address vs IP Address
* Packet Flow Through a Router
* Network Troubleshooting Flowchart


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