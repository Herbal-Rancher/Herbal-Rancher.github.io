---

layout: post
title: "Systems Administration | Creating an iSCSI Storage Target and Virtual SAN Disk"
lab_title: "Creating an iSCSI Storage Target and Virtual SAN Disk"

lesson: "4.0"
lesson_id: "14.01.05"
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
* [Trading+](/trading/)
* [Bible Study](/bible-study/)
* [About the Portfolio](/about/)

---
---
---