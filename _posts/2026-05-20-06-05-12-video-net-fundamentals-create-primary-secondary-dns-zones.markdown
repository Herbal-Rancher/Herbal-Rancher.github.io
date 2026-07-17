---
layout: post
title: "Windows Server DNS | Create Primary and Secondary Forward Lookup Zones"
lab_title: "Create Primary and Secondary Forward Lookup Zones"

lesson: "4.0"
lesson_id: "06.05.12"
sort_order: "060512"

categories: [portfolio, videos]

category: windows-server
category_display: Windows Server

subcategory: dns
subcategory_display: Domain Name System (DNS)

content_type: video
content_type_display: Guided Technical Walkthrough

tags:

- dns
- windows-server
- forward-lookup-zone
- primary-zone
- secondary-zone
- zone-transfers

topics:

- dns-zones
- forward-lookup-zones
- zone-replication
- windows-server-dns
- enterprise-networking

tools:

- Windows Server
- DNS Manager

protocols:

- DNS
- TCP-IP

permalink: /network-portfolio/videos/06-05-12-create-primary-secondary-dns-zones/

status: complete

video_id: "IcGvzFyx5kE"
video_url: "https://youtu.be/IcGvzFyx5kE"
thumbnail: "https://img.youtube.com/vi/IcGvzFyx5kE/hqdefault.jpg"
---

## Overview

This guided walkthrough demonstrates how to create both primary and secondary forward lookup zones using Windows Server DNS Manager.

<!--more-->

The exercise introduces standard DNS zones, zone transfers, and the relationship between primary and secondary DNS servers in an enterprise environment.

---

## Video Walkthrough

Watch the complete walkthrough:

<a href="{{ page.video_url }}" target="_blank" rel="noopener noreferrer">
  <img src="{{ page.thumbnail }}"
       alt="{{ page.title }}"
       style="width:420px; border-radius:8px;">
</a>

---

> **Portfolio Note**
>
> This page documents my personal learning journey through networking, systems administration, and cybersecurity. The accompanying walkthrough demonstrates concepts and techniques using a hands-on lab environment for educational purposes.

---

## Preconditions

The DNS server infrastructure has already been installed and configured.

Use the lab instructions or environment image as a reference for:

- Zone name
- Master DNS server
- Zone transfer settings

![Create primary secondary dns zones image](/assets/images/labs/060512-create-standard-dns-zones-2.png)

---

## Before You Begin

DNS zones organize and store DNS records.

A **Primary Zone** contains the writable copy of the DNS database.

A **Secondary Zone** stores a read-only copy obtained through zone transfers, providing redundancy and faster name resolution.

---

## Objectives

In this walkthrough you will:

- Create a primary forward lookup zone.
- Configure zone settings.
- Allow zone transfers.
- Create a secondary forward lookup zone.
- Specify the master DNS server.
- Verify successful zone replication.

---

## Guided Walkthrough

### Create the Primary Zone

1. Open **DNS Manager**.
2. Create a new **Primary Forward Lookup Zone**.
3. Configure the required zone settings.
4. Save the new zone.

---

### Configure Zone Transfers

1. Open the zone properties.
2. Enable zone transfers.
3. Apply the required transfer settings.

---

### Create the Secondary Zone

1. Create a new **Secondary Forward Lookup Zone**.
2. Specify the master DNS server.
3. Complete the wizard.
4. Verify successful zone synchronization.

---

## Verification

Verify that:

- The primary zone was created successfully.
- Zone transfers are enabled.
- The secondary zone loads correctly.
- DNS records replicate successfully.

---

## Skills Practiced

- Windows Server Administration
- DNS Administration
- Primary DNS Zones
- Secondary DNS Zones
- Forward Lookup Zones
- Zone Transfers
- Enterprise DNS Configuration
- Technical Documentation

---

## Related Exercise

Course Module

- 4.0

Original Exercise

- Create Standard DNS Zones (Lab: 6.5.12)

---

## Why This Matters

Enterprise DNS environments commonly use multiple DNS servers for redundancy and performance.

Understanding how primary and secondary zones work together helps administrators improve availability while reducing single points of failure.

---

## Key Takeaways

Primary and secondary DNS zones improve reliability by distributing DNS data across multiple servers. Properly configuring zone transfers ensures that secondary servers maintain accurate, read-only copies of the DNS database.

---

## Related Resources

Study Diagrams

- DNS Resolution Process
- Primary vs Secondary DNS Zones
- Forward Lookup Zones

Reference Tools

- DNS Manager
- nslookup
- ipconfig /all



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