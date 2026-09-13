---
layout: page
title: "SF 1041 Domain 3 | Secure Wireless & 802.1X"
date: 2026-09-12 09:15:00 -0700
permalink: /network-portfolio/sf-1041-network-exam-prep/review/wireless-802-1x/
categories:
  - portfolio
  - study-tools
  - networking
tags:
  - sf-1041
  - wireless
  - 802-1x
status: active
---

<div class="prep-nav">
  <a href="/network-portfolio/network-readiness-lab/">Test Readiness Lab</a> ·······
  <a href="/network-portfolio/sf-1041-network-exam-prep/">Exam Prep</a> ·······
  <a href="/network-portfolio/sf-1041-network-exam-prep/review/">Targeted Review</a> ·······
  <a href="/network-portfolio/network-portfolio/sf-1041-practice-engine/">Test Engine</a>
</div>

<style>
.prep-nav { margin: 1rem 0 1.4rem; padding: .75rem 1rem; border: 1px solid rgba(127,127,127,.35); border-radius: 10px; }
.prep-nav a { font-weight: 700; }
.domain-card { margin: 1rem 0; padding: 1rem; border: 1px solid rgba(127,127,127,.35); border-radius: 10px; }
</style>

---
---
---

# Domain 3 — Secure Wireless & 802.1X

## Wireless Fundamentals

A Service Set Identifier (SSID) names a wireless network. An Access Point (AP) bridges wireless clients into the wired network. Signal strength alone does not guarantee performance: interference, channel use, retransmissions, channel width, and too many clients can reduce throughput.

- 2.4 gigahertz (GHz) reaches farther but has fewer non-overlapping channels. In the United States, use channels 1, 6, and 11 in a 20-megahertz design.
- 5 GHz normally provides more channels and less legacy interference.
- 6 GHz provides additional clean spectrum but requires compatible equipment and has shorter effective range.
- Omnidirectional antennas cover broadly; directional antennas focus energy.
- Wider channels increase potential speed but consume more spectrum and can worsen contention.

## Association, Authentication, and Addressing

These are separate stages:

1. **Discovery/association:** client finds and joins the AP.
2. **Authentication:** client proves identity or possession of a key.
3. **Authorization:** policy assigns permitted access, role, or VLAN.
4. **Addressing:** Dynamic Host Configuration Protocol supplies an address.
5. **Application access:** Domain Name System, routes, and firewall rules permit services.

A client can associate successfully and still fail authentication. It can authenticate successfully and still receive the wrong VLAN or fail DHCP.

## Wireless Security

- Wi-Fi Protected Access 3 (WPA3) is preferred when clients support it.
- WPA2/WPA3 Enterprise normally uses IEEE 802.1X and individual identities.
- A Pre-Shared Key (PSK) is shared by multiple users and provides less accountability.
- A guest captive portal supports guest terms and temporary access, but it is not a substitute for encryption and segmentation.
- MAC filtering is weak because MAC addresses can be observed and spoofed.

## 802.1X Roles and Flow

| Role | Job |
|---|---|
| Supplicant | Endpoint software requesting access |
| Authenticator | Switch or AP controlling the port/session |
| Authentication server | Usually Remote Authentication Dial-In User Service (RADIUS); validates identity and returns policy |

```text
Supplicant -- EAPOL --> Authenticator -- RADIUS --> Authentication server
```

Extensible Authentication Protocol over LAN (EAPOL) operates between endpoint and authenticator. RADIUS carries the exchange between authenticator and authentication server. The server decides; the authenticator enforces.

- **EAP-Transport Layer Security (EAP-TLS):** certificate-based mutual authentication.
- **Protected EAP (PEAP):** encrypted tunnel, often protecting password authentication.
- **MAC Authentication Bypass (MAB):** fallback for devices unable to perform 802.1X; weaker than user or certificate identity.
- **Change of Authorization (CoA):** lets RADIUS alter policy for an active session.

## Troubleshooting Sequence

1. Cannot see/join SSID: check radio, SSID, signal, band, channel, and security compatibility.
2. 802.1X never starts: check supplicant service and authenticator port configuration.
3. RADIUS receives nothing: check server address, routes, firewall ports, and shared secret.
4. Credentials/certificates fail: check identity, EAP method, certificate chain, expiration, name, trust, and time.
5. Authentication succeeds but access is wrong: check returned VLAN, Access Control List (ACL), role, and policy.
6. Client has no address: check DHCP scope, relay, and assigned VLAN.
7. Connection drops while moving: inspect coverage overlap, roaming design, interference, and controller logs.

## Check Your Understanding

1. Which 802.1X component makes the authentication decision?
2. Why can successful authentication still produce no network access?
3. Why can incorrect time cause EAP-TLS failures?

## Video Review

- **Sunny Classroom — 802.1X and EAP**
  - <https://youtube.com/@sunnyclassroom24/search?query=802.1X%20EAP>
- **Sunny Classroom — AAA and RADIUS**
  - <https://youtube.com/@sunnyclassroom24/search?query=AAA%20RADIUS>
- **Professor Messer — Wireless Networking, N10-009**
  - <https://www.professormesser.com/network-plus/n10-009/n10-009-video/wireless-networking-n10-009/>

## Acronyms

- **AAA** — Authentication, Authorization, and Accounting
- **ACL** — Access Control List
- **AP** — Access Point
- **CoA** — Change of Authorization
- **DHCP** — Dynamic Host Configuration Protocol
- **EAP** — Extensible Authentication Protocol
- **EAPOL** — Extensible Authentication Protocol over LAN
- **EAP-TLS** — Extensible Authentication Protocol–Transport Layer Security
- **GHz** — Gigahertz
- **MAB** — MAC Authentication Bypass
- **PEAP** — Protected Extensible Authentication Protocol
- **PSK** — Pre-Shared Key
- **RADIUS** — Remote Authentication Dial-In User Service
- **SSID** — Service Set Identifier
- **WPA** — Wi-Fi Protected Access


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