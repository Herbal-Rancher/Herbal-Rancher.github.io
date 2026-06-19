---
layout: post
title: "Infrastructure | Configure Initial Router Settings"
lab_title: "Configure Initial Router Settings"

lesson: "11.0"
lesson_id: "11.04.00"
sort_order: "110400"

categories: [portfolio, labs]

category: infrastructure
category_display: Infrastructure

subcategory: routing
subcategory_display: Routing

content_type: lab
content_type_display: Lab

topics: [router-configuration, routing, device-management, infrastructure]

tools: [Router]


tags: 
  - packet-tracer
  - router
  - cisco-ios
  - security
  - configuration

permalink: /network-portfolio/labs/module-11-0/configure-initial-router-settings/
status: complete

date: 2026-04-03 04:44:11 -0700
video: ""
pdf: ""
diagram: ""

protocols: []
---

In this lab, I configured basic administrative and security settings on a Cisco router using Cisco IOS.

Skills practiced:

- Console connectivity
- Router CLI navigation
- Password security
- MOTD banners
- Configuration verification
- Saving configurations
- Flash backups

<!--more-->
---

## Step 1: Connect to R1 via Console

In Packet Tracer:

- Select **Console cable**
- Connect **PCA → RS-232**
- Connect **R1 → Console**
- Open:

PCA → Desktop → Terminal → OK → Press Enter

---

## Step 2: Enter Privileged EXEC Mode

```bash
Router> enable
Router#
```

---

## Step 3: Review Current Configuration

View current configuration then saved configuration. Nothing should have been saved to NVRAM yet so Startup-config should display ```startup-config is not present```: 
```bash 
Router# show running-config
Router# show startup-config
```

---

## Step 4: Configure Hostname

```bash
Router# configure terminal
  Configuring from terminal, memory, or network [terminal]? 
  Enter configuration commands, one per line.  End with CNTL/Z.
Router(config)# 
Router(config)# hostname R1
R1(config)# 
```
---

## Step 5: Configure MOTD Banner

```bash
R1(config)# banner motd "Unauthorized access is strictly prohibited."
```
This warns unauthorized users before login.

---

## Step 6: Configure Enable Password

```bash
R1(config)# enable password cisco
```

---

## Step 7: Configure Enable Secret Password

```bash
R1(config)# enable secret itsasecret
```
The secret password overrides the regular enable password because it is encrypted.

---

## Step 8: Secure Console Access and Virtual Terminal

```bash
R1(config)# line console 0
R1(config-line)# password letmein
R1(config-line)# login
R1(config)# line vty 0 4
R1(config-line)# password letmein
R1(config-line)# exit
```

Without `login`, password authentication will not work.

---

## Step 9: Encrypt All Plain Text Passwords

```bash
R1(config)# service password-encryption
```

This encrypts:

- Console passwords
- VTY passwords
- Enable passwords
- Future passwords

---

## Step 10: Verify Configuration

```bash
R1# show running-config 
```

Confirm:

- Hostname
- Banner
- Passwords
- Encryption settings

---

## Step 11: Test Login Security

Exit the session:

```bash
R1# exit
R> 
```

You should now see:

- MOTD banner
- Password prompts

---

## Step 12: Save Configuration to NVRAM

```bash
R1# copy running-config startup-config
```

Shortcut:

```bash
R1# copy run start
```

Shortest version:

```bash
R1# cop r st
```

---

## Step 13: Verify Flash Storage

```bash
R1# show flash
```

Look for the IOS `.bin` file.

Example:

```bash
c1900-universalk9-mz.SPA.152-4.M3.bin
```

---

## Step 14: Backup Startup Config to Flash

```bash
R1# copy startup-config flash
```

Press Enter to accept default filename.

Verify backup:

```bash
R1# show flash
```

---

# Troubleshooting

If no password prompt appears:

```bash
R1(config)# line console 0
login
```

---

If passwords are still plain text:

```bash
R1(config)# service password-encryption
```

---

If configuration disappears after reboot:

```bash
R1(config)# copy running-config startup-config
```

---

# Key Commands Summary

```bash
Router> enable
Router# show running-config
Router# show startup-config
Router# configure terminal
Router(config)# hostname R1
R1(config)# banner motd "Unauthorized access is strictly prohibited."
R1(config)# enable password cisco
R1(config)# enable secret itsasecret
R1(config)# line console 0
R1(config)# password letmein
R1(config)# login
R1(config)# service password-encryption
R1# copy running-config startup-config
R1# show flash
R1# copy startup-config flash
```

---

# Key Takeaways

This lab reinforced:

- Router administration
- CLI security
- Password management
- Configuration backups
- Basic Cisco operational practices

These are foundational skills for future Cisco labs and :contentReference[oaicite:0]{index=0} preparation.


---
---
---

## 🔗 Navigation

* **[HOME](/)**
* [Network+ Portfolio](/network-portfolio/)
  * [Formative Lessons](/network-portfolio/formative-lessons/)
  * [Video Walkthroughs](/network-portfolio/videos/)
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* [Bible Study](/network-portfolio/Bible-Study/)
* [Behind the Portfolio](/network-portfolio/behind-the-portfolio/)

---
---
---