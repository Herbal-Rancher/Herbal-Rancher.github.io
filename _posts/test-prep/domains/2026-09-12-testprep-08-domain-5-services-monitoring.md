---
layout: page
title: "SF 1041 Domain 5 | Services, Tools & Monitoring"
date: 2026-09-12 09:25:00 -0700
permalink: /network-portfolio/sf-1041-network-exam-prep/review/services-monitoring/
categories:
  - portfolio
  - study-tools
  - networking
tags:
  - sf-1041
  - services
  - monitoring
status: active
---

<div class="prep-nav">
  <a href="/network-portfolio/network-readiness-lab/">Test Readiness Lab</a> ·······
  <a href="/network-portfolio/sf-1041-network-exam-prep/">Exam Prep</a> ·······
  <a href="/network-portfolio/sf-1041-network-exam-prep/review/">Targeted Review</a> ·······
  <a href="/network-portfolio/sf-1041-practice-engine/">Practice Test Engine</a>
</div>

<style>
.prep-nav { margin: 1rem 0 1.4rem; padding: .75rem 1rem; border: 1px solid rgba(127,127,127,.35); border-radius: 10px; }
.prep-nav a { font-weight: 700; }
.domain-card { margin: 1rem 0; padding: 1rem; border: 1px solid rgba(127,127,127,.35); border-radius: 10px; }
</style>

---
---
---

# Domain 5 — Services, Tools & Monitoring

## DHCP

Dynamic Host Configuration Protocol (DHCP) supplies client settings through Discover, Offer, Request, and Acknowledge (DORA). The initial client broadcast cannot cross a router without a DHCP relay or IP helper.

- An Automatic Private IP Addressing (APIPA) address in `169.254.0.0/16` often means DHCP failed.
- A scope includes subnet, address range, exclusions, lease time, gateway, Domain Name System (DNS) servers, and options.
- A reservation maps a client identifier or Media Access Control address to a predictable leased address.
- A wrong gateway delivered by DHCP can break remote access while local access still works.
- A rogue DHCP server can supply incorrect gateways or DNS settings.

Troubleshoot in this order: link and VLAN → client request → relay → server reachability → active scope → available leases → correct options.

## DNS

| Record | Purpose |
|---|---|
| A / AAAA | Hostname to IPv4 / IPv6 address |
| CNAME | Alias to canonical name |
| MX | Mail exchanger |
| PTR | Reverse address-to-name lookup |
| NS | Authoritative name server |
| SRV | Service location, port, priority, and weight |
| TXT | Text used for verification and policy |

A recursive resolver pursues an answer for a client. An authoritative server holds official records for its zone. Time to Live (TTL) controls caching, so a corrected record may not appear everywhere immediately.

If an IP address works but the hostname fails, investigate DNS. Confirm the client is using the expected resolver, query the record directly, and distinguish a missing record from a stale cached answer.

## Monitoring and Evidence

- Network Time Protocol (NTP) aligns timestamps; correlation fails when clocks disagree.
- Syslog transports event messages to centralized storage.
- Simple Network Management Protocol (SNMP) polling asks devices for data.
- An SNMP trap is an unsolicited notification pushed by the device.
- SNMP version 3 adds authentication and privacy capabilities.
- A Security Information and Event Management (SIEM) system correlates events across sources.
- A baseline defines normal performance. A threshold decides when to alert.

Polling provides regular measurements but may miss brief events between intervals. Traps provide immediate events but can be lost, so mature monitoring often uses both.

## Important Ports

| Service | Port(s) | Transport |
|---|---:|---|
| DNS | 53 | User Datagram Protocol (UDP) and Transmission Control Protocol (TCP) |
| DHCP | 67/68 | UDP |
| Secure Shell (SSH) | 22 | TCP |
| HTTP / HTTPS | 80/443 | TCP |
| NTP | 123 | UDP |
| SNMP polling / traps | 161/162 | UDP |
| RADIUS authentication / accounting | 1812/1813 | UDP |
| TACACS+ | 49 | TCP |
| Server Message Block (SMB) | 445 | TCP |
| Internet Printing Protocol (IPP) | 631 | TCP |
| RAW printing | 9100 | TCP |

Memorize the service, number, and transport together. A correct port with the wrong transport is still an incorrect answer.

## Choose the Right Tool

| Need | Useful tool |
|---|---|
| Test reachability and round-trip behavior | `ping` |
| See the Layer 3 path | `traceroute` / `tracert` |
| Inspect local IP configuration | `ip`, `ipconfig`, `ifconfig` |
| Query DNS directly | `dig`, `nslookup` |
| Inspect local neighbor mappings | `arp`, `ip neigh` |
| Inspect sessions and listening ports | `ss`, `netstat` |
| Capture packets | `tcpdump`, Wireshark |
| Scan authorized hosts and services | `nmap` |

## Check Your Understanding

1. Why can DHCP work in one VLAN but fail in another?
2. What is the operational difference between SNMP polling and a trap?
3. Why might a repaired DNS record still return the previous answer?

## Video Review

- **Sunny Classroom — DHCP and DNS**
  - <https://youtube.com/@sunnyclassroom24/search?query=DHCP%20DNS>
- **Sunny Classroom — SNMP, Syslog, and SIEM**
  - <https://youtube.com/@sunnyclassroom24/search?query=SNMP%20Syslog%20SIEM>
- **Professor Messer — Command Line Tools, N10-009**
  - <https://www.professormesser.com/network-plus/n10-009/n10-009-video/command-line-tools-n10-009/>

## Acronyms

- **APIPA** — Automatic Private IP Addressing
- **DHCP** — Dynamic Host Configuration Protocol
- **DNS** — Domain Name System
- **DORA** — Discover, Offer, Request, Acknowledge
- **HTTP/HTTPS** — Hypertext Transfer Protocol / Hypertext Transfer Protocol Secure
- **IPP** — Internet Printing Protocol
- **NTP** — Network Time Protocol
- **RADIUS** — Remote Authentication Dial-In User Service
- **SIEM** — Security Information and Event Management
- **SMB** — Server Message Block
- **SNMP** — Simple Network Management Protocol
- **SSH** — Secure Shell
- **TCP/UDP** — Transmission Control Protocol / User Datagram Protocol
- **TTL** — Time to Live


---
---
---

## 🔗 Navigation

* [Home](/)
* [Network Portfolio](/network-portfolio/)
  * [Formative Modules](/network-portfolio/formative-modules/)
  * [Video Walkthroughs](/network-portfolio/videos/)
  * [Study Diagrams](/network-portfolio/study-diagrams/)
  * **[NETWORK TEST READINESS LAB](/network-portfolio/network-readiness-lab/)**
* [Trading+](/trading/)
* [Bible Study](/bible-study/)
* [About the Portfolio](/about/)

---
---
---