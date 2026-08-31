---
layout: post
title: "Networking Fundamentals | Use nslookup"
lab_title: "Use nslookup"

lesson: "4.0"
lesson_id: "06.06.06"
sort_order: "040606"

categories: [portfolio, labs]

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: dhcp-dns
subcategory_display: DHCP & DNS

content_type: lab
content_type_display: Lab

topics: [dns, nslookup, mx-records, name-resolution, dns-troubleshooting]

tools: [Nslookup, DNS, Windows-Terminal, ip, ping]
sort_order: "040606"

tags: 
  - switch-security
  - linux
  - windows
  - dns
  - nslookup
  - terminal
  - networking
  - network-plus


permalink: /network-portfolio/labs/module-6-0/lab-6-6-6-use-nslookup/
status: complete

date: 2026-04-03 19:11:11 -0700
video: ""
pdf: ""
diagram: ""

protocols: [DNS]
---

In this lab, I used `nslookup` from the Linux terminal to query DNS records and verify mail server information for a domain.

This lab reinforced the relationship between domain names, DNS servers, and MX records while also helping bridge common Windows networking commands into their Linux equivalents.

<!--more-->

---
## Video Walkthrough

Watch the complete walkthrough:

<a href="{{ page.video_url }}" target="_blank" rel="noopener noreferrer">
  <img src="{{ page.thumbnail }}"
       alt="{{ page.title }}"
       style="width:420px; border-radius:8px;">
</a>

---

# Lab Objectives

In this lab, I performed the following tasks:

- Query the default DNS server for the primary IP address of `corpnet.xyz`
- Query the mail server (MX record) for `corpnet.xyz`
- Verify DNS information using an external DNS server

---

# Windows to Linux Networking Command Conversion

One of the biggest adjustments when moving from Windows to Linux networking is learning the modern Linux command equivalents.

---

## Show IP Configuration

Windows:

```powershell
ipconfig
````

Linux:

```bash
ip addr
```

Short version:

```bash
ip a
```

---

## Show Detailed Network Information

Windows:

```powershell
ipconfig /all
```

Linux:

```bash
ip addr
ip route
cat /etc/resolv.conf
```

---

## Show Routing Table

Windows:

```powershell
route print
```

Linux:

```bash
ip route
```

---

## Flush DNS Cache

Windows:

```powershell
ipconfig /flushdns
```

Linux:

```bash
resolvectl flush-caches
```

---

## Query DNS Records

Windows:

```powershell
nslookup corpnet.xyz
```

Linux:

```bash
nslookup corpnet.xyz
```

---

## Test Connectivity

Windows:

```powershell
ping 8.8.8.8
```

Linux:

```bash
ping 8.8.8.8
```

---

# Part 1: Query the Default DNS Server

---

## Query the Primary IP Address

```bash
nslookup corpnet.xyz
```

This command queries the configured default DNS server and returns the IP address associated with the domain.

---

# Part 2: Query the Mail Server (MX Record)

---

## Query MX Records

```bash
nslookup -type=mx corpnet.xyz
```

This command identifies which mail server is responsible for handling email for the domain.

Look for:

```text
mail exchanger
```

or:

```text
MX preference
```

---

# Part 3: Verify Using an External DNS Server

---

## Query External DNS Server

```bash
nslookup corpnet.xyz ns1.nethost.net
```

This confirms the DNS records using an external authoritative DNS server rather than the locally configured resolver.

---

# Common Linux Networking Commands

---

## Show Network Interfaces

```bash
ip link
```

---

## Show IP Addresses

```bash
ip addr
```

---

## Show DNS Server Configuration

```bash
cat /etc/resolv.conf
```

---

## Show Active Connections

```bash
ss -tulnp
```

---

## Trace Network Path

```bash
traceroute google.com
```

---

# Troubleshooting

If `nslookup` fails:

Check:

* network connectivity
* DNS server configuration
* interface status
* routing table entries

---

## Verify Connectivity

```bash
ping 8.8.8.8
```

---

## Verify DNS Server Configuration

```bash
cat /etc/resolv.conf
```

---

## Verify Routing Table

```bash
ip route
```

---

# Commands Used (In Order)

```bash
nslookup corpnet.xyz

nslookup -type=mx corpnet.xyz

nslookup corpnet.xyz ns1.nethost.net

ip addr

ip route

cat /etc/resolv.conf

ping 8.8.8.8
```

---

# Key Takeaways

This lab reinforced:

* DNS resolution
* MX record identification
* external DNS verification
* Linux terminal networking commands
* Windows to Linux command conversion

This was one of my first labs where I began translating familiar Windows networking concepts into Linux administration workflows.


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