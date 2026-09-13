---
layout: page
title: "SF 1041 Domain 2 | Switching, VLANs & Redundancy"
date: 2026-09-12 09:10:00 -0700
permalink: /network-portfolio/sf-1041-network-exam-prep/review/switching-vlans/
categories:
  - portfolio
  - study-tools
  - networking
tags:
  - sf-1041
  - switching
  - vlan
status: active
---

<div class="prep-nav">
  <a href="/network-portfolio/test-prep/">Test Prep Index</a> ·······
  <a href="/network-portfolio/sf-1041-network-exam-prep/">SF 1041 Home</a> ·······
  <a href="/network-portfolio/sf-1041-network-exam-prep/review/">Targeted Review</a> ·······
  <a href="/network-portfolio/sf-1041-network-exam-prep/test-engine/">Focused Test</a>
</div>

<style>
.prep-nav { margin: 1rem 0 1.4rem; padding: .75rem 1rem; border: 1px solid rgba(127,127,127,.35); border-radius: 10px; }
.prep-nav a { font-weight: 700; }
.domain-card { margin: 1rem 0; padding: 1rem; border: 1px solid rgba(127,127,127,.35); border-radius: 10px; }
</style>

---
---
---

# Domain 2 — Switching, VLANs & Redundancy

## Ethernet Switching

A switch learns the source Media Access Control (MAC) address of each received frame and associates it with the incoming port. It forwards a known unicast toward the learned destination port. Unknown unicasts, broadcasts, and relevant multicasts are flooded only within the same Virtual Local Area Network (VLAN).

- MAC entries age out when not refreshed.
- A MAC address moving rapidly between ports can indicate a loop, bad cabling, or expected virtualization behavior.
- A Layer 2 switch cannot route traffic between VLANs.
- Full-duplex Ethernet has no collisions; duplex mismatches can cause poor performance and errors.

## VLANs, Access Ports, and Trunks

- **Access port:** carries one endpoint VLAN; ordinary endpoint frames are untagged.
- **Trunk:** carries multiple VLANs using Institute of Electrical and Electronics Engineers (IEEE) 802.1Q tags.
- **Native VLAN:** normally crosses an 802.1Q trunk untagged.
- **Allowed VLAN list:** controls which VLANs may traverse a trunk.
- **Switch Virtual Interface (SVI):** logical Layer 3 interface used for management or inter-VLAN routing.
- **Router-on-a-stick:** router subinterfaces provide gateways for multiple tagged VLANs.
- **Voice VLAN:** carries phone traffic while an attached computer uses the access VLAN.

A trunk can be operational while one VLAN still fails because that VLAN is missing, inactive, or excluded from the allowed list. A native VLAN mismatch can produce warnings, connectivity problems, and unintended VLAN crossing.

## Inter-VLAN Routing

Hosts in different VLANs require a Layer 3 device. Each host needs the correct address, subnet mask, and default gateway in its own subnet. The router subinterface or SVI must be up, assigned to the right VLAN, and have a route to the destination.

Troubleshooting order:

1. Confirm the host's VLAN and access port.
2. Confirm the VLAN exists and is active.
3. Confirm the VLAN traverses every required trunk.
4. Confirm the gateway SVI or router subinterface is up.
5. Confirm routing and security policy permit the flow.

## STP and RSTP

Spanning Tree Protocol (STP) prevents Layer 2 loops while allowing redundant physical links. The switch with the lowest bridge identifier becomes the root bridge. Every non-root switch selects a root port. Each segment selects a designated port; unnecessary paths block.

Rapid Spanning Tree Protocol (RSTP) converges faster than classic STP.

- **Bridge Protocol Data Unit (BPDU):** control frame switches use to exchange spanning-tree information.
- **PortFast:** moves an appropriate endpoint port to forwarding quickly.
- **BPDU Guard:** can err-disable a PortFast/edge port that receives an unexpected BPDU.
- **Root Guard:** prevents a port from accepting a superior BPDU and changing the intended root location.

Broadcast storms, duplicate frames, high switch central processing unit use, and an unstable MAC table strongly suggest a Layer 2 loop.

## EtherChannel and LACP

EtherChannel combines compatible physical links into one logical port channel. Link Aggregation Control Protocol (LACP) negotiates standards-based bundles.

| Local mode | Remote mode | Bundle forms? |
|---|---|---|
| Active | Active | Yes |
| Active | Passive | Yes |
| Passive | Passive | No |

Members must agree on speed, duplex, access/trunk state, native VLAN, and allowed VLANs. A hash distributes conversations; one flow normally does not use the bandwidth of every member simultaneously.

## Verification

```text
show mac address-table
show vlan brief
show interfaces switchport
show interfaces trunk
show spanning-tree
show spanning-tree root
show etherchannel summary
show interfaces counters errors
show ip interface brief
```

| Symptom | First checks |
|---|---|
| One VLAN fails across switches | VLAN existence and allowed list on every trunk |
| Same VLAN works; remote VLAN fails | Gateway, SVI/subinterface, routing, ACL |
| Port channel does not form | Member consistency and LACP modes |
| Failure after redundant link added | STP state and loop evidence |
| Phone works; attached computer fails | Voice VLAN versus access VLAN |

## Check Your Understanding

1. Why can VLAN 20 fail across a trunk while VLAN 10 continues working?
2. Why will LACP passive/passive not form a channel?
3. What evidence distinguishes a Layer 2 loop from a routing failure?

## Video Review

- **Sunny Classroom — VLAN fundamentals**
  - <https://youtube.com/@sunnyclassroom24/search?query=VLAN>
- **Sunny Classroom — STP and LACP**
  - <https://youtube.com/@sunnyclassroom24/search?query=STP%20LACP>
- **Professor Messer — Switching Issues, N10-009**
  - <https://www.professormesser.com/network-plus/n10-009/n10-009-video/switching-issues-n10-009/>

## Acronyms

- **BPDU** — Bridge Protocol Data Unit
- **IEEE** — Institute of Electrical and Electronics Engineers
- **LACP** — Link Aggregation Control Protocol
- **MAC** — Media Access Control
- **RSTP** — Rapid Spanning Tree Protocol
- **STP** — Spanning Tree Protocol
- **SVI** — Switch Virtual Interface
- **VLAN** — Virtual Local Area Network

