---
layout: page
title: "SF 1041 Domain 1 | Routing & EIGRP"
date: 2026-09-12 09:05:00 -0700
permalink: /network-portfolio/sf-1041-network-exam-prep/review/routing-eigrp/
categories:
  - portfolio
  - study-tools
  - networking
tags:
  - sf-1041
  - routing
  - eigrp
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

# Domain 1 — Routing & EIGRP

## The Big Picture

A router reads the destination Internet Protocol (IP) address, searches its routing table, and forwards the packet using the best matching route. A route identifies a destination prefix, next hop or exit interface, route source, and often a metric.

## Route Selection: The Order Matters

1. Find every route whose network prefix contains the destination address.
2. Choose the **longest prefix match**—the most specific route.
3. When identical prefixes come from different route sources, choose the lowest **administrative distance (AD)**.
4. When identical prefixes come from the same routing protocol, choose the best protocol **metric**.
5. If equal-cost paths remain and the router supports it, install multiple routes for load balancing.

Example: For destination `10.10.10.25`, a `/24` route wins over `/16` and `/8` routes even if the `/24` has a higher AD. Prefix length is evaluated before AD.

| What is compared? | Decision value | Question it answers |
|---|---|---|
| Different prefix lengths | Longest prefix match | Which route is most specific? |
| Same prefix, different sources | Administrative distance | Which source is more trusted? |
| Same prefix and same protocol | Metric | Which path does that protocol prefer? |

Common Cisco AD values: connected `0`, static `1`, Enhanced Interior Gateway Routing Protocol (EIGRP) summary `5`, external Border Gateway Protocol (BGP) `20`, internal EIGRP `90`, Open Shortest Path First (OSPF) `110`, Routing Information Protocol (RIP) `120`, and external EIGRP `170`.

## Static, Default, and Floating Static Routes

```text
ip route DESTINATION MASK NEXT-HOP [ADMINISTRATIVE-DISTANCE]
ip route 0.0.0.0 0.0.0.0 NEXT-HOP
```

- A **static route** is manually configured.
- A **default route** (`0.0.0.0/0`) is the least-specific route and is used only when no more-specific route matches.
- A **floating static route** is a backup static route configured with an AD higher than the primary route's AD.

Example: Internal EIGRP routes use AD `90`. A static backup with AD `95` remains out of the routing table while EIGRP is available, then “floats” into use if the EIGRP route disappears.

```text
ip route 192.0.2.0 255.255.255.0 10.0.0.2 95
```

The static route does not monitor application health by itself. It becomes eligible when the competing route is removed. If the next hop stays technically reachable over a failed service path, object tracking may be needed.

## EIGRP Neighbor Formation

EIGRP routers must become neighbors before they exchange routes. They discover one another with Hello packets sent to multicast address `224.0.0.10` for IPv4.

Neighbors normally require:

- Interfaces that are up/up and have Layer 3 connectivity.
- Addresses in the same primary IP subnet on the shared link.
- Matching EIGRP autonomous system (AS) numbers in classic EIGRP.
- Compatible EIGRP metric K-values.
- Matching authentication settings when authentication is configured.
- Interfaces participating in EIGRP and not blocking Hello packets.

Hello and hold timers do **not** have to match exactly. Each router advertises its hold time. A neighbor is removed if no Hello is received before that hold time expires.

```text
show ip eigrp neighbors
show ip protocols
show ip interface brief
show running-config | section router eigrp
```

If there is no neighbor, do not start by changing route metrics. First confirm interface state, subnet, AS number, EIGRP activation, K-values, authentication, and packet filtering.

## EIGRP's Three Tables

| Table | Contains |
|---|---|
| Neighbor table | Directly connected EIGRP neighbors |
| Topology table | EIGRP-learned destinations and candidate paths |
| Routing table | Best usable routes selected for forwarding |

Learning a route into the topology table does not guarantee installation in the routing table. A more-specific route or a lower-AD source may win.

## DUAL, Successors, and Feasible Successors

EIGRP uses the **Diffusing Update Algorithm (DUAL)** to calculate loop-free routes.

- **Successor:** best EIGRP route; installed in the routing table.
- **Feasible distance (FD):** local router's best total metric to the destination.
- **Reported distance (RD):** neighbor's advertised distance from itself to the destination; also called advertised distance.
- **Feasible successor:** prequalified loop-free backup path.
- **Feasibility condition:** the neighbor's RD must be lower than the current successor's FD: `RD < FD`.

A backup path can be valid and reachable without meeting the feasibility condition. In that case it is not a feasible successor, and DUAL may need to query neighbors after the successor fails.

## Convergence—What It Actually Means

**Convergence** is the point at which routers have processed a topology change and their routing information is again consistent and stable. It is more than “all tables were updated”; routers must agree on usable paths and forwarding must stabilize.

When a successor fails:

1. EIGRP detects the loss through interface state, an expired hold timer, or another event.
2. If a feasible successor exists, DUAL installs it immediately—fast local convergence.
3. If none exists, the route becomes **Active** and the router sends Queries.
4. Neighbors search for alternatives and send Replies.
5. DUAL selects a new loop-free successor; the route returns to **Passive**, the normal stable state.

**Stuck in Active (SIA)** means a required Query Reply was not received before the active timer expired. It does not mean the route is simply busy.

## Metric and Load Balancing

Classic EIGRP uses minimum bandwidth and cumulative delay by default. Load and reliability exist as K-value components but are not used by default. The path with the lowest composite metric becomes the successor.

EIGRP can perform unequal-cost load balancing with `variance`, but a path must still satisfy the feasibility condition and fall within the allowed metric multiplier.

## Protocol Comparison

| Protocol | Type and scope | Main decision |
|---|---|---|
| RIP | Distance-vector Interior Gateway Protocol (IGP) | Lowest hop count; 15 hops maximum usable |
| OSPF | Link-state IGP | Lowest accumulated cost |
| EIGRP | Advanced distance-vector IGP | Lowest composite metric |
| BGP | Path-vector Exterior Gateway Protocol (EGP) | Policy and path attributes, including AS path |

## Verification and Troubleshooting

```text
show ip route
show ip route 192.0.2.25
show ip protocols
show ip eigrp neighbors
show ip eigrp topology
show ip eigrp topology all-links
show ip interface brief
ping 192.0.2.25
traceroute 192.0.2.25
```

| Symptom | Strong first checks |
|---|---|
| No EIGRP neighbor | Interface, subnet, AS, activation, K-values, authentication |
| Neighbor exists; route missing | Topology table, advertisement, filters, summary, competing route |
| Unexpected route installed | Prefix length, then AD, then metric |
| Slow recovery | Feasible successor, query scope, SIA evidence |
| Floating route never appears | Backup AD, next-hop reachability, primary route still installed |

## Check Your Understanding

1. OSPF advertises `10.1.0.0/16`; a static route advertises `10.1.2.0/24` with AD 200. Which route forwards traffic to `10.1.2.50`, and why?
2. An EIGRP neighbor appears, but a destination is absent from `show ip route`. Which table should you inspect next?
3. EIGRP's successor fails and a feasible successor exists. Does the route need to become Active?
4. Why must a floating static route have an AD higher than the primary dynamic route?

## Video Review

- **Sunny Classroom — EIGRP and routing videos**
  - <https://youtube.com/@sunnyclassroom24/search?query=EIGRP%20routing>
- **Sunny Classroom — Subnetting videos**
  - <https://youtube.com/@sunnyclassroom24/search?query=subnetting>
- **Professor Messer — Dynamic Routing, N10-009**
  - <https://www.professormesser.com/network-plus/n10-009/n10-009-video/dynamic-routing-n10-009/>

## Acronyms

- **AD** — Administrative Distance
- **AS** — Autonomous System
- **BGP** — Border Gateway Protocol
- **DUAL** — Diffusing Update Algorithm
- **EGP** — Exterior Gateway Protocol
- **EIGRP** — Enhanced Interior Gateway Routing Protocol
- **FD** — Feasible Distance
- **IGP** — Interior Gateway Protocol
- **IP** — Internet Protocol
- **OSPF** — Open Shortest Path First
- **RD** — Reported Distance
- **RIP** — Routing Information Protocol
- **SIA** — Stuck in Active

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