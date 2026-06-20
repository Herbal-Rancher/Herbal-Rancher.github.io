---
layout: post
title: "Systems Administration | Connecting an iSCSI Initiator to Network Storage"
lab_title: "Connecting an iSCSI Initiator to Network Storage"

lesson: "4.0"
lesson_id: "14.01.06"
sort_order: "140106"

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
- disk-management
- volume-management
- enterprise-storage

topics:
- iscsi-initiator
- storage-area-network
- storage-connectivity
- disk-provisioning
- volume-creation
- enterprise-storage

tools:
- Windows-Server
- iSCSI-Initiator
- Disk-Management

protocols:
- iSCSI
- TCP-IP

permalink: /portfolio/videos/iscsi-initiator-storage-configuration/

status: complete

video_id: "AN-Jk9wIdDo"
video_url: "https://www.youtube.com/watch?v=AN-Jk9wIdDo"
thumbnail: "https://img.youtube.com/vi/AN-Jk9wIdDo/hqdefault.jpg"

date: 2026-06-19 19:00:00 -0700
last_updated: 2026-06-19 19:00:00 -0700

---

## Overview

This walkthrough demonstrates how a server can connect to centralized storage through an iSCSI Storage Area Network (SAN) and make that storage available for operating system and user access.

<!--more-->

Once storage is provisioned by an iSCSI target, authorized servers can discover the resource, establish a connection, bring the disk online, and create usable volumes.

---

## Concepts Explored

* Storage Area Networks (SAN)
* iSCSI Initiators
* Network Storage
* Disk Management
* Volume Provisioning
* Enterprise Infrastructure

---

## Understanding the iSCSI Workflow

A complete iSCSI implementation consists of two primary components:

### iSCSI Target

The target server hosts storage resources and makes them available across the network.

Responsibilities include:

* Hosting virtual disks
* Managing access permissions
* Providing centralized storage

---

### iSCSI Initiator

The initiator is the client system that consumes the storage resources.

Responsibilities include:

* Discovering storage targets
* Establishing connections
* Accessing remote disks
* Creating usable volumes

---

## Storage Provisioning Process

### Discover Available Targets

The initiator identifies storage resources that have been assigned to it.

Benefits include:

* Centralized storage management
* Controlled access
* Simplified administration

---

### Connect to Storage

Once discovered, the initiator establishes a session with the storage target.

This allows the remote storage device to appear as a local disk.

---

### Bring the Disk Online

Newly connected storage often appears offline until explicitly activated by the operating system.

Once online, the storage becomes available for partitioning and volume creation.

---

### Create a Volume

After the disk is online:

* A volume can be created
* A file system can be applied
* A drive letter can be assigned
* Storage becomes available to users and applications

---

## Why NTFS Is Commonly Used

NTFS provides:

* File permissions
* Encryption support
* Compression
* Reliability
* Large volume support

It remains one of the most widely used file systems in Windows Server environments.

---

## Skills Practiced

* Storage Administration
* SAN Connectivity
* Disk Provisioning
* Volume Management
* Enterprise Storage
* Systems Administration

---

## Real-World Applications

iSCSI storage solutions are commonly deployed in:

* File Servers
* Virtualization Hosts
* Backup Servers
* Database Servers
* Hyper-V Environments
* Enterprise Storage Systems

---

## Relationship to the Previous iSCSI Target Configuration

In the previous exercise, storage resources were created and published by an iSCSI target server.

In this exercise, those storage resources are consumed by an authorized initiator system and configured for operational use.

Together, these two processes demonstrate the complete lifecycle of iSCSI storage deployment.

---

## Video Walkthrough

<a href="{{ page.video_url }}" target="_blank" rel="noopener noreferrer">
  <img src="{{ page.thumbnail }}"
       alt="{{ page.title }}"
       style="width:420px; border-radius:8px;">
</a>

---

## Key Takeaway

iSCSI allows organizations to deliver enterprise storage across standard Ethernet infrastructure. Understanding how initiators discover, connect to, and provision remote storage is a foundational skill for modern systems administrators and infrastructure engineers.


---
---
---

## 🔗 Navigation

* [Home](/)
* [Network+ Portfolio](/network-portfolio/)
  * [Formative Lessons](/network-portfolio/formative-lessons/)
  * **[VIDEO WALKTHROUGHS](/network-portfolio/videos/)**
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* [Bible Study](/network-portfolio/Bible-Study/)
* [Behind the Portfolio](/network-portfolio/behind-the-portfolio/)

---
---
---