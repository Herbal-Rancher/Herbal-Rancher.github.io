---
layout: post
title: "Windows Server DNS | Create Host (A) and Pointer (PTR) Records"
lab_title: "Create Host (A) and Pointer (PTR) Records"

lesson: "4.0"
lesson_id: "06.05.13"
sort_order: "060513"

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
- host-records
- a-records
- ptr-records
- reverse-lookup-zone

topics:

- dns-records
- forward-lookup-zone
- reverse-lookup-zone
- active-directory-dns
- name-resolution

tools:

- Windows Server
- DNS Manager

protocols:

- DNS
- IPv4
- TCP-IP

permalink: /network-portfolio/videos/06-05-13-create-host-and-ptr-records/

status: complete

video_id: "REPLACE_WITH_YOUTUBE_ID"
video_url: "REPLACE_WITH_YOUTUBE_URL"
thumbnail: "https://img.youtube.com/vi/REPLACE_WITH_YOUTUBE_ID/hqdefault.jpg"
---

## Overview

This guided walkthrough demonstrates how to create a reverse lookup zone and add Host (A) records with automatically generated Pointer (PTR) records using Windows Server DNS.

<!--more-->

The exercise introduces forward and reverse name resolution while demonstrating how DNS records support device identification across a network.

---

> **Portfolio Note**
>
> This page documents my personal learning journey through networking, systems administration, and cybersecurity. The accompanying walkthrough demonstrates concepts and techniques using a hands-on lab environment for educational purposes.

---

## Preconditions

The DNS server has already been installed and configured.

Use the lab environment or provided reference image for:

- Reverse lookup subnet
- Host names
- IPv4 addresses

![Create Host and PTR Records 1 image](/assets/images/labs/060513-create-host-1.png)

![Create Host and PTR Records 2 image](/assets/images/labs/060513-create-host-2.png)

---

## Before You Begin

DNS uses **Host (A) records** to translate host names into IPv4 addresses.

**Pointer (PTR) records** perform the opposite function by resolving IPv4 addresses back to host names.

Creating the reverse lookup zone before adding Host (A) records allows PTR records to be created automatically.

---

## Objectives

In this walkthrough you will:

- Create a reverse lookup zone.
- Configure an Active Directory-integrated zone.
- Add Host (A) records.
- Automatically create Pointer (PTR) records.
- Verify forward and reverse name resolution.

---

## Guided Walkthrough

### Create the Reverse Lookup Zone

1. Open **DNS Manager**.
2. Create a new **IPv4 Reverse Lookup Zone**.
3. Configure the zone using the required settings.
4. Complete the wizard.

---

### Create Host Records

1. Open the forward lookup zone.
2. Create each Host (A) record.
3. Enable creation of the associated PTR record.
4. Save each record.

---

### Verify DNS Records

1. Confirm each Host (A) record exists.
2. Confirm each Pointer (PTR) record was created.
3. Verify forward and reverse name resolution.

---

## Verification

Verify that:

- The reverse lookup zone exists.
- All Host (A) records were created successfully.
- All PTR records were created successfully.
- Forward and reverse lookups resolve correctly.

---

## Skills Practiced

- Windows Server Administration
- DNS Administration
- Forward Lookup Zones
- Reverse Lookup Zones
- Host (A) Records
- Pointer (PTR) Records
- Active Directory Integrated DNS
- Name Resolution
- Technical Documentation

---

## Related Exercise

Course Module

- 4.0

Original Exercise

- Create Host Records (Lab: 6.5.13)

---

## Why This Matters

DNS depends on accurate resource records to resolve names and addresses across enterprise networks.

Host (A) records support forward name resolution, while Pointer (PTR) records provide reverse lookups that are commonly used for troubleshooting, logging, and security applications.

---

## Video Walkthrough

<a href="{{ page.video_url }}" target="_blank" rel="noopener noreferrer">

<img src="{{ page.thumbnail }}"
alt="{{ page.title }}"
style="width:420px; border-radius:8px;">

</a>

---

## Key Takeaways

Host (A) and Pointer (PTR) records work together to provide complete forward and reverse name resolution. Understanding how these records are created and managed is an essential skill for Windows Server and enterprise network administrators.

---

## Related Resources

Study Diagrams

- DNS Resolution Process
- Forward vs. Reverse Lookup Zones
- DNS Record Types

Reference Tools

- DNS Manager
- nslookup
- ipconfig /all
- ping


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
* [About the Portfolio](/zabout-the-portfolio/)

---
---
---