---

layout: post
title: "Lab 18| Cisco Networking Labs - Configure Basic Wireless Security"
lab_title: "Configure Basic Wireless Security"

lesson: "14.0"
lesson_id: "14.18.00"
sort_order: "141800"

categories:
- portfolio
- videos

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: wireless-networking
subcategory_display: Wireless Networking

content_type: video
content_type_display: Video

tags:
- packet-tracer
- wireless-security
- wpa2
- wireless-router
- wlan
- connectivity-testing

topics:

- wireless-security
- wpa2-personal
- wireless-router-configuration
- wireless-client-configuration
- connectivity-testing

tools:

- cisco-packet-tracer
- wireless-router
- laptop
- web-browser

protocols:
- WPA2
- HTTP
- TCP-IP

permalink: /network-portfolio/videos/13-18-configure-basic-wireless-security/

status: complete

video_id: "UUtZbu1gTKk"
video_url: "https://youtu.be/UUtZbu1gTKk"
thumbnail: "https://img.youtube.com/vi/UUtZbu1gTKk/hqdefault.jpg"


lab_pdf: "/assets/pdfs/Module-14-Lab-18-Packet-Tracer-Configure-basic-wireless-security.pdf"
completed_lab: "/assets/pdfs/Module-14-Lab-18-Packet-Tracer-Configure-basic-wireless-security.pdf"
---

## Overview

This Packet Tracer walkthrough demonstrates how I configured **WPA2 Personal wireless security** on a small-business wireless network. I secured the 2.4 GHz WLAN with a pre-shared key, updated the laptop's wireless configuration, reconnected it to the secured network, and verified connectivity.

<!--more-->
---

## Preconditions

![Packet Tracer Lab 18 - Configure Basic Wireless Security](/assets/images/packet-tracer/cisco-lab-topology-module-14-lab-18.png)

---

## Skills Practiced

* Configure Basic Wireless Security (Packet Tracer Lab 18)
* Configure WPA2 Personal wireless security
* Configure a wireless pre-shared key
* Connect a client to a secured WLAN
* Verify wireless network connectivity
* Troubleshoot wireless configuration issues

---

## Video Walkthrough

{% if page.video_id and page.video_id != "" %}

<div class="video-container">
  <iframe
    src="https://www.youtube.com/embed/{{ page.video_id }}"
    title="{{ page.lab_title }}"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
  </iframe>
</div>
{% else %}
*Video walkthrough coming soon.*
{% endif %}

## Configuration

| Setting           | Configuration                         |
| ----------------- | ------------------------------------- |
| Wireless Router   | 192.168.1.1                           |
| Wireless Network  | Academy                               |
| Wireless Band     | 2.4 GHz                               |
| Security Mode     | WPA2 Personal                         |
| Pre-Shared Key    | Network123                            |
| Client            | Laptop                                |
| Connectivity Test | [www.cisco.pka](http://www.cisco.pka) |

---

---

## Walkthrough

### 1. Verify Initial Connectivity

From the laptop, I opened **Desktop > Web Browser** and accessed `www.cisco.pka` to verify connectivity before changing the wireless configuration.

### 2. Configure WPA2 Personal

I accessed the wireless router at `192.168.1.1`, opened **Wireless > Wireless Security**, and configured the 2.4 GHz network with:

* **Security Mode:** WPA2 Personal
* **Passphrase:** Network123

I then saved the configuration.

### 3. Reconnect the Laptop

From **Desktop > PC Wireless > Connect**, I selected the **Academy** wireless network and entered `Network123` as the pre-shared key.

### 4. Verify Connectivity

After reconnecting to the secured WLAN, I opened the web browser and successfully accessed `www.cisco.pka`.

---

## Validation

The completed lab confirmed that:

* WPA2 Personal was enabled on the 2.4 GHz WLAN.
* The laptop connected using the correct pre-shared key.
* The **Academy** wireless network remained accessible.
* Web connectivity continued after wireless security was enabled.

---

## Completed Lab

{% if page.completed_lab and page.completed_lab != "" %}
[View Completed Lab PDF]({{ page.completed_lab | relative_url }})
{% endif %}

---

## Related Exercises

* Packet Tracer Lab 17 — Configure DHCP on a Wireless Router
* Wireless Router Configuration
* WPA2 Personal Security
* Wireless Client Configuration
* Wireless Connectivity Troubleshooting


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