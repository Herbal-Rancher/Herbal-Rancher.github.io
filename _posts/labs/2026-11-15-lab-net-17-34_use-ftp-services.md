---
layout: post
title: "Lab 34| Cisco Networking Labs - Use FTP Services"
lab_title: "Use FTP Services"

lesson: "17.0"
lesson_id: "17.34.00"
sort_order: "173400"

categories:
  - portfolio
  - labs

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: network-services
subcategory_display: Network Services

content_type: lab
content_type_display: Lab Documentation

tags:
  - packet-tracer
  - ftp
  - file-transfer
  - client-server
  - tcp

topics:
  - ftp-client-operations
  - upload-and-download
  - file-transfer-verification

tools:
  - cisco-packet-tracer
  - ftp-client
  - command-prompt

protocols:
  - FTP
  - TCP
  - IPv4

status: complete

video_id: ""
video_url: ""
thumbnail: ""

completed_lab: "/assets/pdfs/Module-17-Lab-34-Packet-Tracer-Use-FTP-Server.pdf"
lab_pdf: "/assets/pdfs/Module-17-Lab-34-Packet-Tracer-Use-FTP-Server.pdf"
permalink: /network-portfolio/videos/17-34-use-ftp-services/
diagram: ""
---

## Overview

Practice client–server file transfer using Packet Tracer FTP services. Connect to `ftp.pka` (`209.165.200.226`), inspect remote files, upload a sample file, and retrieve a file to the local workstation.

<!--more-->

---

## Preconditions

![Packet Tracer Lab 34 - Use FTP Services - Preconditions](/assets/images/packet-tracer/cisco-lab-topology-module-17-Lab-34.png)

---

## Skills Practiced

- Connect and authenticate to an FTP server
- Use directory listing and file-transfer commands
- Verify uploads and downloads from client and server perspectives

---

## Video Walkthrough

This lab is documented as a written exercise; no video walkthrough is planned.

{% if page.video_id != "" %}
<iframe width="560" height="315" src="https://www.youtube.com/embed/{{ page.video_id }}" title="{{ page.title }}" frameborder="0" allowfullscreen></iframe>
{% endif %}

---

## Completed Lab Documentation

- Note: [Completed Lab PDF may be available upon request]

---

## Key Observations

FTP separates commands from file data and supports remote file management. Standard FTP does not encrypt credentials or transferred content, so secure alternatives are preferable on real networks.

### Activity Focus

1. Locate `sampleFile.txt` on PC-A and establish an FTP session.
2. Use FTP commands to list files and transfer a local file to the server.
3. Practice remote file management and retrieve a file to the client.

### Notes

The worksheet uses traditional FTP in a controlled lab. For production environments, evaluate SFTP or FTPS instead.

---

## Validation

Confirm the expected file appears in the remote directory and the downloaded file is present locally.


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
