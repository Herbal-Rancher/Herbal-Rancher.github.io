---

layout: post
title: "Systems Administration | Creating an iSCSI Storage Target and Virtual SAN Disk"
lab_title: "Creating an iSCSI Storage Target and Virtual SAN Disk"

lesson: "4.0"
lesson_id: "14.01.05"
---

layout: post
title: "Systems Administration | Configuring a Static IPv4 Address on Linux"
lab_title: "Configuring a Static IPv4 Address on Linux"

lesson: "4.0"
lesson_id: "04.02.11"

sort_order: "040211"

categories: [portfolio, videos]

category: systems-administration
category_display: Systems Administration

subcategory: linux-administration
subcategory_display: Linux Administration

content_type: video
content_type_display: Video

tags:

* linux
* ipv4
* dns
* networking
* static-ip
* tcp-ip

topics:

* linux-networking
* ipv4-addressing
* dns-configuration
* network-troubleshooting
* command-line-administration
* connectivity-testing

tools:

* Linux
* Terminal
* Ping
* Network-Interface

protocols:

* IPv4
* ICMP
* DNS
* TCP-IP

permalink: /portfolio/videos/linux-static-ip-configuration/

status: complete

video_id: "REPLACE_WITH_YOUTUBE_ID"
video_url: "REPLACE_WITH_YOUTUBE_URL"
thumbnail: "https://img.youtube.com/vi/REPLACE_WITH_YOUTUBE_ID/hqdefault.jpg"

date: 2026-06-19 22:00:00 -0700
last_updated: 2026-06-19 22:00:00 -0700
---------------------------------------

## Overview

This walkthrough demonstrates how to manually configure IPv4 networking on a Linux system using terminal-based administration tools.

<!--more-->

Many servers, network appliances, and infrastructure devices rely on static IP addressing. Understanding how to configure networking manually is a foundational Linux administration skill.

---

## Concepts Explored

* Linux Networking
* IPv4 Addressing
* DNS Configuration
* Default Gateways
* Network Interfaces
* Connectivity Testing

---

## Why Use Static IP Addresses?

Static addressing provides predictable network connectivity and is commonly used for:

* Servers
* Network Infrastructure
* Printers
* Storage Systems
* Virtualization Hosts
* Security Appliances

Benefits include:

* Consistent addressing
* Simplified administration
* Easier troubleshooting
* Reliable service availability

---

## Core IPv4 Components

### IP Address

The IP address uniquely identifies the device on the network.

Example:

192.168.0.254

---

### Subnet Mask

The subnet mask identifies the network and host portions of an address.

Example:

255.255.255.0

This configuration supports a Class C private network.

---

### Broadcast Address

The broadcast address allows communication to all devices within the subnet.

Example:

192.168.0.255

Broadcast traffic is often used for discovery and network services.

---

### Default Gateway

The default gateway forwards traffic destined for remote networks.

Example:

192.168.0.5

Without a gateway, communication is typically limited to the local subnet.

---

## DNS Configuration

DNS servers translate human-friendly names into IP addresses.

Examples:

* Web servers
* Email servers
* Cloud services
* Internal applications

Proper DNS configuration is required for successful hostname resolution.

---

## Removing Dynamic Configuration

Many Linux systems are initially configured to obtain network settings automatically.

When implementing a static configuration, administrators should ensure that:

* Dynamic address assignment is disabled
* Static settings are applied consistently
* DNS settings are defined manually
* Routing information is configured correctly

---

## Connectivity Verification

After configuring the interface, connectivity should be tested.

### Test Local Connectivity

Verify communication with the local gateway.

Purpose:

* Confirm interface configuration
* Verify local network access

---

### Test External Connectivity

Verify communication with an external network resource.

Purpose:

* Confirm internet connectivity
* Verify routing functionality

---

### Test DNS Resolution

Verify hostname resolution.

Purpose:

* Confirm DNS configuration
* Verify name resolution services

Successful hostname resolution confirms both network connectivity and DNS functionality.

---

## Skills Practiced

* Linux Administration
* Network Configuration
* DNS Management
* Command Line Operations
* Troubleshooting
* Connectivity Testing

---

## Real-World Applications

Linux network administration skills are commonly used in:

* Enterprise Servers
* Cloud Environments
* Data Centers
* Cybersecurity Operations
* Virtualization Platforms
* Network Infrastructure

Understanding how to manually configure networking remains an essential skill for systems administrators and network engineers.

---

## Video Walkthrough

<a href="{{ page.video_url }}" target="_blank" rel="noopener noreferrer">
  <img src="{{ page.thumbnail }}"
       alt="{{ page.title }}"
       style="width:420px; border-radius:8px;">
</a>

---

## Example Configuration

Example network parameters used in this demonstration:

* IPv4 Address: 192.168.0.254
* Subnet Mask: 255.255.255.0
* Broadcast Address: 192.168.0.255
* Default Gateway: 192.168.0.5

Example DNS Servers:

* 163.128.78.93
* 163.128.80.93

---

## Key Takeaway

Linux administrators must understand how IP addressing, gateways, DNS services, and network interfaces work together. Mastering manual network configuration provides the foundation for managing servers, cloud systems, and enterprise infrastructure.

sort_order: "140105"

categories: [portfolio, videos]

category: systems-administration
category_display: Systems Administration

subcategory: storage-and-virtualization
subcategory_display: Storage & Virtualization

content_type: video
content_type_display: Video

tags:

- iscsi
- san
- storage
- virtualization
- virtual-disks
- storage-management

topics:

- iscsi-storage
- storage-area-network
- virtual-disk-management
- storage-provisioning
- enterprise-storage
- storage-administration

tools:

- Windows-Server
- iSCSI-Target
- Storage-Services

protocols:

- iSCSI
- TCP-IP

permalink: /portfolio/videos/iscsi-storage-target-configuration/

status: complete

video_id: "1yhCzcHFPP8"
video_url: "https://youtu.be/1yhCzcHFPP8"
thumbnail: "https://img.youtube.com/vi/1yhCzcHFPP8/hqdefault.jpg"

date: 2026-06-19 18:00:00 -0700
last_updated: 2026-06-19 18:00:00 -0700

---

## Overview

This walkthrough demonstrates how Storage Area Networks (SANs) can be implemented using iSCSI technology and standard Ethernet networking infrastructure.

<!--more-->

iSCSI provides organizations with a cost-effective method of delivering centralized storage resources over existing network infrastructure without requiring specialized Fibre Channel hardware.

---

## Concepts Explored

* Storage Area Networks (SAN)
* iSCSI Storage
* Virtual Disk Creation
* Storage Provisioning
* Storage Virtualization
* Enterprise Infrastructure

---

## What Is a SAN?

A Storage Area Network (SAN) is a dedicated storage solution that provides centralized disk resources to servers across a network.

Benefits include:

* Centralized storage management
* Improved scalability
* Simplified backups
* High availability
* Flexible resource allocation

---

## What Is iSCSI?

Internet Small Computer Systems Interface (iSCSI) allows storage traffic to be transmitted across standard TCP/IP Ethernet networks.

Benefits include:

* Lower implementation costs
* Existing Ethernet infrastructure support
* Simplified deployment
* Enterprise scalability
* Broad compatibility

---

## Core Components

### iSCSI Target

The target hosts storage resources and makes them available to authorized systems.

Responsibilities include:

* Hosting virtual disks
* Managing storage access
* Providing storage services

---

### iSCSI Initiator

The initiator is the client system that connects to and consumes storage resources.

Responsibilities include:

* Discovering available targets
* Connecting to shared storage
* Accessing virtual disks

---

### Virtual Disks

Virtual disks provide logical storage resources that can be allocated to servers and applications.

Advantages include:

* Flexible sizing
* Simplified management
* Efficient storage allocation
* Dynamic expansion options

---

## Dynamic Storage Allocation

Dynamically expanding virtual disks grow as storage is consumed.

Benefits include:

* Improved storage efficiency
* Reduced wasted disk space
* Simplified capacity planning
* Better resource utilization

---

## Skills Practiced

* Storage Administration
* SAN Deployment
* iSCSI Configuration
* Virtual Disk Management
* Storage Provisioning
* Systems Administration

---

## Real-World Applications

iSCSI storage solutions are commonly used in:

* Virtualization environments
* File servers
* Backup systems
* Small and medium businesses
* Enterprise storage infrastructures
* Hyper-V environments

---

## Video Walkthrough

<a href="{{ page.video_url }}" target="_blank" rel="noopener noreferrer">
  <img src="{{ page.thumbnail }}"
       alt="{{ page.title }}"
       style="width:420px; border-radius:8px;">
</a>

---

## Key Takeaway

iSCSI provides a powerful and cost-effective way to implement centralized storage using standard Ethernet infrastructure, making SAN technologies accessible to organizations of all sizes while supporting scalability, flexibility, and enterprise storage management.


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
* [Behind the Portfolio](/network-portfolio/behind-the-portfolio/)

---
---
---