---
layout: post
title: "Windows Server DNS | Create Alias (CNAME) Records"
lab_title: "Create Alias (CNAME) Records"

lesson: "4.0"
lesson_id: "06.05.14"
sort_order: "060514"

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
- cname
- alias-record
- dns-records
- name-resolution

topics:

- dns-records
- cname-records
- forward-lookup-zone
- enterprise-networking
- windows-server-dns

tools:

- Windows Server
- DNS Manager

protocols:

- DNS
- IPv4
- TCP-IP
- HTTP

permalink: /network-portfolio/videos/06-05-14-create-cname-records/

status: complete

video_id: "REPLACE_WITH_YOUTUBE_ID"
video_url: "REPLACE_WITH_YOUTUBE_URL"
thumbnail: "https://img.youtube.com/vi/REPLACE_WITH_YOUTUBE_ID/hqdefault.jpg"
---

## Overview

This guided walkthrough demonstrates how to create Alias (CNAME) records using Windows Server DNS Manager.

<!--more-->

The exercise shows how multiple DNS names can reference a single host, allowing users to access the same service through different, easy-to-remember names.

---

> **Portfolio Note**
>
> This page documents my personal learning journey through networking, systems administration, and cybersecurity. The accompanying walkthrough demonstrates concepts and techniques using a hands-on lab environment for educational purposes.

---

## Preconditions

A forward lookup zone has already been created.

The destination host already exists in DNS.

Use the lab environment or reference image for:

- Zone name
- Alias names
- Target host (FQDN)


![Create CNAME Records image](/assets/images/labs/060514-create-cname-records.png)

---

## Before You Begin

A Canonical Name (CNAME) record creates an alias that points to another DNS host record.

Instead of assigning multiple IP addresses to a server, multiple DNS names can reference a single host.

This simplifies administration because only the Host (A) record must be updated if the server's IP address changes.

---

## Objectives

In this walkthrough you will:

- Open the DNS Manager console.
- Create Alias (CNAME) records.
- Specify the target host.
- Verify successful name resolution.

---

## Guided Walkthrough

### Create Alias Records

1. Open **DNS Manager**.
2. Browse to the forward lookup zone.
3. Create a new **Alias (CNAME)** record.
4. Specify the alias name.
5. Enter the fully qualified domain name (FQDN) of the destination host.
6. Save the record.
7. Repeat for each required alias.

---

## Verification

Verify that:

- Each Alias (CNAME) record exists.
- Each alias references the correct destination host.
- Name resolution succeeds for each alias.
- All aliases resolve to the same server.

---

## Skills Practiced

- Windows Server Administration
- DNS Administration
- Alias (CNAME) Records
- Forward Lookup Zones
- DNS Name Resolution
- Enterprise DNS Configuration
- Configuration Verification
- Technical Documentation

---

## Related Exercise

Course Module

- 4.0

Original Exercise

- Create CNAME Records (Lab: 6.5.14)

---

## Why This Matters

CNAME records allow administrators to provide multiple friendly names for the same service without creating duplicate Host (A) records.

This simplifies DNS management and reduces administrative overhead when server IP addresses change.

---

## Video Walkthrough

<a href="{{ page.video_url }}" target="_blank" rel="noopener noreferrer">

<img src="{{ page.thumbnail }}"
alt="{{ page.title }}"
style="width:420px; border-radius:8px;">

</a>

---

## Key Takeaways

Alias (CNAME) records provide flexible name resolution by allowing multiple DNS names to reference a single host. They are commonly used for websites, applications, and services that require multiple user-friendly addresses.

---

## DNS Concepts Reinforced

- A CNAME record points to another DNS host name—not directly to an IP address.
- Multiple aliases can reference the same destination host.
- Updating a single Host (A) record automatically benefits all associated aliases.
- CNAME records simplify DNS administration and improve maintainability.

---

## Related Resources

Study Diagrams

- DNS Record Types
- Host (A) vs. Alias (CNAME)
- Forward Lookup Zones

Reference Tools

- DNS Manager
- nslookup
- ping
- ipconfig /displaydns


---
---
---

## 🔗 Navigation

* **[HOME](/)**
* [Network+ Portfolio](/network-portfolio/)
  * [Formative Modules](/network-portfolio/formative-modules/)
  * [Video Walkthroughs](/network-portfolio/videos/)
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* [Bible Study](/bible-study/)
* [Behind the Portfolio](/network-portfolio/behind-the-portfolio/)

---
---
---