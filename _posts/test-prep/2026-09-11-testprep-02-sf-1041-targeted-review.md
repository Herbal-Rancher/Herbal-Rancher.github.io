---
layout: page
title: "SF 1041 Networks Core | Targeted Review"
date: 2026-09-10 14:00:00 -0700
permalink: /network-portfolio/sf-1041-network-exam-prep/review/
categories:
  - portfolio
  - study-tools
  - networking
tags:
  - sf-1041
  - eigrp
  - routing
  - switching
  - vlan
  - 802-1x
  - firewall
  - troubleshooting
status: active
---


<div class="prep-nav">
  <a href="/network-portfolio/test-prep/">Test Prep Index</a> ·
  <a href="/network-portfolio/sf-1041-network-exam-prep/">SF 1041 Home</a> ·
  <a href="/network-portfolio/sf-1041-network-exam-prep/review/">Targeted Review</a> ·
  <a href="/network-portfolio/sf-1041-network-exam-prep/test-engine/">Test Engine</a>
</div>

<style>
.prep-nav { margin: 1rem 0 1.4rem; padding: .75rem 1rem; border: 1px solid rgba(127,127,127,.35); border-radius: 10px; }
.prep-nav a { font-weight: 700; }
</style>
# Targeted Review

This review is intentionally detailed enough to explain the **why**, but compact enough to use during a short exam-preparation window. Each domain includes key definitions, troubleshooting clues, and optional videos. Study the high-priority text first; use the links only when a concept still feels unclear.

> **Best workflow:** Review one domain -> explain it in your own words -> run a focused test -> study only the missed concepts -> retest.

## 1. Routing & EIGRP — HIGH PRIORITY

### Routing Decision Order

1. Find matching routes.
2. Choose the **longest prefix match**.
3. If the same prefix is learned from different sources, compare **administrative distance**.
4. Within the selected routing protocol, use that protocol's **metric**.

### EIGRP

- Interior gateway routing protocol.
- Uses **DUAL — Diffusing Update Algorithm**.
- **Successor:** current best route.
- **Feasible successor:** qualified loop-free backup route.
- Internal EIGRP commonly uses administrative distance **90**.
- External EIGRP commonly uses administrative distance **170**.
- Know neighbor formation, convergence, route selection, and floating static routes.

#### EIGRP Terms That Can Separate Close Answers

| Term | Meaning |
|---|---|
| **DUAL** | EIGRP algorithm that calculates loop-free paths and supports rapid convergence |
| **Successor** | Best EIGRP path; installed in the routing table |
| **Feasible successor** | Prequalified loop-free backup path in the EIGRP topology table |
| **Feasible distance (FD)** | Best total metric from the local router to the destination |
| **Reported distance (RD)** | Neighbor's advertised distance from itself to the destination |
| **Feasibility condition** | A neighbor's RD must be lower than the current FD to qualify as a feasible successor |
| **Passive route** | Stable EIGRP route; this is the normal condition |
| **Active route** | EIGRP is querying for a replacement path; it does **not** mean “working normally” |
| **Stuck in Active (SIA)** | EIGRP did not receive a required query reply in time |
| **Variance** | EIGRP feature that allows unequal-cost load balancing |

EIGRP's classic metric uses **bandwidth and delay by default**. Reliability and load are available components but are not included by default.

#### Verify Before Changing

```text
show ip route
show ip protocols
show ip eigrp neighbors
show ip eigrp topology
show ip interface brief
```

- No neighbor: check link/interface state, IP subnet, EIGRP autonomous-system number, and advertised interfaces.
- Neighbor exists but route is missing: inspect the topology table, network statements, filtering, and summarization.
- Unexpected route: compare prefix length first, then administrative distance, then metric.

### OSPF, RIP, BGP

- **OSPF:** link-state IGP; metric = cost.
- **RIP:** distance-vector IGP; metric = hop count; 15 usable hops maximum.
- **BGP:** path-vector EGP used between autonomous systems.

### Subnetting

Be able to identify:

- Prefix and dotted-decimal mask
- Network address
- Broadcast address
- Usable range
- Whether two addresses are in the same subnet
- /30 point-to-point logic
- Longest-prefix routing decisions

### Definitions & Video Review

- Definition: [Cisco - What Is Routing?](https://www.cisco.com/site/us/en/learn/topics/networking/what-is-routing.html)
- Professor Messer: [Static Routing - N10-009](https://www.professormesser.com/network-plus/n10-009/n10-009-video/static-routing-n10-009/)
- Professor Messer: [Dynamic Routing - N10-009](https://www.professormesser.com/network-plus/n10-009/n10-009-video/dynamic-routing-n10-009/)
- Professor Messer: [Routing Technologies - N10-009](https://www.professormesser.com/network-plus/n10-009/n10-009-video/routing-technologies-n10-009/)
- Professor Messer: [Routing and IP Issues - N10-009](https://www.professormesser.com/network-plus/n10-009/n10-009-video/routing-and-ip-issues-n10-009/)
- Sunny Classroom: [EIGRP and routing videos](https://www.youtube.com/@SunnyClassroom/search?query=EIGRP%20routing)
- Sunny Classroom: [Subnetting videos](https://www.youtube.com/@SunnyClassroom/search?query=subnetting)

> **Routing memory rule:** Most-specific prefix -> lowest administrative distance -> lowest protocol metric.

---

## 2. Switching, VLANs & Redundancy — HIGH PRIORITY

### VLANs

- A VLAN is a separate Layer 2 broadcast domain.
- Access ports normally carry one endpoint VLAN.
- 802.1Q trunks carry multiple VLANs.
- Native VLAN traffic is normally untagged on the trunk.
- An SVI is a logical Layer 3 interface associated with a VLAN.

#### Common and Uncommon VLAN Terms

| Term | Meaning |
|---|---|
| **Access port** | Normally carries one endpoint data VLAN, untagged |
| **Trunk** | Carries multiple VLANs using 802.1Q tags |
| **Native VLAN** | VLAN normally carried untagged across an 802.1Q trunk |
| **Allowed VLAN list** | VLANs permitted to cross a trunk; one missing VLAN can create a very selective outage |
| **SVI** | Logical switch interface for a VLAN, used for management or Layer 3 routing |
| **Router-on-a-stick** | One physical router interface uses tagged subinterfaces for inter-VLAN routing |
| **Voice VLAN** | Separate VLAN for an IP phone while its attached PC uses the access VLAN |
| **CAM table** | Another term commonly used for the switch MAC address table |
| **Unknown unicast** | Destination MAC is not learned, so the frame is flooded inside its VLAN |

### STP / RSTP

- Prevent Layer 2 loops.
- Redundant physical paths can exist while STP (Spanning Tree Protocol) blocks selected paths.
- Root bridge election is based on the lowest bridge ID.
- Use PortFast only on appropriate edge ports.

- **BPDU:** STP control frame used to exchange topology information.
- **Root port:** best path from a non-root switch toward the root bridge.
- **Designated port:** forwarding port selected for a network segment.
- **BPDU Guard:** can disable an edge/PortFast port if an unexpected BPDU arrives.
- **Broadcast storm:** uncontrolled frame circulation, often caused by a Layer 2 loop.

### LACP / EtherChannel

- Combines compatible physical links into one logical link.
- Adds redundancy and can increase aggregate capacity.
- Links in the same bundle must have compatible settings.

LACP (Link Aggregation Control Protocol) **active** initiates negotiation and **passive** responds. Active/active and active/passive can form; passive/passive cannot. Member ports must agree on properties such as speed, duplex, access/trunk mode, native VLAN, and allowed VLANs.

### Cisco Verification Commands

```text
show vlan brief
show interfaces switchport
show interfaces trunk
show mac address-table
show spanning-tree
show etherchannel summary
show ip interface brief
```

### Scenario Clues

| Symptom | Check first |
|---|---|
| One VLAN fails only between switches | VLAN existence and trunk allowed-VLAN list |
| Local VLAN communication works; remote VLAN fails | Default gateway and inter-VLAN routing |
| Port-channel is suspended or individual links remain separate | Member settings and LACP modes |
| Severe slowdown begins after adding a redundant switch link | STP state and Layer 2 loop evidence |
| Phone works but attached PC fails | Voice VLAN versus access VLAN configuration |

### Definitions & Video Review

- Definition: [Cisco - VLAN and Segmentation Overview](https://www.cisco.com/c/en/us/products/collateral/switches/campus-lan-access-switches/white-paper-c11-744670.html)
- Definition: [Cisco - Understanding 802.1Q Trunking](https://www.cisco.com/c/en/us/support/docs/lan-switching/8021q/17056-741-4.html)
- Professor Messer: [Switching Issues - N10-009](https://www.professormesser.com/network-plus/n10-009/n10-009-video/switching-issues-n10-009/)
- Professor Messer: [Complete N10-009 Course - VLANs, Trunking, STP](https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/)
- Sunny Classroom: [What Is VLAN and Why VLAN?](https://www.youtube.com/watch?v=_PPaArOxHhw)
- Sunny Classroom: [Default VLAN and Native VLAN](https://www.youtube.com/watch?v=zW_-mf6v3fs)
- Sunny Classroom: [802.1Q trunking videos](https://www.youtube.com/@SunnyClassroom/search?query=802.1Q%20trunking)
- Sunny Classroom: [STP and LACP videos](https://www.youtube.com/@SunnyClassroom/search?query=STP%20LACP)

---

## 3. Secure Wireless & 802.1X — HIGH PRIORITY

### 802.1X Roles

- **Supplicant:** endpoint requesting access.
- **Authenticator:** switch or access point controlling the port.
- **Authentication server:** commonly RADIUS.

The exchange is commonly:

```text
Supplicant → EAPOL → Authenticator → RADIUS → Authentication server
```

The authentication server makes the identity/policy decision; the switch or AP enforces the result.

#### Important 802.1X Terms

| Term | Meaning |
|---|---|
| **AAA** | Authentication, Authorization, and Accounting |
| **EAP** | Framework supporting multiple authentication methods |
| **EAPOL** | EAP over LAN between the supplicant and authenticator |
| **EAP-TLS** | Strong certificate-based mutual authentication; requires certificate/PKI management |
| **PEAP** | Creates a protected TLS tunnel, often carrying password authentication inside |
| **MAB** | MAC Authentication Bypass for devices unable to use 802.1X; weaker than identity/certificate authentication |
| **CoA** | RADIUS Change of Authorization; changes policy for an active session |

### Enterprise Wireless

- WPA2/WPA3 Enterprise commonly uses 802.1X/EAP.
- Prefer individual credentials over one shared PSK for enterprise identity.
- Captive portals are useful for guest terms and temporary access.
- MAC filtering alone is weak because MAC addresses can be spoofed.

### RF Concepts

- 2.4 GHz is crowded and susceptible to microwave interference.
- Common non-overlapping 20 MHz channels in the U.S.: **1, 6, 11**.
- 5 GHz provides additional spectrum and usually less legacy interference.
- Directional antennas focus energy; omnidirectional antennas provide broad local coverage.
- Strong signal does not guarantee high throughput if airtime is congested.

### Troubleshooting Order

1. Association failure: check SSID, signal, radio, encryption, and compatibility.
2. 802.1X does not begin: check supplicant and authenticator configuration.
3. RADIUS request never arrives: check routing, firewall, RADIUS ports, and shared secret.
4. Credentials are rejected: check identity, EAP method, certificates, time, and trust.
5. Authentication succeeds but access is wrong: check authorization policy, assigned VLAN, role, and ACL.

### Definitions & Video Review

- Definition: [Cisco - 802.1X Configuration and Concepts](https://www.cisco.com/c/en/us/support/docs/lan-switching/8021x/116063-configure-product-00.html)
- Professor Messer: [Wireless Networking - N10-009](https://www.professormesser.com/network-plus/n10-009/n10-009-video/wireless-networking-n10-009/)
- Professor Messer: [Wireless Technologies - N10-009](https://www.professormesser.com/network-plus/n10-009/n10-009-video/wireless-technologies-n10-009/)
- Professor Messer: [Wireless Security Settings - Security+](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/wireless-security-settings-sy0-701/)
- Sunny Classroom: [AAA Framework and RADIUS](https://www.youtube.com/watch?v=feHpDc1cLXM)
- Sunny Classroom: [802.1X and EAP videos](https://www.youtube.com/@SunnyClassroom/search?query=802.1X%20EAP)

> Do not confuse **802.1Q** (VLAN tagging), **802.1X** (access control), and **802.11** (wireless LANs).

---

## 4. Firewalls, ACLs & Secure Management — HIGH PRIORITY

### Firewall Logic

Evaluate each flow by:

- Source
- Destination
- Protocol
- Port/service
- Direction
- Action
- Rule order

ACLs are processed top to bottom and stop on the **first match**. Unmatched traffic reaches the **implicit deny**. A stateful firewall also tracks connection state so legitimate return traffic can be recognized.

### Security Concepts

- **Least privilege:** allow only what is required.
- **ACL:** permit/deny traffic based on defined criteria.
- **DMZ / screened subnet:** isolates public-facing systems.
- **Segmentation:** limits broadcast scope and lateral movement.
- **SSH:** encrypted remote CLI management.
- **Out-of-band management:** independent management path.
- **IPsec ESP:** provides confidentiality through encryption.
- **Port security:** restricts MAC learning/usage on access ports.
- **IDS:** detects/alerts.
- **IPS:** can operate inline and block.

### Less-Common Security Terms

| Term | Meaning |
|---|---|
| **North-south traffic** | Traffic entering or leaving the internal network/data center |
| **East-west traffic** | Lateral traffic between internal systems |
| **Microsegmentation** | Fine-grained isolation between workloads or endpoints |
| **NGFW** | Firewall adding features such as application identity, users, IPS, and content awareness |
| **Port mirroring / SPAN** | Copies switch traffic to a passive monitoring sensor |
| **Hairpin NAT** | Internal user reaches an internal service by using its public address |
| **PAT / NAT overload** | Many private devices share a public IP through unique port translations |

### Definitions & Video Review

- Sunny Classroom: [NAT - SNAT, DNAT, PAT, and Port Forwarding](https://www.youtube.com/watch?v=wg8Hosr20yw)
- Sunny Classroom: [Firewall and ACL videos](https://www.youtube.com/@SunnyClassroom/search?query=firewall%20ACL)
- Professor Messer: [Rogue Services - N10-009](https://www.professormesser.com/network-plus/n10-009/n10-009-video/rogue-services-n10-009/)
- Professor Messer: [Firewall and ACL videos](https://www.youtube.com/@professormesser/search?query=Network%2B%20firewall%20ACL)

---

## 5. Services, Tools & Monitoring — KNOW IT

### DHCP

- DORA: Discover, Offer, Request, Acknowledge.
- APIPA/169.254.0.0/16 often indicates DHCP failure.
- DHCP relay/IP helper forwards DHCP requests across routed boundaries.
- Reservations are useful for infrastructure devices that should keep stable addresses.

### DNS

- **A:** IPv4 address
- **AAAA:** IPv6 address
- **CNAME:** alias
- **MX:** mail exchanger
- **PTR:** reverse lookup
- **NS:** authoritative nameserver
- **TTL:** cache lifetime

- **SRV:** locates a named service and includes port/priority information.
- **TXT:** stores text used for verification and policies such as email security.
- **Recursive resolver:** pursues an answer for a client.
- **Authoritative server:** holds official records for its DNS zone.
- **Split-horizon DNS:** returns different answers based on the query's origin.

### Monitoring

- **NTP:** synchronized timestamps.
- **Syslog:** centralized logs/events.
- **SNMP:** device monitoring/management.
- **SNMPv3:** authentication/privacy capabilities.
- **SIEM:** correlates and analyzes events across sources.
- Establish a baseline before deciding that utilization is abnormal.

### Tools

```text
ping
tracert / traceroute
ipconfig / ifconfig / ip
nslookup / dig
arp
netstat / ss
nmap
tcpdump / Wireshark
```

### Ports Worth Recognizing

| Service | Port(s) | Transport |
|---|---:|---|
| DNS | 53 | UDP/TCP |
| DHCP | 67/68 | UDP |
| SSH | 22 | TCP |
| HTTP/HTTPS | 80/443 | TCP |
| NTP | 123 | UDP |
| SNMP polling/traps | 161/162 | UDP |
| RADIUS authentication/accounting | 1812/1813 | UDP |
| TACACS+ | 49 | TCP |
| SMB | 445 | TCP |
| IPP printing | 631 | TCP |
| RAW printing | 9100 | TCP |

### Definitions & Video Review

- Professor Messer: [Software Tools - N10-009](https://www.professormesser.com/network-plus/n10-009/n10-009-video/software-tools-n10-009/)
- Professor Messer: [Command Line Tools - N10-009](https://www.professormesser.com/network-plus/n10-009/n10-009-video/command-line-tools-n10-009/)
- Professor Messer: [Basic Network Device Commands - N10-009](https://www.professormesser.com/network-plus/n10-009/n10-009-video/basic-network-device-commands-n10-009/)
- Sunny Classroom: [DHCP and DNS videos](https://www.youtube.com/@SunnyClassroom/search?query=DHCP%20DNS)
- Sunny Classroom: [SNMP, Syslog, and SIEM videos](https://www.youtube.com/@SunnyClassroom/search?query=SNMP%20Syslog%20SIEM)

---

## 6. Troubleshooting & Analytical Thinking — HIGH PRIORITY

Use a disciplined sequence:

1. Identify the problem.
2. Establish a theory of probable cause.
3. Test the theory.
4. Create a plan of action.
5. Implement the solution or escalate.
6. Verify full functionality and preventive measures.
7. Document findings, actions, and outcomes.

### Fast Isolation Pattern

```text
Physical link / interface state
        ↓
IP address / subnet mask
        ↓
Local subnet communication
        ↓
Default gateway
        ↓
Routing path
        ↓
DNS / service
        ↓
Firewall / ACL
        ↓
Application
```

Always ask:

- Is this one host, one VLAN, one site, or everyone?
- What still works?
- What changed?
- What evidence would prove or disprove the theory?
- What is the smallest safe change?

### Symptom-to-Cause Shortcuts

| Symptom | Strong first theory or check |
|---|---|
| `169.254.x.x` address | DHCP failure; inspect link, scope, relay, and server reachability |
| Same subnet works; remote networks fail | Default gateway or routing |
| IP address works; hostname fails | DNS |
| One VLAN fails across a trunk | VLAN absent or not allowed on trunk |
| CRC/input errors increase | Cable, transceiver, interference, or duplex issue |
| Route out works but reply fails | Missing return route or asymmetric filtering |
| Strong Wi-Fi signal but poor performance | Congestion, interference, or airtime utilization |
| Certificates fail across several systems | Time/NTP or CA trust problem |

#### Performance Terms

- **Bandwidth:** theoretical capacity.
- **Throughput:** actual delivered rate.
- **Goodput:** useful application data after overhead/retransmissions.
- **Latency:** travel time.
- **Jitter:** variation in latency.
- **Attenuation:** signal weakening over distance.
- **CRC error:** failed frame integrity check, often pointing toward Layer 1 trouble.

### Video Review

- Professor Messer: [Routing and IP Issues - N10-009](https://www.professormesser.com/network-plus/n10-009/n10-009-video/routing-and-ip-issues-n10-009/)
- Professor Messer: [Switching Issues - N10-009](https://www.professormesser.com/network-plus/n10-009/n10-009-video/switching-issues-n10-009/)
- Sunny Classroom: [Network troubleshooting videos](https://www.youtube.com/@SunnyClassroom/search?query=network%20troubleshooting)
- Sunny Classroom: [Collision Domain vs. Broadcast Domain](https://www.youtube.com/watch?v=ck3gx9HB9-k)

---

## 7. Multifunction Devices & Documentation — DO NOT SKIP

### Networked MFP / Printer

Verify:

- IP address
- Subnet mask
- Default gateway
- DNS
- VLAN membership
- DHCP reservation or static assignment
- Print service/port
- Firmware
- Access control
- Reachability

Printing can work while another MFP function fails because each service has separate dependencies:

| Failure | Check |
|---|---|
| Scan-to-email | SMTP server, DNS, gateway, TLS, credentials, and relay policy |
| Scan-to-folder | SMB path, DNS, service account, and share/file permissions |
| One user cannot print | Client queue, driver, permissions, and local spooler |
| Everyone cannot print | Device link/address, print server/queue, and print protocol |

### Documentation

Maintain:

- Physical topology
- Logical topology
- Device and interface names
- IP addresses and prefixes
- VLAN IDs
- Trunks
- Gateways
- Routing relationships
- Security controls
- Dependencies
- Change history
- Validation results
- Rollback steps

Know the difference between:

- **Physical topology:** devices, media, ports, racks, and physical links.
- **Logical topology:** subnets, VLANs, routes, zones, and dependencies.
- **Baseline:** approved or known-normal state used for comparison.
- **Runbook:** repeatable operational or incident-response steps.
- **Change record:** reason, risk, approval, implementation, validation, and rollback.
- **RCA:** root cause analysis; identifies the underlying cause, not only the symptom.
- **Configuration drift:** current settings have diverged from the approved baseline.
- **Blast radius:** systems and users a change or failure could affect.

---

## Final High-Value Distinctions

| Do not confuse | Correct distinction |
|---|---|
| Metric vs. administrative distance | Path comparison inside one protocol vs. trust between route sources |
| Successor vs. feasible successor | Installed EIGRP best path vs. qualified backup |
| STP vs. LACP | Loop prevention vs. link aggregation |
| Native VLAN vs. management VLAN | Untagged trunk VLAN vs. VLAN used to manage devices |
| Authentication vs. authorization | Proves identity vs. determines allowed access |
| IDS vs. IPS | Detects/alerts vs. can block inline |
| SNMP trap vs. polling | Device sends event vs. manager requests data |
| Syslog vs. SIEM | Event collection/transport vs. cross-source correlation and analysis |
| NAT vs. PAT | Address translation vs. many-to-one translation using ports |
| RTO vs. RPO | Maximum restoration time vs. acceptable data-loss interval |

## Complete Video Hubs

- [Professor Messer's Complete N10-009 Network+ Course](https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/)
- [Sunny Classroom YouTube Channel](https://www.youtube.com/@SunnyClassroom)
- [Sunny Classroom Playlists](https://www.youtube.com/@SunnyClassroom/playlists)

> External links sometimes move. If a direct video becomes unavailable, use the linked channel search and the exact concept name.

[Go to Test Engine](/network-portfolio/sf-1041-network-exam-prep/test-engine/)


---
---
---

## 🔗 Navigation

* [Home](/)
* [Network Portfolio](/network-portfolio/)
  * [Formative Modules](/network-portfolio/formative-modules/)
  * [Video Walkthroughs](/network-portfolio/videos/)
  * [Study Diagrams](/network-portfolio/study-diagrams/)
  * **[TEST PREP](/network-portfolio/test-prep/)**
* [Trading+](/trading/)
* [Bible Study](/bible-study/)
* [About the Portfolio](/about/)

---
---
---