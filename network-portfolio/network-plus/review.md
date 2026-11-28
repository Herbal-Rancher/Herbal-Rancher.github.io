---
layout: page
hr_theme: network
title: Network+ Objective Review
permalink: /network-portfolio/network-plus/review/
---

[Study Center](/network-portfolio/network-plus/) · [Practice](/network-portfolio/network-plus/practice/) · [Test Readiness Lab](/test-readiness-lab/)

v0.8 technical review: concept contrasts, deployment reasoning, hands-on verification and further reading for all 25 objectives. Not an exhaustive exam syllabus.

<a id="objective-1-1"></a>

## 1.1 — OSI and encapsulation

### Technical distinctions

- **Physical layer:** Signal encoding and bit transmission.
- **Data link layer:** MAC addressing and frame delivery.
- **Network layer:** Logical addressing and routing.
- **Transport layer:** End-to-end port multiplexing and reliability.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


Application data is carried by TCP segments or UDP datagrams, then IP packets, then link-layer frames. Routers replace link-layer headers at each routed hop; IP addresses normally persist absent NAT. TCP ports identify endpoints, not physical interfaces. TLS does not fit perfectly into one OSI layer.


### Deep dive — Encapsulation and forwarding

A switch uses destination MAC addresses within a VLAN; a router uses destination IP prefixes between networks. TCP sequence numbers support ordered delivery; UDP has no built-in retransmission. Session and presentation functions include dialogue management and representation, though real protocols span layers.

**Hands-on verification:** Capture a ping on both sides of a router and compare Ethernet addresses, IP addresses and TTL.

**Reference for further study:** RFC 8200.

[Practice this objective](../practice/?objective=1.1) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| PDU | Protocol data unit; layer-specific representation of data |
| MAC | Media access control; link-layer addressing |
| MTU | Maximum transmission unit; largest network-layer packet carried without fragmentation on a link |

### Technical quick-reference table

| Layer | Evidence | Interpretation |
| --- | --- | --- |
| Physical | Link light, signal | No carrier suggests physical fault |
| Data link | MAC table, VLAN | Incorrect VLAN isolates hosts |
| Network | IP route, TTL | Missing route prevents forwarding |
| Transport | TCP SYN/ACK | No reply may indicate filtering or service failure |
| Application | DNS response, HTTP status | Successful transport does not guarantee application success |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>Which header is normally replaced at each routed Ethernet hop?</summary>

**Answer:** Ethernet header

Application data is carried by TCP segments or UDP datagrams, then IP packets, then link-layer frames. Routers replace link-layer headers at each routed hop; IP addresses normally persist absent NAT. TCP ports identify endpoints, not physical interfaces. TLS does not fit perfectly into one OSI layer.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: signals and bit transmission?</summary>

**Answer:** Physical

Physical: Signals and bit transmission. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: local frame delivery using MAC addresses?</summary>

**Answer:** Data link

Data link: Local frame delivery using MAC addresses. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: forwarding packets between IP networks?</summary>

**Answer:** Network

Network: Forwarding packets between IP networks. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: end-to-end multiplexing using ports?</summary>

**Answer:** Transport

Transport: End-to-end multiplexing using ports. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: conceptual layer for representation and encoding?</summary>

**Answer:** Presentation

Presentation: Conceptual layer for representation and encoding. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>A capture shows the destination MAC changes at a router but the destination IP stays the same. Which layer is being rebuilt for the next hop?</summary>

**Answer:** Data link

A router constructs a new local frame for the next link while normally retaining the destination IP.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Data link?</summary>

**Answer:** Local frame delivery using MAC addresses

Data link refers to local frame delivery using MAC addresses. The alternatives instead describe Physical, Network, Transport.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Network?</summary>

**Answer:** Forwarding packets between IP networks

Network refers to forwarding packets between IP networks. The alternatives instead describe Physical, Data link, Transport.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Transport?</summary>

**Answer:** End-to-end multiplexing using ports

Transport refers to end-to-end multiplexing using ports. The alternatives instead describe Physical, Data link, Network.

</details>

<details class="hr-qa" markdown="1">
<summary>A capture shows valid Ethernet frames but TCP retransmissions after a remote firewall change. Which layer should you investigate for blocked destination ports?</summary>

**Answer:** Transport

TCP ports are transport-layer identifiers; valid frames do not establish end-to-end delivery. Physical and data link concern local transmission; presentation concerns representation.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: signal encoding and bit transmission?</summary>

**Answer:** Physical layer

Physical layer: Signal encoding and bit transmission; Data link layer: MAC addressing and frame delivery; Network layer: Logical addressing and routing; Transport layer: End-to-end port multiplexing and reliability.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Physical layer from the alternatives?</summary>

**Answer:** Signal encoding and bit transmission

Physical layer: Signal encoding and bit transmission; Data link layer: MAC addressing and frame delivery; Network layer: Logical addressing and routing; Transport layer: End-to-end port multiplexing and reliability.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: mAC addressing and frame delivery?</summary>

**Answer:** Data link layer

Physical layer: Signal encoding and bit transmission; Data link layer: MAC addressing and frame delivery; Network layer: Logical addressing and routing; Transport layer: End-to-end port multiplexing and reliability.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Data link layer from the alternatives?</summary>

**Answer:** MAC addressing and frame delivery

Physical layer: Signal encoding and bit transmission; Data link layer: MAC addressing and frame delivery; Network layer: Logical addressing and routing; Transport layer: End-to-end port multiplexing and reliability.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: logical addressing and routing?</summary>

**Answer:** Network layer

Physical layer: Signal encoding and bit transmission; Data link layer: MAC addressing and frame delivery; Network layer: Logical addressing and routing; Transport layer: End-to-end port multiplexing and reliability.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Network layer from the alternatives?</summary>

**Answer:** Logical addressing and routing

Physical layer: Signal encoding and bit transmission; Data link layer: MAC addressing and frame delivery; Network layer: Logical addressing and routing; Transport layer: End-to-end port multiplexing and reliability.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: end-to-end port multiplexing and reliability?</summary>

**Answer:** Transport layer

Physical layer: Signal encoding and bit transmission; Data link layer: MAC addressing and frame delivery; Network layer: Logical addressing and routing; Transport layer: End-to-end port multiplexing and reliability.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Transport layer from the alternatives?</summary>

**Answer:** End-to-end port multiplexing and reliability

Physical layer: Signal encoding and bit transmission; Data link layer: MAC addressing and frame delivery; Network layer: Logical addressing and routing; Transport layer: End-to-end port multiplexing and reliability.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes Data link layer for a task that requires: signal encoding and bit transmission. Which alternative is the better match?</summary>

**Answer:** Physical layer

Physical layer: Signal encoding and bit transmission; Data link layer: MAC addressing and frame delivery; Network layer: Logical addressing and routing; Transport layer: End-to-end port multiplexing and reliability.

</details>

<details class="hr-qa" markdown="1">
<summary>A frame arrives with a bad FCS — which answer best fits?</summary>

**Answer:** Data link

Data link is the best match for this situation. A switch uses destination MAC addresses within a VLAN; a router uses destination IP prefixes between networks. TCP sequence numbers support ordered delivery; UDP has no built-in retransmission. Session and presentation functions include dialogue management and representation, though real protocols span layers.

</details>

<details class="hr-qa" markdown="1">
<summary>A router decrements IPv4 TTL — which answer best fits?</summary>

**Answer:** Network

Network is the best match for this situation. A switch uses destination MAC addresses within a VLAN; a router uses destination IP prefixes between networks. TCP sequence numbers support ordered delivery; UDP has no built-in retransmission. Session and presentation functions include dialogue management and representation, though real protocols span layers.

</details>

<details class="hr-qa" markdown="1">
<summary>A TCP receiver detects missing sequence numbers — which answer best fits?</summary>

**Answer:** Transport

Transport is the best match for this situation. A switch uses destination MAC addresses within a VLAN; a router uses destination IP prefixes between networks. TCP sequence numbers support ordered delivery; UDP has no built-in retransmission. Session and presentation functions include dialogue management and representation, though real protocols span layers.

</details>

<details class="hr-qa" markdown="1">
<summary>A fiber receiver loses optical signal — which answer best fits?</summary>

**Answer:** Physical

Physical is the best match for this situation. A switch uses destination MAC addresses within a VLAN; a router uses destination IP prefixes between networks. TCP sequence numbers support ordered delivery; UDP has no built-in retransmission. Session and presentation functions include dialogue management and representation, though real protocols span layers.

</details>

<details class="hr-qa" markdown="1">
<summary>A client encodes text as UTF-8 — which answer best fits?</summary>

**Answer:** Presentation

Presentation is the best match for this situation. A switch uses destination MAC addresses within a VLAN; a router uses destination IP prefixes between networks. TCP sequence numbers support ordered delivery; UDP has no built-in retransmission. Session and presentation functions include dialogue management and representation, though real protocols span layers.

</details>

<details class="hr-qa" markdown="1">
<summary>A switch learns a source MAC — which answer best fits?</summary>

**Answer:** Data link

Data link is the best match for this situation. A switch uses destination MAC addresses within a VLAN; a router uses destination IP prefixes between networks. TCP sequence numbers support ordered delivery; UDP has no built-in retransmission. Session and presentation functions include dialogue management and representation, though real protocols span layers.

</details>

<details class="hr-qa" markdown="1">
<summary>A browser sends an HTTP request — which answer best fits?</summary>

**Answer:** Application

Application is the best match for this situation. A switch uses destination MAC addresses within a VLAN; a router uses destination IP prefixes between networks. TCP sequence numbers support ordered delivery; UDP has no built-in retransmission. Session and presentation functions include dialogue management and representation, though real protocols span layers.

</details>

<details class="hr-qa" markdown="1">
<summary>A dialogue is established and managed between applications in the OSI abstraction — which answer best fits?</summary>

**Answer:** Session

Session is the best match for this situation. A switch uses destination MAC addresses within a VLAN; a router uses destination IP prefixes between networks. TCP sequence numbers support ordered delivery; UDP has no built-in retransmission. Session and presentation functions include dialogue management and representation, though real protocols span layers.

</details>

<details class="hr-qa" markdown="1">
<summary>A host multiplexes connections by TCP port — which answer best fits?</summary>

**Answer:** Transport

Transport is the best match for this situation. A switch uses destination MAC addresses within a VLAN; a router uses destination IP prefixes between networks. TCP sequence numbers support ordered delivery; UDP has no built-in retransmission. Session and presentation functions include dialogue management and representation, though real protocols span layers.

</details>

<details class="hr-qa" markdown="1">
<summary>A router forwards to a different Ethernet segment without NAT; which address normally changes — which answer best fits?</summary>

**Answer:** Destination MAC

Destination MAC is the best match for this situation. A switch uses destination MAC addresses within a VLAN; a router uses destination IP prefixes between networks. TCP sequence numbers support ordered delivery; UDP has no built-in retransmission. Session and presentation functions include dialogue management and representation, though real protocols span layers.

</details>


### Visual learning

- [Networking Fundamentals — Ethernet Frame Structure Study Diagram"
](/network-portfolio/study-diagrams/ethernet-frame-structure/)
- [Networking Fundamentals — MAC Address vs IP Address Study Diagram"
](/network-portfolio/study-diagrams/mac-address-vs-ip-address/)
- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)

<a id="objective-1-2"></a>

## 1.2 — Network appliances

### Technical distinctions

- **Stateful firewall:** Tracks connection state to enforce policy.
- **IDS:** Alerts on suspicious traffic without inline blocking.
- **Load balancer:** Distributes client requests among healthy servers.
- **SAN:** Provides block-level storage access.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


Switches learn source MAC addresses and forward frames; routers choose IP routes. A stateful firewall tracks connections; IDS alerts while IPS can block. NAS exposes file shares; SAN exposes block storage. Load balancers distribute requests and proxies mediate connections.


### Deep dive — Appliance placement

A proxy terminates or mediates application connections; a load balancer distributes requests. A CDN caches content near consumers. QoS prioritizes traffic under contention, and TTL limits forwarding lifetime. Wireless controllers coordinate AP configuration. Virtual appliances perform similar functions in software.

**Hands-on verification:** Draw a client-to-web-server path including firewall, load balancer and backend; label where each decision occurs.

**Reference for further study:** RFC 1812.

[Practice this objective](../practice/?objective=1.2) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| IDS | Intrusion detection system; alerts on suspicious activity |
| IPS | Intrusion prevention system; can block suspicious traffic |
| WAF | Web application firewall; filters HTTP application traffic |

### Technical quick-reference table

| Device | Decision basis | Example |
| --- | --- | --- |
| Switch | MAC and VLAN | Local frame forwarding |
| Router | Destination prefix | Inter-subnet traffic |
| Firewall | Policy and connection state | Permit established return traffic |
| Load balancer | Health and distribution policy | Avoid unhealthy servers |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>Which storage architecture normally presents block devices to hosts?</summary>

**Answer:** SAN

Switches learn source MAC addresses and forward frames; routers choose IP routes. A stateful firewall tracks connections; IDS alerts while IPS can block. NAS exposes file shares; SAN exposes block storage. Load balancers distribute requests and proxies mediate connections.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: detects suspicious traffic and raises alerts without inline blocking?</summary>

**Answer:** IDS

IDS: Detects suspicious traffic and raises alerts without inline blocking. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: inline inspection capable of dropping malicious traffic?</summary>

**Answer:** IPS

IPS: Inline inspection capable of dropping malicious traffic. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: shared file-level storage over a network?</summary>

**Answer:** NAS

NAS: Shared file-level storage over a network. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: distributes incoming requests among healthy servers?</summary>

**Answer:** Load balancer

Load balancer: Distributes incoming requests among healthy servers. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: prioritizes delay-sensitive traffic during contention?</summary>

**Answer:** QoS

QoS: Prioritizes delay-sensitive traffic during contention. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>A web service has three replicas. One stops responding and requests must be sent only to healthy replicas. What should perform this function?</summary>

**Answer:** Health-checking load balancer

Health checks allow a load balancer to remove an unavailable backend from rotation.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes IPS?</summary>

**Answer:** Inline inspection capable of dropping malicious traffic

IPS refers to inline inspection capable of dropping malicious traffic. The alternatives instead describe IDS, NAS, Load balancer.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes NAS?</summary>

**Answer:** Shared file-level storage over a network

NAS refers to shared file-level storage over a network. The alternatives instead describe IDS, IPS, Load balancer.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Load balancer?</summary>

**Answer:** Distributes incoming requests among healthy servers

Load balancer refers to distributes incoming requests among healthy servers. The alternatives instead describe IDS, IPS, NAS.

</details>

<details class="hr-qa" markdown="1">
<summary>A web service needs requests distributed among three healthy backend servers. Which component directly provides this function?</summary>

**Answer:** Load balancer

A load balancer selects backend servers; NAS provides file storage, a relay forwards DHCP, and an access switch forwards local frames.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: tracks connection state to enforce policy?</summary>

**Answer:** Stateful firewall

Stateful firewall: Tracks connection state to enforce policy; IDS: Alerts on suspicious traffic without inline blocking; Load balancer: Distributes client requests among healthy servers; SAN: Provides block-level storage access.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Stateful firewall from the alternatives?</summary>

**Answer:** Tracks connection state to enforce policy

Stateful firewall: Tracks connection state to enforce policy; IDS: Alerts on suspicious traffic without inline blocking; Load balancer: Distributes client requests among healthy servers; SAN: Provides block-level storage access.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: alerts on suspicious traffic without inline blocking?</summary>

**Answer:** IDS

Stateful firewall: Tracks connection state to enforce policy; IDS: Alerts on suspicious traffic without inline blocking; Load balancer: Distributes client requests among healthy servers; SAN: Provides block-level storage access.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes IDS from the alternatives?</summary>

**Answer:** Alerts on suspicious traffic without inline blocking

Stateful firewall: Tracks connection state to enforce policy; IDS: Alerts on suspicious traffic without inline blocking; Load balancer: Distributes client requests among healthy servers; SAN: Provides block-level storage access.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: distributes client requests among healthy servers?</summary>

**Answer:** Load balancer

Stateful firewall: Tracks connection state to enforce policy; IDS: Alerts on suspicious traffic without inline blocking; Load balancer: Distributes client requests among healthy servers; SAN: Provides block-level storage access.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Load balancer from the alternatives?</summary>

**Answer:** Distributes client requests among healthy servers

Stateful firewall: Tracks connection state to enforce policy; IDS: Alerts on suspicious traffic without inline blocking; Load balancer: Distributes client requests among healthy servers; SAN: Provides block-level storage access.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: provides block-level storage access?</summary>

**Answer:** SAN

Stateful firewall: Tracks connection state to enforce policy; IDS: Alerts on suspicious traffic without inline blocking; Load balancer: Distributes client requests among healthy servers; SAN: Provides block-level storage access.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes SAN from the alternatives?</summary>

**Answer:** Provides block-level storage access

Stateful firewall: Tracks connection state to enforce policy; IDS: Alerts on suspicious traffic without inline blocking; Load balancer: Distributes client requests among healthy servers; SAN: Provides block-level storage access.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes IDS for a task that requires: tracks connection state to enforce policy. Which alternative is the better match?</summary>

**Answer:** Stateful firewall

Stateful firewall: Tracks connection state to enforce policy; IDS: Alerts on suspicious traffic without inline blocking; Load balancer: Distributes client requests among healthy servers; SAN: Provides block-level storage access.

</details>

<details class="hr-qa" markdown="1">
<summary>A website needs cached static assets near global users — which answer best fits?</summary>

**Answer:** CDN

CDN is the best match for this situation. A proxy terminates or mediates application connections; a load balancer distributes requests. A CDN caches content near consumers. QoS prioritizes traffic under contention, and TTL limits forwarding lifetime. Wireless controllers coordinate AP configuration. Virtual appliances perform similar functions in software.

</details>

<details class="hr-qa" markdown="1">
<summary>A security sensor must block malicious packets inline — which answer best fits?</summary>

**Answer:** IPS

IPS is the best match for this situation. A proxy terminates or mediates application connections; a load balancer distributes requests. A CDN caches content near consumers. QoS prioritizes traffic under contention, and TTL limits forwarding lifetime. Wireless controllers coordinate AP configuration. Virtual appliances perform similar functions in software.

</details>

<details class="hr-qa" markdown="1">
<summary>A service needs requests distributed across healthy servers — which answer best fits?</summary>

**Answer:** Load balancer

Load balancer is the best match for this situation. A proxy terminates or mediates application connections; a load balancer distributes requests. A CDN caches content near consumers. QoS prioritizes traffic under contention, and TTL limits forwarding lifetime. Wireless controllers coordinate AP configuration. Virtual appliances perform similar functions in software.

</details>

<details class="hr-qa" markdown="1">
<summary>A host needs shared file access via SMB — which answer best fits?</summary>

**Answer:** NAS

NAS is the best match for this situation. A proxy terminates or mediates application connections; a load balancer distributes requests. A CDN caches content near consumers. QoS prioritizes traffic under contention, and TTL limits forwarding lifetime. Wireless controllers coordinate AP configuration. Virtual appliances perform similar functions in software.

</details>

<details class="hr-qa" markdown="1">
<summary>A branch needs encrypted connectivity over the internet — which answer best fits?</summary>

**Answer:** VPN

VPN is the best match for this situation. A proxy terminates or mediates application connections; a load balancer distributes requests. A CDN caches content near consumers. QoS prioritizes traffic under contention, and TTL limits forwarding lifetime. Wireless controllers coordinate AP configuration. Virtual appliances perform similar functions in software.

</details>

<details class="hr-qa" markdown="1">
<summary>A campus needs centralized AP configuration — which answer best fits?</summary>

**Answer:** Wireless controller

Wireless controller is the best match for this situation. A proxy terminates or mediates application connections; a load balancer distributes requests. A CDN caches content near consumers. QoS prioritizes traffic under contention, and TTL limits forwarding lifetime. Wireless controllers coordinate AP configuration. Virtual appliances perform similar functions in software.

</details>

<details class="hr-qa" markdown="1">
<summary>A policy must prioritize voice during congestion — which answer best fits?</summary>

**Answer:** QoS

QoS is the best match for this situation. A proxy terminates or mediates application connections; a load balancer distributes requests. A CDN caches content near consumers. QoS prioritizes traffic under contention, and TTL limits forwarding lifetime. Wireless controllers coordinate AP configuration. Virtual appliances perform similar functions in software.

</details>

<details class="hr-qa" markdown="1">
<summary>A client must access web resources through an intermediary — which answer best fits?</summary>

**Answer:** Proxy

Proxy is the best match for this situation. A proxy terminates or mediates application connections; a load balancer distributes requests. A CDN caches content near consumers. QoS prioritizes traffic under contention, and TTL limits forwarding lifetime. Wireless controllers coordinate AP configuration. Virtual appliances perform similar functions in software.

</details>

<details class="hr-qa" markdown="1">
<summary>A server needs remote block storage — which answer best fits?</summary>

**Answer:** SAN

SAN is the best match for this situation. A proxy terminates or mediates application connections; a load balancer distributes requests. A CDN caches content near consumers. QoS prioritizes traffic under contention, and TTL limits forwarding lifetime. Wireless controllers coordinate AP configuration. Virtual appliances perform similar functions in software.

</details>

<details class="hr-qa" markdown="1">
<summary>A packet must not circulate indefinitely through routers — which answer best fits?</summary>

**Answer:** TTL

TTL is the best match for this situation. A proxy terminates or mediates application connections; a load balancer distributes requests. A CDN caches content near consumers. QoS prioritizes traffic under contention, and TTL limits forwarding lifetime. Wireless controllers coordinate AP configuration. Virtual appliances perform similar functions in software.

</details>


### Visual learning

- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)

<a id="objective-1-3"></a>

## 1.3 — Cloud networking

### Technical distinctions

- **IaaS:** Customer manages guest operating systems.
- **PaaS:** Provider manages runtime and underlying infrastructure.
- **SaaS:** Customer consumes a hosted application.
- **Private endpoint:** Accesses a cloud service through private addressing.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


IaaS exposes virtual infrastructure, PaaS manages the runtime, SaaS delivers an application. A virtual private cloud isolates logical networks; route tables and security rules control connectivity. Public, private and hybrid deployment models differ from service models.


### Deep dive — Cloud paths and responsibility

A VPC is a logical network with subnets and routing. Internet gateways provide internet paths; NAT gateways commonly allow outbound connections from private IPv4 subnets. Security groups and subnet ACLs differ by provider; verify statefulness. Elasticity adjusts capacity with demand, while scalability is the ability to grow. NFV implements network functions in software.

**Hands-on verification:** Sketch public and private subnets; trace an outbound update and an inbound web request separately.

**Reference for further study:** NIST SP 800-145.

[Practice this objective](../practice/?objective=1.3) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| IaaS | Infrastructure as a service; virtual compute and networking |
| PaaS | Platform as a service; managed application runtime |
| SaaS | Software as a service; hosted application |
| VPC | Virtual private cloud; isolated logical network |

### Technical quick-reference table

| Model | Responsibility | Example |
| --- | --- | --- |
| IaaS | Customer manages guest OS | Virtual router |
| PaaS | Provider manages runtime | Managed application platform |
| SaaS | Provider manages application | Hosted email |
| VPC | Logical network isolation | Private subnets and route tables |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>Which service model lets you manage the guest OS on a rented VM?</summary>

**Answer:** IaaS

IaaS exposes virtual infrastructure, PaaS manages the runtime, SaaS delivers an application. A virtual private cloud isolates logical networks; route tables and security rules control connectivity. Public, private and hybrid deployment models differ from service models.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: managed application runtime without managing guest operating systems?</summary>

**Answer:** PaaS

PaaS: Managed application runtime without managing guest operating systems. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: provider-operated application consumed by end users?</summary>

**Answer:** SaaS

SaaS: Provider-operated application consumed by end users. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: allows private IPv4 workloads to initiate external connections using translated addresses?</summary>

**Answer:** NAT gateway

NAT gateway: Allows private IPv4 workloads to initiate external connections using translated addresses. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: automatically adjusting capacity as demand rises and falls?</summary>

**Answer:** Elasticity

Elasticity: Automatically adjusting capacity as demand rises and falls. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: running network functions as software rather than dedicated appliances?</summary>

**Answer:** NFV

NFV: Running network functions as software rather than dedicated appliances. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Private cloud instances need outbound package updates but must not accept unsolicited internet connections. Which component is most appropriate for IPv4 egress?</summary>

**Answer:** NAT gateway

A NAT gateway supports outbound translations; routing and security rules must also permit the traffic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes SaaS?</summary>

**Answer:** Provider-operated application consumed by end users

SaaS refers to provider-operated application consumed by end users. The alternatives instead describe PaaS, NAT gateway, Elasticity.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes NAT gateway?</summary>

**Answer:** Allows private IPv4 workloads to initiate external connections using translated addresses

NAT gateway refers to allows private IPv4 workloads to initiate external connections using translated addresses. The alternatives instead describe PaaS, SaaS, Elasticity.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Elasticity?</summary>

**Answer:** Automatically adjusting capacity as demand rises and falls

Elasticity refers to automatically adjusting capacity as demand rises and falls. The alternatives instead describe PaaS, SaaS, NAT gateway.

</details>

<details class="hr-qa" markdown="1">
<summary>Private cloud instances need outbound internet access without accepting unsolicited inbound connections. Which gateway is appropriate?</summary>

**Answer:** NAT gateway

A NAT gateway translates outbound connections and permits return traffic; DNS resolves names, a circuit provides connectivity, and a bridge forwards frames.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: customer manages guest operating systems?</summary>

**Answer:** IaaS

IaaS: Customer manages guest operating systems; PaaS: Provider manages runtime and underlying infrastructure; SaaS: Customer consumes a hosted application; Private endpoint: Accesses a cloud service through private addressing.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes IaaS from the alternatives?</summary>

**Answer:** Customer manages guest operating systems

IaaS: Customer manages guest operating systems; PaaS: Provider manages runtime and underlying infrastructure; SaaS: Customer consumes a hosted application; Private endpoint: Accesses a cloud service through private addressing.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: provider manages runtime and underlying infrastructure?</summary>

**Answer:** PaaS

IaaS: Customer manages guest operating systems; PaaS: Provider manages runtime and underlying infrastructure; SaaS: Customer consumes a hosted application; Private endpoint: Accesses a cloud service through private addressing.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes PaaS from the alternatives?</summary>

**Answer:** Provider manages runtime and underlying infrastructure

IaaS: Customer manages guest operating systems; PaaS: Provider manages runtime and underlying infrastructure; SaaS: Customer consumes a hosted application; Private endpoint: Accesses a cloud service through private addressing.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: customer consumes a hosted application?</summary>

**Answer:** SaaS

IaaS: Customer manages guest operating systems; PaaS: Provider manages runtime and underlying infrastructure; SaaS: Customer consumes a hosted application; Private endpoint: Accesses a cloud service through private addressing.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes SaaS from the alternatives?</summary>

**Answer:** Customer consumes a hosted application

IaaS: Customer manages guest operating systems; PaaS: Provider manages runtime and underlying infrastructure; SaaS: Customer consumes a hosted application; Private endpoint: Accesses a cloud service through private addressing.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: accesses a cloud service through private addressing?</summary>

**Answer:** Private endpoint

IaaS: Customer manages guest operating systems; PaaS: Provider manages runtime and underlying infrastructure; SaaS: Customer consumes a hosted application; Private endpoint: Accesses a cloud service through private addressing.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Private endpoint from the alternatives?</summary>

**Answer:** Accesses a cloud service through private addressing

IaaS: Customer manages guest operating systems; PaaS: Provider manages runtime and underlying infrastructure; SaaS: Customer consumes a hosted application; Private endpoint: Accesses a cloud service through private addressing.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes PaaS for a task that requires: customer manages guest operating systems. Which alternative is the better match?</summary>

**Answer:** IaaS

IaaS: Customer manages guest operating systems; PaaS: Provider manages runtime and underlying infrastructure; SaaS: Customer consumes a hosted application; Private endpoint: Accesses a cloud service through private addressing.

</details>

<details class="hr-qa" markdown="1">
<summary>Private IPv4 instances need outbound internet without unsolicited inbound sessions — which answer best fits?</summary>

**Answer:** NAT gateway

NAT gateway is the best match for this situation. A VPC is a logical network with subnets and routing. Internet gateways provide internet paths; NAT gateways commonly allow outbound connections from private IPv4 subnets. Security groups and subnet ACLs differ by provider; verify statefulness. Elasticity adjusts capacity with demand, while scalability is the ability to grow. NFV implements network functions in software.

</details>

<details class="hr-qa" markdown="1">
<summary>A business rents VMs and patches guest OSs — which answer best fits?</summary>

**Answer:** IaaS

IaaS is the best match for this situation. A VPC is a logical network with subnets and routing. Internet gateways provide internet paths; NAT gateways commonly allow outbound connections from private IPv4 subnets. Security groups and subnet ACLs differ by provider; verify statefulness. Elasticity adjusts capacity with demand, while scalability is the ability to grow. NFV implements network functions in software.

</details>

<details class="hr-qa" markdown="1">
<summary>A developer deploys code without managing the runtime OS — which answer best fits?</summary>

**Answer:** PaaS

PaaS is the best match for this situation. A VPC is a logical network with subnets and routing. Internet gateways provide internet paths; NAT gateways commonly allow outbound connections from private IPv4 subnets. Security groups and subnet ACLs differ by provider; verify statefulness. Elasticity adjusts capacity with demand, while scalability is the ability to grow. NFV implements network functions in software.

</details>

<details class="hr-qa" markdown="1">
<summary>A company uses a hosted email application — which answer best fits?</summary>

**Answer:** SaaS

SaaS is the best match for this situation. A VPC is a logical network with subnets and routing. Internet gateways provide internet paths; NAT gateways commonly allow outbound connections from private IPv4 subnets. Security groups and subnet ACLs differ by provider; verify statefulness. Elasticity adjusts capacity with demand, while scalability is the ability to grow. NFV implements network functions in software.

</details>

<details class="hr-qa" markdown="1">
<summary>Capacity automatically shrinks after a demand spike — which answer best fits?</summary>

**Answer:** Elasticity

Elasticity is the best match for this situation. A VPC is a logical network with subnets and routing. Internet gateways provide internet paths; NAT gateways commonly allow outbound connections from private IPv4 subnets. Security groups and subnet ACLs differ by provider; verify statefulness. Elasticity adjusts capacity with demand, while scalability is the ability to grow. NFV implements network functions in software.

</details>

<details class="hr-qa" markdown="1">
<summary>A provider shares infrastructure while isolating customers — which answer best fits?</summary>

**Answer:** Multitenancy

Multitenancy is the best match for this situation. A VPC is a logical network with subnets and routing. Internet gateways provide internet paths; NAT gateways commonly allow outbound connections from private IPv4 subnets. Security groups and subnet ACLs differ by provider; verify statefulness. Elasticity adjusts capacity with demand, while scalability is the ability to grow. NFV implements network functions in software.

</details>

<details class="hr-qa" markdown="1">
<summary>A company links its own data center to public cloud resources — which answer best fits?</summary>

**Answer:** Hybrid cloud

Hybrid cloud is the best match for this situation. A VPC is a logical network with subnets and routing. Internet gateways provide internet paths; NAT gateways commonly allow outbound connections from private IPv4 subnets. Security groups and subnet ACLs differ by provider; verify statefulness. Elasticity adjusts capacity with demand, while scalability is the ability to grow. NFV implements network functions in software.

</details>

<details class="hr-qa" markdown="1">
<summary>A virtual firewall replaces a dedicated appliance — which answer best fits?</summary>

**Answer:** NFV

NFV is the best match for this situation. A VPC is a logical network with subnets and routing. Internet gateways provide internet paths; NAT gateways commonly allow outbound connections from private IPv4 subnets. Security groups and subnet ACLs differ by provider; verify statefulness. Elasticity adjusts capacity with demand, while scalability is the ability to grow. NFV implements network functions in software.

</details>

<details class="hr-qa" markdown="1">
<summary>A predictable private circuit to a cloud provider is required — which answer best fits?</summary>

**Answer:** Dedicated cloud connection

Dedicated cloud connection is the best match for this situation. A VPC is a logical network with subnets and routing. Internet gateways provide internet paths; NAT gateways commonly allow outbound connections from private IPv4 subnets. Security groups and subnet ACLs differ by provider; verify statefulness. Elasticity adjusts capacity with demand, while scalability is the ability to grow. NFV implements network functions in software.

</details>

<details class="hr-qa" markdown="1">
<summary>A subnet has no route to an internet gateway; what should be inspected first — which answer best fits?</summary>

**Answer:** Route table

Route table is the best match for this situation. A VPC is a logical network with subnets and routing. Internet gateways provide internet paths; NAT gateways commonly allow outbound connections from private IPv4 subnets. Security groups and subnet ACLs differ by provider; verify statefulness. Elasticity adjusts capacity with demand, while scalability is the ability to grow. NFV implements network functions in software.

</details>


### Visual learning

- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)

<a id="objective-1-4"></a>

## 1.4 — Protocols and ports

### Technical distinctions

- **DNS:** Resolves names using port 53.
- **SSH:** Encrypted remote shell on TCP 22.
- **SNMP:** Queries device management data on UDP 161.
- **NTP:** Synchronizes clocks using UDP 123.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


TCP provides ordered reliable delivery; UDP does not guarantee delivery. DNS uses UDP and TCP 53; DHCPv4 uses UDP 67/68; SSH and SFTP use TCP 22; HTTPS commonly uses TCP 443 or UDP 443 for HTTP/3. ICMP and GRE use IP protocol numbers rather than transport ports.

[Related completed lab](/network-portfolio/videos/lab-6-1-7-tcp-three-way-handshake/)


### Deep dive — Service flows

TCP establishes connections; UDP sends datagrams. DNS uses UDP and TCP 53; DHCP uses UDP 67/68. SSH/SFTP use TCP 22; HTTPS normally TCP 443 (HTTP/3 uses QUIC over UDP). SMTP submission commonly uses 587 with STARTTLS, implicit TLS 465. IPsec ESP protects payloads, AH authenticates without encryption, IKE negotiates security associations. GRE alone does not encrypt.

**Hands-on verification:** Use a capture to identify source ephemeral ports and destination service ports; distinguish TCP SYN from UDP.

**Reference for further study:** IANA service name registry.

[Practice this objective](../practice/?objective=1.4) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| DNS | Domain name system; resolves names and other records |
| SSH | Secure shell; encrypted remote access, TCP 22 |
| HTTPS | HTTP over TLS; normally TCP 443, HTTP/3 uses QUIC over UDP |
| NTP | Network time protocol; typically UDP 123 |

### Technical quick-reference table

| Protocol | Default transport/port | Purpose |
| --- | --- | --- |
| SSH | TCP 22 | Secure shell |
| DNS | UDP/TCP 53 | Name resolution |
| DHCPv4 | UDP 67/68 | Address configuration |
| HTTPS | TCP 443 (HTTP/3 uses UDP 443) | Secure web |
| SNMP | UDP 161/162 | Queries and notifications |
| NTP | UDP 123 | Time synchronization |
| LDAP | TCP 389 | Directory access |
| LDAPS | TCP 636 | TLS-protected directory access |
| SMB | TCP 445 | File sharing |
| SMTP | TCP 25 | Mail relay |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>A DNS response is truncated over UDP. Which transport can the client retry on port 53?</summary>

**Answer:** TCP

TCP provides ordered reliable delivery; UDP does not guarantee delivery. DNS uses UDP and TCP 53; DHCPv4 uses UDP 67/68; SSH and SFTP use TCP 22; HTTPS commonly uses TCP 443 or UDP 443 for HTTP/3. ICMP and GRE use IP protocol numbers rather than transport ports.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: secure remote shell, typically TCP 22?</summary>

**Answer:** SSH

SSH: Secure remote shell, typically TCP 22. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: clock synchronization, typically UDP 123?</summary>

**Answer:** NTP

NTP: Clock synchronization, typically UDP 123. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: windows-style file sharing, typically TCP 445?</summary>

**Answer:** SMB

SMB: Windows-style file sharing, typically TCP 445. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: iP control and diagnostic messages without TCP or UDP ports?</summary>

**Answer:** ICMP

ICMP: IP control and diagnostic messages without TCP or UDP ports. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: multiple locations advertise the same destination address and routing selects one?</summary>

**Answer:** Anycast

Anycast: Multiple locations advertise the same destination address and routing selects one. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>A firewall permits UDP 53 but large DNS responses fail when clients retry over TCP. Which additional destination port and transport should be permitted to the resolver?</summary>

**Answer:** TCP 53

DNS can retry truncated UDP responses using TCP on port 53.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes NTP?</summary>

**Answer:** Clock synchronization, typically UDP 123

NTP refers to clock synchronization, typically UDP 123. The alternatives instead describe SSH, SMB, ICMP.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes SMB?</summary>

**Answer:** Windows-style file sharing, typically TCP 445

SMB refers to windows-style file sharing, typically TCP 445. The alternatives instead describe SSH, NTP, ICMP.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes ICMP?</summary>

**Answer:** IP control and diagnostic messages without TCP or UDP ports

ICMP refers to iP control and diagnostic messages without TCP or UDP ports. The alternatives instead describe SSH, NTP, SMB.

</details>

<details class="hr-qa" markdown="1">
<summary>A firewall allows UDP 53 but blocks TCP 53. Small DNS replies work while some large replies fail. What should be allowed?</summary>

**Answer:** TCP 53

DNS can retry truncated UDP replies over TCP 53. The other ports serve mail, DHCP and SMB respectively.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: resolves names using port 53?</summary>

**Answer:** DNS

DNS: Resolves names using port 53; SSH: Encrypted remote shell on TCP 22; SNMP: Queries device management data on UDP 161; NTP: Synchronizes clocks using UDP 123.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes DNS from the alternatives?</summary>

**Answer:** Resolves names using port 53

DNS: Resolves names using port 53; SSH: Encrypted remote shell on TCP 22; SNMP: Queries device management data on UDP 161; NTP: Synchronizes clocks using UDP 123.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: encrypted remote shell on TCP 22?</summary>

**Answer:** SSH

DNS: Resolves names using port 53; SSH: Encrypted remote shell on TCP 22; SNMP: Queries device management data on UDP 161; NTP: Synchronizes clocks using UDP 123.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes SSH from the alternatives?</summary>

**Answer:** Encrypted remote shell on TCP 22

DNS: Resolves names using port 53; SSH: Encrypted remote shell on TCP 22; SNMP: Queries device management data on UDP 161; NTP: Synchronizes clocks using UDP 123.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: queries device management data on UDP 161?</summary>

**Answer:** SNMP

DNS: Resolves names using port 53; SSH: Encrypted remote shell on TCP 22; SNMP: Queries device management data on UDP 161; NTP: Synchronizes clocks using UDP 123.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes SNMP from the alternatives?</summary>

**Answer:** Queries device management data on UDP 161

DNS: Resolves names using port 53; SSH: Encrypted remote shell on TCP 22; SNMP: Queries device management data on UDP 161; NTP: Synchronizes clocks using UDP 123.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: synchronizes clocks using UDP 123?</summary>

**Answer:** NTP

DNS: Resolves names using port 53; SSH: Encrypted remote shell on TCP 22; SNMP: Queries device management data on UDP 161; NTP: Synchronizes clocks using UDP 123.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes NTP from the alternatives?</summary>

**Answer:** Synchronizes clocks using UDP 123

DNS: Resolves names using port 53; SSH: Encrypted remote shell on TCP 22; SNMP: Queries device management data on UDP 161; NTP: Synchronizes clocks using UDP 123.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes SSH for a task that requires: resolves names using port 53. Which alternative is the better match?</summary>

**Answer:** DNS

DNS: Resolves names using port 53; SSH: Encrypted remote shell on TCP 22; SNMP: Queries device management data on UDP 161; NTP: Synchronizes clocks using UDP 123.

</details>

<details class="hr-qa" markdown="1">
<summary>A firewall must allow secure shell administration — which answer best fits?</summary>

**Answer:** TCP 22

TCP 22 is the best match for this situation. TCP establishes connections; UDP sends datagrams. DNS uses UDP and TCP 53; DHCP uses UDP 67/68. SSH/SFTP use TCP 22; HTTPS normally TCP 443 (HTTP/3 uses QUIC over UDP). SMTP submission commonly uses 587 with STARTTLS, implicit TLS 465. IPsec ESP protects payloads, AH authenticates without encryption, IKE negotiates security associations. GRE alone does not encrypt.

</details>

<details class="hr-qa" markdown="1">
<summary>A DNS zone transfer needs its normal transport — which answer best fits?</summary>

**Answer:** TCP 53

TCP 53 is the best match for this situation. TCP establishes connections; UDP sends datagrams. DNS uses UDP and TCP 53; DHCP uses UDP 67/68. SSH/SFTP use TCP 22; HTTPS normally TCP 443 (HTTP/3 uses QUIC over UDP). SMTP submission commonly uses 587 with STARTTLS, implicit TLS 465. IPsec ESP protects payloads, AH authenticates without encryption, IKE negotiates security associations. GRE alone does not encrypt.

</details>

<details class="hr-qa" markdown="1">
<summary>A device sends an SNMP notification to a manager — which answer best fits?</summary>

**Answer:** UDP 162

UDP 162 is the best match for this situation. TCP establishes connections; UDP sends datagrams. DNS uses UDP and TCP 53; DHCP uses UDP 67/68. SSH/SFTP use TCP 22; HTTPS normally TCP 443 (HTTP/3 uses QUIC over UDP). SMTP submission commonly uses 587 with STARTTLS, implicit TLS 465. IPsec ESP protects payloads, AH authenticates without encryption, IKE negotiates security associations. GRE alone does not encrypt.

</details>

<details class="hr-qa" markdown="1">
<summary>A workstation synchronizes its clock — which answer best fits?</summary>

**Answer:** UDP 123

UDP 123 is the best match for this situation. TCP establishes connections; UDP sends datagrams. DNS uses UDP and TCP 53; DHCP uses UDP 67/68. SSH/SFTP use TCP 22; HTTPS normally TCP 443 (HTTP/3 uses QUIC over UDP). SMTP submission commonly uses 587 with STARTTLS, implicit TLS 465. IPsec ESP protects payloads, AH authenticates without encryption, IKE negotiates security associations. GRE alone does not encrypt.

</details>

<details class="hr-qa" markdown="1">
<summary>A Windows client opens an SMB share — which answer best fits?</summary>

**Answer:** TCP 445

TCP 445 is the best match for this situation. TCP establishes connections; UDP sends datagrams. DNS uses UDP and TCP 53; DHCP uses UDP 67/68. SSH/SFTP use TCP 22; HTTPS normally TCP 443 (HTTP/3 uses QUIC over UDP). SMTP submission commonly uses 587 with STARTTLS, implicit TLS 465. IPsec ESP protects payloads, AH authenticates without encryption, IKE negotiates security associations. GRE alone does not encrypt.

</details>

<details class="hr-qa" markdown="1">
<summary>A client submits mail using STARTTLS on the submission service — which answer best fits?</summary>

**Answer:** TCP 587

TCP 587 is the best match for this situation. TCP establishes connections; UDP sends datagrams. DNS uses UDP and TCP 53; DHCP uses UDP 67/68. SSH/SFTP use TCP 22; HTTPS normally TCP 443 (HTTP/3 uses QUIC over UDP). SMTP submission commonly uses 587 with STARTTLS, implicit TLS 465. IPsec ESP protects payloads, AH authenticates without encryption, IKE negotiates security associations. GRE alone does not encrypt.

</details>

<details class="hr-qa" markdown="1">
<summary>A remote desktop client uses the default service port — which answer best fits?</summary>

**Answer:** 3389

3389 is the best match for this situation. TCP establishes connections; UDP sends datagrams. DNS uses UDP and TCP 53; DHCP uses UDP 67/68. SSH/SFTP use TCP 22; HTTPS normally TCP 443 (HTTP/3 uses QUIC over UDP). SMTP submission commonly uses 587 with STARTTLS, implicit TLS 465. IPsec ESP protects payloads, AH authenticates without encryption, IKE negotiates security associations. GRE alone does not encrypt.

</details>

<details class="hr-qa" markdown="1">
<summary>A packet is delivered to one of several servers advertising the same address — which answer best fits?</summary>

**Answer:** Anycast

Anycast is the best match for this situation. TCP establishes connections; UDP sends datagrams. DNS uses UDP and TCP 53; DHCP uses UDP 67/68. SSH/SFTP use TCP 22; HTTPS normally TCP 443 (HTTP/3 uses QUIC over UDP). SMTP submission commonly uses 587 with STARTTLS, implicit TLS 465. IPsec ESP protects payloads, AH authenticates without encryption, IKE negotiates security associations. GRE alone does not encrypt.

</details>

<details class="hr-qa" markdown="1">
<summary>A tunnel needs confidentiality for IP payloads — which answer best fits?</summary>

**Answer:** IPsec ESP with encryption

IPsec ESP with encryption is the best match for this situation. TCP establishes connections; UDP sends datagrams. DNS uses UDP and TCP 53; DHCP uses UDP 67/68. SSH/SFTP use TCP 22; HTTPS normally TCP 443 (HTTP/3 uses QUIC over UDP). SMTP submission commonly uses 587 with STARTTLS, implicit TLS 465. IPsec ESP protects payloads, AH authenticates without encryption, IKE negotiates security associations. GRE alone does not encrypt.

</details>

<details class="hr-qa" markdown="1">
<summary>A phone uses SIP over TLS on its conventional port — which answer best fits?</summary>

**Answer:** 5061

5061 is the best match for this situation. TCP establishes connections; UDP sends datagrams. DNS uses UDP and TCP 53; DHCP uses UDP 67/68. SSH/SFTP use TCP 22; HTTPS normally TCP 443 (HTTP/3 uses QUIC over UDP). SMTP submission commonly uses 587 with STARTTLS, implicit TLS 465. IPsec ESP protects payloads, AH authenticates without encryption, IKE negotiates security associations. GRE alone does not encrypt.

</details>


### Visual learning

- [Technical Communication — Network Protocols Ultimate Quick Reference & Learning Tool"
](/network-portfolio/study-diagrams/network-protocols-ultimate-reference/)
- [Networking Fundamentals — Top Network Ports Study Guide"
](/network-portfolio/study-diagrams/top-network-ports/)
- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)

<a id="objective-1-5"></a>

## 1.5 — Media and transceivers

### Technical distinctions

- **Single-mode fiber:** Long-distance optical links with narrow core.
- **Multimode fiber:** Shorter optical links with multiple propagation modes.
- **Twinax DAC:** Short direct copper connection between compatible ports.
- **Cat 6A:** Balanced copper supporting 10GBASE-T up to 100 meters.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


Copper Ethernet uses electrical signaling; fiber uses light. Single-mode fiber supports long distances; multimode commonly serves shorter links. Match transceiver wavelength, fiber type and link budget. DAC is useful for short rack connections. T568A and T568B specify pair placement.


### Deep dive — Media engineering

Single-mode fiber supports long optical paths; multimode is common for shorter links. Match wavelength, fiber type, connector and supported speed at both ends. DAC is useful for short rack links. Copper Ethernet distance depends on the standard; typical balanced twisted-pair channels are 100 m. Plenum rating concerns fire/smoke requirements, not speed.

**Hands-on verification:** Read transceiver labels and compare both ends before replacing a link; inspect and clean fiber using approved procedures.

**Reference for further study:** IEEE 802.3.

[Practice this objective](../practice/?objective=1.5) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| SMF | Single-mode fiber; narrow core for long links |
| MMF | Multimode fiber; multiple light paths for shorter links |
| SFP | Small form-factor pluggable; modular transceiver |
| DAC | Direct attach cable; short copper interconnect |

### Technical quick-reference table

| Medium | Strength | Limitation |
| --- | --- | --- |
| Copper twisted pair | Low cost and PoE | Distance and interference |
| Multimode fiber | Short optical links | Modal dispersion |
| Single-mode fiber | Long optical links | Optics compatibility |
| DAC | Short rack connections | Limited reach |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>Which medium is immune to electromagnetic interference along its transmission path?</summary>

**Answer:** Optical fiber

Copper Ethernet uses electrical signaling; fiber uses light. Single-mode fiber supports long distances; multimode commonly serves shorter links. Match transceiver wavelength, fiber type and link budget. DAC is useful for short rack connections. T568A and T568B specify pair placement.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: optical medium suited to long-distance links with a small core?</summary>

**Answer:** Single-mode fiber

Single-mode fiber: Optical medium suited to long-distance links with a small core. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: short direct-attach copper link between compatible switch ports?</summary>

**Answer:** DAC

DAC: Short direct-attach copper link between compatible switch ports. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: compact fiber connector commonly used with SFP optics?</summary>

**Answer:** LC

LC: Compact fiber connector commonly used with SFP optics. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: cable jacket rated for applicable environmental air-handling spaces?</summary>

**Answer:** Plenum-rated cable

Plenum-rated cable: Cable jacket rated for applicable environmental air-handling spaces. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: pluggable form factor commonly supporting multiple high-speed lanes?</summary>

**Answer:** QSFP

QSFP: Pluggable form factor commonly supporting multiple high-speed lanes. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Two buildings are 4 km apart and the route passes near heavy electrical equipment. Which medium is the best starting choice?</summary>

**Answer:** Single-mode fiber

Single-mode fiber supports long links and is immune to electromagnetic interference along the optical path; select compatible optics and verify link budget.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes DAC?</summary>

**Answer:** Short direct-attach copper link between compatible switch ports

DAC refers to short direct-attach copper link between compatible switch ports. The alternatives instead describe Single-mode fiber, LC, Plenum-rated cable.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes LC?</summary>

**Answer:** Compact fiber connector commonly used with SFP optics

LC refers to compact fiber connector commonly used with SFP optics. The alternatives instead describe Single-mode fiber, DAC, Plenum-rated cable.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Plenum-rated cable?</summary>

**Answer:** Cable jacket rated for applicable environmental air-handling spaces

Plenum-rated cable refers to cable jacket rated for applicable environmental air-handling spaces. The alternatives instead describe Single-mode fiber, DAC, LC.

</details>

<details class="hr-qa" markdown="1">
<summary>A campus link crosses a high-interference industrial area over 2 km. Which medium is most appropriate?</summary>

**Answer:** Single-mode fiber

Single-mode fiber supports long optical links and resists electromagnetic interference. DAC and copper Ethernet have much shorter typical reach; USB is not a campus backbone medium.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: long-distance optical links with narrow core?</summary>

**Answer:** Single-mode fiber

Single-mode fiber: Long-distance optical links with narrow core; Multimode fiber: Shorter optical links with multiple propagation modes; Twinax DAC: Short direct copper connection between compatible ports; Cat 6A: Balanced copper supporting 10GBASE-T up to 100 meters.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Single-mode fiber from the alternatives?</summary>

**Answer:** Long-distance optical links with narrow core

Single-mode fiber: Long-distance optical links with narrow core; Multimode fiber: Shorter optical links with multiple propagation modes; Twinax DAC: Short direct copper connection between compatible ports; Cat 6A: Balanced copper supporting 10GBASE-T up to 100 meters.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: shorter optical links with multiple propagation modes?</summary>

**Answer:** Multimode fiber

Single-mode fiber: Long-distance optical links with narrow core; Multimode fiber: Shorter optical links with multiple propagation modes; Twinax DAC: Short direct copper connection between compatible ports; Cat 6A: Balanced copper supporting 10GBASE-T up to 100 meters.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Multimode fiber from the alternatives?</summary>

**Answer:** Shorter optical links with multiple propagation modes

Single-mode fiber: Long-distance optical links with narrow core; Multimode fiber: Shorter optical links with multiple propagation modes; Twinax DAC: Short direct copper connection between compatible ports; Cat 6A: Balanced copper supporting 10GBASE-T up to 100 meters.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: short direct copper connection between compatible ports?</summary>

**Answer:** Twinax DAC

Single-mode fiber: Long-distance optical links with narrow core; Multimode fiber: Shorter optical links with multiple propagation modes; Twinax DAC: Short direct copper connection between compatible ports; Cat 6A: Balanced copper supporting 10GBASE-T up to 100 meters.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Twinax DAC from the alternatives?</summary>

**Answer:** Short direct copper connection between compatible ports

Single-mode fiber: Long-distance optical links with narrow core; Multimode fiber: Shorter optical links with multiple propagation modes; Twinax DAC: Short direct copper connection between compatible ports; Cat 6A: Balanced copper supporting 10GBASE-T up to 100 meters.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: balanced copper supporting 10GBASE-T up to 100 meters?</summary>

**Answer:** Cat 6A

Single-mode fiber: Long-distance optical links with narrow core; Multimode fiber: Shorter optical links with multiple propagation modes; Twinax DAC: Short direct copper connection between compatible ports; Cat 6A: Balanced copper supporting 10GBASE-T up to 100 meters.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Cat 6A from the alternatives?</summary>

**Answer:** Balanced copper supporting 10GBASE-T up to 100 meters

Single-mode fiber: Long-distance optical links with narrow core; Multimode fiber: Shorter optical links with multiple propagation modes; Twinax DAC: Short direct copper connection between compatible ports; Cat 6A: Balanced copper supporting 10GBASE-T up to 100 meters.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes Multimode fiber for a task that requires: long-distance optical links with narrow core. Which alternative is the better match?</summary>

**Answer:** Single-mode fiber

Single-mode fiber: Long-distance optical links with narrow core; Multimode fiber: Shorter optical links with multiple propagation modes; Twinax DAC: Short direct copper connection between compatible ports; Cat 6A: Balanced copper supporting 10GBASE-T up to 100 meters.

</details>

<details class="hr-qa" markdown="1">
<summary>A 10 km optical link needs a suitable medium — which answer best fits?</summary>

**Answer:** Single-mode fiber

Single-mode fiber is the best match for this situation. Single-mode fiber supports long optical paths; multimode is common for shorter links. Match wavelength, fiber type, connector and supported speed at both ends. DAC is useful for short rack links. Copper Ethernet distance depends on the standard; typical balanced twisted-pair channels are 100 m. Plenum rating concerns fire/smoke requirements, not speed.

</details>

<details class="hr-qa" markdown="1">
<summary>Two adjacent rack switches need a short inexpensive supported link — which answer best fits?</summary>

**Answer:** DAC

DAC is the best match for this situation. Single-mode fiber supports long optical paths; multimode is common for shorter links. Match wavelength, fiber type, connector and supported speed at both ends. DAC is useful for short rack links. Copper Ethernet distance depends on the standard; typical balanced twisted-pair channels are 100 m. Plenum rating concerns fire/smoke requirements, not speed.

</details>

<details class="hr-qa" markdown="1">
<summary>A cable runs through an environmental air-handling space requiring plenum rating — which answer best fits?</summary>

**Answer:** Plenum-rated cable

Plenum-rated cable is the best match for this situation. Single-mode fiber supports long optical paths; multimode is common for shorter links. Match wavelength, fiber type, connector and supported speed at both ends. DAC is useful for short rack links. Copper Ethernet distance depends on the standard; typical balanced twisted-pair channels are 100 m. Plenum rating concerns fire/smoke requirements, not speed.

</details>

<details class="hr-qa" markdown="1">
<summary>A duplex optical link uses small latch connectors — which answer best fits?</summary>

**Answer:** LC

LC is the best match for this situation. Single-mode fiber supports long optical paths; multimode is common for shorter links. Match wavelength, fiber type, connector and supported speed at both ends. DAC is useful for short rack links. Copper Ethernet distance depends on the standard; typical balanced twisted-pair channels are 100 m. Plenum rating concerns fire/smoke requirements, not speed.

</details>

<details class="hr-qa" markdown="1">
<summary>A parallel optical assembly uses a multifiber connector — which answer best fits?</summary>

**Answer:** MPO

MPO is the best match for this situation. Single-mode fiber supports long optical paths; multimode is common for shorter links. Match wavelength, fiber type, connector and supported speed at both ends. DAC is useful for short rack links. Copper Ethernet distance depends on the standard; typical balanced twisted-pair channels are 100 m. Plenum rating concerns fire/smoke requirements, not speed.

</details>

<details class="hr-qa" markdown="1">
<summary>A coax cable modem uses a threaded connector — which answer best fits?</summary>

**Answer:** F-type

F-type is the best match for this situation. Single-mode fiber supports long optical paths; multimode is common for shorter links. Match wavelength, fiber type, connector and supported speed at both ends. DAC is useful for short rack links. Copper Ethernet distance depends on the standard; typical balanced twisted-pair channels are 100 m. Plenum rating concerns fire/smoke requirements, not speed.

</details>

<details class="hr-qa" markdown="1">
<summary>A 40G switch port uses a supported quad-lane module form factor — which answer best fits?</summary>

**Answer:** QSFP

QSFP is the best match for this situation. Single-mode fiber supports long optical paths; multimode is common for shorter links. Match wavelength, fiber type, connector and supported speed at both ends. DAC is useful for short rack links. Copper Ethernet distance depends on the standard; typical balanced twisted-pair channels are 100 m. Plenum rating concerns fire/smoke requirements, not speed.

</details>

<details class="hr-qa" markdown="1">
<summary>A storage fabric uses a dedicated optical protocol — which answer best fits?</summary>

**Answer:** Fibre Channel

Fibre Channel is the best match for this situation. Single-mode fiber supports long optical paths; multimode is common for shorter links. Match wavelength, fiber type, connector and supported speed at both ends. DAC is useful for short rack links. Copper Ethernet distance depends on the standard; typical balanced twisted-pair channels are 100 m. Plenum rating concerns fire/smoke requirements, not speed.

</details>

<details class="hr-qa" markdown="1">
<summary>A copper run crosses strong electrical interference; which medium avoids electromagnetic pickup — which answer best fits?</summary>

**Answer:** Fiber

Fiber is the best match for this situation. Single-mode fiber supports long optical paths; multimode is common for shorter links. Match wavelength, fiber type, connector and supported speed at both ends. DAC is useful for short rack links. Copper Ethernet distance depends on the standard; typical balanced twisted-pair channels are 100 m. Plenum rating concerns fire/smoke requirements, not speed.

</details>

<details class="hr-qa" markdown="1">
<summary>Two optics have incompatible wavelengths; what is the appropriate fix — which answer best fits?</summary>

**Answer:** Use compatible optics and fiber

Use compatible optics and fiber is the best match for this situation. Single-mode fiber supports long optical paths; multimode is common for shorter links. Match wavelength, fiber type, connector and supported speed at both ends. DAC is useful for short rack links. Copper Ethernet distance depends on the standard; typical balanced twisted-pair channels are 100 m. Plenum rating concerns fire/smoke requirements, not speed.

</details>


### Visual learning

- [Networking Fundamentals — Fiber Optic Connectors Complete Reference Guide"
](/network-portfolio/study-diagrams/fiber-optic-connectors-complete-reference-guide/)
- [Networking Fundamentals — Multimode Fiber Cabling"
](/network-portfolio/study-diagrams/multimode-fiber/)
- [Networking Fundamentals — Single-Mode Fiber Cabling"
](/network-portfolio/study-diagrams/single-mode-fiber-cabling/)
- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)

<a id="objective-1-6"></a>

## 1.6 — Topologies and architectures

### Technical distinctions

- **Spine-leaf:** Predictable east-west paths through spine switches.
- **Star:** Endpoints connect to a central device.
- **Mesh:** Multiple alternate paths between nodes.
- **Three-tier:** Access distribution and core layers.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


Star networks centralize connections; mesh provides multiple paths. Spine-leaf designs connect each leaf to each spine to provide predictable east-west paths. Three-tier campus designs separate access, distribution and core. Point-to-point links join two endpoints.


### Deep dive — Topology and traffic

A three-tier campus separates access, distribution and core. A collapsed core combines distribution and core. Spine-leaf fabrics connect each leaf to every spine, supporting predictable east-west paths. Mesh improves path redundancy but adds links and management. North-south traffic crosses a network boundary; east-west moves among internal workloads.

**Hands-on verification:** Draw a campus and a spine-leaf fabric; trace traffic between two servers and from a client to the internet.

**Reference for further study:** RFC 7938.

[Practice this objective](../practice/?objective=1.6) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| LAN | Local area network; local connectivity |
| WAN | Wide area network; connects distant sites |
| SAN | Storage area network; dedicated storage connectivity |
| MAN | Metropolitan area network; city-scale connectivity |

### Technical quick-reference table

| Topology | Benefit | Tradeoff |
| --- | --- | --- |
| Star | Central management | Central failure point |
| Mesh | Alternate paths | More links and complexity |
| Spine-leaf | Predictable east-west hops | Fabric design complexity |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>Which architecture connects each leaf switch to every spine switch?</summary>

**Answer:** Spine-leaf

Star networks centralize connections; mesh provides multiple paths. Spine-leaf designs connect each leaf to each spine to provide predictable east-west paths. Three-tier campus designs separate access, distribution and core. Point-to-point links join two endpoints.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: data center fabric where each leaf connects to every spine?</summary>

**Answer:** Spine-leaf

Spine-leaf: Data center fabric where each leaf connects to every spine. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: traffic between workloads inside a data center?</summary>

**Answer:** East-west

East-west: Traffic between workloads inside a data center. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: campus tier connecting end devices?</summary>

**Answer:** Access layer

Access layer: Campus tier connecting end devices. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: combines core and distribution roles?</summary>

**Answer:** Collapsed core

Collapsed core: Combines core and distribution roles. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: every node has a direct link to every other node?</summary>

**Answer:** Full mesh

Full mesh: Every node has a direct link to every other node. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>A data center needs predictable paths between racks and high east-west capacity. Which topology is most appropriate?</summary>

**Answer:** Spine-leaf

A spine-leaf fabric gives leaf switches multiple paths through spines and supports scalable east-west traffic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes East-west?</summary>

**Answer:** Traffic between workloads inside a data center

East-west refers to traffic between workloads inside a data center. The alternatives instead describe Spine-leaf, Access layer, Collapsed core.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Access layer?</summary>

**Answer:** Campus tier connecting end devices

Access layer refers to campus tier connecting end devices. The alternatives instead describe Spine-leaf, East-west, Collapsed core.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Collapsed core?</summary>

**Answer:** Combines core and distribution roles

Collapsed core refers to combines core and distribution roles. The alternatives instead describe Spine-leaf, East-west, Access layer.

</details>

<details class="hr-qa" markdown="1">
<summary>A data center needs predictable paths between server racks with substantial east-west traffic. Which architecture fits?</summary>

**Answer:** Spine-leaf

Spine-leaf provides multiple paths and consistent hop counts between racks; the alternatives lack comparable fabric scalability.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: predictable east-west paths through spine switches?</summary>

**Answer:** Spine-leaf

Spine-leaf: Predictable east-west paths through spine switches; Star: Endpoints connect to a central device; Mesh: Multiple alternate paths between nodes; Three-tier: Access distribution and core layers.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Spine-leaf from the alternatives?</summary>

**Answer:** Predictable east-west paths through spine switches

Spine-leaf: Predictable east-west paths through spine switches; Star: Endpoints connect to a central device; Mesh: Multiple alternate paths between nodes; Three-tier: Access distribution and core layers.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: endpoints connect to a central device?</summary>

**Answer:** Star

Spine-leaf: Predictable east-west paths through spine switches; Star: Endpoints connect to a central device; Mesh: Multiple alternate paths between nodes; Three-tier: Access distribution and core layers.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Star from the alternatives?</summary>

**Answer:** Endpoints connect to a central device

Spine-leaf: Predictable east-west paths through spine switches; Star: Endpoints connect to a central device; Mesh: Multiple alternate paths between nodes; Three-tier: Access distribution and core layers.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: multiple alternate paths between nodes?</summary>

**Answer:** Mesh

Spine-leaf: Predictable east-west paths through spine switches; Star: Endpoints connect to a central device; Mesh: Multiple alternate paths between nodes; Three-tier: Access distribution and core layers.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Mesh from the alternatives?</summary>

**Answer:** Multiple alternate paths between nodes

Spine-leaf: Predictable east-west paths through spine switches; Star: Endpoints connect to a central device; Mesh: Multiple alternate paths between nodes; Three-tier: Access distribution and core layers.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: access distribution and core layers?</summary>

**Answer:** Three-tier

Spine-leaf: Predictable east-west paths through spine switches; Star: Endpoints connect to a central device; Mesh: Multiple alternate paths between nodes; Three-tier: Access distribution and core layers.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Three-tier from the alternatives?</summary>

**Answer:** Access distribution and core layers

Spine-leaf: Predictable east-west paths through spine switches; Star: Endpoints connect to a central device; Mesh: Multiple alternate paths between nodes; Three-tier: Access distribution and core layers.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes Star for a task that requires: predictable east-west paths through spine switches. Which alternative is the better match?</summary>

**Answer:** Spine-leaf

Spine-leaf: Predictable east-west paths through spine switches; Star: Endpoints connect to a central device; Mesh: Multiple alternate paths between nodes; Three-tier: Access distribution and core layers.

</details>

<details class="hr-qa" markdown="1">
<summary>Servers exchange traffic within a data center — which answer best fits?</summary>

**Answer:** East-west

East-west is the best match for this situation. A three-tier campus separates access, distribution and core. A collapsed core combines distribution and core. Spine-leaf fabrics connect each leaf to every spine, supporting predictable east-west paths. Mesh improves path redundancy but adds links and management. North-south traffic crosses a network boundary; east-west moves among internal workloads.

</details>

<details class="hr-qa" markdown="1">
<summary>A user accesses an external internet service — which answer best fits?</summary>

**Answer:** North-south

North-south is the best match for this situation. A three-tier campus separates access, distribution and core. A collapsed core combines distribution and core. Spine-leaf fabrics connect each leaf to every spine, supporting predictable east-west paths. Mesh improves path redundancy but adds links and management. North-south traffic crosses a network boundary; east-west moves among internal workloads.

</details>

<details class="hr-qa" markdown="1">
<summary>Every leaf connects to every spine — which answer best fits?</summary>

**Answer:** Spine-leaf

Spine-leaf is the best match for this situation. A three-tier campus separates access, distribution and core. A collapsed core combines distribution and core. Spine-leaf fabrics connect each leaf to every spine, supporting predictable east-west paths. Mesh improves path redundancy but adds links and management. North-south traffic crosses a network boundary; east-west moves among internal workloads.

</details>

<details class="hr-qa" markdown="1">
<summary>A small campus combines distribution and core — which answer best fits?</summary>

**Answer:** Collapsed core

Collapsed core is the best match for this situation. A three-tier campus separates access, distribution and core. A collapsed core combines distribution and core. Spine-leaf fabrics connect each leaf to every spine, supporting predictable east-west paths. Mesh improves path redundancy but adds links and management. North-south traffic crosses a network boundary; east-west moves among internal workloads.

</details>

<details class="hr-qa" markdown="1">
<summary>Endpoint ports attach at which campus tier — which answer best fits?</summary>

**Answer:** Access

Access is the best match for this situation. A three-tier campus separates access, distribution and core. A collapsed core combines distribution and core. Spine-leaf fabrics connect each leaf to every spine, supporting predictable east-west paths. Mesh improves path redundancy but adds links and management. North-south traffic crosses a network boundary; east-west moves among internal workloads.

</details>

<details class="hr-qa" markdown="1">
<summary>A backbone provides fast interdistribution forwarding — which answer best fits?</summary>

**Answer:** Core

Core is the best match for this situation. A three-tier campus separates access, distribution and core. A collapsed core combines distribution and core. Spine-leaf fabrics connect each leaf to every spine, supporting predictable east-west paths. Mesh improves path redundancy but adds links and management. North-south traffic crosses a network boundary; east-west moves among internal workloads.

</details>

<details class="hr-qa" markdown="1">
<summary>A branch WAN has one central site and multiple remote sites — which answer best fits?</summary>

**Answer:** Hub and spoke

Hub and spoke is the best match for this situation. A three-tier campus separates access, distribution and core. A collapsed core combines distribution and core. Spine-leaf fabrics connect each leaf to every spine, supporting predictable east-west paths. Mesh improves path redundancy but adds links and management. North-south traffic crosses a network boundary; east-west moves among internal workloads.

</details>

<details class="hr-qa" markdown="1">
<summary>Two sites have one dedicated direct link — which answer best fits?</summary>

**Answer:** Point-to-point

Point-to-point is the best match for this situation. A three-tier campus separates access, distribution and core. A collapsed core combines distribution and core. Spine-leaf fabrics connect each leaf to every spine, supporting predictable east-west paths. Mesh improves path redundancy but adds links and management. North-south traffic crosses a network boundary; east-west moves among internal workloads.

</details>

<details class="hr-qa" markdown="1">
<summary>Every site has direct links to all other sites — which answer best fits?</summary>

**Answer:** Full mesh

Full mesh is the best match for this situation. A three-tier campus separates access, distribution and core. A collapsed core combines distribution and core. Spine-leaf fabrics connect each leaf to every spine, supporting predictable east-west paths. Mesh improves path redundancy but adds links and management. North-south traffic crosses a network boundary; east-west moves among internal workloads.

</details>

<details class="hr-qa" markdown="1">
<summary>A network mixes star access with mesh WAN — which answer best fits?</summary>

**Answer:** Hybrid topology

Hybrid topology is the best match for this situation. A three-tier campus separates access, distribution and core. A collapsed core combines distribution and core. Spine-leaf fabrics connect each leaf to every spine, supporting predictable east-west paths. Mesh improves path redundancy but adds links and management. North-south traffic crosses a network boundary; east-west moves among internal workloads.

</details>


### Visual learning

- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)

<a id="objective-1-7"></a>

## 1.7 — IPv4 addressing and subnetting

### Technical distinctions

- **RFC 1918:** Private IPv4 address space not globally routed.
- **APIPA:** Self-assigned IPv4 link-local address in 169.254/16.
- **CIDR:** Prefix length describes network bits.
- **VLSM:** Different prefix lengths allocate different subnet sizes.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


IPv4 uses 32 bits. A /26 leaves six host bits: 64 addresses and normally 62 usable hosts. Network boundaries increment by 64 in the final octet. RFC1918 ranges are 10/8, 172.16/12 and 192.168/16; 169.254/16 is link-local. Longest prefix matching determines route specificity.

[Related completed lab](/network-portfolio/videos/16-31-implement-subnetted-ipv6-addressing-scheme/)


### Deep dive — IPv4 calculations

CIDR prefixes identify network bits; the remaining bits identify addresses. For ordinary /30 or larger LAN subnets, usable hosts are 2^(32-prefix)-2; /31 point-to-point links are a special case. VLSM assigns different prefix sizes. Private ranges are 10/8, 172.16/12 and 192.168/16; 169.254/16 is link-local. Classful ranges are historical, not modern route selection.

**Hands-on verification:** Allocate largest VLSM subnet first, align boundaries, then verify no overlap. Practice /25 through /30 in the exercise lab.

**Reference for further study:** RFC 4632.

[Practice this objective](../practice/?objective=1.7) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| CIDR | Classless inter-domain routing; prefix-length notation |
| APIPA | Automatic private IP addressing; IPv4 link-local 169.254/16 |
| VLSM | Variable length subnet masking; different subnet sizes |

### Technical quick-reference table

| Prefix | Addresses | Conventional usable hosts |
| --- | --- | --- |
| /24 | 256 | 254 |
| /25 | 128 | 126 |
| /26 | 64 | 62 |
| /27 | 32 | 30 |
| /28 | 16 | 14 |
| /29 | 8 | 6 |
| /30 | 4 | 2 |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>What is the network address of 192.168.10.77/26?</summary>

**Answer:** 192.168.10.64

IPv4 uses 32 bits. A /26 leaves six host bits: 64 addresses and normally 62 usable hosts. Network boundaries increment by 64 in the final octet. RFC1918 ranges are 10/8, 172.16/12 and 192.168/16; 169.254/16 is link-local. Longest prefix matching determines route specificity.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: iPv4 link-local self-assignment in 169.254.0.0/16?</summary>

**Answer:** APIPA

APIPA: IPv4 link-local self-assignment in 169.254.0.0/16. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: private IPv4 ranges including 10.0.0.0/8?</summary>

**Answer:** RFC1918

RFC1918: Private IPv4 ranges including 10.0.0.0/8. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: local IPv4 testing using 127.0.0.1?</summary>

**Answer:** Loopback

Loopback: Local IPv4 testing using 127.0.0.1. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: allocating different prefix lengths according to subnet size needs?</summary>

**Answer:** VLSM

VLSM: Allocating different prefix lengths according to subnet size needs. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: prefix-length notation independent of historical address classes?</summary>

**Answer:** CIDR

CIDR: Prefix-length notation independent of historical address classes. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>A subnet must support 50 conventional IPv4 hosts. What is the smallest prefix that fits?</summary>

**Answer:** /26

Six host bits give 64 addresses, 62 usable after network and broadcast addresses.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes RFC1918?</summary>

**Answer:** Private IPv4 ranges including 10.0.0.0/8

RFC1918 refers to private IPv4 ranges including 10.0.0.0/8. The alternatives instead describe APIPA, Loopback, VLSM.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Loopback?</summary>

**Answer:** Local IPv4 testing using 127.0.0.1

Loopback refers to local IPv4 testing using 127.0.0.1. The alternatives instead describe APIPA, RFC1918, VLSM.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes VLSM?</summary>

**Answer:** Allocating different prefix lengths according to subnet size needs

VLSM refers to allocating different prefix lengths according to subnet size needs. The alternatives instead describe APIPA, RFC1918, Loopback.

</details>

<details class="hr-qa" markdown="1">
<summary>A host has address 192.0.2.77/27. Which is its network address?</summary>

**Answer:** 192.0.2.64

A /27 has blocks of 32; 77 falls in 64–95. The other boundaries are different subnets and 77 is a host address.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: private IPv4 address space not globally routed?</summary>

**Answer:** RFC 1918

RFC 1918: Private IPv4 address space not globally routed; APIPA: Self-assigned IPv4 link-local address in 169.254/16; CIDR: Prefix length describes network bits; VLSM: Different prefix lengths allocate different subnet sizes.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes RFC 1918 from the alternatives?</summary>

**Answer:** Private IPv4 address space not globally routed

RFC 1918: Private IPv4 address space not globally routed; APIPA: Self-assigned IPv4 link-local address in 169.254/16; CIDR: Prefix length describes network bits; VLSM: Different prefix lengths allocate different subnet sizes.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: self-assigned IPv4 link-local address in 169.254/16?</summary>

**Answer:** APIPA

RFC 1918: Private IPv4 address space not globally routed; APIPA: Self-assigned IPv4 link-local address in 169.254/16; CIDR: Prefix length describes network bits; VLSM: Different prefix lengths allocate different subnet sizes.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes APIPA from the alternatives?</summary>

**Answer:** Self-assigned IPv4 link-local address in 169.254/16

RFC 1918: Private IPv4 address space not globally routed; APIPA: Self-assigned IPv4 link-local address in 169.254/16; CIDR: Prefix length describes network bits; VLSM: Different prefix lengths allocate different subnet sizes.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: prefix length describes network bits?</summary>

**Answer:** CIDR

RFC 1918: Private IPv4 address space not globally routed; APIPA: Self-assigned IPv4 link-local address in 169.254/16; CIDR: Prefix length describes network bits; VLSM: Different prefix lengths allocate different subnet sizes.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes CIDR from the alternatives?</summary>

**Answer:** Prefix length describes network bits

RFC 1918: Private IPv4 address space not globally routed; APIPA: Self-assigned IPv4 link-local address in 169.254/16; CIDR: Prefix length describes network bits; VLSM: Different prefix lengths allocate different subnet sizes.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: different prefix lengths allocate different subnet sizes?</summary>

**Answer:** VLSM

RFC 1918: Private IPv4 address space not globally routed; APIPA: Self-assigned IPv4 link-local address in 169.254/16; CIDR: Prefix length describes network bits; VLSM: Different prefix lengths allocate different subnet sizes.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes VLSM from the alternatives?</summary>

**Answer:** Different prefix lengths allocate different subnet sizes

RFC 1918: Private IPv4 address space not globally routed; APIPA: Self-assigned IPv4 link-local address in 169.254/16; CIDR: Prefix length describes network bits; VLSM: Different prefix lengths allocate different subnet sizes.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes APIPA for a task that requires: private IPv4 address space not globally routed. Which alternative is the better match?</summary>

**Answer:** RFC 1918

RFC 1918: Private IPv4 address space not globally routed; APIPA: Self-assigned IPv4 link-local address in 169.254/16; CIDR: Prefix length describes network bits; VLSM: Different prefix lengths allocate different subnet sizes.

</details>

<details class="hr-qa" markdown="1">
<summary>A LAN needs 50 usable IPv4 addresses — which answer best fits?</summary>

**Answer:** /26

/26 is the best match for this situation. CIDR prefixes identify network bits; the remaining bits identify addresses. For ordinary /30 or larger LAN subnets, usable hosts are 2^(32-prefix)-2; /31 point-to-point links are a special case. VLSM assigns different prefix sizes. Private ranges are 10/8, 172.16/12 and 192.168/16; 169.254/16 is link-local. Classful ranges are historical, not modern route selection.

</details>

<details class="hr-qa" markdown="1">
<summary>A LAN needs 100 usable IPv4 addresses — which answer best fits?</summary>

**Answer:** /25

/25 is the best match for this situation. CIDR prefixes identify network bits; the remaining bits identify addresses. For ordinary /30 or larger LAN subnets, usable hosts are 2^(32-prefix)-2; /31 point-to-point links are a special case. VLSM assigns different prefix sizes. Private ranges are 10/8, 172.16/12 and 192.168/16; 169.254/16 is link-local. Classful ranges are historical, not modern route selection.

</details>

<details class="hr-qa" markdown="1">
<summary>A host is 192.168.5.77/26; identify its network — which answer best fits?</summary>

**Answer:** 192.168.5.64

192.168.5.64 is the best match for this situation. CIDR prefixes identify network bits; the remaining bits identify addresses. For ordinary /30 or larger LAN subnets, usable hosts are 2^(32-prefix)-2; /31 point-to-point links are a special case. VLSM assigns different prefix sizes. Private ranges are 10/8, 172.16/12 and 192.168/16; 169.254/16 is link-local. Classful ranges are historical, not modern route selection.

</details>

<details class="hr-qa" markdown="1">
<summary>A host is 192.168.5.77/26; identify broadcast — which answer best fits?</summary>

**Answer:** 192.168.5.127

192.168.5.127 is the best match for this situation. CIDR prefixes identify network bits; the remaining bits identify addresses. For ordinary /30 or larger LAN subnets, usable hosts are 2^(32-prefix)-2; /31 point-to-point links are a special case. VLSM assigns different prefix sizes. Private ranges are 10/8, 172.16/12 and 192.168/16; 169.254/16 is link-local. Classful ranges are historical, not modern route selection.

</details>

<details class="hr-qa" markdown="1">
<summary>A /28 LAN has how many conventional usable hosts — which answer best fits?</summary>

**Answer:** 14

14 is the best match for this situation. CIDR prefixes identify network bits; the remaining bits identify addresses. For ordinary /30 or larger LAN subnets, usable hosts are 2^(32-prefix)-2; /31 point-to-point links are a special case. VLSM assigns different prefix sizes. Private ranges are 10/8, 172.16/12 and 192.168/16; 169.254/16 is link-local. Classful ranges are historical, not modern route selection.

</details>

<details class="hr-qa" markdown="1">
<summary>A /27 mask ends in which decimal octet — which answer best fits?</summary>

**Answer:** 224

224 is the best match for this situation. CIDR prefixes identify network bits; the remaining bits identify addresses. For ordinary /30 or larger LAN subnets, usable hosts are 2^(32-prefix)-2; /31 point-to-point links are a special case. VLSM assigns different prefix sizes. Private ranges are 10/8, 172.16/12 and 192.168/16; 169.254/16 is link-local. Classful ranges are historical, not modern route selection.

</details>

<details class="hr-qa" markdown="1">
<summary>Which address is within RFC1918 space — which answer best fits?</summary>

**Answer:** 172.31.5.8

172.31.5.8 is the best match for this situation. CIDR prefixes identify network bits; the remaining bits identify addresses. For ordinary /30 or larger LAN subnets, usable hosts are 2^(32-prefix)-2; /31 point-to-point links are a special case. VLSM assigns different prefix sizes. Private ranges are 10/8, 172.16/12 and 192.168/16; 169.254/16 is link-local. Classful ranges are historical, not modern route selection.

</details>

<details class="hr-qa" markdown="1">
<summary>A host self-assigns 169.254.7.9; which address category is this — which answer best fits?</summary>

**Answer:** IPv4 link-local

IPv4 link-local is the best match for this situation. CIDR prefixes identify network bits; the remaining bits identify addresses. For ordinary /30 or larger LAN subnets, usable hosts are 2^(32-prefix)-2; /31 point-to-point links are a special case. VLSM assigns different prefix sizes. Private ranges are 10/8, 172.16/12 and 192.168/16; 169.254/16 is link-local. Classful ranges are historical, not modern route selection.

</details>

<details class="hr-qa" markdown="1">
<summary>A router needs to aggregate 10.4.0.0/24 and 10.4.1.0/24 — which answer best fits?</summary>

**Answer:** 10.4.0.0/23

10.4.0.0/23 is the best match for this situation. CIDR prefixes identify network bits; the remaining bits identify addresses. For ordinary /30 or larger LAN subnets, usable hosts are 2^(32-prefix)-2; /31 point-to-point links are a special case. VLSM assigns different prefix sizes. Private ranges are 10/8, 172.16/12 and 192.168/16; 169.254/16 is link-local. Classful ranges are historical, not modern route selection.

</details>

<details class="hr-qa" markdown="1">
<summary>A design allocates /26 and /28 networks from one block — which answer best fits?</summary>

**Answer:** VLSM

VLSM is the best match for this situation. CIDR prefixes identify network bits; the remaining bits identify addresses. For ordinary /30 or larger LAN subnets, usable hosts are 2^(32-prefix)-2; /31 point-to-point links are a special case. VLSM assigns different prefix sizes. Private ranges are 10/8, 172.16/12 and 192.168/16; 169.254/16 is link-local. Classful ranges are historical, not modern route selection.

</details>


### Visual learning

- [Networking Fundamentals — IPv4 Subnet Masks, Network Bits & CIDR Study Diagram"
](/network-portfolio/study-diagrams/subnet-masks-network-bits-cidr/)
- [Networking Fundamentals — IPv4 Addressing Study Diagram"
](/network-portfolio/study-diagrams/ipv4-addressing/)
- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)

<a id="objective-1-8"></a>

## 1.8 — Modern networking and IPv6

### Technical distinctions

- **SD-WAN:** Policy-driven selection across WAN transports.
- **VXLAN:** Encapsulates layer-two segments over an IP underlay.
- **Zero trust:** Explicit verification and least privilege without implicit network trust.
- **IPv6 SLAAC:** Host forms addresses using advertised prefixes.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


SDN separates control decisions from forwarding; VXLAN encapsulates Layer 2 over Layer 3. Zero trust evaluates access explicitly; SASE combines network and security services. Infrastructure as code makes configuration repeatable. IPv6 uses 128-bit addresses, NDP and typically /64 LAN prefixes; dual stack runs both IP versions.

[Related completed lab](/network-portfolio/videos/17-38-ipv6-neighbor-discovery/)


### Deep dive — Programmable networks and IPv6

SDN separates control logic from forwarding; SD-WAN selects paths based on policy and application needs. VXLAN carries layer-2 frames over IP overlays. SASE combines WAN and cloud security capabilities; SSE focuses on security services. Zero trust requires explicit policy decisions. IaC uses versioned desired state and detects drift. IPv6 transition uses dual stack, tunneling or NAT64 as appropriate.

**Hands-on verification:** Compare a desired configuration in Git with actual device state; review a diff before deploying. Practice hexadecimal /64 increments.

**Reference for further study:** RFC 7348; RFC 6146.

[Practice this objective](../practice/?objective=1.8) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| SDN | Software-defined networking; separates control and forwarding abstractions |
| VXLAN | Virtual extensible LAN; overlay encapsulation |
| SLAAC | Stateless address autoconfiguration; IPv6 address configuration using router advertisements |
| NDP | Neighbor discovery protocol; IPv6 neighbor and router discovery |

### Technical quick-reference table

| Concept | Purpose | Distinction |
| --- | --- | --- |
| SDN | Programmable control | Separates control logic from forwarding |
| VXLAN | Overlay segmentation | Encapsulates Ethernet over UDP |
| IPv6 SLAAC | Address autoconfiguration | Uses router advertisements |
| NAT64 | IPv6 to IPv4 translation | Often paired with DNS64 |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>Which technology uses a VNI to identify an overlay segment?</summary>

**Answer:** VXLAN

SDN separates control decisions from forwarding; VXLAN encapsulates Layer 2 over Layer 3. Zero trust evaluates access explicitly; SASE combines network and security services. Infrastructure as code makes configuration repeatable. IPv6 uses 128-bit addresses, NDP and typically /64 LAN prefixes; dual stack runs both IP versions.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: layer 2 overlay encapsulated across an IP underlay?</summary>

**Answer:** VXLAN

VXLAN: Layer 2 overlay encapsulated across an IP underlay. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: central policy and application-aware selection across WAN transports?</summary>

**Answer:** SD-WAN

SD-WAN: Central policy and application-aware selection across WAN transports. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: translation allowing IPv6 clients to communicate with IPv4 services?</summary>

**Answer:** NAT64

NAT64: Translation allowing IPv6 clients to communicate with IPv4 services. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: running IPv4 and IPv6 concurrently?</summary>

**Answer:** Dual stack

Dual stack: Running IPv4 and IPv6 concurrently. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: version-controlled declarative or scripted infrastructure configuration?</summary>

**Answer:** Infrastructure as code

Infrastructure as code: Version-controlled declarative or scripted infrastructure configuration. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>An IPv6-only client needs to reach an IPv4-only server through a translation service. Which technology is appropriate?</summary>

**Answer:** NAT64

NAT64 translates between IPv6 and IPv4; DNS64 may assist name-based access.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes SD-WAN?</summary>

**Answer:** Central policy and application-aware selection across WAN transports

SD-WAN refers to central policy and application-aware selection across WAN transports. The alternatives instead describe VXLAN, NAT64, Dual stack.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes NAT64?</summary>

**Answer:** Translation allowing IPv6 clients to communicate with IPv4 services

NAT64 refers to translation allowing IPv6 clients to communicate with IPv4 services. The alternatives instead describe VXLAN, SD-WAN, Dual stack.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Dual stack?</summary>

**Answer:** Running IPv4 and IPv6 concurrently

Dual stack refers to running IPv4 and IPv6 concurrently. The alternatives instead describe VXLAN, SD-WAN, NAT64.

</details>

<details class="hr-qa" markdown="1">
<summary>An IPv6-only client must reach an IPv4-only server through a translation service. Which technology addresses this?</summary>

**Answer:** NAT64

NAT64 translates between IPv6 and IPv4. LACP aggregates links, STP prevents bridging loops, and 802.1X controls access.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: policy-driven selection across WAN transports?</summary>

**Answer:** SD-WAN

SD-WAN: Policy-driven selection across WAN transports; VXLAN: Encapsulates layer-two segments over an IP underlay; Zero trust: Explicit verification and least privilege without implicit network trust; IPv6 SLAAC: Host forms addresses using advertised prefixes.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes SD-WAN from the alternatives?</summary>

**Answer:** Policy-driven selection across WAN transports

SD-WAN: Policy-driven selection across WAN transports; VXLAN: Encapsulates layer-two segments over an IP underlay; Zero trust: Explicit verification and least privilege without implicit network trust; IPv6 SLAAC: Host forms addresses using advertised prefixes.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: encapsulates layer-two segments over an IP underlay?</summary>

**Answer:** VXLAN

SD-WAN: Policy-driven selection across WAN transports; VXLAN: Encapsulates layer-two segments over an IP underlay; Zero trust: Explicit verification and least privilege without implicit network trust; IPv6 SLAAC: Host forms addresses using advertised prefixes.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes VXLAN from the alternatives?</summary>

**Answer:** Encapsulates layer-two segments over an IP underlay

SD-WAN: Policy-driven selection across WAN transports; VXLAN: Encapsulates layer-two segments over an IP underlay; Zero trust: Explicit verification and least privilege without implicit network trust; IPv6 SLAAC: Host forms addresses using advertised prefixes.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: explicit verification and least privilege without implicit network trust?</summary>

**Answer:** Zero trust

SD-WAN: Policy-driven selection across WAN transports; VXLAN: Encapsulates layer-two segments over an IP underlay; Zero trust: Explicit verification and least privilege without implicit network trust; IPv6 SLAAC: Host forms addresses using advertised prefixes.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Zero trust from the alternatives?</summary>

**Answer:** Explicit verification and least privilege without implicit network trust

SD-WAN: Policy-driven selection across WAN transports; VXLAN: Encapsulates layer-two segments over an IP underlay; Zero trust: Explicit verification and least privilege without implicit network trust; IPv6 SLAAC: Host forms addresses using advertised prefixes.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: host forms addresses using advertised prefixes?</summary>

**Answer:** IPv6 SLAAC

SD-WAN: Policy-driven selection across WAN transports; VXLAN: Encapsulates layer-two segments over an IP underlay; Zero trust: Explicit verification and least privilege without implicit network trust; IPv6 SLAAC: Host forms addresses using advertised prefixes.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes IPv6 SLAAC from the alternatives?</summary>

**Answer:** Host forms addresses using advertised prefixes

SD-WAN: Policy-driven selection across WAN transports; VXLAN: Encapsulates layer-two segments over an IP underlay; Zero trust: Explicit verification and least privilege without implicit network trust; IPv6 SLAAC: Host forms addresses using advertised prefixes.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes VXLAN for a task that requires: policy-driven selection across WAN transports. Which alternative is the better match?</summary>

**Answer:** SD-WAN

SD-WAN: Policy-driven selection across WAN transports; VXLAN: Encapsulates layer-two segments over an IP underlay; Zero trust: Explicit verification and least privilege without implicit network trust; IPv6 SLAAC: Host forms addresses using advertised prefixes.

</details>

<details class="hr-qa" markdown="1">
<summary>A branch chooses WAN links by application latency policy — which answer best fits?</summary>

**Answer:** SD-WAN

SD-WAN is the best match for this situation. SDN separates control logic from forwarding; SD-WAN selects paths based on policy and application needs. VXLAN carries layer-2 frames over IP overlays. SASE combines WAN and cloud security capabilities; SSE focuses on security services. Zero trust requires explicit policy decisions. IaC uses versioned desired state and detects drift. IPv6 transition uses dual stack, tunneling or NAT64 as appropriate.

</details>

<details class="hr-qa" markdown="1">
<summary>A data center carries Ethernet segments over an IP fabric — which answer best fits?</summary>

**Answer:** VXLAN

VXLAN is the best match for this situation. SDN separates control logic from forwarding; SD-WAN selects paths based on policy and application needs. VXLAN carries layer-2 frames over IP overlays. SASE combines WAN and cloud security capabilities; SSE focuses on security services. Zero trust requires explicit policy decisions. IaC uses versioned desired state and detects drift. IPv6 transition uses dual stack, tunneling or NAT64 as appropriate.

</details>

<details class="hr-qa" markdown="1">
<summary>An IPv6-only client needs access to an IPv4-only service through translation — which answer best fits?</summary>

**Answer:** NAT64

NAT64 is the best match for this situation. SDN separates control logic from forwarding; SD-WAN selects paths based on policy and application needs. VXLAN carries layer-2 frames over IP overlays. SASE combines WAN and cloud security capabilities; SSE focuses on security services. Zero trust requires explicit policy decisions. IaC uses versioned desired state and detects drift. IPv6 transition uses dual stack, tunneling or NAT64 as appropriate.

</details>

<details class="hr-qa" markdown="1">
<summary>A host runs both IPv4 and IPv6 natively — which answer best fits?</summary>

**Answer:** Dual stack

Dual stack is the best match for this situation. SDN separates control logic from forwarding; SD-WAN selects paths based on policy and application needs. VXLAN carries layer-2 frames over IP overlays. SASE combines WAN and cloud security capabilities; SSE focuses on security services. Zero trust requires explicit policy decisions. IaC uses versioned desired state and detects drift. IPv6 transition uses dual stack, tunneling or NAT64 as appropriate.

</details>

<details class="hr-qa" markdown="1">
<summary>A device configuration differs from the versioned desired state — which answer best fits?</summary>

**Answer:** Configuration drift

Configuration drift is the best match for this situation. SDN separates control logic from forwarding; SD-WAN selects paths based on policy and application needs. VXLAN carries layer-2 frames over IP overlays. SASE combines WAN and cloud security capabilities; SSE focuses on security services. Zero trust requires explicit policy decisions. IaC uses versioned desired state and detects drift. IPv6 transition uses dual stack, tunneling or NAT64 as appropriate.

</details>

<details class="hr-qa" markdown="1">
<summary>A new branch device configures itself from a central service — which answer best fits?</summary>

**Answer:** Zero-touch provisioning

Zero-touch provisioning is the best match for this situation. SDN separates control logic from forwarding; SD-WAN selects paths based on policy and application needs. VXLAN carries layer-2 frames over IP overlays. SASE combines WAN and cloud security capabilities; SSE focuses on security services. Zero trust requires explicit policy decisions. IaC uses versioned desired state and detects drift. IPv6 transition uses dual stack, tunneling or NAT64 as appropriate.

</details>

<details class="hr-qa" markdown="1">
<summary>A change must be reviewed before merging into the main configuration — which answer best fits?</summary>

**Answer:** Version control branch and review

Version control branch and review is the best match for this situation. SDN separates control logic from forwarding; SD-WAN selects paths based on policy and application needs. VXLAN carries layer-2 frames over IP overlays. SASE combines WAN and cloud security capabilities; SSE focuses on security services. Zero trust requires explicit policy decisions. IaC uses versioned desired state and detects drift. IPv6 transition uses dual stack, tunneling or NAT64 as appropriate.

</details>

<details class="hr-qa" markdown="1">
<summary>A user is authenticated and authorized for each protected resource based on policy — which answer best fits?</summary>

**Answer:** Zero trust

Zero trust is the best match for this situation. SDN separates control logic from forwarding; SD-WAN selects paths based on policy and application needs. VXLAN carries layer-2 frames over IP overlays. SASE combines WAN and cloud security capabilities; SSE focuses on security services. Zero trust requires explicit policy decisions. IaC uses versioned desired state and detects drift. IPv6 transition uses dual stack, tunneling or NAT64 as appropriate.

</details>

<details class="hr-qa" markdown="1">
<summary>Cloud-delivered security services without WAN transport integration are requested — which answer best fits?</summary>

**Answer:** SSE

SSE is the best match for this situation. SDN separates control logic from forwarding; SD-WAN selects paths based on policy and application needs. VXLAN carries layer-2 frames over IP overlays. SASE combines WAN and cloud security capabilities; SSE focuses on security services. Zero trust requires explicit policy decisions. IaC uses versioned desired state and detects drift. IPv6 transition uses dual stack, tunneling or NAT64 as appropriate.

</details>

<details class="hr-qa" markdown="1">
<summary>A /60 IPv6 allocation contains how many /64 subnets — which answer best fits?</summary>

**Answer:** 16

16 is the best match for this situation. SDN separates control logic from forwarding; SD-WAN selects paths based on policy and application needs. VXLAN carries layer-2 frames over IP overlays. SASE combines WAN and cloud security capabilities; SSE focuses on security services. Zero trust requires explicit policy decisions. IaC uses versioned desired state and detects drift. IPv6 transition uses dual stack, tunneling or NAT64 as appropriate.

</details>


### Visual learning

- [Networking Fundamentals — Dual-Stack Networking Study Diagram"
](/network-portfolio/study-diagrams/dual-stack-networking/)
- [Networking Fundamentals — ICMPv6 Overview Study Diagram"
](/network-portfolio/study-diagrams/icmpv6-overview/)
- [Networking Fundamentals — IPv4 vs IPv6 Study Diagram"
](/network-portfolio/study-diagrams/ipv4-vs-ipv6/)
- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)

<a id="objective-2-1"></a>

## 2.1 — Routing

### Technical distinctions

- **OSPF:** Link-state routing within an autonomous system.
- **BGP:** Policy-based path-vector routing between autonomous systems.
- **PAT:** Multiple private hosts share a public address using ports.
- **FHRP:** Provides a redundant virtual default gateway.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


Routers choose longest matching prefixes before comparing route preferences for identical prefixes. OSPF is link-state, BGP is path-vector, EIGRP is advanced distance-vector. NAT changes addresses; PAT multiplexes flows using ports. A floating static route has a less preferred administrative distance.


### Deep dive — Routing decisions

Forwarding uses longest prefix first. For competing routes to the same prefix, administrative distance selects the source and protocol metrics select paths within a protocol. OSPF uses link state, EIGRP uses DUAL, BGP exchanges policy-based reachability. NAT translates addresses; PAT also distinguishes flows by ports. FHRP provides a shared gateway IP.

**Hands-on verification:** Inspect show ip route and compare a /24 with a default route; test gateway failover in a lab.

**Reference for further study:** RFC 2328; RFC 4271.

[Practice this objective](../practice/?objective=2.1) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| OSPF | Open shortest path first; link-state routing |
| BGP | Border gateway protocol; policy-based path-vector routing |
| EIGRP | Enhanced interior gateway routing protocol; advanced distance-vector routing |
| PAT | Port address translation; shares an address using transport identifiers |
| FHRP | First hop redundancy protocol; resilient default gateway |

### Technical quick-reference table

| Decision | Rule | Example |
| --- | --- | --- |
| Forwarding | Longest matching prefix | /24 wins over /16 |
| Route source | Administrative distance | Compare sources for same prefix |
| Protocol metric | Protocol-specific path preference | OSPF cost |
| PAT | Translate addresses and ports | Many clients share public address |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>A /24 and /28 both match a destination. Which route wins first?</summary>

**Answer:** /28

Routers choose longest matching prefixes before comparing route preferences for identical prefixes. OSPF is link-state, BGP is path-vector, EIGRP is advanced distance-vector. NAT changes addresses; PAT multiplexes flows using ports. A floating static route has a less preferred administrative distance.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: link-state interior routing using a shortest-path calculation?</summary>

**Answer:** OSPF

OSPF: Link-state interior routing using a shortest-path calculation. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: policy-oriented routing between autonomous systems?</summary>

**Answer:** BGP

BGP: Policy-oriented routing between autonomous systems. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: many internal connections share a public address using transport identifiers?</summary>

**Answer:** PAT

PAT: Many internal connections share a public address using transport identifiers. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: redundant default gateway service using a shared virtual IP?</summary>

**Answer:** FHRP

FHRP: Redundant default gateway service using a shared virtual IP. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: logical router interface often associated with an 802.1Q VLAN?</summary>

**Answer:** Subinterface

Subinterface: Logical router interface often associated with an 802.1Q VLAN. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>A router has routes to 10.20.0.0/16 and 10.20.30.0/24. Which is used for 10.20.30.45?</summary>

**Answer:** 10.20.30.0/24

Longest prefix match selects the more specific /24 regardless of the administrative distance of the less specific route.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes BGP?</summary>

**Answer:** Policy-oriented routing between autonomous systems

BGP refers to policy-oriented routing between autonomous systems. The alternatives instead describe OSPF, PAT, FHRP.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes PAT?</summary>

**Answer:** Many internal connections share a public address using transport identifiers

PAT refers to many internal connections share a public address using transport identifiers. The alternatives instead describe OSPF, BGP, FHRP.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes FHRP?</summary>

**Answer:** Redundant default gateway service using a shared virtual IP

FHRP refers to redundant default gateway service using a shared virtual IP. The alternatives instead describe OSPF, BGP, PAT.

</details>

<details class="hr-qa" markdown="1">
<summary>A routing table has 198.51.100.0/24 and 198.51.100.128/25. Which prefix matches 198.51.100.200 most specifically?</summary>

**Answer:** /25

Longest prefix match selects /25; /24 is less specific and default is least specific.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: link-state routing within an autonomous system?</summary>

**Answer:** OSPF

OSPF: Link-state routing within an autonomous system; BGP: Policy-based path-vector routing between autonomous systems; PAT: Multiple private hosts share a public address using ports; FHRP: Provides a redundant virtual default gateway.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes OSPF from the alternatives?</summary>

**Answer:** Link-state routing within an autonomous system

OSPF: Link-state routing within an autonomous system; BGP: Policy-based path-vector routing between autonomous systems; PAT: Multiple private hosts share a public address using ports; FHRP: Provides a redundant virtual default gateway.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: policy-based path-vector routing between autonomous systems?</summary>

**Answer:** BGP

OSPF: Link-state routing within an autonomous system; BGP: Policy-based path-vector routing between autonomous systems; PAT: Multiple private hosts share a public address using ports; FHRP: Provides a redundant virtual default gateway.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes BGP from the alternatives?</summary>

**Answer:** Policy-based path-vector routing between autonomous systems

OSPF: Link-state routing within an autonomous system; BGP: Policy-based path-vector routing between autonomous systems; PAT: Multiple private hosts share a public address using ports; FHRP: Provides a redundant virtual default gateway.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: multiple private hosts share a public address using ports?</summary>

**Answer:** PAT

OSPF: Link-state routing within an autonomous system; BGP: Policy-based path-vector routing between autonomous systems; PAT: Multiple private hosts share a public address using ports; FHRP: Provides a redundant virtual default gateway.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes PAT from the alternatives?</summary>

**Answer:** Multiple private hosts share a public address using ports

OSPF: Link-state routing within an autonomous system; BGP: Policy-based path-vector routing between autonomous systems; PAT: Multiple private hosts share a public address using ports; FHRP: Provides a redundant virtual default gateway.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: provides a redundant virtual default gateway?</summary>

**Answer:** FHRP

OSPF: Link-state routing within an autonomous system; BGP: Policy-based path-vector routing between autonomous systems; PAT: Multiple private hosts share a public address using ports; FHRP: Provides a redundant virtual default gateway.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes FHRP from the alternatives?</summary>

**Answer:** Provides a redundant virtual default gateway

OSPF: Link-state routing within an autonomous system; BGP: Policy-based path-vector routing between autonomous systems; PAT: Multiple private hosts share a public address using ports; FHRP: Provides a redundant virtual default gateway.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes BGP for a task that requires: link-state routing within an autonomous system. Which alternative is the better match?</summary>

**Answer:** OSPF

OSPF: Link-state routing within an autonomous system; BGP: Policy-based path-vector routing between autonomous systems; PAT: Multiple private hosts share a public address using ports; FHRP: Provides a redundant virtual default gateway.

</details>

<details class="hr-qa" markdown="1">
<summary>A /24 and /16 both match a destination — which answer best fits?</summary>

**Answer:** /24 route

/24 route is the best match for this situation. Forwarding uses longest prefix first. For competing routes to the same prefix, administrative distance selects the source and protocol metrics select paths within a protocol. OSPF uses link state, EIGRP uses DUAL, BGP exchanges policy-based reachability. NAT translates addresses; PAT also distinguishes flows by ports. FHRP provides a shared gateway IP.

</details>

<details class="hr-qa" markdown="1">
<summary>Two OSPF paths to the same prefix differ in cost — which answer best fits?</summary>

**Answer:** Lower OSPF cost

Lower OSPF cost is the best match for this situation. Forwarding uses longest prefix first. For competing routes to the same prefix, administrative distance selects the source and protocol metrics select paths within a protocol. OSPF uses link state, EIGRP uses DUAL, BGP exchanges policy-based reachability. NAT translates addresses; PAT also distinguishes flows by ports. FHRP provides a shared gateway IP.

</details>

<details class="hr-qa" markdown="1">
<summary>A backup static route should lose to the primary dynamic route — which answer best fits?</summary>

**Answer:** Higher administrative distance

Higher administrative distance is the best match for this situation. Forwarding uses longest prefix first. For competing routes to the same prefix, administrative distance selects the source and protocol metrics select paths within a protocol. OSPF uses link state, EIGRP uses DUAL, BGP exchanges policy-based reachability. NAT translates addresses; PAT also distinguishes flows by ports. FHRP provides a shared gateway IP.

</details>

<details class="hr-qa" markdown="1">
<summary>Two autonomous systems exchange reachability policy — which answer best fits?</summary>

**Answer:** BGP

BGP is the best match for this situation. Forwarding uses longest prefix first. For competing routes to the same prefix, administrative distance selects the source and protocol metrics select paths within a protocol. OSPF uses link state, EIGRP uses DUAL, BGP exchanges policy-based reachability. NAT translates addresses; PAT also distinguishes flows by ports. FHRP provides a shared gateway IP.

</details>

<details class="hr-qa" markdown="1">
<summary>A routing protocol floods link-state information — which answer best fits?</summary>

**Answer:** OSPF

OSPF is the best match for this situation. Forwarding uses longest prefix first. For competing routes to the same prefix, administrative distance selects the source and protocol metrics select paths within a protocol. OSPF uses link state, EIGRP uses DUAL, BGP exchanges policy-based reachability. NAT translates addresses; PAT also distinguishes flows by ports. FHRP provides a shared gateway IP.

</details>

<details class="hr-qa" markdown="1">
<summary>A Cisco routing protocol uses DUAL — which answer best fits?</summary>

**Answer:** EIGRP

EIGRP is the best match for this situation. Forwarding uses longest prefix first. For competing routes to the same prefix, administrative distance selects the source and protocol metrics select paths within a protocol. OSPF uses link state, EIGRP uses DUAL, BGP exchanges policy-based reachability. NAT translates addresses; PAT also distinguishes flows by ports. FHRP provides a shared gateway IP.

</details>

<details class="hr-qa" markdown="1">
<summary>Multiple inside hosts share one public IPv4 address using ports — which answer best fits?</summary>

**Answer:** PAT

PAT is the best match for this situation. Forwarding uses longest prefix first. For competing routes to the same prefix, administrative distance selects the source and protocol metrics select paths within a protocol. OSPF uses link state, EIGRP uses DUAL, BGP exchanges policy-based reachability. NAT translates addresses; PAT also distinguishes flows by ports. FHRP provides a shared gateway IP.

</details>

<details class="hr-qa" markdown="1">
<summary>Two routers present a shared default gateway — which answer best fits?</summary>

**Answer:** FHRP

FHRP is the best match for this situation. Forwarding uses longest prefix first. For competing routes to the same prefix, administrative distance selects the source and protocol metrics select paths within a protocol. OSPF uses link state, EIGRP uses DUAL, BGP exchanges policy-based reachability. NAT translates addresses; PAT also distinguishes flows by ports. FHRP provides a shared gateway IP.

</details>

<details class="hr-qa" markdown="1">
<summary>A router-on-a-stick separates VLANs on one physical port — which answer best fits?</summary>

**Answer:** 802.1Q subinterfaces

802.1Q subinterfaces is the best match for this situation. Forwarding uses longest prefix first. For competing routes to the same prefix, administrative distance selects the source and protocol metrics select paths within a protocol. OSPF uses link state, EIGRP uses DUAL, BGP exchanges policy-based reachability. NAT translates addresses; PAT also distinguishes flows by ports. FHRP provides a shared gateway IP.

</details>

<details class="hr-qa" markdown="1">
<summary>A destination matches no specific route but a default exists — which answer best fits?</summary>

**Answer:** Use default route

Use default route is the best match for this situation. Forwarding uses longest prefix first. For competing routes to the same prefix, administrative distance selects the source and protocol metrics select paths within a protocol. OSPF uses link state, EIGRP uses DUAL, BGP exchanges policy-based reachability. NAT translates addresses; PAT also distinguishes flows by ports. FHRP provides a shared gateway IP.

</details>


### Visual learning

- [Infrastructure — Distance Vector vs Link State Routing Protocols"
](/network-portfolio/study-diagrams/distance-vector-vs-link-state/)
- [Networking Fundamentals — Packet Flow Through a Router Study Diagram"
](/network-portfolio/study-diagrams/packet-flow-through-router/)
- [Networking Fundamentals — Routing Protocols Cheat Sheet"
](/network-portfolio/study-diagrams/routing-protocols-cheat-sheet/)
- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)

<a id="objective-2-2"></a>

## 2.2 — Switching

### Technical distinctions

- **802.1Q:** Tags Ethernet frames to identify VLANs.
- **RSTP:** Converges loop-free switched topology rapidly.
- **LACP:** Negotiates aggregation of compatible links.
- **Voice VLAN:** Separates voice traffic from ordinary access data.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


Access ports normally carry one VLAN; trunks carry multiple VLANs using 802.1Q tags. STP prevents Layer 2 loops; LACP negotiates link aggregation. A Layer 3 interface or router is needed to route between VLANs. MTU mismatch can impair traffic.


### Deep dive — Switch configuration

Access ports associate endpoints with one data VLAN; trunks carry tagged VLANs and may carry native untagged traffic. An SVI provides a logical layer-3 interface. STP blocks redundant layer-2 paths; LACP negotiates bundles. MTU mismatch can cause drops. Voice VLANs separate phone traffic.

**Hands-on verification:** Use show vlan brief, show interfaces trunk, show spanning-tree and show etherchannel summary; verify both ends.

**Reference for further study:** IEEE 802.1Q.

[Practice this objective](../practice/?objective=2.2) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| VLAN | Virtual local area network; logical broadcast domain |
| STP | Spanning tree protocol; prevents Layer 2 loops |
| RSTP | Rapid spanning tree protocol; faster convergence |
| LACP | Link aggregation control protocol; negotiates aggregated links |
| PoE | Power over Ethernet; supplies power over compatible cabling |

### Technical quick-reference table

| Feature | Purpose | Verification |
| --- | --- | --- |
| VLAN | Broadcast domain | show vlan brief |
| Trunk | Carry tagged VLANs | show interfaces trunk |
| STP | Prevent Layer 2 loops | show spanning-tree |
| LACP | Aggregate compatible links | show etherchannel summary |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>Which protocol negotiates an Ethernet link aggregation group?</summary>

**Answer:** LACP

Access ports normally carry one VLAN; trunks carry multiple VLANs using 802.1Q tags. STP prevents Layer 2 loops; LACP negotiates link aggregation. A Layer 3 interface or router is needed to route between VLANs. MTU mismatch can impair traffic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: identifies VLAN membership on tagged Ethernet frames?</summary>

**Answer:** 802.1Q

802.1Q: Identifies VLAN membership on tagged Ethernet frames. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: logical Layer 3 interface associated with a switch VLAN?</summary>

**Answer:** SVI

SVI: Logical Layer 3 interface associated with a switch VLAN. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: negotiates aggregation of compatible physical links?</summary>

**Answer:** LACP

LACP: Negotiates aggregation of compatible physical links. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: prevents Layer 2 forwarding loops by selecting a loop-free topology?</summary>

**Answer:** STP

STP: Prevents Layer 2 forwarding loops by selecting a loop-free topology. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: maximum packet size supported by an interface at the relevant layer?</summary>

**Answer:** MTU

MTU: Maximum packet size supported by an interface at the relevant layer. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>VLAN 30 works within each switch but not between switches. Other VLANs work over the trunk. What should be checked first?</summary>

**Answer:** Whether VLAN 30 is allowed on the trunk

The working trunk and other VLANs narrow the issue to VLAN-specific forwarding or configuration.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes SVI?</summary>

**Answer:** Logical Layer 3 interface associated with a switch VLAN

SVI refers to logical Layer 3 interface associated with a switch VLAN. The alternatives instead describe 802.1Q, LACP, STP.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes LACP?</summary>

**Answer:** Negotiates aggregation of compatible physical links

LACP refers to negotiates aggregation of compatible physical links. The alternatives instead describe 802.1Q, SVI, STP.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes STP?</summary>

**Answer:** Prevents Layer 2 forwarding loops by selecting a loop-free topology

STP refers to prevents Layer 2 forwarding loops by selecting a loop-free topology. The alternatives instead describe 802.1Q, SVI, LACP.

</details>

<details class="hr-qa" markdown="1">
<summary>Two switches carry VLANs 10 and 20 across one link, but VLAN 20 is absent from the allowed list. What change restores that VLAN?</summary>

**Answer:** Permit VLAN 20 on the trunk

The trunk must permit VLAN 20. Moving hosts changes segmentation, disabling STP risks loops, and DNS is unrelated.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: tags Ethernet frames to identify VLANs?</summary>

**Answer:** 802.1Q

802.1Q: Tags Ethernet frames to identify VLANs; RSTP: Converges loop-free switched topology rapidly; LACP: Negotiates aggregation of compatible links; Voice VLAN: Separates voice traffic from ordinary access data.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes 802.1Q from the alternatives?</summary>

**Answer:** Tags Ethernet frames to identify VLANs

802.1Q: Tags Ethernet frames to identify VLANs; RSTP: Converges loop-free switched topology rapidly; LACP: Negotiates aggregation of compatible links; Voice VLAN: Separates voice traffic from ordinary access data.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: converges loop-free switched topology rapidly?</summary>

**Answer:** RSTP

802.1Q: Tags Ethernet frames to identify VLANs; RSTP: Converges loop-free switched topology rapidly; LACP: Negotiates aggregation of compatible links; Voice VLAN: Separates voice traffic from ordinary access data.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes RSTP from the alternatives?</summary>

**Answer:** Converges loop-free switched topology rapidly

802.1Q: Tags Ethernet frames to identify VLANs; RSTP: Converges loop-free switched topology rapidly; LACP: Negotiates aggregation of compatible links; Voice VLAN: Separates voice traffic from ordinary access data.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: negotiates aggregation of compatible links?</summary>

**Answer:** LACP

802.1Q: Tags Ethernet frames to identify VLANs; RSTP: Converges loop-free switched topology rapidly; LACP: Negotiates aggregation of compatible links; Voice VLAN: Separates voice traffic from ordinary access data.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes LACP from the alternatives?</summary>

**Answer:** Negotiates aggregation of compatible links

802.1Q: Tags Ethernet frames to identify VLANs; RSTP: Converges loop-free switched topology rapidly; LACP: Negotiates aggregation of compatible links; Voice VLAN: Separates voice traffic from ordinary access data.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: separates voice traffic from ordinary access data?</summary>

**Answer:** Voice VLAN

802.1Q: Tags Ethernet frames to identify VLANs; RSTP: Converges loop-free switched topology rapidly; LACP: Negotiates aggregation of compatible links; Voice VLAN: Separates voice traffic from ordinary access data.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Voice VLAN from the alternatives?</summary>

**Answer:** Separates voice traffic from ordinary access data

802.1Q: Tags Ethernet frames to identify VLANs; RSTP: Converges loop-free switched topology rapidly; LACP: Negotiates aggregation of compatible links; Voice VLAN: Separates voice traffic from ordinary access data.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes RSTP for a task that requires: tags Ethernet frames to identify VLANs. Which alternative is the better match?</summary>

**Answer:** 802.1Q

802.1Q: Tags Ethernet frames to identify VLANs; RSTP: Converges loop-free switched topology rapidly; LACP: Negotiates aggregation of compatible links; Voice VLAN: Separates voice traffic from ordinary access data.

</details>

<details class="hr-qa" markdown="1">
<summary>A PC port should carry only VLAN 20 data — which answer best fits?</summary>

**Answer:** Access VLAN 20

Access VLAN 20 is the best match for this situation. Access ports associate endpoints with one data VLAN; trunks carry tagged VLANs and may carry native untagged traffic. An SVI provides a logical layer-3 interface. STP blocks redundant layer-2 paths; LACP negotiates bundles. MTU mismatch can cause drops. Voice VLANs separate phone traffic.

</details>

<details class="hr-qa" markdown="1">
<summary>Two switches must carry VLANs 10 and 20 over one link — which answer best fits?</summary>

**Answer:** 802.1Q trunk

802.1Q trunk is the best match for this situation. Access ports associate endpoints with one data VLAN; trunks carry tagged VLANs and may carry native untagged traffic. An SVI provides a logical layer-3 interface. STP blocks redundant layer-2 paths; LACP negotiates bundles. MTU mismatch can cause drops. Voice VLANs separate phone traffic.

</details>

<details class="hr-qa" markdown="1">
<summary>A multilayer switch routes for VLAN 30 — which answer best fits?</summary>

**Answer:** SVI for VLAN 30

SVI for VLAN 30 is the best match for this situation. Access ports associate endpoints with one data VLAN; trunks carry tagged VLANs and may carry native untagged traffic. An SVI provides a logical layer-3 interface. STP blocks redundant layer-2 paths; LACP negotiates bundles. MTU mismatch can cause drops. Voice VLANs separate phone traffic.

</details>

<details class="hr-qa" markdown="1">
<summary>Redundant links create a layer-2 loop — which answer best fits?</summary>

**Answer:** STP

STP is the best match for this situation. Access ports associate endpoints with one data VLAN; trunks carry tagged VLANs and may carry native untagged traffic. An SVI provides a logical layer-3 interface. STP blocks redundant layer-2 paths; LACP negotiates bundles. MTU mismatch can cause drops. Voice VLANs separate phone traffic.

</details>

<details class="hr-qa" markdown="1">
<summary>Two physical links should negotiate one logical bundle — which answer best fits?</summary>

**Answer:** LACP

LACP is the best match for this situation. Access ports associate endpoints with one data VLAN; trunks carry tagged VLANs and may carry native untagged traffic. An SVI provides a logical layer-3 interface. STP blocks redundant layer-2 paths; LACP negotiates bundles. MTU mismatch can cause drops. Voice VLANs separate phone traffic.

</details>

<details class="hr-qa" markdown="1">
<summary>A phone and PC share one switch port with separate traffic classes — which answer best fits?</summary>

**Answer:** Voice VLAN and data VLAN

Voice VLAN and data VLAN is the best match for this situation. Access ports associate endpoints with one data VLAN; trunks carry tagged VLANs and may carry native untagged traffic. An SVI provides a logical layer-3 interface. STP blocks redundant layer-2 paths; LACP negotiates bundles. MTU mismatch can cause drops. Voice VLANs separate phone traffic.

</details>

<details class="hr-qa" markdown="1">
<summary>Untagged frames on a trunk map to which configured VLAN — which answer best fits?</summary>

**Answer:** Native VLAN

Native VLAN is the best match for this situation. Access ports associate endpoints with one data VLAN; trunks carry tagged VLANs and may carry native untagged traffic. An SVI provides a logical layer-3 interface. STP blocks redundant layer-2 paths; LACP negotiates bundles. MTU mismatch can cause drops. Voice VLANs separate phone traffic.

</details>

<details class="hr-qa" markdown="1">
<summary>Large frames fail across a path with inconsistent frame limits — which answer best fits?</summary>

**Answer:** MTU mismatch

MTU mismatch is the best match for this situation. Access ports associate endpoints with one data VLAN; trunks carry tagged VLANs and may carry native untagged traffic. An SVI provides a logical layer-3 interface. STP blocks redundant layer-2 paths; LACP negotiates bundles. MTU mismatch can cause drops. Voice VLANs separate phone traffic.

</details>

<details class="hr-qa" markdown="1">
<summary>A new VLAN is missing from an uplink allowed list — which answer best fits?</summary>

**Answer:** Permit the required VLAN on the trunk

Permit the required VLAN on the trunk is the best match for this situation. Access ports associate endpoints with one data VLAN; trunks carry tagged VLANs and may carry native untagged traffic. An SVI provides a logical layer-3 interface. STP blocks redundant layer-2 paths; LACP negotiates bundles. MTU mismatch can cause drops. Voice VLANs separate phone traffic.

</details>

<details class="hr-qa" markdown="1">
<summary>One side is forced full duplex and the other falls back to half — which answer best fits?</summary>

**Answer:** Duplex mismatch

Duplex mismatch is the best match for this situation. Access ports associate endpoints with one data VLAN; trunks carry tagged VLANs and may carry native untagged traffic. An SVI provides a logical layer-3 interface. STP blocks redundant layer-2 paths; LACP negotiates bundles. MTU mismatch can cause drops. Voice VLANs separate phone traffic.

</details>


### Visual learning

- [Networking Fundamentals — VLANs, Trunk Ports, Broadcast Domains, and Inter-VLAN Routing Study Diagram"
](/network-portfolio/study-diagrams/vlans-trunk-ports-broadcast-domains-inter-vlan-routing/)
- [Infrastructure — Spanning Tree Protocol: Topology Change Notification"
](/network-portfolio/study-diagrams/stp-tcn/)
- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)

<a id="objective-2-3"></a>

## 2.3 — Wireless

### Technical distinctions

- **WPA3-Personal:** Uses SAE for password-based wireless authentication.
- **WPA2-Enterprise:** Uses 802.1X authentication with an authentication server.
- **Directional antenna:** Concentrates radio energy toward a specific area.
- **Channel planning:** Reduces interference by coordinating frequency use.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


Wi-Fi shares radio airtime. Channel width, interference, signal strength and client density affect performance. WPA3 provides modern authentication and encryption options; enterprise authentication commonly uses 802.1X. A site survey helps determine coverage and channel reuse.


### Deep dive — Wireless design

2.4 GHz generally reaches farther but has fewer nonoverlapping channels; 5 and 6 GHz offer more capacity subject to regulations and client support. WPA3 uses stronger authentication modes; enterprise Wi-Fi commonly uses 802.1X. Channel width trades capacity for interference exposure. Survey coverage, SNR and channel utilization.

**Hands-on verification:** Survey RSSI and SNR at client locations; compare channel utilization before changing power or channel width.

**Reference for further study:** IEEE 802.11.

[Practice this objective](../practice/?objective=2.3) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| SSID | Service set identifier; wireless network name |
| BSSID | Basic service set identifier; identifies a basic service set |
| WPA3 | Wi-Fi protected access 3; wireless security suite |
| RSSI | Received signal strength indicator; received signal measurement |

### Technical quick-reference table

| Feature | Purpose | Caveat |
| --- | --- | --- |
| 2.4 GHz | Coverage | Few nonoverlapping channels |
| 5 GHz | Capacity | Shorter typical reach |
| 6 GHz | Additional spectrum | Compatible clients required |
| WPA3 | Stronger authentication options | Check client compatibility |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>Which action best addresses overlapping-channel interference?</summary>

**Answer:** Plan nonoverlapping channels

Wi-Fi shares radio airtime. Channel width, interference, signal strength and client density affect performance. WPA3 provides modern authentication and encryption options; enterprise authentication commonly uses 802.1X. A site survey helps determine coverage and channel reuse.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: identifier of a particular wireless basic service set, commonly an AP radio MAC?</summary>

**Answer:** BSSID

BSSID: Identifier of a particular wireless basic service set, commonly an AP radio MAC. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: concentrates radio energy toward a particular direction?</summary>

**Answer:** Directional antenna

Directional antenna: Concentrates radio energy toward a particular direction. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: uses SAE for password-based Wi-Fi authentication?</summary>

**Answer:** WPA3-Personal

WPA3-Personal: Uses SAE for password-based Wi-Fi authentication. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: web-based guest access or acceptance workflow?</summary>

**Answer:** Captive portal

Captive portal: Web-based guest access or acceptance workflow. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: encourages capable clients to use a preferred frequency band?</summary>

**Answer:** Band steering

Band steering: Encourages capable clients to use a preferred frequency band. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Three nearby 2.4 GHz APs in a US deployment use 20 MHz channels. Which conventional channel plan minimizes overlap?</summary>

**Answer:** 1, 6, 11

Channels 1, 6 and 11 are the conventional nonoverlapping 20 MHz plan in the US.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Directional antenna?</summary>

**Answer:** Concentrates radio energy toward a particular direction

Directional antenna refers to concentrates radio energy toward a particular direction. The alternatives instead describe BSSID, WPA3-Personal, Captive portal.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes WPA3-Personal?</summary>

**Answer:** Uses SAE for password-based Wi-Fi authentication

WPA3-Personal refers to uses SAE for password-based Wi-Fi authentication. The alternatives instead describe BSSID, Directional antenna, Captive portal.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Captive portal?</summary>

**Answer:** Web-based guest access or acceptance workflow

Captive portal refers to web-based guest access or acceptance workflow. The alternatives instead describe BSSID, Directional antenna, WPA3-Personal.

</details>

<details class="hr-qa" markdown="1">
<summary>An office has three nearby 2.4 GHz APs using 20 MHz channels in the US. Which plan minimizes mutual overlap?</summary>

**Answer:** 1, 6, 11

Channels 1, 6 and 11 are the conventional non-overlapping plan; adjacent channels overlap and identical channels contend.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: uses SAE for password-based wireless authentication?</summary>

**Answer:** WPA3-Personal

WPA3-Personal: Uses SAE for password-based wireless authentication; WPA2-Enterprise: Uses 802.1X authentication with an authentication server; Directional antenna: Concentrates radio energy toward a specific area; Channel planning: Reduces interference by coordinating frequency use.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes WPA3-Personal from the alternatives?</summary>

**Answer:** Uses SAE for password-based wireless authentication

WPA3-Personal: Uses SAE for password-based wireless authentication; WPA2-Enterprise: Uses 802.1X authentication with an authentication server; Directional antenna: Concentrates radio energy toward a specific area; Channel planning: Reduces interference by coordinating frequency use.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: uses 802.1X authentication with an authentication server?</summary>

**Answer:** WPA2-Enterprise

WPA3-Personal: Uses SAE for password-based wireless authentication; WPA2-Enterprise: Uses 802.1X authentication with an authentication server; Directional antenna: Concentrates radio energy toward a specific area; Channel planning: Reduces interference by coordinating frequency use.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes WPA2-Enterprise from the alternatives?</summary>

**Answer:** Uses 802.1X authentication with an authentication server

WPA3-Personal: Uses SAE for password-based wireless authentication; WPA2-Enterprise: Uses 802.1X authentication with an authentication server; Directional antenna: Concentrates radio energy toward a specific area; Channel planning: Reduces interference by coordinating frequency use.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: concentrates radio energy toward a specific area?</summary>

**Answer:** Directional antenna

WPA3-Personal: Uses SAE for password-based wireless authentication; WPA2-Enterprise: Uses 802.1X authentication with an authentication server; Directional antenna: Concentrates radio energy toward a specific area; Channel planning: Reduces interference by coordinating frequency use.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Directional antenna from the alternatives?</summary>

**Answer:** Concentrates radio energy toward a specific area

WPA3-Personal: Uses SAE for password-based wireless authentication; WPA2-Enterprise: Uses 802.1X authentication with an authentication server; Directional antenna: Concentrates radio energy toward a specific area; Channel planning: Reduces interference by coordinating frequency use.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: reduces interference by coordinating frequency use?</summary>

**Answer:** Channel planning

WPA3-Personal: Uses SAE for password-based wireless authentication; WPA2-Enterprise: Uses 802.1X authentication with an authentication server; Directional antenna: Concentrates radio energy toward a specific area; Channel planning: Reduces interference by coordinating frequency use.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Channel planning from the alternatives?</summary>

**Answer:** Reduces interference by coordinating frequency use

WPA3-Personal: Uses SAE for password-based wireless authentication; WPA2-Enterprise: Uses 802.1X authentication with an authentication server; Directional antenna: Concentrates radio energy toward a specific area; Channel planning: Reduces interference by coordinating frequency use.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes WPA2-Enterprise for a task that requires: uses SAE for password-based wireless authentication. Which alternative is the better match?</summary>

**Answer:** WPA3-Personal

WPA3-Personal: Uses SAE for password-based wireless authentication; WPA2-Enterprise: Uses 802.1X authentication with an authentication server; Directional antenna: Concentrates radio energy toward a specific area; Channel planning: Reduces interference by coordinating frequency use.

</details>

<details class="hr-qa" markdown="1">
<summary>Three 20 MHz 2.4 GHz APs in the US need nonoverlapping channels — which answer best fits?</summary>

**Answer:** 1, 6, 11

1, 6, 11 is the best match for this situation. 2.4 GHz generally reaches farther but has fewer nonoverlapping channels; 5 and 6 GHz offer more capacity subject to regulations and client support. WPA3 uses stronger authentication modes; enterprise Wi-Fi commonly uses 802.1X. Channel width trades capacity for interference exposure. Survey coverage, SNR and channel utilization.

</details>

<details class="hr-qa" markdown="1">
<summary>Enterprise Wi-Fi requires per-user authentication — which answer best fits?</summary>

**Answer:** 802.1X with RADIUS

802.1X with RADIUS is the best match for this situation. 2.4 GHz generally reaches farther but has fewer nonoverlapping channels; 5 and 6 GHz offer more capacity subject to regulations and client support. WPA3 uses stronger authentication modes; enterprise Wi-Fi commonly uses 802.1X. Channel width trades capacity for interference exposure. Survey coverage, SNR and channel utilization.

</details>

<details class="hr-qa" markdown="1">
<summary>A dense deployment has overlapping wide channels — which answer best fits?</summary>

**Answer:** Consider narrower channels after survey

Consider narrower channels after survey is the best match for this situation. 2.4 GHz generally reaches farther but has fewer nonoverlapping channels; 5 and 6 GHz offer more capacity subject to regulations and client support. WPA3 uses stronger authentication modes; enterprise Wi-Fi commonly uses 802.1X. Channel width trades capacity for interference exposure. Survey coverage, SNR and channel utilization.

</details>

<details class="hr-qa" markdown="1">
<summary>A client sees strong signal but high noise — which answer best fits?</summary>

**Answer:** Low SNR may impair service

Low SNR may impair service is the best match for this situation. 2.4 GHz generally reaches farther but has fewer nonoverlapping channels; 5 and 6 GHz offer more capacity subject to regulations and client support. WPA3 uses stronger authentication modes; enterprise Wi-Fi commonly uses 802.1X. Channel width trades capacity for interference exposure. Survey coverage, SNR and channel utilization.

</details>

<details class="hr-qa" markdown="1">
<summary>An AP needs to cover a long narrow outdoor path — which answer best fits?</summary>

**Answer:** Directional antenna

Directional antenna is the best match for this situation. 2.4 GHz generally reaches farther but has fewer nonoverlapping channels; 5 and 6 GHz offer more capacity subject to regulations and client support. WPA3 uses stronger authentication modes; enterprise Wi-Fi commonly uses 802.1X. Channel width trades capacity for interference exposure. Survey coverage, SNR and channel utilization.

</details>

<details class="hr-qa" markdown="1">
<summary>A guest network must not reach internal servers — which answer best fits?</summary>

**Answer:** Guest isolation and firewall policy

Guest isolation and firewall policy is the best match for this situation. 2.4 GHz generally reaches farther but has fewer nonoverlapping channels; 5 and 6 GHz offer more capacity subject to regulations and client support. WPA3 uses stronger authentication modes; enterprise Wi-Fi commonly uses 802.1X. Channel width trades capacity for interference exposure. Survey coverage, SNR and channel utilization.

</details>

<details class="hr-qa" markdown="1">
<summary>A modern personal network needs SAE authentication — which answer best fits?</summary>

**Answer:** WPA3-Personal

WPA3-Personal is the best match for this situation. 2.4 GHz generally reaches farther but has fewer nonoverlapping channels; 5 and 6 GHz offer more capacity subject to regulations and client support. WPA3 uses stronger authentication modes; enterprise Wi-Fi commonly uses 802.1X. Channel width trades capacity for interference exposure. Survey coverage, SNR and channel utilization.

</details>

<details class="hr-qa" markdown="1">
<summary>A 6 GHz-only SSID is invisible to an older 2.4 GHz client — which answer best fits?</summary>

**Answer:** Client lacks band support

Client lacks band support is the best match for this situation. 2.4 GHz generally reaches farther but has fewer nonoverlapping channels; 5 and 6 GHz offer more capacity subject to regulations and client support. WPA3 uses stronger authentication modes; enterprise Wi-Fi commonly uses 802.1X. Channel width trades capacity for interference exposure. Survey coverage, SNR and channel utilization.

</details>

<details class="hr-qa" markdown="1">
<summary>A wireless bridge connects two buildings — which answer best fits?</summary>

**Answer:** Point-to-point wireless

Point-to-point wireless is the best match for this situation. 2.4 GHz generally reaches farther but has fewer nonoverlapping channels; 5 and 6 GHz offer more capacity subject to regulations and client support. WPA3 uses stronger authentication modes; enterprise Wi-Fi commonly uses 802.1X. Channel width trades capacity for interference exposure. Survey coverage, SNR and channel utilization.

</details>

<details class="hr-qa" markdown="1">
<summary>Clients remain attached to a distant AP despite closer coverage — which answer best fits?</summary>

**Answer:** Investigate roaming and cell design

Investigate roaming and cell design is the best match for this situation. 2.4 GHz generally reaches farther but has fewer nonoverlapping channels; 5 and 6 GHz offer more capacity subject to regulations and client support. WPA3 uses stronger authentication modes; enterprise Wi-Fi commonly uses 802.1X. Channel width trades capacity for interference exposure. Survey coverage, SNR and channel utilization.

</details>


### Visual learning

- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)

<a id="objective-2-4"></a>

## 2.4 — Physical installation

### Technical distinctions

- **UPS:** Provides temporary power during an outage.
- **PDU:** Distributes electrical power to rack equipment.
- **Patch panel:** Terminates and organizes permanent cabling.
- **Hot aisle:** Collects warm exhaust from equipment racks.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


Plan rack space, power, cooling, grounding, cable paths and physical access. UPS supplies temporary power; PDU distributes power. Label both cable ends and document patch-panel mappings. Verify environmental limits and redundancy.


### Deep dive — Installation constraints

MDF and IDF organize distribution; patch panels provide termination. Calculate PoE demand against switch budget and UPS capacity against load/runtime. Maintain airflow, temperature, humidity and grounding per code. Use labels, cable management and physical access control.

**Hands-on verification:** Inventory rack power, PoE class, uplink type and UPS runtime; verify against manufacturer ratings.

**Reference for further study:** IEEE 802.3.

[Practice this objective](../practice/?objective=2.4) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| MDF | Main distribution frame; central cabling distribution |
| IDF | Intermediate distribution frame; local distribution |
| UPS | Uninterruptible power supply; temporary power during interruption |

### Technical quick-reference table

| Concern | Check | Mitigation |
| --- | --- | --- |
| Power | PoE budget and UPS | Size for actual load |
| Cooling | Airflow and temperature | Avoid blocked vents |
| Cabling | Labels and bend radius | Follow manufacturer limits |
| Grounding | Bonding requirements | Follow applicable electrical codes |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>Which device supplies temporary power during an outage?</summary>

**Answer:** UPS

Plan rack space, power, cooling, grounding, cable paths and physical access. UPS supplies temporary power; PDU distributes power. Label both cable ends and document patch-panel mappings. Verify environmental limits and redundancy.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: main facility distribution point for network cabling?</summary>

**Answer:** MDF

MDF: Main facility distribution point for network cabling. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: intermediate distribution point serving a local area or floor?</summary>

**Answer:** IDF

IDF: Intermediate distribution point serving a local area or floor. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: temporary electrical power during an outage?</summary>

**Answer:** UPS

UPS: Temporary electrical power during an outage. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: distributes electrical power to rack equipment?</summary>

**Answer:** PDU

PDU: Distributes electrical power to rack equipment. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: organizes and terminates permanent copper cabling?</summary>

**Answer:** Patch panel

Patch panel: Organizes and terminates permanent copper cabling. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>A rack needs to remain powered during a brief utility interruption. Which device provides stored energy?</summary>

**Answer:** UPS

A UPS supplies temporary power; a passive PDU distributes power but does not store it.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes IDF?</summary>

**Answer:** Intermediate distribution point serving a local area or floor

IDF refers to intermediate distribution point serving a local area or floor. The alternatives instead describe MDF, UPS, PDU.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes UPS?</summary>

**Answer:** Temporary electrical power during an outage

UPS refers to temporary electrical power during an outage. The alternatives instead describe MDF, IDF, PDU.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes PDU?</summary>

**Answer:** Distributes electrical power to rack equipment

PDU refers to distributes electrical power to rack equipment. The alternatives instead describe MDF, IDF, UPS.

</details>

<details class="hr-qa" markdown="1">
<summary>A rack must keep switches running during a brief utility outage. Which device provides temporary power?</summary>

**Answer:** UPS

A UPS supplies stored energy; a basic PDU distributes power and the other devices organize cabling.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: provides temporary power during an outage?</summary>

**Answer:** UPS

UPS: Provides temporary power during an outage; PDU: Distributes electrical power to rack equipment; Patch panel: Terminates and organizes permanent cabling; Hot aisle: Collects warm exhaust from equipment racks.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes UPS from the alternatives?</summary>

**Answer:** Provides temporary power during an outage

UPS: Provides temporary power during an outage; PDU: Distributes electrical power to rack equipment; Patch panel: Terminates and organizes permanent cabling; Hot aisle: Collects warm exhaust from equipment racks.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: distributes electrical power to rack equipment?</summary>

**Answer:** PDU

UPS: Provides temporary power during an outage; PDU: Distributes electrical power to rack equipment; Patch panel: Terminates and organizes permanent cabling; Hot aisle: Collects warm exhaust from equipment racks.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes PDU from the alternatives?</summary>

**Answer:** Distributes electrical power to rack equipment

UPS: Provides temporary power during an outage; PDU: Distributes electrical power to rack equipment; Patch panel: Terminates and organizes permanent cabling; Hot aisle: Collects warm exhaust from equipment racks.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: terminates and organizes permanent cabling?</summary>

**Answer:** Patch panel

UPS: Provides temporary power during an outage; PDU: Distributes electrical power to rack equipment; Patch panel: Terminates and organizes permanent cabling; Hot aisle: Collects warm exhaust from equipment racks.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Patch panel from the alternatives?</summary>

**Answer:** Terminates and organizes permanent cabling

UPS: Provides temporary power during an outage; PDU: Distributes electrical power to rack equipment; Patch panel: Terminates and organizes permanent cabling; Hot aisle: Collects warm exhaust from equipment racks.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: collects warm exhaust from equipment racks?</summary>

**Answer:** Hot aisle

UPS: Provides temporary power during an outage; PDU: Distributes electrical power to rack equipment; Patch panel: Terminates and organizes permanent cabling; Hot aisle: Collects warm exhaust from equipment racks.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Hot aisle from the alternatives?</summary>

**Answer:** Collects warm exhaust from equipment racks

UPS: Provides temporary power during an outage; PDU: Distributes electrical power to rack equipment; Patch panel: Terminates and organizes permanent cabling; Hot aisle: Collects warm exhaust from equipment racks.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes PDU for a task that requires: provides temporary power during an outage. Which alternative is the better match?</summary>

**Answer:** UPS

UPS: Provides temporary power during an outage; PDU: Distributes electrical power to rack equipment; Patch panel: Terminates and organizes permanent cabling; Hot aisle: Collects warm exhaust from equipment racks.

</details>

<details class="hr-qa" markdown="1">
<summary>A switch has 120 W PoE budget and eight 20 W devices — which answer best fits?</summary>

**Answer:** Budget insufficient for all eight

Budget insufficient for all eight is the best match for this situation. MDF and IDF organize distribution; patch panels provide termination. Calculate PoE demand against switch budget and UPS capacity against load/runtime. Maintain airflow, temperature, humidity and grounding per code. Use labels, cable management and physical access control.

</details>

<details class="hr-qa" markdown="1">
<summary>A rack needs temporary power during utility failure — which answer best fits?</summary>

**Answer:** UPS

UPS is the best match for this situation. MDF and IDF organize distribution; patch panels provide termination. Calculate PoE demand against switch budget and UPS capacity against load/runtime. Maintain airflow, temperature, humidity and grounding per code. Use labels, cable management and physical access control.

</details>

<details class="hr-qa" markdown="1">
<summary>A building floor needs local cable distribution — which answer best fits?</summary>

**Answer:** IDF

IDF is the best match for this situation. MDF and IDF organize distribution; patch panels provide termination. Calculate PoE demand against switch budget and UPS capacity against load/runtime. Maintain airflow, temperature, humidity and grounding per code. Use labels, cable management and physical access control.

</details>

<details class="hr-qa" markdown="1">
<summary>Permanent horizontal cables terminate in a rack — which answer best fits?</summary>

**Answer:** Patch panel

Patch panel is the best match for this situation. MDF and IDF organize distribution; patch panels provide termination. Calculate PoE demand against switch budget and UPS capacity against load/runtime. Maintain airflow, temperature, humidity and grounding per code. Use labels, cable management and physical access control.

</details>

<details class="hr-qa" markdown="1">
<summary>A rack exhaust faces another rack intake causing overheating — which answer best fits?</summary>

**Answer:** Correct airflow arrangement

Correct airflow arrangement is the best match for this situation. MDF and IDF organize distribution; patch panels provide termination. Calculate PoE demand against switch budget and UPS capacity against load/runtime. Maintain airflow, temperature, humidity and grounding per code. Use labels, cable management and physical access control.

</details>

<details class="hr-qa" markdown="1">
<summary>A cabinet needs protection from unauthorized physical access — which answer best fits?</summary>

**Answer:** Lock and access logging

Lock and access logging is the best match for this situation. MDF and IDF organize distribution; patch panels provide termination. Calculate PoE demand against switch budget and UPS capacity against load/runtime. Maintain airflow, temperature, humidity and grounding per code. Use labels, cable management and physical access control.

</details>

<details class="hr-qa" markdown="1">
<summary>A fiber cable exceeds minimum bend radius constraints — which answer best fits?</summary>

**Answer:** Reroute within specified bend radius

Reroute within specified bend radius is the best match for this situation. MDF and IDF organize distribution; patch panels provide termination. Calculate PoE demand against switch budget and UPS capacity against load/runtime. Maintain airflow, temperature, humidity and grounding per code. Use labels, cable management and physical access control.

</details>

<details class="hr-qa" markdown="1">
<summary>A new rack requires electrical bonding — which answer best fits?</summary>

**Answer:** Follow code and qualified installation

Follow code and qualified installation is the best match for this situation. MDF and IDF organize distribution; patch panels provide termination. Calculate PoE demand against switch budget and UPS capacity against load/runtime. Maintain airflow, temperature, humidity and grounding per code. Use labels, cable management and physical access control.

</details>

<details class="hr-qa" markdown="1">
<summary>A UPS must support a 500 W load — which answer best fits?</summary>

**Answer:** Check watt rating and runtime at 500 W

Check watt rating and runtime at 500 W is the best match for this situation. MDF and IDF organize distribution; patch panels provide termination. Calculate PoE demand against switch budget and UPS capacity against load/runtime. Maintain airflow, temperature, humidity and grounding per code. Use labels, cable management and physical access control.

</details>

<details class="hr-qa" markdown="1">
<summary>Technicians cannot identify both ends of a cable — which answer best fits?</summary>

**Answer:** Apply consistent labels and update records

Apply consistent labels and update records is the best match for this situation. MDF and IDF organize distribution; patch panels provide termination. Calculate PoE demand against switch budget and UPS capacity against load/runtime. Maintain airflow, temperature, humidity and grounding per code. Use labels, cable management and physical access control.

</details>


### Visual learning

- [Networking Fundamentals — Structured Cabling Systems"
](/network-portfolio/study-diagrams/structured-cabling-systems/)
- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)

<a id="objective-3-1"></a>

## 3.1 — Documentation and change management

### Technical distinctions

- **Baseline:** Records normal behavior for later comparison.
- **Change approval:** Authorizes planned modifications before implementation.
- **IPAM:** Tracks address allocations and utilization.
- **Logical diagram:** Shows VLANs subnets and routing relationships.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


Maintain physical and logical diagrams, IPAM, inventories, baselines and configuration backups. Changes require impact analysis, approval, validation and rollback planning. Track end-of-life and end-of-support separately.


### Deep dive — Operational records

Physical and logical diagrams serve different purposes. IPAM records address allocation; inventory records assets and lifecycle. Baselines describe expected behavior. Change management defines scope, approval, validation and rollback. Configuration backups should be secured and tested. EOL and EOS dates guide replacement.

**Hands-on verification:** Draft a VLAN change with prechecks, rollback triggers, maintenance window and postchecks.

**Reference for further study:** NIST SP 800-128.

[Practice this objective](../practice/?objective=3.1) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| IPAM | IP address management; tracks address allocation |
| SLA | Service level agreement; agreed service commitments |
| EOL | End of life; lifecycle milestone |
| EOS | End of support; support termination milestone |

### Technical quick-reference table

| Record | Purpose | Example |
| --- | --- | --- |
| IPAM | Address inventory | Subnet allocations |
| Baseline | Normal behavior | Typical link utilization |
| Change record | Accountability | Rollback plan |
| Diagram | Dependency mapping | Logical VLAN topology |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>What should be prepared before a risky configuration change?</summary>

**Answer:** Rollback plan

Maintain physical and logical diagrams, IPAM, inventories, baselines and configuration backups. Changes require impact analysis, approval, validation and rollback planning. Track end-of-life and end-of-support separately.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: tracks IP allocations and address space utilization?</summary>

**Answer:** IPAM

IPAM: Tracks IP allocations and address space utilization. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: defines agreed service performance and availability commitments?</summary>

**Answer:** SLA

SLA: Defines agreed service performance and availability commitments. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: approved reference configuration used for comparison?</summary>

**Answer:** Golden configuration

Golden configuration: Approved reference configuration used for comparison. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: records proposed work, approvals and impact before implementation?</summary>

**Answer:** Change request

Change request: Records proposed work, approvals and impact before implementation. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: tracks devices, software, licenses and support information?</summary>

**Answer:** Asset inventory

Asset inventory: Tracks devices, software, licenses and support information. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>A switch configuration changed overnight. Which artifact best identifies deviations from the approved settings?</summary>

**Answer:** Golden configuration

Comparing the running configuration to an approved baseline identifies configuration drift.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes SLA?</summary>

**Answer:** Defines agreed service performance and availability commitments

SLA refers to defines agreed service performance and availability commitments. The alternatives instead describe IPAM, Golden configuration, Change request.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Golden configuration?</summary>

**Answer:** Approved reference configuration used for comparison

Golden configuration refers to approved reference configuration used for comparison. The alternatives instead describe IPAM, SLA, Change request.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Change request?</summary>

**Answer:** Records proposed work, approvals and impact before implementation

Change request refers to records proposed work, approvals and impact before implementation. The alternatives instead describe IPAM, SLA, Golden configuration.

</details>

<details class="hr-qa" markdown="1">
<summary>A firmware update breaks connectivity. Which artifact best supports restoration of the prior settings?</summary>

**Answer:** Pre-change configuration backup

A configuration backup preserves settings; the other documents describe assets, coverage or physical placement.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: records normal behavior for later comparison?</summary>

**Answer:** Baseline

Baseline: Records normal behavior for later comparison; Change approval: Authorizes planned modifications before implementation; IPAM: Tracks address allocations and utilization; Logical diagram: Shows VLANs subnets and routing relationships.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Baseline from the alternatives?</summary>

**Answer:** Records normal behavior for later comparison

Baseline: Records normal behavior for later comparison; Change approval: Authorizes planned modifications before implementation; IPAM: Tracks address allocations and utilization; Logical diagram: Shows VLANs subnets and routing relationships.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: authorizes planned modifications before implementation?</summary>

**Answer:** Change approval

Baseline: Records normal behavior for later comparison; Change approval: Authorizes planned modifications before implementation; IPAM: Tracks address allocations and utilization; Logical diagram: Shows VLANs subnets and routing relationships.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Change approval from the alternatives?</summary>

**Answer:** Authorizes planned modifications before implementation

Baseline: Records normal behavior for later comparison; Change approval: Authorizes planned modifications before implementation; IPAM: Tracks address allocations and utilization; Logical diagram: Shows VLANs subnets and routing relationships.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: tracks address allocations and utilization?</summary>

**Answer:** IPAM

Baseline: Records normal behavior for later comparison; Change approval: Authorizes planned modifications before implementation; IPAM: Tracks address allocations and utilization; Logical diagram: Shows VLANs subnets and routing relationships.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes IPAM from the alternatives?</summary>

**Answer:** Tracks address allocations and utilization

Baseline: Records normal behavior for later comparison; Change approval: Authorizes planned modifications before implementation; IPAM: Tracks address allocations and utilization; Logical diagram: Shows VLANs subnets and routing relationships.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: shows VLANs subnets and routing relationships?</summary>

**Answer:** Logical diagram

Baseline: Records normal behavior for later comparison; Change approval: Authorizes planned modifications before implementation; IPAM: Tracks address allocations and utilization; Logical diagram: Shows VLANs subnets and routing relationships.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Logical diagram from the alternatives?</summary>

**Answer:** Shows VLANs subnets and routing relationships

Baseline: Records normal behavior for later comparison; Change approval: Authorizes planned modifications before implementation; IPAM: Tracks address allocations and utilization; Logical diagram: Shows VLANs subnets and routing relationships.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes Change approval for a task that requires: records normal behavior for later comparison. Which alternative is the better match?</summary>

**Answer:** Baseline

Baseline: Records normal behavior for later comparison; Change approval: Authorizes planned modifications before implementation; IPAM: Tracks address allocations and utilization; Logical diagram: Shows VLANs subnets and routing relationships.

</details>

<details class="hr-qa" markdown="1">
<summary>An engineer needs rack and cable locations — which answer best fits?</summary>

**Answer:** Physical diagram

Physical diagram is the best match for this situation. Physical and logical diagrams serve different purposes. IPAM records address allocation; inventory records assets and lifecycle. Baselines describe expected behavior. Change management defines scope, approval, validation and rollback. Configuration backups should be secured and tested. EOL and EOS dates guide replacement.

</details>

<details class="hr-qa" markdown="1">
<summary>An engineer needs VLAN and subnet relationships — which answer best fits?</summary>

**Answer:** Logical diagram

Logical diagram is the best match for this situation. Physical and logical diagrams serve different purposes. IPAM records address allocation; inventory records assets and lifecycle. Baselines describe expected behavior. Change management defines scope, approval, validation and rollback. Configuration backups should be secured and tested. EOL and EOS dates guide replacement.

</details>

<details class="hr-qa" markdown="1">
<summary>Two teams allocate overlapping subnets — which answer best fits?</summary>

**Answer:** IPAM

IPAM is the best match for this situation. Physical and logical diagrams serve different purposes. IPAM records address allocation; inventory records assets and lifecycle. Baselines describe expected behavior. Change management defines scope, approval, validation and rollback. Configuration backups should be secured and tested. EOL and EOS dates guide replacement.

</details>

<details class="hr-qa" markdown="1">
<summary>A firmware update may disrupt production — which answer best fits?</summary>

**Answer:** Approved change with rollback plan

Approved change with rollback plan is the best match for this situation. Physical and logical diagrams serve different purposes. IPAM records address allocation; inventory records assets and lifecycle. Baselines describe expected behavior. Change management defines scope, approval, validation and rollback. Configuration backups should be secured and tested. EOL and EOS dates guide replacement.

</details>

<details class="hr-qa" markdown="1">
<summary>A device will no longer receive vendor support — which answer best fits?</summary>

**Answer:** Lifecycle replacement planning

Lifecycle replacement planning is the best match for this situation. Physical and logical diagrams serve different purposes. IPAM records address allocation; inventory records assets and lifecycle. Baselines describe expected behavior. Change management defines scope, approval, validation and rollback. Configuration backups should be secured and tested. EOL and EOS dates guide replacement.

</details>

<details class="hr-qa" markdown="1">
<summary>A team needs expected normal utilization — which answer best fits?</summary>

**Answer:** Performance baseline

Performance baseline is the best match for this situation. Physical and logical diagrams serve different purposes. IPAM records address allocation; inventory records assets and lifecycle. Baselines describe expected behavior. Change management defines scope, approval, validation and rollback. Configuration backups should be secured and tested. EOL and EOS dates guide replacement.

</details>

<details class="hr-qa" markdown="1">
<summary>A switch fails after a configuration change — which answer best fits?</summary>

**Answer:** Restore validated configuration per rollback plan

Restore validated configuration per rollback plan is the best match for this situation. Physical and logical diagrams serve different purposes. IPAM records address allocation; inventory records assets and lifecycle. Baselines describe expected behavior. Change management defines scope, approval, validation and rollback. Configuration backups should be secured and tested. EOL and EOS dates guide replacement.

</details>

<details class="hr-qa" markdown="1">
<summary>A new device must be tracked by serial and owner — which answer best fits?</summary>

**Answer:** Asset inventory

Asset inventory is the best match for this situation. Physical and logical diagrams serve different purposes. IPAM records address allocation; inventory records assets and lifecycle. Baselines describe expected behavior. Change management defines scope, approval, validation and rollback. Configuration backups should be secured and tested. EOL and EOS dates guide replacement.

</details>

<details class="hr-qa" markdown="1">
<summary>A provider promises monthly availability — which answer best fits?</summary>

**Answer:** SLA

SLA is the best match for this situation. Physical and logical diagrams serve different purposes. IPAM records address allocation; inventory records assets and lifecycle. Baselines describe expected behavior. Change management defines scope, approval, validation and rollback. Configuration backups should be secured and tested. EOL and EOS dates guide replacement.

</details>

<details class="hr-qa" markdown="1">
<summary>A technician needs the approved sequence for routine work — which answer best fits?</summary>

**Answer:** Standard operating procedure

Standard operating procedure is the best match for this situation. Physical and logical diagrams serve different purposes. IPAM records address allocation; inventory records assets and lifecycle. Baselines describe expected behavior. Change management defines scope, approval, validation and rollback. Configuration backups should be secured and tested. EOL and EOS dates guide replacement.

</details>


### Visual learning

- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)

<a id="objective-3-2"></a>

## 3.2 — Monitoring

### Technical distinctions

- **SNMPv3:** Supports authenticated and encrypted management messages.
- **Flow records:** Summarize conversations and traffic volume.
- **Syslog:** Collects timestamped device event messages.
- **Packet capture:** Records individual frames or packets for inspection.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


SNMP polls counters and receives notifications; syslog records events; flow telemetry summarizes conversations; packet captures show packet detail. Baselines distinguish normal variation from anomalies. SIEM correlates logs across sources.

[Related completed lab](/network-portfolio/formative-modules/lesson-18-0/summative-network-monitoring-tcp-udp-communications-lab-43/)


### Deep dive — Monitoring evidence

SNMP polls counters and receives notifications; v3 supports authentication and privacy. Flow telemetry summarizes conversations, while packet capture provides packet detail. Syslog centralizes events; synchronized time enables correlation. Baselines and thresholds should reflect normal patterns and alert severity.

**Hands-on verification:** Compare interface errors, utilization and flow data during a reported slowdown; correlate timestamps.

**Reference for further study:** RFC 3411; RFC 5424.

[Practice this objective](../practice/?objective=3.2) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| SNMP | Simple network management protocol; monitoring and management |
| MIB | Management information base; managed object definitions |
| OID | Object identifier; identifies a managed object |
| SIEM | Security information and event management; correlates event data |

### Technical quick-reference table

| Telemetry | Reveals | Limitation |
| --- | --- | --- |
| SNMP | Counters and status | Polling interval matters |
| Flow records | Conversation metadata | Not full payload |
| Packet capture | Packet-level evidence | Visibility depends on capture point |
| Syslog | Event messages | Time synchronization needed |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>Which tool provides packet-level protocol fields for analysis?</summary>

**Answer:** Packet capture

SNMP polls counters and receives notifications; syslog records events; flow telemetry summarizes conversations; packet captures show packet detail. Baselines distinguish normal variation from anomalies. SIEM correlates logs across sources.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: authenticated and encrypted SNMP management messages?</summary>

**Answer:** SNMPv3 authPriv

SNMPv3 authPriv: Authenticated and encrypted SNMP management messages. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: unsolicited event notification from a managed device?</summary>

**Answer:** SNMP trap

SNMP trap: Unsolicited event notification from a managed device. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: summarized conversations and traffic volumes without full packet payloads?</summary>

**Answer:** Flow data

Flow data: Summarized conversations and traffic volumes without full packet payloads. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: copies switch traffic to a monitoring interface?</summary>

**Answer:** Port mirroring

Port mirroring: Copies switch traffic to a monitoring interface. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: correlates security events from multiple log sources?</summary>

**Answer:** SIEM

SIEM: Correlates security events from multiple log sources. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>A team needs to inspect TCP retransmissions and individual packet headers. Which collection method is best?</summary>

**Answer:** Packet capture

Packet captures provide individual headers and timing; flow summaries aggregate conversations.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes SNMP trap?</summary>

**Answer:** Unsolicited event notification from a managed device

SNMP trap refers to unsolicited event notification from a managed device. The alternatives instead describe SNMPv3 authPriv, Flow data, Port mirroring.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Flow data?</summary>

**Answer:** Summarized conversations and traffic volumes without full packet payloads

Flow data refers to summarized conversations and traffic volumes without full packet payloads. The alternatives instead describe SNMPv3 authPriv, SNMP trap, Port mirroring.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Port mirroring?</summary>

**Answer:** Copies switch traffic to a monitoring interface

Port mirroring refers to copies switch traffic to a monitoring interface. The alternatives instead describe SNMPv3 authPriv, SNMP trap, Flow data.

</details>

<details class="hr-qa" markdown="1">
<summary>An analyst needs to identify which endpoints consume the most bandwidth without recording payloads. Which source is best?</summary>

**Answer:** Flow records

Flow records summarize endpoints and byte counts; payload capture is unnecessary, and diagrams and zone files do not measure traffic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: supports authenticated and encrypted management messages?</summary>

**Answer:** SNMPv3

SNMPv3: Supports authenticated and encrypted management messages; Flow records: Summarize conversations and traffic volume; Syslog: Collects timestamped device event messages; Packet capture: Records individual frames or packets for inspection.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes SNMPv3 from the alternatives?</summary>

**Answer:** Supports authenticated and encrypted management messages

SNMPv3: Supports authenticated and encrypted management messages; Flow records: Summarize conversations and traffic volume; Syslog: Collects timestamped device event messages; Packet capture: Records individual frames or packets for inspection.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: summarize conversations and traffic volume?</summary>

**Answer:** Flow records

SNMPv3: Supports authenticated and encrypted management messages; Flow records: Summarize conversations and traffic volume; Syslog: Collects timestamped device event messages; Packet capture: Records individual frames or packets for inspection.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Flow records from the alternatives?</summary>

**Answer:** Summarize conversations and traffic volume

SNMPv3: Supports authenticated and encrypted management messages; Flow records: Summarize conversations and traffic volume; Syslog: Collects timestamped device event messages; Packet capture: Records individual frames or packets for inspection.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: collects timestamped device event messages?</summary>

**Answer:** Syslog

SNMPv3: Supports authenticated and encrypted management messages; Flow records: Summarize conversations and traffic volume; Syslog: Collects timestamped device event messages; Packet capture: Records individual frames or packets for inspection.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Syslog from the alternatives?</summary>

**Answer:** Collects timestamped device event messages

SNMPv3: Supports authenticated and encrypted management messages; Flow records: Summarize conversations and traffic volume; Syslog: Collects timestamped device event messages; Packet capture: Records individual frames or packets for inspection.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: records individual frames or packets for inspection?</summary>

**Answer:** Packet capture

SNMPv3: Supports authenticated and encrypted management messages; Flow records: Summarize conversations and traffic volume; Syslog: Collects timestamped device event messages; Packet capture: Records individual frames or packets for inspection.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Packet capture from the alternatives?</summary>

**Answer:** Records individual frames or packets for inspection

SNMPv3: Supports authenticated and encrypted management messages; Flow records: Summarize conversations and traffic volume; Syslog: Collects timestamped device event messages; Packet capture: Records individual frames or packets for inspection.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes Flow records for a task that requires: supports authenticated and encrypted management messages. Which alternative is the better match?</summary>

**Answer:** SNMPv3

SNMPv3: Supports authenticated and encrypted management messages; Flow records: Summarize conversations and traffic volume; Syslog: Collects timestamped device event messages; Packet capture: Records individual frames or packets for inspection.

</details>

<details class="hr-qa" markdown="1">
<summary>A manager needs interface octet counters periodically — which answer best fits?</summary>

**Answer:** SNMP polling

SNMP polling is the best match for this situation. SNMP polls counters and receives notifications; v3 supports authentication and privacy. Flow telemetry summarizes conversations, while packet capture provides packet detail. Syslog centralizes events; synchronized time enables correlation. Baselines and thresholds should reflect normal patterns and alert severity.

</details>

<details class="hr-qa" markdown="1">
<summary>A device should notify a manager when a link goes down — which answer best fits?</summary>

**Answer:** SNMP trap or inform

SNMP trap or inform is the best match for this situation. SNMP polls counters and receives notifications; v3 supports authentication and privacy. Flow telemetry summarizes conversations, while packet capture provides packet detail. Syslog centralizes events; synchronized time enables correlation. Baselines and thresholds should reflect normal patterns and alert severity.

</details>

<details class="hr-qa" markdown="1">
<summary>A team needs top talkers without full packet payloads — which answer best fits?</summary>

**Answer:** Flow telemetry

Flow telemetry is the best match for this situation. SNMP polls counters and receives notifications; v3 supports authentication and privacy. Flow telemetry summarizes conversations, while packet capture provides packet detail. Syslog centralizes events; synchronized time enables correlation. Baselines and thresholds should reflect normal patterns and alert severity.

</details>

<details class="hr-qa" markdown="1">
<summary>A team needs TCP retransmission packet details — which answer best fits?</summary>

**Answer:** Packet capture

Packet capture is the best match for this situation. SNMP polls counters and receives notifications; v3 supports authentication and privacy. Flow telemetry summarizes conversations, while packet capture provides packet detail. Syslog centralizes events; synchronized time enables correlation. Baselines and thresholds should reflect normal patterns and alert severity.

</details>

<details class="hr-qa" markdown="1">
<summary>Logs from devices differ by several minutes — which answer best fits?</summary>

**Answer:** Synchronize clocks with NTP

Synchronize clocks with NTP is the best match for this situation. SNMP polls counters and receives notifications; v3 supports authentication and privacy. Flow telemetry summarizes conversations, while packet capture provides packet detail. Syslog centralizes events; synchronized time enables correlation. Baselines and thresholds should reflect normal patterns and alert severity.

</details>

<details class="hr-qa" markdown="1">
<summary>SNMP monitoring requires authentication and encryption — which answer best fits?</summary>

**Answer:** SNMPv3 authPriv

SNMPv3 authPriv is the best match for this situation. SNMP polls counters and receives notifications; v3 supports authentication and privacy. Flow telemetry summarizes conversations, while packet capture provides packet detail. Syslog centralizes events; synchronized time enables correlation. Baselines and thresholds should reflect normal patterns and alert severity.

</details>

<details class="hr-qa" markdown="1">
<summary>A recurring backup spike triggers unnecessary alerts — which answer best fits?</summary>

**Answer:** Tune threshold using baseline and schedule

Tune threshold using baseline and schedule is the best match for this situation. SNMP polls counters and receives notifications; v3 supports authentication and privacy. Flow telemetry summarizes conversations, while packet capture provides packet detail. Syslog centralizes events; synchronized time enables correlation. Baselines and thresholds should reflect normal patterns and alert severity.

</details>

<details class="hr-qa" markdown="1">
<summary>A security team needs centralized device event messages — which answer best fits?</summary>

**Answer:** Syslog collector

Syslog collector is the best match for this situation. SNMP polls counters and receives notifications; v3 supports authentication and privacy. Flow telemetry summarizes conversations, while packet capture provides packet detail. Syslog centralizes events; synchronized time enables correlation. Baselines and thresholds should reflect normal patterns and alert severity.

</details>

<details class="hr-qa" markdown="1">
<summary>A switch must copy traffic to an analyzer port — which answer best fits?</summary>

**Answer:** Port mirroring

Port mirroring is the best match for this situation. SNMP polls counters and receives notifications; v3 supports authentication and privacy. Flow telemetry summarizes conversations, while packet capture provides packet detail. Syslog centralizes events; synchronized time enables correlation. Baselines and thresholds should reflect normal patterns and alert severity.

</details>

<details class="hr-qa" markdown="1">
<summary>A team needs notification when service latency exceeds a threshold — which answer best fits?</summary>

**Answer:** Active monitoring alert

Active monitoring alert is the best match for this situation. SNMP polls counters and receives notifications; v3 supports authentication and privacy. Flow telemetry summarizes conversations, while packet capture provides packet detail. Syslog centralizes events; synchronized time enables correlation. Baselines and thresholds should reflect normal patterns and alert severity.

</details>


### Visual learning

- [Infrastructure — Passive TAP vs Port Mirroring"
](/network-portfolio/study-diagrams/passive-tap-vs-port-mirroring/)
- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)

<a id="objective-3-3"></a>

## 3.3 — Disaster recovery

### Technical distinctions

- **RPO:** Maximum tolerable data loss measured in time.
- **RTO:** Target time to restore a service.
- **Hot site:** Recovery location with ready infrastructure.
- **Cold site:** Recovery location requiring substantial setup.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


RPO is acceptable data loss measured in time; RTO is the target restoration time. Hot sites are more ready than cold sites. Redundancy reduces single points of failure but does not replace backups. Test recovery plans and validate restored services.


### Deep dive — Recovery planning

RPO is tolerable data loss measured in time; RTO is target restoration time. MTTR measures repair/recovery duration; MTBF measures operating time between failures. Hot sites are ready sooner than cold sites. HA reduces interruption but does not replace backups. Test restores and failover.

**Hands-on verification:** Design a recovery exercise with explicit RPO/RTO and verify restored data, not merely backup completion.

**Reference for further study:** NIST SP 800-34.

[Practice this objective](../practice/?objective=3.3) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| RPO | Recovery point objective; tolerable data loss measured in time |
| RTO | Recovery time objective; target restoration duration |
| MTTR | Mean time to repair or restore; average recovery duration |
| MTBF | Mean time between failures; reliability measure |

### Technical quick-reference table

| Metric | Meaning | Example |
| --- | --- | --- |
| RPO | Tolerable data loss in time | 15 minutes |
| RTO | Target restoration time | 2 hours |
| MTTR | Mean time to repair or restore | Track incident duration |
| MTBF | Mean time between failures | Reliability estimate |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>Which metric specifies acceptable data loss in time?</summary>

**Answer:** RPO

RPO is acceptable data loss measured in time; RTO is the target restoration time. Hot sites are more ready than cold sites. Redundancy reduces single points of failure but does not replace backups. Test recovery plans and validate restored services.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: maximum acceptable data loss expressed as time?</summary>

**Answer:** RPO

RPO: Maximum acceptable data loss expressed as time. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: target duration to restore service after disruption?</summary>

**Answer:** RTO

RTO: Target duration to restore service after disruption. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: average operating time between failures for repairable equipment?</summary>

**Answer:** MTBF

MTBF: Average operating time between failures for repairable equipment. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: recovery facility equipped for rapid service resumption?</summary>

**Answer:** Hot site

Hot site: Recovery facility equipped for rapid service resumption. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: standby system takes over when the active system fails?</summary>

**Answer:** Active-passive

Active-passive: Standby system takes over when the active system fails. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Backups run every 15 minutes and service must return within two hours. Which pair describes the targets?</summary>

**Answer:** RPO 15 minutes, RTO 2 hours

RPO is tolerable data loss and RTO is target restoration time; backup frequency alone does not guarantee recovery.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes RTO?</summary>

**Answer:** Target duration to restore service after disruption

RTO refers to target duration to restore service after disruption. The alternatives instead describe RPO, MTBF, Hot site.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes MTBF?</summary>

**Answer:** Average operating time between failures for repairable equipment

MTBF refers to average operating time between failures for repairable equipment. The alternatives instead describe RPO, RTO, Hot site.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Hot site?</summary>

**Answer:** Recovery facility equipped for rapid service resumption

Hot site refers to recovery facility equipped for rapid service resumption. The alternatives instead describe RPO, RTO, MTBF.

</details>

<details class="hr-qa" markdown="1">
<summary>Backups occur every four hours and recovery takes 45 minutes. Which metric describes the potential four-hour data loss window?</summary>

**Answer:** RPO

RPO concerns recoverable data age; RTO concerns restoration time, MTTR repair time and MTBF reliability intervals.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: maximum tolerable data loss measured in time?</summary>

**Answer:** RPO

RPO: Maximum tolerable data loss measured in time; RTO: Target time to restore a service; Hot site: Recovery location with ready infrastructure; Cold site: Recovery location requiring substantial setup.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes RPO from the alternatives?</summary>

**Answer:** Maximum tolerable data loss measured in time

RPO: Maximum tolerable data loss measured in time; RTO: Target time to restore a service; Hot site: Recovery location with ready infrastructure; Cold site: Recovery location requiring substantial setup.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: target time to restore a service?</summary>

**Answer:** RTO

RPO: Maximum tolerable data loss measured in time; RTO: Target time to restore a service; Hot site: Recovery location with ready infrastructure; Cold site: Recovery location requiring substantial setup.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes RTO from the alternatives?</summary>

**Answer:** Target time to restore a service

RPO: Maximum tolerable data loss measured in time; RTO: Target time to restore a service; Hot site: Recovery location with ready infrastructure; Cold site: Recovery location requiring substantial setup.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: recovery location with ready infrastructure?</summary>

**Answer:** Hot site

RPO: Maximum tolerable data loss measured in time; RTO: Target time to restore a service; Hot site: Recovery location with ready infrastructure; Cold site: Recovery location requiring substantial setup.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Hot site from the alternatives?</summary>

**Answer:** Recovery location with ready infrastructure

RPO: Maximum tolerable data loss measured in time; RTO: Target time to restore a service; Hot site: Recovery location with ready infrastructure; Cold site: Recovery location requiring substantial setup.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: recovery location requiring substantial setup?</summary>

**Answer:** Cold site

RPO: Maximum tolerable data loss measured in time; RTO: Target time to restore a service; Hot site: Recovery location with ready infrastructure; Cold site: Recovery location requiring substantial setup.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Cold site from the alternatives?</summary>

**Answer:** Recovery location requiring substantial setup

RPO: Maximum tolerable data loss measured in time; RTO: Target time to restore a service; Hot site: Recovery location with ready infrastructure; Cold site: Recovery location requiring substantial setup.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes RTO for a task that requires: maximum tolerable data loss measured in time. Which alternative is the better match?</summary>

**Answer:** RPO

RPO: Maximum tolerable data loss measured in time; RTO: Target time to restore a service; Hot site: Recovery location with ready infrastructure; Cold site: Recovery location requiring substantial setup.

</details>

<details class="hr-qa" markdown="1">
<summary>A business can lose at most 15 minutes of data — which answer best fits?</summary>

**Answer:** RPO 15 minutes

RPO 15 minutes is the best match for this situation. RPO is tolerable data loss measured in time; RTO is target restoration time. MTTR measures repair/recovery duration; MTBF measures operating time between failures. Hot sites are ready sooner than cold sites. HA reduces interruption but does not replace backups. Test restores and failover.

</details>

<details class="hr-qa" markdown="1">
<summary>A service must resume within two hours — which answer best fits?</summary>

**Answer:** RTO two hours

RTO two hours is the best match for this situation. RPO is tolerable data loss measured in time; RTO is target restoration time. MTTR measures repair/recovery duration; MTBF measures operating time between failures. Hot sites are ready sooner than cold sites. HA reduces interruption but does not replace backups. Test restores and failover.

</details>

<details class="hr-qa" markdown="1">
<summary>A recovery site has equipment running and current data — which answer best fits?</summary>

**Answer:** Hot site

Hot site is the best match for this situation. RPO is tolerable data loss measured in time; RTO is target restoration time. MTTR measures repair/recovery duration; MTBF measures operating time between failures. Hot sites are ready sooner than cold sites. HA reduces interruption but does not replace backups. Test restores and failover.

</details>

<details class="hr-qa" markdown="1">
<summary>A recovery site has space and utilities but no ready systems — which answer best fits?</summary>

**Answer:** Cold site

Cold site is the best match for this situation. RPO is tolerable data loss measured in time; RTO is target restoration time. MTTR measures repair/recovery duration; MTBF measures operating time between failures. Hot sites are ready sooner than cold sites. HA reduces interruption but does not replace backups. Test restores and failover.

</details>

<details class="hr-qa" markdown="1">
<summary>A team needs average time to repair failures — which answer best fits?</summary>

**Answer:** MTTR

MTTR is the best match for this situation. RPO is tolerable data loss measured in time; RTO is target restoration time. MTTR measures repair/recovery duration; MTBF measures operating time between failures. Hot sites are ready sooner than cold sites. HA reduces interruption but does not replace backups. Test restores and failover.

</details>

<details class="hr-qa" markdown="1">
<summary>A team needs average operating interval between failures — which answer best fits?</summary>

**Answer:** MTBF

MTBF is the best match for this situation. RPO is tolerable data loss measured in time; RTO is target restoration time. MTTR measures repair/recovery duration; MTBF measures operating time between failures. Hot sites are ready sooner than cold sites. HA reduces interruption but does not replace backups. Test restores and failover.

</details>

<details class="hr-qa" markdown="1">
<summary>A redundant gateway fails and standby takes over — which answer best fits?</summary>

**Answer:** High availability failover

High availability failover is the best match for this situation. RPO is tolerable data loss measured in time; RTO is target restoration time. MTTR measures repair/recovery duration; MTBF measures operating time between failures. Hot sites are ready sooner than cold sites. HA reduces interruption but does not replace backups. Test restores and failover.

</details>

<details class="hr-qa" markdown="1">
<summary>A backup job reports success; how verify recoverability — which answer best fits?</summary>

**Answer:** Perform test restore

Perform test restore is the best match for this situation. RPO is tolerable data loss measured in time; RTO is target restoration time. MTTR measures repair/recovery duration; MTBF measures operating time between failures. Hot sites are ready sooner than cold sites. HA reduces interruption but does not replace backups. Test restores and failover.

</details>

<details class="hr-qa" markdown="1">
<summary>A regional outage could affect both local copies — which answer best fits?</summary>

**Answer:** Geographically separate recovery resources

Geographically separate recovery resources is the best match for this situation. RPO is tolerable data loss measured in time; RTO is target restoration time. MTTR measures repair/recovery duration; MTBF measures operating time between failures. Hot sites are ready sooner than cold sites. HA reduces interruption but does not replace backups. Test restores and failover.

</details>

<details class="hr-qa" markdown="1">
<summary>A recovery plan must be exercised without disrupting production — which answer best fits?</summary>

**Answer:** Controlled tabletop or isolated test

Controlled tabletop or isolated test is the best match for this situation. RPO is tolerable data loss measured in time; RTO is target restoration time. MTTR measures repair/recovery duration; MTBF measures operating time between failures. Hot sites are ready sooner than cold sites. HA reduces interruption but does not replace backups. Test restores and failover.

</details>


### Visual learning

- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)

<a id="objective-3-4"></a>

## 3.4 — IP services

### Technical distinctions

- **DHCP relay:** Forwards DHCP requests across routed boundaries.
- **AAAA record:** Maps a hostname to an IPv6 address.
- **PTR record:** Supports reverse DNS lookup.
- **Router advertisement:** Communicates IPv6 prefixes and default router information.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


DHCPv4 uses Discover, Offer, Request, Acknowledge. Relays forward requests across routed boundaries. DNS A and AAAA records map names to IPv4 and IPv6; PTR supports reverse lookup. NTP synchronizes clocks. IPv6 SLAAC uses router advertisements.

[Related completed lab](/network-portfolio/labs/module-6-0/lab-6-6-6-use-nslookup/)


### Deep dive — Address and name services

DHCPv4 uses discover, offer, request, acknowledge; relays forward requests across routed boundaries. IPv6 router advertisements supply default-router information and may enable SLAAC; DHCPv6 can supply addresses or other options. DNS A/AAAA map names, PTR reverses, MX directs mail, CNAME aliases. NTP aligns time.

**Hands-on verification:** Inspect ipconfig /all or ip addr, query A/AAAA/MX with nslookup or dig, then compare gateway reachability.

**Reference for further study:** RFC 2131; RFC 4861; RFC 1035.

[Practice this objective](../practice/?objective=3.4) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| DHCP | Dynamic host configuration protocol; distributes addressing settings |
| DORA | Discover offer request acknowledge; typical DHCPv4 initial exchange |
| PTR | Pointer record; reverse DNS mapping |
| MX | Mail exchange record; identifies mail servers |

### Technical quick-reference table

| Service | Evidence | Diagnostic |
| --- | --- | --- |
| DHCP | Lease and options | ipconfig /all |
| DNS | Record and response | nslookup |
| NTP | Clock offset | Check configured peers |
| SLAAC | Router advertisement | Inspect IPv6 configuration |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>Which DNS record maps a hostname to IPv6?</summary>

**Answer:** AAAA

DHCPv4 uses Discover, Offer, Request, Acknowledge. Relays forward requests across routed boundaries. DNS A and AAAA records map names to IPv4 and IPv6; PTR supports reverse lookup. NTP synchronizes clocks. IPv6 SLAAC uses router advertisements.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: forwards client address requests across routed subnet boundaries?</summary>

**Answer:** DHCP relay

DHCP relay: Forwards client address requests across routed subnet boundaries. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: dNS record containing an IPv6 address?</summary>

**Answer:** AAAA

AAAA: DNS record containing an IPv6 address. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: dNS record commonly used for reverse address-to-name lookup?</summary>

**Answer:** PTR

PTR: DNS record commonly used for reverse address-to-name lookup. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: authenticates DNS data origin and integrity through signatures?</summary>

**Answer:** DNSSEC

DNSSEC: Authenticates DNS data origin and integrity through signatures. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: iPv6 host address configuration using router advertisements?</summary>

**Answer:** SLAAC

SLAAC: IPv6 host address configuration using router advertisements. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>A new VLAN has no DHCP leases; the server works for other VLANs and is on another subnet. What should be checked?</summary>

**Answer:** DHCP relay on the new gateway

DHCP broadcasts need a relay to reach a server across a router.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes AAAA?</summary>

**Answer:** DNS record containing an IPv6 address

AAAA refers to dNS record containing an IPv6 address. The alternatives instead describe DHCP relay, PTR, DNSSEC.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes PTR?</summary>

**Answer:** DNS record commonly used for reverse address-to-name lookup

PTR refers to dNS record commonly used for reverse address-to-name lookup. The alternatives instead describe DHCP relay, AAAA, DNSSEC.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes DNSSEC?</summary>

**Answer:** Authenticates DNS data origin and integrity through signatures

DNSSEC refers to authenticates DNS data origin and integrity through signatures. The alternatives instead describe DHCP relay, AAAA, PTR.

</details>

<details class="hr-qa" markdown="1">
<summary>A mail administrator needs DNS to identify the receiving mail servers for a domain. Which record is appropriate?</summary>

**Answer:** MX

MX specifies mail exchangers; PTR supports reverse lookup, AAAA stores IPv6 addresses and CNAME aliases names.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: forwards DHCP requests across routed boundaries?</summary>

**Answer:** DHCP relay

DHCP relay: Forwards DHCP requests across routed boundaries; AAAA record: Maps a hostname to an IPv6 address; PTR record: Supports reverse DNS lookup; Router advertisement: Communicates IPv6 prefixes and default router information.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes DHCP relay from the alternatives?</summary>

**Answer:** Forwards DHCP requests across routed boundaries

DHCP relay: Forwards DHCP requests across routed boundaries; AAAA record: Maps a hostname to an IPv6 address; PTR record: Supports reverse DNS lookup; Router advertisement: Communicates IPv6 prefixes and default router information.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: maps a hostname to an IPv6 address?</summary>

**Answer:** AAAA record

DHCP relay: Forwards DHCP requests across routed boundaries; AAAA record: Maps a hostname to an IPv6 address; PTR record: Supports reverse DNS lookup; Router advertisement: Communicates IPv6 prefixes and default router information.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes AAAA record from the alternatives?</summary>

**Answer:** Maps a hostname to an IPv6 address

DHCP relay: Forwards DHCP requests across routed boundaries; AAAA record: Maps a hostname to an IPv6 address; PTR record: Supports reverse DNS lookup; Router advertisement: Communicates IPv6 prefixes and default router information.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: supports reverse DNS lookup?</summary>

**Answer:** PTR record

DHCP relay: Forwards DHCP requests across routed boundaries; AAAA record: Maps a hostname to an IPv6 address; PTR record: Supports reverse DNS lookup; Router advertisement: Communicates IPv6 prefixes and default router information.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes PTR record from the alternatives?</summary>

**Answer:** Supports reverse DNS lookup

DHCP relay: Forwards DHCP requests across routed boundaries; AAAA record: Maps a hostname to an IPv6 address; PTR record: Supports reverse DNS lookup; Router advertisement: Communicates IPv6 prefixes and default router information.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: communicates IPv6 prefixes and default router information?</summary>

**Answer:** Router advertisement

DHCP relay: Forwards DHCP requests across routed boundaries; AAAA record: Maps a hostname to an IPv6 address; PTR record: Supports reverse DNS lookup; Router advertisement: Communicates IPv6 prefixes and default router information.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Router advertisement from the alternatives?</summary>

**Answer:** Communicates IPv6 prefixes and default router information

DHCP relay: Forwards DHCP requests across routed boundaries; AAAA record: Maps a hostname to an IPv6 address; PTR record: Supports reverse DNS lookup; Router advertisement: Communicates IPv6 prefixes and default router information.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes AAAA record for a task that requires: forwards DHCP requests across routed boundaries. Which alternative is the better match?</summary>

**Answer:** DHCP relay

DHCP relay: Forwards DHCP requests across routed boundaries; AAAA record: Maps a hostname to an IPv6 address; PTR record: Supports reverse DNS lookup; Router advertisement: Communicates IPv6 prefixes and default router information.

</details>

<details class="hr-qa" markdown="1">
<summary>A DHCP client broadcasts its first message — which answer best fits?</summary>

**Answer:** Discover

Discover is the best match for this situation. DHCPv4 uses discover, offer, request, acknowledge; relays forward requests across routed boundaries. IPv6 router advertisements supply default-router information and may enable SLAAC; DHCPv6 can supply addresses or other options. DNS A/AAAA map names, PTR reverses, MX directs mail, CNAME aliases. NTP aligns time.

</details>

<details class="hr-qa" markdown="1">
<summary>A DHCP server proposes an address — which answer best fits?</summary>

**Answer:** Offer

Offer is the best match for this situation. DHCPv4 uses discover, offer, request, acknowledge; relays forward requests across routed boundaries. IPv6 router advertisements supply default-router information and may enable SLAAC; DHCPv6 can supply addresses or other options. DNS A/AAAA map names, PTR reverses, MX directs mail, CNAME aliases. NTP aligns time.

</details>

<details class="hr-qa" markdown="1">
<summary>A client selects an offered lease — which answer best fits?</summary>

**Answer:** Request

Request is the best match for this situation. DHCPv4 uses discover, offer, request, acknowledge; relays forward requests across routed boundaries. IPv6 router advertisements supply default-router information and may enable SLAAC; DHCPv6 can supply addresses or other options. DNS A/AAAA map names, PTR reverses, MX directs mail, CNAME aliases. NTP aligns time.

</details>

<details class="hr-qa" markdown="1">
<summary>A server confirms a lease — which answer best fits?</summary>

**Answer:** ACK

ACK is the best match for this situation. DHCPv4 uses discover, offer, request, acknowledge; relays forward requests across routed boundaries. IPv6 router advertisements supply default-router information and may enable SLAAC; DHCPv6 can supply addresses or other options. DNS A/AAAA map names, PTR reverses, MX directs mail, CNAME aliases. NTP aligns time.

</details>

<details class="hr-qa" markdown="1">
<summary>A DHCP server is on another routed subnet — which answer best fits?</summary>

**Answer:** DHCP relay

DHCP relay is the best match for this situation. DHCPv4 uses discover, offer, request, acknowledge; relays forward requests across routed boundaries. IPv6 router advertisements supply default-router information and may enable SLAAC; DHCPv6 can supply addresses or other options. DNS A/AAAA map names, PTR reverses, MX directs mail, CNAME aliases. NTP aligns time.

</details>

<details class="hr-qa" markdown="1">
<summary>A DNS record maps a name to IPv6 — which answer best fits?</summary>

**Answer:** AAAA

AAAA is the best match for this situation. DHCPv4 uses discover, offer, request, acknowledge; relays forward requests across routed boundaries. IPv6 router advertisements supply default-router information and may enable SLAAC; DHCPv6 can supply addresses or other options. DNS A/AAAA map names, PTR reverses, MX directs mail, CNAME aliases. NTP aligns time.

</details>

<details class="hr-qa" markdown="1">
<summary>A DNS record identifies mail exchangers — which answer best fits?</summary>

**Answer:** MX

MX is the best match for this situation. DHCPv4 uses discover, offer, request, acknowledge; relays forward requests across routed boundaries. IPv6 router advertisements supply default-router information and may enable SLAAC; DHCPv6 can supply addresses or other options. DNS A/AAAA map names, PTR reverses, MX directs mail, CNAME aliases. NTP aligns time.

</details>

<details class="hr-qa" markdown="1">
<summary>A reverse lookup needs a name for an IP — which answer best fits?</summary>

**Answer:** PTR

PTR is the best match for this situation. DHCPv4 uses discover, offer, request, acknowledge; relays forward requests across routed boundaries. IPv6 router advertisements supply default-router information and may enable SLAAC; DHCPv6 can supply addresses or other options. DNS A/AAAA map names, PTR reverses, MX directs mail, CNAME aliases. NTP aligns time.

</details>

<details class="hr-qa" markdown="1">
<summary>An IPv6 host learns its default router — which answer best fits?</summary>

**Answer:** Router advertisement

Router advertisement is the best match for this situation. DHCPv4 uses discover, offer, request, acknowledge; relays forward requests across routed boundaries. IPv6 router advertisements supply default-router information and may enable SLAAC; DHCPv6 can supply addresses or other options. DNS A/AAAA map names, PTR reverses, MX directs mail, CNAME aliases. NTP aligns time.

</details>

<details class="hr-qa" markdown="1">
<summary>A host forms its own IPv6 address from advertised prefix — which answer best fits?</summary>

**Answer:** SLAAC

SLAAC is the best match for this situation. DHCPv4 uses discover, offer, request, acknowledge; relays forward requests across routed boundaries. IPv6 router advertisements supply default-router information and may enable SLAAC; DHCPv6 can supply addresses or other options. DNS A/AAAA map names, PTR reverses, MX directs mail, CNAME aliases. NTP aligns time.

</details>


### Visual learning

- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)

<a id="objective-3-5"></a>

## 3.5 — Access and management

### Technical distinctions

- **SSH:** Encrypted command-line remote administration.
- **Console:** Local management independent of production IP connectivity.
- **API:** Programmatic access to management functions.
- **Jump host:** Controlled intermediary for administrative access.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


SSH protects remote CLI sessions; HTTPS protects web management. Out-of-band management uses a separate access path. VPNs provide protected tunnels; split tunneling routes only selected traffic through them. Restrict management access to authorized networks.

[Related completed lab](/network-portfolio/videos/17-40-configure-secure-passwords-and-ssh/)


### Deep dive — Management paths

In-band management shares production connectivity; out-of-band uses a separate path such as console or dedicated management network. SSH protects CLI traffic; HTTPS protects web administration. APIs enable automation but require scoped credentials and audit. Console access is useful when IP configuration is broken.

**Hands-on verification:** Compare console, SSH and web access; verify management ACLs and retain a recovery path before changes.

**Reference for further study:** RFC 4251.

[Practice this objective](../practice/?objective=3.5) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| VPN | Virtual private network; protected logical connectivity |
| OOB | Out of band; separate management path |
| API | Application programming interface; programmatic interaction |
| CLI | Command line interface; text-based management |

### Technical quick-reference table

| Method | Purpose | Risk control |
| --- | --- | --- |
| SSH | Encrypted CLI | Key or strong authentication |
| HTTPS | Web management | Validate certificate |
| Console | Local access | Physical security |
| Out-of-band | Separate management path | Restrict access |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>Which approach allows management when the production network is down?</summary>

**Answer:** Out-of-band management

SSH protects remote CLI sessions; HTTPS protects web management. Out-of-band management uses a separate access path. VPNs provide protected tunnels; split tunneling routes only selected traffic through them. Restrict management access to authorized networks.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: separate management path independent of the production forwarding network?</summary>

**Answer:** Out-of-band management

Out-of-band management: Separate management path independent of the production forwarding network. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: controlled intermediary for administrative connections?</summary>

**Answer:** Jump host

Jump host: Controlled intermediary for administrative connections. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: only selected traffic traverses the remote access VPN?</summary>

**Answer:** Split tunnel

Split tunnel: Only selected traffic traverses the remote access VPN. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: encrypted connection between network gateways?</summary>

**Answer:** Site-to-site VPN

Site-to-site VPN: Encrypted connection between network gateways. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: direct local device management independent of configured IP reachability?</summary>

**Answer:** Console

Console: Direct local device management independent of configured IP reachability. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>A routing change disconnects production management access. Which previously provisioned path is most useful?</summary>

**Answer:** Independent out-of-band console network

An independent management path avoids reliance on the failed production route.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Jump host?</summary>

**Answer:** Controlled intermediary for administrative connections

Jump host refers to controlled intermediary for administrative connections. The alternatives instead describe Out-of-band management, Split tunnel, Site-to-site VPN.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Split tunnel?</summary>

**Answer:** Only selected traffic traverses the remote access VPN

Split tunnel refers to only selected traffic traverses the remote access VPN. The alternatives instead describe Out-of-band management, Jump host, Site-to-site VPN.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Site-to-site VPN?</summary>

**Answer:** Encrypted connection between network gateways

Site-to-site VPN refers to encrypted connection between network gateways. The alternatives instead describe Out-of-band management, Jump host, Split tunnel.

</details>

<details class="hr-qa" markdown="1">
<summary>A router loses its production network connection but its console server is reachable on a separate management network. Which method is this?</summary>

**Answer:** Out-of-band management

The separate management path is out-of-band; in-band shares production connectivity, split tunneling selects VPN routes and mirroring copies traffic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: encrypted command-line remote administration?</summary>

**Answer:** SSH

SSH: Encrypted command-line remote administration; Console: Local management independent of production IP connectivity; API: Programmatic access to management functions; Jump host: Controlled intermediary for administrative access.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes SSH from the alternatives?</summary>

**Answer:** Encrypted command-line remote administration

SSH: Encrypted command-line remote administration; Console: Local management independent of production IP connectivity; API: Programmatic access to management functions; Jump host: Controlled intermediary for administrative access.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: local management independent of production IP connectivity?</summary>

**Answer:** Console

SSH: Encrypted command-line remote administration; Console: Local management independent of production IP connectivity; API: Programmatic access to management functions; Jump host: Controlled intermediary for administrative access.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Console from the alternatives?</summary>

**Answer:** Local management independent of production IP connectivity

SSH: Encrypted command-line remote administration; Console: Local management independent of production IP connectivity; API: Programmatic access to management functions; Jump host: Controlled intermediary for administrative access.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: programmatic access to management functions?</summary>

**Answer:** API

SSH: Encrypted command-line remote administration; Console: Local management independent of production IP connectivity; API: Programmatic access to management functions; Jump host: Controlled intermediary for administrative access.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes API from the alternatives?</summary>

**Answer:** Programmatic access to management functions

SSH: Encrypted command-line remote administration; Console: Local management independent of production IP connectivity; API: Programmatic access to management functions; Jump host: Controlled intermediary for administrative access.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: controlled intermediary for administrative access?</summary>

**Answer:** Jump host

SSH: Encrypted command-line remote administration; Console: Local management independent of production IP connectivity; API: Programmatic access to management functions; Jump host: Controlled intermediary for administrative access.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Jump host from the alternatives?</summary>

**Answer:** Controlled intermediary for administrative access

SSH: Encrypted command-line remote administration; Console: Local management independent of production IP connectivity; API: Programmatic access to management functions; Jump host: Controlled intermediary for administrative access.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes Console for a task that requires: encrypted command-line remote administration. Which alternative is the better match?</summary>

**Answer:** SSH

SSH: Encrypted command-line remote administration; Console: Local management independent of production IP connectivity; API: Programmatic access to management functions; Jump host: Controlled intermediary for administrative access.

</details>

<details class="hr-qa" markdown="1">
<summary>A router loses all IP connectivity but is physically accessible — which answer best fits?</summary>

**Answer:** Console

Console is the best match for this situation. In-band management shares production connectivity; out-of-band uses a separate path such as console or dedicated management network. SSH protects CLI traffic; HTTPS protects web administration. APIs enable automation but require scoped credentials and audit. Console access is useful when IP configuration is broken.

</details>

<details class="hr-qa" markdown="1">
<summary>A remote management path must survive production routing failure — which answer best fits?</summary>

**Answer:** Out-of-band management

Out-of-band management is the best match for this situation. In-band management shares production connectivity; out-of-band uses a separate path such as console or dedicated management network. SSH protects CLI traffic; HTTPS protects web administration. APIs enable automation but require scoped credentials and audit. Console access is useful when IP configuration is broken.

</details>

<details class="hr-qa" markdown="1">
<summary>A CLI session requires encryption — which answer best fits?</summary>

**Answer:** SSH

SSH is the best match for this situation. In-band management shares production connectivity; out-of-band uses a separate path such as console or dedicated management network. SSH protects CLI traffic; HTTPS protects web administration. APIs enable automation but require scoped credentials and audit. Console access is useful when IP configuration is broken.

</details>

<details class="hr-qa" markdown="1">
<summary>A web management session requires TLS — which answer best fits?</summary>

**Answer:** HTTPS

HTTPS is the best match for this situation. In-band management shares production connectivity; out-of-band uses a separate path such as console or dedicated management network. SSH protects CLI traffic; HTTPS protects web administration. APIs enable automation but require scoped credentials and audit. Console access is useful when IP configuration is broken.

</details>

<details class="hr-qa" markdown="1">
<summary>An automation tool needs limited programmatic access — which answer best fits?</summary>

**Answer:** Scoped API credentials

Scoped API credentials is the best match for this situation. In-band management shares production connectivity; out-of-band uses a separate path such as console or dedicated management network. SSH protects CLI traffic; HTTPS protects web administration. APIs enable automation but require scoped credentials and audit. Console access is useful when IP configuration is broken.

</details>

<details class="hr-qa" markdown="1">
<summary>A management interface shares production network — which answer best fits?</summary>

**Answer:** In-band management

In-band management is the best match for this situation. In-band management shares production connectivity; out-of-band uses a separate path such as console or dedicated management network. SSH protects CLI traffic; HTTPS protects web administration. APIs enable automation but require scoped credentials and audit. Console access is useful when IP configuration is broken.

</details>

<details class="hr-qa" markdown="1">
<summary>A technician needs remote access to a serial console — which answer best fits?</summary>

**Answer:** Console server

Console server is the best match for this situation. In-band management shares production connectivity; out-of-band uses a separate path such as console or dedicated management network. SSH protects CLI traffic; HTTPS protects web administration. APIs enable automation but require scoped credentials and audit. Console access is useful when IP configuration is broken.

</details>

<details class="hr-qa" markdown="1">
<summary>A device must be configured centrally using structured requests — which answer best fits?</summary>

**Answer:** Management API

Management API is the best match for this situation. In-band management shares production connectivity; out-of-band uses a separate path such as console or dedicated management network. SSH protects CLI traffic; HTTPS protects web administration. APIs enable automation but require scoped credentials and audit. Console access is useful when IP configuration is broken.

</details>

<details class="hr-qa" markdown="1">
<summary>An administrator should access devices only from approved management subnet — which answer best fits?</summary>

**Answer:** Management ACL

Management ACL is the best match for this situation. In-band management shares production connectivity; out-of-band uses a separate path such as console or dedicated management network. SSH protects CLI traffic; HTTPS protects web administration. APIs enable automation but require scoped credentials and audit. Console access is useful when IP configuration is broken.

</details>

<details class="hr-qa" markdown="1">
<summary>A configuration change risks locking out remote access — which answer best fits?</summary>

**Answer:** Verify alternate console path first

Verify alternate console path first is the best match for this situation. In-band management shares production connectivity; out-of-band uses a separate path such as console or dedicated management network. SSH protects CLI traffic; HTTPS protects web administration. APIs enable automation but require scoped credentials and audit. Console access is useful when IP configuration is broken.

</details>


### Visual learning

- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)

<a id="objective-4-1"></a>

## 4.1 — Security concepts

### Technical distinctions

- **Least privilege:** Grants only permissions needed for a task.
- **MFA:** Requires authentication factors from different categories.
- **PKI:** Uses certificates and trust chains to bind identities to keys.
- **Encryption:** Protects confidentiality of data using cryptographic keys.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


Confidentiality prevents unauthorized disclosure; integrity protects correctness; availability keeps services usable. Authentication establishes identity, authorization grants access, accounting records activity. PKI binds identities to public keys using certificates. Least privilege limits access.


### Deep dive — Security foundations

Confidentiality limits disclosure, integrity protects against unauthorized modification, availability supports access. Authentication verifies identity, authorization grants permissions, accounting records activity. PKI binds identities to public keys through certificates. Segmentation and least privilege reduce exposure; physical controls and data classification complement logical controls.

**Hands-on verification:** Map a management login to authentication, authorization and accounting; inspect certificate hostname, issuer and expiry.

**Reference for further study:** NIST SP 800-207.

[Practice this objective](../practice/?objective=4.1) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| AAA | Authentication authorization accounting; identity, permissions and activity records |
| MFA | Multifactor authentication; distinct factor types |
| PKI | Public key infrastructure; certificate trust and management |
| CIA | Confidentiality integrity availability; security objectives |

### Technical quick-reference table

| Principle | Meaning | Example |
| --- | --- | --- |
| Confidentiality | Limit disclosure | Encryption |
| Integrity | Detect unauthorized changes | Authenticated hashes |
| Availability | Maintain access | Redundancy |
| Least privilege | Minimum permissions | Restricted admin roles |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>Which AAA function determines permitted actions?</summary>

**Answer:** Authorization

Confidentiality prevents unauthorized disclosure; integrity protects correctness; availability keeps services usable. Authentication establishes identity, authorization grants access, accounting records activity. PKI binds identities to public keys using certificates. Least privilege limits access.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: grant only permissions needed for a task?</summary>

**Answer:** Least privilege

Least privilege: Grant only permissions needed for a task. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: authentication using distinct factor categories?</summary>

**Answer:** MFA

MFA: Authentication using distinct factor categories. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: centralized AAA commonly used for network device administration?</summary>

**Answer:** TACACS+

TACACS+: Centralized AAA commonly used for network device administration. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: decoy resource intended to attract and observe suspicious activity?</summary>

**Answer:** Honeypot

Honeypot: Decoy resource intended to attract and observe suspicious activity. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: protection against unauthorized modification?</summary>

**Answer:** Integrity

Integrity: Protection against unauthorized modification. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>A technician needs read-only monitoring but no configuration privileges. Which principle guides the access grant?</summary>

**Answer:** Least privilege

Grant only the permissions necessary for monitoring.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes MFA?</summary>

**Answer:** Authentication using distinct factor categories

MFA refers to authentication using distinct factor categories. The alternatives instead describe Least privilege, TACACS+, Honeypot.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes TACACS+?</summary>

**Answer:** Centralized AAA commonly used for network device administration

TACACS+ refers to centralized AAA commonly used for network device administration. The alternatives instead describe Least privilege, MFA, Honeypot.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Honeypot?</summary>

**Answer:** Decoy resource intended to attract and observe suspicious activity

Honeypot refers to decoy resource intended to attract and observe suspicious activity. The alternatives instead describe Least privilege, MFA, TACACS+.

</details>

<details class="hr-qa" markdown="1">
<summary>A help desk employee should reset passwords but not modify firewall policies. Which principle directly limits permissions?</summary>

**Answer:** Least privilege

Least privilege limits access to required duties; locality concerns data location, availability service access and geofencing geographic conditions.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: grants only permissions needed for a task?</summary>

**Answer:** Least privilege

Least privilege: Grants only permissions needed for a task; MFA: Requires authentication factors from different categories; PKI: Uses certificates and trust chains to bind identities to keys; Encryption: Protects confidentiality of data using cryptographic keys.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Least privilege from the alternatives?</summary>

**Answer:** Grants only permissions needed for a task

Least privilege: Grants only permissions needed for a task; MFA: Requires authentication factors from different categories; PKI: Uses certificates and trust chains to bind identities to keys; Encryption: Protects confidentiality of data using cryptographic keys.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: requires authentication factors from different categories?</summary>

**Answer:** MFA

Least privilege: Grants only permissions needed for a task; MFA: Requires authentication factors from different categories; PKI: Uses certificates and trust chains to bind identities to keys; Encryption: Protects confidentiality of data using cryptographic keys.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes MFA from the alternatives?</summary>

**Answer:** Requires authentication factors from different categories

Least privilege: Grants only permissions needed for a task; MFA: Requires authentication factors from different categories; PKI: Uses certificates and trust chains to bind identities to keys; Encryption: Protects confidentiality of data using cryptographic keys.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: uses certificates and trust chains to bind identities to keys?</summary>

**Answer:** PKI

Least privilege: Grants only permissions needed for a task; MFA: Requires authentication factors from different categories; PKI: Uses certificates and trust chains to bind identities to keys; Encryption: Protects confidentiality of data using cryptographic keys.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes PKI from the alternatives?</summary>

**Answer:** Uses certificates and trust chains to bind identities to keys

Least privilege: Grants only permissions needed for a task; MFA: Requires authentication factors from different categories; PKI: Uses certificates and trust chains to bind identities to keys; Encryption: Protects confidentiality of data using cryptographic keys.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: protects confidentiality of data using cryptographic keys?</summary>

**Answer:** Encryption

Least privilege: Grants only permissions needed for a task; MFA: Requires authentication factors from different categories; PKI: Uses certificates and trust chains to bind identities to keys; Encryption: Protects confidentiality of data using cryptographic keys.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Encryption from the alternatives?</summary>

**Answer:** Protects confidentiality of data using cryptographic keys

Least privilege: Grants only permissions needed for a task; MFA: Requires authentication factors from different categories; PKI: Uses certificates and trust chains to bind identities to keys; Encryption: Protects confidentiality of data using cryptographic keys.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes MFA for a task that requires: grants only permissions needed for a task. Which alternative is the better match?</summary>

**Answer:** Least privilege

Least privilege: Grants only permissions needed for a task; MFA: Requires authentication factors from different categories; PKI: Uses certificates and trust chains to bind identities to keys; Encryption: Protects confidentiality of data using cryptographic keys.

</details>

<details class="hr-qa" markdown="1">
<summary>An encrypted tunnel prevents passive reading — which answer best fits?</summary>

**Answer:** Confidentiality

Confidentiality is the best match for this situation. Confidentiality limits disclosure, integrity protects against unauthorized modification, availability supports access. Authentication verifies identity, authorization grants permissions, accounting records activity. PKI binds identities to public keys through certificates. Segmentation and least privilege reduce exposure; physical controls and data classification complement logical controls.

</details>

<details class="hr-qa" markdown="1">
<summary>A signed configuration detects unauthorized changes — which answer best fits?</summary>

**Answer:** Integrity

Integrity is the best match for this situation. Confidentiality limits disclosure, integrity protects against unauthorized modification, availability supports access. Authentication verifies identity, authorization grants permissions, accounting records activity. PKI binds identities to public keys through certificates. Segmentation and least privilege reduce exposure; physical controls and data classification complement logical controls.

</details>

<details class="hr-qa" markdown="1">
<summary>Redundant infrastructure keeps a service reachable — which answer best fits?</summary>

**Answer:** Availability

Availability is the best match for this situation. Confidentiality limits disclosure, integrity protects against unauthorized modification, availability supports access. Authentication verifies identity, authorization grants permissions, accounting records activity. PKI binds identities to public keys through certificates. Segmentation and least privilege reduce exposure; physical controls and data classification complement logical controls.

</details>

<details class="hr-qa" markdown="1">
<summary>A login verifies a claimed identity — which answer best fits?</summary>

**Answer:** Authentication

Authentication is the best match for this situation. Confidentiality limits disclosure, integrity protects against unauthorized modification, availability supports access. Authentication verifies identity, authorization grants permissions, accounting records activity. PKI binds identities to public keys through certificates. Segmentation and least privilege reduce exposure; physical controls and data classification complement logical controls.

</details>

<details class="hr-qa" markdown="1">
<summary>A policy grants read-only access to a verified user — which answer best fits?</summary>

**Answer:** Authorization

Authorization is the best match for this situation. Confidentiality limits disclosure, integrity protects against unauthorized modification, availability supports access. Authentication verifies identity, authorization grants permissions, accounting records activity. PKI binds identities to public keys through certificates. Segmentation and least privilege reduce exposure; physical controls and data classification complement logical controls.

</details>

<details class="hr-qa" markdown="1">
<summary>A log records which administrator changed a setting — which answer best fits?</summary>

**Answer:** Accounting

Accounting is the best match for this situation. Confidentiality limits disclosure, integrity protects against unauthorized modification, availability supports access. Authentication verifies identity, authorization grants permissions, accounting records activity. PKI binds identities to public keys through certificates. Segmentation and least privilege reduce exposure; physical controls and data classification complement logical controls.

</details>

<details class="hr-qa" markdown="1">
<summary>A user supplies password and hardware security key — which answer best fits?</summary>

**Answer:** Multifactor authentication

Multifactor authentication is the best match for this situation. Confidentiality limits disclosure, integrity protects against unauthorized modification, availability supports access. Authentication verifies identity, authorization grants permissions, accounting records activity. PKI binds identities to public keys through certificates. Segmentation and least privilege reduce exposure; physical controls and data classification complement logical controls.

</details>

<details class="hr-qa" markdown="1">
<summary>A certificate binds a public key to a named service — which answer best fits?</summary>

**Answer:** PKI

PKI is the best match for this situation. Confidentiality limits disclosure, integrity protects against unauthorized modification, availability supports access. Authentication verifies identity, authorization grants permissions, accounting records activity. PKI binds identities to public keys through certificates. Segmentation and least privilege reduce exposure; physical controls and data classification complement logical controls.

</details>

<details class="hr-qa" markdown="1">
<summary>A contractor needs only one application for a week — which answer best fits?</summary>

**Answer:** Least privilege with time-limited access

Least privilege with time-limited access is the best match for this situation. Confidentiality limits disclosure, integrity protects against unauthorized modification, availability supports access. Authentication verifies identity, authorization grants permissions, accounting records activity. PKI binds identities to public keys through certificates. Segmentation and least privilege reduce exposure; physical controls and data classification complement logical controls.

</details>

<details class="hr-qa" markdown="1">
<summary>A business labels records according to sensitivity — which answer best fits?</summary>

**Answer:** Data classification

Data classification is the best match for this situation. Confidentiality limits disclosure, integrity protects against unauthorized modification, availability supports access. Authentication verifies identity, authorization grants permissions, accounting records activity. PKI binds identities to public keys through certificates. Segmentation and least privilege reduce exposure; physical controls and data classification complement logical controls.

</details>


### Visual learning

- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)

<a id="objective-4-2"></a>

## 4.2 — Network attacks

### Technical distinctions

- **ARP poisoning:** Falsifies IPv4 neighbor mappings.
- **Rogue DHCP:** Supplies unauthorized client network settings.
- **Evil twin:** Imitates a legitimate wireless access point.
- **DDoS:** Overwhelms resources using distributed traffic sources.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


ARP spoofing can redirect local traffic; rogue DHCP can supply false settings; DNS poisoning corrupts name resolution. DDoS exhausts resources; social engineering targets people. Investigate anomalies with logs and packet evidence; use segmentation and validated controls.


### Deep dive — Attack recognition

Spoofing falsifies identity information; ARP poisoning can redirect local IPv4 traffic. Rogue DHCP may supply malicious gateway or DNS settings. Evil twin APs imitate trusted Wi-Fi. DoS exhausts resources; DDoS uses distributed sources. Social engineering targets human decisions. VLAN hopping crosses intended layer-2 boundaries. Validate evidence before attribution.

**Hands-on verification:** In an isolated lab, compare legitimate ARP and DHCP messages with a prepared anomalous capture; do not attack production systems.

**Reference for further study:** NIST SP 800-61.

[Practice this objective](../practice/?objective=4.2) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| DoS | Denial of service; disrupts availability |
| DDoS | Distributed denial of service; multiple sources |
| ARP | Address resolution protocol; IPv4 link-layer mapping, susceptible to spoofing |
| MITM | Man in the middle; interception or alteration of communications |

### Technical quick-reference table

| Attack | Observable symptom | Defense |
| --- | --- | --- |
| ARP spoofing | Unexpected MAC mapping | Dynamic ARP inspection |
| Rogue DHCP | Incorrect gateway or DNS | DHCP snooping |
| VLAN hopping | Unauthorized VLAN access | Disable dynamic trunking |
| DoS | Resource exhaustion | Rate limiting and upstream mitigation |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>Which attack associates a gateway IP with an unauthorized MAC address?</summary>

**Answer:** ARP spoofing

ARP spoofing can redirect local traffic; rogue DHCP can supply false settings; DNS poisoning corrupts name resolution. DDoS exhausts resources; social engineering targets people. Investigate anomalies with logs and packet evidence; use segmentation and validated controls.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: unauthorized service distributes incorrect client network settings?</summary>

**Answer:** Rogue DHCP

Rogue DHCP: Unauthorized service distributes incorrect client network settings. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: impersonating a legitimate wireless network to attract clients?</summary>

**Answer:** Evil twin

Evil twin: Impersonating a legitimate wireless network to attract clients. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: false address mappings redirect local IPv4 traffic?</summary>

**Answer:** ARP poisoning

ARP poisoning: False address mappings redirect local IPv4 traffic. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: excessive learned source addresses exhaust switch forwarding table capacity?</summary>

**Answer:** MAC flooding

MAC flooding: Excessive learned source addresses exhaust switch forwarding table capacity. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: distributed sources overwhelm a service or network resource?</summary>

**Answer:** DDoS

DDoS: Distributed sources overwhelm a service or network resource. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Clients suddenly receive a wrong default gateway from an unexpected DHCP server. What is the likely cause?</summary>

**Answer:** Rogue DHCP service

An unauthorized DHCP server can supply incorrect gateway and DNS options.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Evil twin?</summary>

**Answer:** Impersonating a legitimate wireless network to attract clients

Evil twin refers to impersonating a legitimate wireless network to attract clients. The alternatives instead describe Rogue DHCP, ARP poisoning, MAC flooding.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes ARP poisoning?</summary>

**Answer:** False address mappings redirect local IPv4 traffic

ARP poisoning refers to false address mappings redirect local IPv4 traffic. The alternatives instead describe Rogue DHCP, Evil twin, MAC flooding.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes MAC flooding?</summary>

**Answer:** Excessive learned source addresses exhaust switch forwarding table capacity

MAC flooding refers to excessive learned source addresses exhaust switch forwarding table capacity. The alternatives instead describe Rogue DHCP, Evil twin, ARP poisoning.

</details>

<details class="hr-qa" markdown="1">
<summary>A workstation receives false gateway MAC mappings from another LAN host. Which attack best explains this?</summary>

**Answer:** ARP poisoning

ARP poisoning falsifies IPv4-to-MAC mappings; the alternatives target DNS data, radio availability or credentials.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: falsifies IPv4 neighbor mappings?</summary>

**Answer:** ARP poisoning

ARP poisoning: Falsifies IPv4 neighbor mappings; Rogue DHCP: Supplies unauthorized client network settings; Evil twin: Imitates a legitimate wireless access point; DDoS: Overwhelms resources using distributed traffic sources.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes ARP poisoning from the alternatives?</summary>

**Answer:** Falsifies IPv4 neighbor mappings

ARP poisoning: Falsifies IPv4 neighbor mappings; Rogue DHCP: Supplies unauthorized client network settings; Evil twin: Imitates a legitimate wireless access point; DDoS: Overwhelms resources using distributed traffic sources.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: supplies unauthorized client network settings?</summary>

**Answer:** Rogue DHCP

ARP poisoning: Falsifies IPv4 neighbor mappings; Rogue DHCP: Supplies unauthorized client network settings; Evil twin: Imitates a legitimate wireless access point; DDoS: Overwhelms resources using distributed traffic sources.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Rogue DHCP from the alternatives?</summary>

**Answer:** Supplies unauthorized client network settings

ARP poisoning: Falsifies IPv4 neighbor mappings; Rogue DHCP: Supplies unauthorized client network settings; Evil twin: Imitates a legitimate wireless access point; DDoS: Overwhelms resources using distributed traffic sources.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: imitates a legitimate wireless access point?</summary>

**Answer:** Evil twin

ARP poisoning: Falsifies IPv4 neighbor mappings; Rogue DHCP: Supplies unauthorized client network settings; Evil twin: Imitates a legitimate wireless access point; DDoS: Overwhelms resources using distributed traffic sources.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Evil twin from the alternatives?</summary>

**Answer:** Imitates a legitimate wireless access point

ARP poisoning: Falsifies IPv4 neighbor mappings; Rogue DHCP: Supplies unauthorized client network settings; Evil twin: Imitates a legitimate wireless access point; DDoS: Overwhelms resources using distributed traffic sources.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: overwhelms resources using distributed traffic sources?</summary>

**Answer:** DDoS

ARP poisoning: Falsifies IPv4 neighbor mappings; Rogue DHCP: Supplies unauthorized client network settings; Evil twin: Imitates a legitimate wireless access point; DDoS: Overwhelms resources using distributed traffic sources.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes DDoS from the alternatives?</summary>

**Answer:** Overwhelms resources using distributed traffic sources

ARP poisoning: Falsifies IPv4 neighbor mappings; Rogue DHCP: Supplies unauthorized client network settings; Evil twin: Imitates a legitimate wireless access point; DDoS: Overwhelms resources using distributed traffic sources.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes Rogue DHCP for a task that requires: falsifies IPv4 neighbor mappings. Which alternative is the better match?</summary>

**Answer:** ARP poisoning

ARP poisoning: Falsifies IPv4 neighbor mappings; Rogue DHCP: Supplies unauthorized client network settings; Evil twin: Imitates a legitimate wireless access point; DDoS: Overwhelms resources using distributed traffic sources.

</details>

<details class="hr-qa" markdown="1">
<summary>Clients receive an unexpected gateway from an unauthorized DHCP server — which answer best fits?</summary>

**Answer:** Rogue DHCP

Rogue DHCP is the best match for this situation. Spoofing falsifies identity information; ARP poisoning can redirect local IPv4 traffic. Rogue DHCP may supply malicious gateway or DNS settings. Evil twin APs imitate trusted Wi-Fi. DoS exhausts resources; DDoS uses distributed sources. Social engineering targets human decisions. VLAN hopping crosses intended layer-2 boundaries. Validate evidence before attribution.

</details>

<details class="hr-qa" markdown="1">
<summary>An attacker associates the gateway IP with an incorrect MAC in client caches — which answer best fits?</summary>

**Answer:** ARP poisoning

ARP poisoning is the best match for this situation. Spoofing falsifies identity information; ARP poisoning can redirect local IPv4 traffic. Rogue DHCP may supply malicious gateway or DNS settings. Evil twin APs imitate trusted Wi-Fi. DoS exhausts resources; DDoS uses distributed sources. Social engineering targets human decisions. VLAN hopping crosses intended layer-2 boundaries. Validate evidence before attribution.

</details>

<details class="hr-qa" markdown="1">
<summary>An unauthorized AP imitates a trusted SSID to attract users — which answer best fits?</summary>

**Answer:** Evil twin

Evil twin is the best match for this situation. Spoofing falsifies identity information; ARP poisoning can redirect local IPv4 traffic. Rogue DHCP may supply malicious gateway or DNS settings. Evil twin APs imitate trusted Wi-Fi. DoS exhausts resources; DDoS uses distributed sources. Social engineering targets human decisions. VLAN hopping crosses intended layer-2 boundaries. Validate evidence before attribution.

</details>

<details class="hr-qa" markdown="1">
<summary>Many distributed sources flood a public service — which answer best fits?</summary>

**Answer:** DDoS

DDoS is the best match for this situation. Spoofing falsifies identity information; ARP poisoning can redirect local IPv4 traffic. Rogue DHCP may supply malicious gateway or DNS settings. Evil twin APs imitate trusted Wi-Fi. DoS exhausts resources; DDoS uses distributed sources. Social engineering targets human decisions. VLAN hopping crosses intended layer-2 boundaries. Validate evidence before attribution.

</details>

<details class="hr-qa" markdown="1">
<summary>An email impersonates IT to request passwords — which answer best fits?</summary>

**Answer:** Phishing

Phishing is the best match for this situation. Spoofing falsifies identity information; ARP poisoning can redirect local IPv4 traffic. Rogue DHCP may supply malicious gateway or DNS settings. Evil twin APs imitate trusted Wi-Fi. DoS exhausts resources; DDoS uses distributed sources. Social engineering targets human decisions. VLAN hopping crosses intended layer-2 boundaries. Validate evidence before attribution.

</details>

<details class="hr-qa" markdown="1">
<summary>A DNS response points users to an unauthorized IP — which answer best fits?</summary>

**Answer:** DNS poisoning

DNS poisoning is the best match for this situation. Spoofing falsifies identity information; ARP poisoning can redirect local IPv4 traffic. Rogue DHCP may supply malicious gateway or DNS settings. Evil twin APs imitate trusted Wi-Fi. DoS exhausts resources; DDoS uses distributed sources. Social engineering targets human decisions. VLAN hopping crosses intended layer-2 boundaries. Validate evidence before attribution.

</details>

<details class="hr-qa" markdown="1">
<summary>An attacker claims another device's source address — which answer best fits?</summary>

**Answer:** Spoofing

Spoofing is the best match for this situation. Spoofing falsifies identity information; ARP poisoning can redirect local IPv4 traffic. Rogue DHCP may supply malicious gateway or DNS settings. Evil twin APs imitate trusted Wi-Fi. DoS exhausts resources; DDoS uses distributed sources. Social engineering targets human decisions. VLAN hopping crosses intended layer-2 boundaries. Validate evidence before attribution.

</details>

<details class="hr-qa" markdown="1">
<summary>Traffic crosses VLAN boundaries by exploiting switching configuration — which answer best fits?</summary>

**Answer:** VLAN hopping

VLAN hopping is the best match for this situation. Spoofing falsifies identity information; ARP poisoning can redirect local IPv4 traffic. Rogue DHCP may supply malicious gateway or DNS settings. Evil twin APs imitate trusted Wi-Fi. DoS exhausts resources; DDoS uses distributed sources. Social engineering targets human decisions. VLAN hopping crosses intended layer-2 boundaries. Validate evidence before attribution.

</details>

<details class="hr-qa" markdown="1">
<summary>A malicious program encrypts files and demands payment — which answer best fits?</summary>

**Answer:** Ransomware

Ransomware is the best match for this situation. Spoofing falsifies identity information; ARP poisoning can redirect local IPv4 traffic. Rogue DHCP may supply malicious gateway or DNS settings. Evil twin APs imitate trusted Wi-Fi. DoS exhausts resources; DDoS uses distributed sources. Social engineering targets human decisions. VLAN hopping crosses intended layer-2 boundaries. Validate evidence before attribution.

</details>

<details class="hr-qa" markdown="1">
<summary>A person follows an authorized employee through a secured door — which answer best fits?</summary>

**Answer:** Tailgating

Tailgating is the best match for this situation. Spoofing falsifies identity information; ARP poisoning can redirect local IPv4 traffic. Rogue DHCP may supply malicious gateway or DNS settings. Evil twin APs imitate trusted Wi-Fi. DoS exhausts resources; DDoS uses distributed sources. Social engineering targets human decisions. VLAN hopping crosses intended layer-2 boundaries. Validate evidence before attribution.

</details>


### Visual learning

- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)

<a id="objective-4-3"></a>

## 4.3 — Network defense

### Technical distinctions

- **802.1X:** Controls port access through identity authentication.
- **ACL:** Permits or denies traffic using defined match rules.
- **Screened subnet:** Isolates externally accessible services from internal networks.
- **NAC:** Evaluates endpoint access policy and posture.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


Disable unused services and ports, patch devices, restrict management, use ACLs and segmentation. 802.1X authenticates network access using a supplicant, authenticator and authentication server. MAC filtering alone is weak because addresses can be spoofed.


### Deep dive — Defense deployment

Use explicit ACL policy, segmentation, secure management, patching and disable unused services. 802.1X controls port access; RADIUS commonly supports network access authentication, TACACS+ commonly supports device administration. DHCP snooping and dynamic ARP inspection mitigate specific local threats when correctly configured. DMZs isolate exposed services; NAC can assess endpoint compliance.

**Hands-on verification:** Build a management-only ACL in a lab; test permitted and denied flows and preserve console recovery.

**Reference for further study:** IEEE 802.1X.

[Practice this objective](../practice/?objective=4.3) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| ACL | Access control list; traffic or resource rules |
| NAC | Network access control; admission policy |
| DMZ | Demilitarized zone; separated service network |
| 802.1X | Port-based network access control; authenticates network access |

### Technical quick-reference table

| Control | Purpose | Example |
| --- | --- | --- |
| 802.1X | Port authentication | RADIUS-backed access |
| ACL | Traffic filtering | Restrict management subnet |
| Segmentation | Limit lateral movement | Separate guest network |
| IDS/IPS | Detect or block suspicious traffic | Tune signatures |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>Which standard provides port-based network access authentication?</summary>

**Answer:** 802.1X

Disable unused services and ports, patch devices, restrict management, use ACLs and segmentation. 802.1X authenticates network access using a supplicant, authenticator and authentication server. MAC filtering alone is weak because addresses can be spoofed.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: authenticates devices or users before granting normal port access?</summary>

**Answer:** 802.1X

802.1X: Authenticates devices or users before granting normal port access. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: rule set permitting or denying traffic based on specified criteria?</summary>

**Answer:** ACL

ACL: Rule set permitting or denying traffic based on specified criteria. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: separated network zone for externally accessible services?</summary>

**Answer:** Screened subnet

Screened subnet: Separated network zone for externally accessible services. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: limits or controls learned source MAC addresses on switch ports?</summary>

**Answer:** Port security

Port security: Limits or controls learned source MAC addresses on switch ports. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: replacing cryptographic keys according to policy or compromise response?</summary>

**Answer:** Key rotation

Key rotation: Replacing cryptographic keys according to policy or compromise response. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>A public web server must be reachable from the internet but isolated from employee workstations. Which design is best?</summary>

**Answer:** Screened subnet with restrictive firewall rules

A separate zone and explicit traffic policy limit access to internal resources.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes ACL?</summary>

**Answer:** Rule set permitting or denying traffic based on specified criteria

ACL refers to rule set permitting or denying traffic based on specified criteria. The alternatives instead describe 802.1X, Screened subnet, Port security.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Screened subnet?</summary>

**Answer:** Separated network zone for externally accessible services

Screened subnet refers to separated network zone for externally accessible services. The alternatives instead describe 802.1X, ACL, Port security.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Port security?</summary>

**Answer:** Limits or controls learned source MAC addresses on switch ports

Port security refers to limits or controls learned source MAC addresses on switch ports. The alternatives instead describe 802.1X, ACL, Screened subnet.

</details>

<details class="hr-qa" markdown="1">
<summary>Guest devices must reach the internet but never internal file servers. Which design best enforces this?</summary>

**Answer:** Separate guest VLAN with restrictive firewall policy

Segmentation plus enforced policy limits paths; SSID alone need not isolate traffic, and logging or leases do not enforce access.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: controls port access through identity authentication?</summary>

**Answer:** 802.1X

802.1X: Controls port access through identity authentication; ACL: Permits or denies traffic using defined match rules; Screened subnet: Isolates externally accessible services from internal networks; NAC: Evaluates endpoint access policy and posture.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes 802.1X from the alternatives?</summary>

**Answer:** Controls port access through identity authentication

802.1X: Controls port access through identity authentication; ACL: Permits or denies traffic using defined match rules; Screened subnet: Isolates externally accessible services from internal networks; NAC: Evaluates endpoint access policy and posture.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: permits or denies traffic using defined match rules?</summary>

**Answer:** ACL

802.1X: Controls port access through identity authentication; ACL: Permits or denies traffic using defined match rules; Screened subnet: Isolates externally accessible services from internal networks; NAC: Evaluates endpoint access policy and posture.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes ACL from the alternatives?</summary>

**Answer:** Permits or denies traffic using defined match rules

802.1X: Controls port access through identity authentication; ACL: Permits or denies traffic using defined match rules; Screened subnet: Isolates externally accessible services from internal networks; NAC: Evaluates endpoint access policy and posture.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: isolates externally accessible services from internal networks?</summary>

**Answer:** Screened subnet

802.1X: Controls port access through identity authentication; ACL: Permits or denies traffic using defined match rules; Screened subnet: Isolates externally accessible services from internal networks; NAC: Evaluates endpoint access policy and posture.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Screened subnet from the alternatives?</summary>

**Answer:** Isolates externally accessible services from internal networks

802.1X: Controls port access through identity authentication; ACL: Permits or denies traffic using defined match rules; Screened subnet: Isolates externally accessible services from internal networks; NAC: Evaluates endpoint access policy and posture.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: evaluates endpoint access policy and posture?</summary>

**Answer:** NAC

802.1X: Controls port access through identity authentication; ACL: Permits or denies traffic using defined match rules; Screened subnet: Isolates externally accessible services from internal networks; NAC: Evaluates endpoint access policy and posture.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes NAC from the alternatives?</summary>

**Answer:** Evaluates endpoint access policy and posture

802.1X: Controls port access through identity authentication; ACL: Permits or denies traffic using defined match rules; Screened subnet: Isolates externally accessible services from internal networks; NAC: Evaluates endpoint access policy and posture.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes ACL for a task that requires: controls port access through identity authentication. Which alternative is the better match?</summary>

**Answer:** 802.1X

802.1X: Controls port access through identity authentication; ACL: Permits or denies traffic using defined match rules; Screened subnet: Isolates externally accessible services from internal networks; NAC: Evaluates endpoint access policy and posture.

</details>

<details class="hr-qa" markdown="1">
<summary>A switch must authenticate endpoints before granting access — which answer best fits?</summary>

**Answer:** 802.1X

802.1X is the best match for this situation. Use explicit ACL policy, segmentation, secure management, patching and disable unused services. 802.1X controls port access; RADIUS commonly supports network access authentication, TACACS+ commonly supports device administration. DHCP snooping and dynamic ARP inspection mitigate specific local threats when correctly configured. DMZs isolate exposed services; NAC can assess endpoint compliance.

</details>

<details class="hr-qa" markdown="1">
<summary>A public web server should be isolated from internal clients — which answer best fits?</summary>

**Answer:** DMZ

DMZ is the best match for this situation. Use explicit ACL policy, segmentation, secure management, patching and disable unused services. 802.1X controls port access; RADIUS commonly supports network access authentication, TACACS+ commonly supports device administration. DHCP snooping and dynamic ARP inspection mitigate specific local threats when correctly configured. DMZs isolate exposed services; NAC can assess endpoint compliance.

</details>

<details class="hr-qa" markdown="1">
<summary>A switch must reject DHCP offers from untrusted access ports — which answer best fits?</summary>

**Answer:** DHCP snooping

DHCP snooping is the best match for this situation. Use explicit ACL policy, segmentation, secure management, patching and disable unused services. 802.1X controls port access; RADIUS commonly supports network access authentication, TACACS+ commonly supports device administration. DHCP snooping and dynamic ARP inspection mitigate specific local threats when correctly configured. DMZs isolate exposed services; NAC can assess endpoint compliance.

</details>

<details class="hr-qa" markdown="1">
<summary>A switch validates ARP messages against trusted bindings — which answer best fits?</summary>

**Answer:** Dynamic ARP inspection

Dynamic ARP inspection is the best match for this situation. Use explicit ACL policy, segmentation, secure management, patching and disable unused services. 802.1X controls port access; RADIUS commonly supports network access authentication, TACACS+ commonly supports device administration. DHCP snooping and dynamic ARP inspection mitigate specific local threats when correctly configured. DMZs isolate exposed services; NAC can assess endpoint compliance.

</details>

<details class="hr-qa" markdown="1">
<summary>An unused access port presents unnecessary exposure — which answer best fits?</summary>

**Answer:** Administratively disable it

Administratively disable it is the best match for this situation. Use explicit ACL policy, segmentation, secure management, patching and disable unused services. 802.1X controls port access; RADIUS commonly supports network access authentication, TACACS+ commonly supports device administration. DHCP snooping and dynamic ARP inspection mitigate specific local threats when correctly configured. DMZs isolate exposed services; NAC can assess endpoint compliance.

</details>

<details class="hr-qa" markdown="1">
<summary>A firewall should permit only required application flows — which answer best fits?</summary>

**Answer:** Least-privilege ACL

Least-privilege ACL is the best match for this situation. Use explicit ACL policy, segmentation, secure management, patching and disable unused services. 802.1X controls port access; RADIUS commonly supports network access authentication, TACACS+ commonly supports device administration. DHCP snooping and dynamic ARP inspection mitigate specific local threats when correctly configured. DMZs isolate exposed services; NAC can assess endpoint compliance.

</details>

<details class="hr-qa" markdown="1">
<summary>A device administration system needs centralized command authorization — which answer best fits?</summary>

**Answer:** TACACS+

TACACS+ is the best match for this situation. Use explicit ACL policy, segmentation, secure management, patching and disable unused services. 802.1X controls port access; RADIUS commonly supports network access authentication, TACACS+ commonly supports device administration. DHCP snooping and dynamic ARP inspection mitigate specific local threats when correctly configured. DMZs isolate exposed services; NAC can assess endpoint compliance.

</details>

<details class="hr-qa" markdown="1">
<summary>Enterprise network access authentication commonly uses — which answer best fits?</summary>

**Answer:** RADIUS

RADIUS is the best match for this situation. Use explicit ACL policy, segmentation, secure management, patching and disable unused services. 802.1X controls port access; RADIUS commonly supports network access authentication, TACACS+ commonly supports device administration. DHCP snooping and dynamic ARP inspection mitigate specific local threats when correctly configured. DMZs isolate exposed services; NAC can assess endpoint compliance.

</details>

<details class="hr-qa" markdown="1">
<summary>An endpoint must satisfy security posture before access — which answer best fits?</summary>

**Answer:** NAC

NAC is the best match for this situation. Use explicit ACL policy, segmentation, secure management, patching and disable unused services. 802.1X controls port access; RADIUS commonly supports network access authentication, TACACS+ commonly supports device administration. DHCP snooping and dynamic ARP inspection mitigate specific local threats when correctly configured. DMZs isolate exposed services; NAC can assess endpoint compliance.

</details>

<details class="hr-qa" markdown="1">
<summary>A device runs vulnerable firmware — which answer best fits?</summary>

**Answer:** Test and apply approved security update

Test and apply approved security update is the best match for this situation. Use explicit ACL policy, segmentation, secure management, patching and disable unused services. 802.1X controls port access; RADIUS commonly supports network access authentication, TACACS+ commonly supports device administration. DHCP snooping and dynamic ARP inspection mitigate specific local threats when correctly configured. DMZs isolate exposed services; NAC can assess endpoint compliance.

</details>


### Visual learning

- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)

<a id="objective-5-1"></a>

## 5.1 — Troubleshooting methodology

### Technical distinctions

- **Identify problem:** Collect symptoms scope and recent changes.
- **Test theory:** Use evidence to confirm or reject suspected cause.
- **Verify functionality:** Confirm service restoration and check side effects.
- **Document findings:** Record cause actions and outcome for future reference.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


Identify the problem, establish a theory, test it, plan a solution, implement or escalate, verify functionality and preventive measures, document outcomes. If testing disproves a theory, establish a new one. Assess change impact before implementation.

[Existing troubleshooting workspace](/network-portfolio/network-troubleshooting-checklist/) (six-step presentation; planning and implementation are combined there).


### Deep dive — Evidence-driven troubleshooting

Identify scope and symptoms, establish a probable cause, test the theory, plan and implement a fix, verify full functionality and document findings. Escalate when evidence or authorization is insufficient. Change one variable at a time and use rollback plans. Verify with affected users and monitoring.

**Hands-on verification:** Use the portfolio checklist to record observations, hypotheses, test results, fix and verification for a simulated outage.

**Reference for further study:** CompTIA N10-009 objective 5.1.

[Practice this objective](../practice/?objective=5.1) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| RCA | Root cause analysis; identifies underlying cause |
| SOP | Standard operating procedure; repeatable approved process |

### Technical quick-reference table

| Stage | Action | Evidence |
| --- | --- | --- |
| Identify | Gather symptoms | Scope and recent changes |
| Hypothesize | Form likely cause | Compare working host |
| Test | Verify hypothesis | One controlled change |
| Resolve | Implement and verify | Restore service and document |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>After a theory is confirmed, what comes next?</summary>

**Answer:** Establish a plan of action

Identify the problem, establish a theory, test it, plan a solution, implement or escalate, verify functionality and preventive measures, document outcomes. If testing disproves a theory, establish a new one. Assess change impact before implementation.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: gather symptoms, scope and recent changes before selecting a cause?</summary>

**Answer:** Identify problem

Identify problem: Gather symptoms, scope and recent changes before selecting a cause. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: collect evidence to confirm or reject a suspected cause?</summary>

**Answer:** Test theory

Test theory: Collect evidence to confirm or reject a suspected cause. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: assess impact and rollback before applying a confirmed fix?</summary>

**Answer:** Plan action

Plan action: Assess impact and rollback before applying a confirmed fix. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: confirm restored service and check for unintended effects after a fix?</summary>

**Answer:** Verify functionality

Verify functionality: Confirm restored service and check for unintended effects after a fix. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: record findings, changes and lessons for future incidents?</summary>

**Answer:** Document outcomes

Document outcomes: Record findings, changes and lessons for future incidents. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>A proposed switch replacement may disconnect an entire floor. The fault is confirmed. What should happen before replacement?</summary>

**Answer:** Plan impact, maintenance window and rollback

Planning limits unintended outages and establishes recovery steps before implementation.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Test theory?</summary>

**Answer:** Collect evidence to confirm or reject a suspected cause

Test theory refers to collect evidence to confirm or reject a suspected cause. The alternatives instead describe Identify problem, Plan action, Verify functionality.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Plan action?</summary>

**Answer:** Assess impact and rollback before applying a confirmed fix

Plan action refers to assess impact and rollback before applying a confirmed fix. The alternatives instead describe Identify problem, Test theory, Verify functionality.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Verify functionality?</summary>

**Answer:** Confirm restored service and check for unintended effects after a fix

Verify functionality refers to confirm restored service and check for unintended effects after a fix. The alternatives instead describe Identify problem, Test theory, Plan action.

</details>

<details class="hr-qa" markdown="1">
<summary>A technician suspects a damaged patch cable. Before replacing a switch, what should happen next?</summary>

**Answer:** Test the cable hypothesis with a known-good cable

A controlled test verifies the suspected cause before broader changes; the alternatives are premature or disruptive.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: collect symptoms scope and recent changes?</summary>

**Answer:** Identify problem

Identify problem: Collect symptoms scope and recent changes; Test theory: Use evidence to confirm or reject suspected cause; Verify functionality: Confirm service restoration and check side effects; Document findings: Record cause actions and outcome for future reference.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Identify problem from the alternatives?</summary>

**Answer:** Collect symptoms scope and recent changes

Identify problem: Collect symptoms scope and recent changes; Test theory: Use evidence to confirm or reject suspected cause; Verify functionality: Confirm service restoration and check side effects; Document findings: Record cause actions and outcome for future reference.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: use evidence to confirm or reject suspected cause?</summary>

**Answer:** Test theory

Identify problem: Collect symptoms scope and recent changes; Test theory: Use evidence to confirm or reject suspected cause; Verify functionality: Confirm service restoration and check side effects; Document findings: Record cause actions and outcome for future reference.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Test theory from the alternatives?</summary>

**Answer:** Use evidence to confirm or reject suspected cause

Identify problem: Collect symptoms scope and recent changes; Test theory: Use evidence to confirm or reject suspected cause; Verify functionality: Confirm service restoration and check side effects; Document findings: Record cause actions and outcome for future reference.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: confirm service restoration and check side effects?</summary>

**Answer:** Verify functionality

Identify problem: Collect symptoms scope and recent changes; Test theory: Use evidence to confirm or reject suspected cause; Verify functionality: Confirm service restoration and check side effects; Document findings: Record cause actions and outcome for future reference.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Verify functionality from the alternatives?</summary>

**Answer:** Confirm service restoration and check side effects

Identify problem: Collect symptoms scope and recent changes; Test theory: Use evidence to confirm or reject suspected cause; Verify functionality: Confirm service restoration and check side effects; Document findings: Record cause actions and outcome for future reference.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: record cause actions and outcome for future reference?</summary>

**Answer:** Document findings

Identify problem: Collect symptoms scope and recent changes; Test theory: Use evidence to confirm or reject suspected cause; Verify functionality: Confirm service restoration and check side effects; Document findings: Record cause actions and outcome for future reference.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Document findings from the alternatives?</summary>

**Answer:** Record cause actions and outcome for future reference

Identify problem: Collect symptoms scope and recent changes; Test theory: Use evidence to confirm or reject suspected cause; Verify functionality: Confirm service restoration and check side effects; Document findings: Record cause actions and outcome for future reference.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes Test theory for a task that requires: collect symptoms scope and recent changes. Which alternative is the better match?</summary>

**Answer:** Identify problem

Identify problem: Collect symptoms scope and recent changes; Test theory: Use evidence to confirm or reject suspected cause; Verify functionality: Confirm service restoration and check side effects; Document findings: Record cause actions and outcome for future reference.

</details>

<details class="hr-qa" markdown="1">
<summary>A user reports intermittent connectivity; what comes first — which answer best fits?</summary>

**Answer:** Gather symptoms and scope

Gather symptoms and scope is the best match for this situation. Identify scope and symptoms, establish a probable cause, test the theory, plan and implement a fix, verify full functionality and document findings. Escalate when evidence or authorization is insufficient. Change one variable at a time and use rollback plans. Verify with affected users and monitoring.

</details>

<details class="hr-qa" markdown="1">
<summary>Only one floor is affected; what should be established next — which answer best fits?</summary>

**Answer:** Evidence-based probable cause

Evidence-based probable cause is the best match for this situation. Identify scope and symptoms, establish a probable cause, test the theory, plan and implement a fix, verify full functionality and document findings. Escalate when evidence or authorization is insufficient. Change one variable at a time and use rollback plans. Verify with affected users and monitoring.

</details>

<details class="hr-qa" markdown="1">
<summary>A suspected bad patch cable is identified — which answer best fits?</summary>

**Answer:** Test with a known-good cable

Test with a known-good cable is the best match for this situation. Identify scope and symptoms, establish a probable cause, test the theory, plan and implement a fix, verify full functionality and document findings. Escalate when evidence or authorization is insufficient. Change one variable at a time and use rollback plans. Verify with affected users and monitoring.

</details>

<details class="hr-qa" markdown="1">
<summary>A theory is disproved — which answer best fits?</summary>

**Answer:** Develop another theory or escalate

Develop another theory or escalate is the best match for this situation. Identify scope and symptoms, establish a probable cause, test the theory, plan and implement a fix, verify full functionality and document findings. Escalate when evidence or authorization is insufficient. Change one variable at a time and use rollback plans. Verify with affected users and monitoring.

</details>

<details class="hr-qa" markdown="1">
<summary>A proposed fix affects production — which answer best fits?</summary>

**Answer:** Plan change and rollback before implementation

Plan change and rollback before implementation is the best match for this situation. Identify scope and symptoms, establish a probable cause, test the theory, plan and implement a fix, verify full functionality and document findings. Escalate when evidence or authorization is insufficient. Change one variable at a time and use rollback plans. Verify with affected users and monitoring.

</details>

<details class="hr-qa" markdown="1">
<summary>A fix restores ping but users still cannot access email — which answer best fits?</summary>

**Answer:** Verify full service functionality

Verify full service functionality is the best match for this situation. Identify scope and symptoms, establish a probable cause, test the theory, plan and implement a fix, verify full functionality and document findings. Escalate when evidence or authorization is insufficient. Change one variable at a time and use rollback plans. Verify with affected users and monitoring.

</details>

<details class="hr-qa" markdown="1">
<summary>A fix succeeds and preventive action is identified — which answer best fits?</summary>

**Answer:** Document findings and actions

Document findings and actions is the best match for this situation. Identify scope and symptoms, establish a probable cause, test the theory, plan and implement a fix, verify full functionality and document findings. Escalate when evidence or authorization is insufficient. Change one variable at a time and use rollback plans. Verify with affected users and monitoring.

</details>

<details class="hr-qa" markdown="1">
<summary>A technician lacks authorization for a risky change — which answer best fits?</summary>

**Answer:** Escalate to authorized personnel

Escalate to authorized personnel is the best match for this situation. Identify scope and symptoms, establish a probable cause, test the theory, plan and implement a fix, verify full functionality and document findings. Escalate when evidence or authorization is insufficient. Change one variable at a time and use rollback plans. Verify with affected users and monitoring.

</details>

<details class="hr-qa" markdown="1">
<summary>A problem began after a change — which answer best fits?</summary>

**Answer:** Review change history and test correlation

Review change history and test correlation is the best match for this situation. Identify scope and symptoms, establish a probable cause, test the theory, plan and implement a fix, verify full functionality and document findings. Escalate when evidence or authorization is insufficient. Change one variable at a time and use rollback plans. Verify with affected users and monitoring.

</details>

<details class="hr-qa" markdown="1">
<summary>A test changes several variables simultaneously — which answer best fits?</summary>

**Answer:** Isolate variables for interpretable evidence

Isolate variables for interpretable evidence is the best match for this situation. Identify scope and symptoms, establish a probable cause, test the theory, plan and implement a fix, verify full functionality and document findings. Escalate when evidence or authorization is insufficient. Change one variable at a time and use rollback plans. Verify with affected users and monitoring.

</details>


### Visual learning

- [Networking Fundamentals — Network Troubleshooting Flowchart"
](/network-portfolio/study-diagrams/network-troubleshooting-flowchart/)
- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)

<a id="objective-5-2"></a>

## 5.2 — Physical troubleshooting

### Technical distinctions

- **Wire map tester:** Detects incorrect conductor pin assignments.
- **OTDR:** Locates optical fiber faults by reflected light.
- **CRC errors:** Indicate frames failing integrity checks.
- **Duplex mismatch:** Can cause collisions and poor throughput on Ethernet.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


Check link state, cable seating, interface counters, speed and duplex, optics and power. CRC errors may indicate physical corruption. A cable certifier validates standards; a toner traces copper; an optical power meter measures received light.


### Deep dive — Physical diagnostics

CRC/FCS errors can indicate corrupted frames from cabling, optics or duplex issues. Check link state, speed, duplex, error trends and transceiver compatibility. Cable testers identify wire faults; certification validates performance; optical power meters measure light. PoE budget and standards must match device demand.

**Hands-on verification:** Compare show interfaces counters before and after a known-good cable swap; avoid looking into optical connectors.

**Reference for further study:** IEEE 802.3.

[Practice this objective](../practice/?objective=5.2) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| CRC | Cyclic redundancy check; detects transmission errors |
| TDR | Time domain reflectometer; locates cable impedance changes |
| OTDR | Optical time domain reflectometer; measures fiber events |

### Technical quick-reference table

| Symptom | Evidence | Next check |
| --- | --- | --- |
| No link | Interface down | Cable and transceiver |
| CRC errors | Error counters rising | Media and duplex |
| Optical loss | Low receive power | Clean connectors and check budget |
| PoE failure | Power denied | Switch budget and device class |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>Which tool measures received optical signal power?</summary>

**Answer:** Optical power meter

Check link state, cable seating, interface counters, speed and duplex, optics and power. CRC errors may indicate physical corruption. A cable certifier validates standards; a toner traces copper; an optical power meter measures received light.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: frames fail integrity checks, potentially indicating link corruption?</summary>

**Answer:** CRC errors

CRC errors: Frames fail integrity checks, potentially indicating link corruption. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: total available switch power for attached powered devices?</summary>

**Answer:** PoE budget

PoE budget: Total available switch power for attached powered devices. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: interface intentionally disabled by configuration?</summary>

**Answer:** Administratively down

Administratively down: Interface intentionally disabled by configuration. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: unwanted coupling of signals between conductors?</summary>

**Answer:** Crosstalk

Crosstalk: Unwanted coupling of signals between conductors. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: fiber transmit and receive paths incorrectly paired?</summary>

**Answer:** TX/RX reversal

TX/RX reversal: Fiber transmit and receive paths incorrectly paired. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>New APs stop powering on after several others are connected. Data links work with externally powered devices. What should be checked?</summary>

**Answer:** Remaining PoE power budget

The pattern suggests the switch may lack remaining power capacity for additional powered devices.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes PoE budget?</summary>

**Answer:** Total available switch power for attached powered devices

PoE budget refers to total available switch power for attached powered devices. The alternatives instead describe CRC errors, Administratively down, Crosstalk.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Administratively down?</summary>

**Answer:** Interface intentionally disabled by configuration

Administratively down refers to interface intentionally disabled by configuration. The alternatives instead describe CRC errors, PoE budget, Crosstalk.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Crosstalk?</summary>

**Answer:** Unwanted coupling of signals between conductors

Crosstalk refers to unwanted coupling of signals between conductors. The alternatives instead describe CRC errors, PoE budget, Administratively down.

</details>

<details class="hr-qa" markdown="1">
<summary>A copper link negotiates at 100 Mbps instead of 1 Gbps after a cable replacement. Which test is most useful first?</summary>

**Answer:** Verify all four wire pairs with a cable tester

Gigabit copper Ethernet requires four pairs; a wire-map test can reveal faults. DNS, routing and time do not determine physical negotiation.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: detects incorrect conductor pin assignments?</summary>

**Answer:** Wire map tester

Wire map tester: Detects incorrect conductor pin assignments; OTDR: Locates optical fiber faults by reflected light; CRC errors: Indicate frames failing integrity checks; Duplex mismatch: Can cause collisions and poor throughput on Ethernet.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Wire map tester from the alternatives?</summary>

**Answer:** Detects incorrect conductor pin assignments

Wire map tester: Detects incorrect conductor pin assignments; OTDR: Locates optical fiber faults by reflected light; CRC errors: Indicate frames failing integrity checks; Duplex mismatch: Can cause collisions and poor throughput on Ethernet.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: locates optical fiber faults by reflected light?</summary>

**Answer:** OTDR

Wire map tester: Detects incorrect conductor pin assignments; OTDR: Locates optical fiber faults by reflected light; CRC errors: Indicate frames failing integrity checks; Duplex mismatch: Can cause collisions and poor throughput on Ethernet.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes OTDR from the alternatives?</summary>

**Answer:** Locates optical fiber faults by reflected light

Wire map tester: Detects incorrect conductor pin assignments; OTDR: Locates optical fiber faults by reflected light; CRC errors: Indicate frames failing integrity checks; Duplex mismatch: Can cause collisions and poor throughput on Ethernet.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: indicate frames failing integrity checks?</summary>

**Answer:** CRC errors

Wire map tester: Detects incorrect conductor pin assignments; OTDR: Locates optical fiber faults by reflected light; CRC errors: Indicate frames failing integrity checks; Duplex mismatch: Can cause collisions and poor throughput on Ethernet.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes CRC errors from the alternatives?</summary>

**Answer:** Indicate frames failing integrity checks

Wire map tester: Detects incorrect conductor pin assignments; OTDR: Locates optical fiber faults by reflected light; CRC errors: Indicate frames failing integrity checks; Duplex mismatch: Can cause collisions and poor throughput on Ethernet.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: can cause collisions and poor throughput on Ethernet?</summary>

**Answer:** Duplex mismatch

Wire map tester: Detects incorrect conductor pin assignments; OTDR: Locates optical fiber faults by reflected light; CRC errors: Indicate frames failing integrity checks; Duplex mismatch: Can cause collisions and poor throughput on Ethernet.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Duplex mismatch from the alternatives?</summary>

**Answer:** Can cause collisions and poor throughput on Ethernet

Wire map tester: Detects incorrect conductor pin assignments; OTDR: Locates optical fiber faults by reflected light; CRC errors: Indicate frames failing integrity checks; Duplex mismatch: Can cause collisions and poor throughput on Ethernet.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes OTDR for a task that requires: detects incorrect conductor pin assignments. Which alternative is the better match?</summary>

**Answer:** Wire map tester

Wire map tester: Detects incorrect conductor pin assignments; OTDR: Locates optical fiber faults by reflected light; CRC errors: Indicate frames failing integrity checks; Duplex mismatch: Can cause collisions and poor throughput on Ethernet.

</details>

<details class="hr-qa" markdown="1">
<summary>A copper cable has a broken conductor — which answer best fits?</summary>

**Answer:** Wiremap tester

Wiremap tester is the best match for this situation. CRC/FCS errors can indicate corrupted frames from cabling, optics or duplex issues. Check link state, speed, duplex, error trends and transceiver compatibility. Cable testers identify wire faults; certification validates performance; optical power meters measure light. PoE budget and standards must match device demand.

</details>

<details class="hr-qa" markdown="1">
<summary>A fiber link has low received optical power — which answer best fits?</summary>

**Answer:** Optical power measurement

Optical power measurement is the best match for this situation. CRC/FCS errors can indicate corrupted frames from cabling, optics or duplex issues. Check link state, speed, duplex, error trends and transceiver compatibility. Cable testers identify wire faults; certification validates performance; optical power meters measure light. PoE budget and standards must match device demand.

</details>

<details class="hr-qa" markdown="1">
<summary>A copper link negotiates 100 Mbps instead of expected 1 Gbps — which answer best fits?</summary>

**Answer:** Inspect cable pairs and negotiation

Inspect cable pairs and negotiation is the best match for this situation. CRC/FCS errors can indicate corrupted frames from cabling, optics or duplex issues. Check link state, speed, duplex, error trends and transceiver compatibility. Cable testers identify wire faults; certification validates performance; optical power meters measure light. PoE budget and standards must match device demand.

</details>

<details class="hr-qa" markdown="1">
<summary>A switch reports rising CRC errors — which answer best fits?</summary>

**Answer:** Inspect physical link and duplex

Inspect physical link and duplex is the best match for this situation. CRC/FCS errors can indicate corrupted frames from cabling, optics or duplex issues. Check link state, speed, duplex, error trends and transceiver compatibility. Cable testers identify wire faults; certification validates performance; optical power meters measure light. PoE budget and standards must match device demand.

</details>

<details class="hr-qa" markdown="1">
<summary>A PoE phone powers off when more devices connect — which answer best fits?</summary>

**Answer:** Check PoE budget

Check PoE budget is the best match for this situation. CRC/FCS errors can indicate corrupted frames from cabling, optics or duplex issues. Check link state, speed, duplex, error trends and transceiver compatibility. Cable testers identify wire faults; certification validates performance; optical power meters measure light. PoE budget and standards must match device demand.

</details>

<details class="hr-qa" markdown="1">
<summary>A cable exceeds supported Ethernet channel length — which answer best fits?</summary>

**Answer:** Use compliant length or suitable alternate medium

Use compliant length or suitable alternate medium is the best match for this situation. CRC/FCS errors can indicate corrupted frames from cabling, optics or duplex issues. Check link state, speed, duplex, error trends and transceiver compatibility. Cable testers identify wire faults; certification validates performance; optical power meters measure light. PoE budget and standards must match device demand.

</details>

<details class="hr-qa" markdown="1">
<summary>A fiber connector is contaminated — which answer best fits?</summary>

**Answer:** Inspect and clean with approved tools

Inspect and clean with approved tools is the best match for this situation. CRC/FCS errors can indicate corrupted frames from cabling, optics or duplex issues. Check link state, speed, duplex, error trends and transceiver compatibility. Cable testers identify wire faults; certification validates performance; optical power meters measure light. PoE budget and standards must match device demand.

</details>

<details class="hr-qa" markdown="1">
<summary>A cable has correct continuity but fails high-speed operation — which answer best fits?</summary>

**Answer:** Cable certification test

Cable certification test is the best match for this situation. CRC/FCS errors can indicate corrupted frames from cabling, optics or duplex issues. Check link state, speed, duplex, error trends and transceiver compatibility. Cable testers identify wire faults; certification validates performance; optical power meters measure light. PoE budget and standards must match device demand.

</details>

<details class="hr-qa" markdown="1">
<summary>A transceiver is not supported by the switch — which answer best fits?</summary>

**Answer:** Check compatibility and replace appropriately

Check compatibility and replace appropriately is the best match for this situation. CRC/FCS errors can indicate corrupted frames from cabling, optics or duplex issues. Check link state, speed, duplex, error trends and transceiver compatibility. Cable testers identify wire faults; certification validates performance; optical power meters measure light. PoE budget and standards must match device demand.

</details>

<details class="hr-qa" markdown="1">
<summary>A link has late collisions and mismatched duplex settings — which answer best fits?</summary>

**Answer:** Correct duplex negotiation on both ends

Correct duplex negotiation on both ends is the best match for this situation. CRC/FCS errors can indicate corrupted frames from cabling, optics or duplex issues. Check link state, speed, duplex, error trends and transceiver compatibility. Cable testers identify wire faults; certification validates performance; optical power meters measure light. PoE budget and standards must match device demand.

</details>


### Visual learning

- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)

<a id="objective-5-3"></a>

## 5.3 — Common network issues

### Technical distinctions

- **DHCP exhaustion:** Prevents new clients obtaining leases when pool is full.
- **Wrong default gateway:** Prevents off-subnet access despite local connectivity.
- **VLAN mismatch:** Places endpoints in unintended broadcast domains.
- **Duplicate IP:** Causes conflicting address ownership and intermittent reachability.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


Check VLAN membership, trunk allowances, STP state, IP address, mask, gateway and route table. Duplicate addresses cause intermittent reachability. APIPA suggests a DHCP failure or unavailable server. Isolate scope before changing configuration.


### Deep dive — Service isolation

Check local address, mask, gateway, VLAN, DHCP and DNS separately. A duplicate IP may cause intermittent ARP changes. A missing VLAN on a trunk isolates that VLAN. STP changes can interrupt forwarding. Routing loops consume TTL; wrong default routes break remote reachability. Exhausted DHCP pools affect new leases.

**Hands-on verification:** Test loopback, local gateway, remote IP and DNS name in sequence; compare a working host on the same VLAN.

**Reference for further study:** RFC 5227.

[Practice this objective](../practice/?objective=5.3) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| DNS | Domain name system; name resolution |
| DHCP | Dynamic host configuration protocol; address configuration |
| ARP | Address resolution protocol; IPv4 neighbor mapping |

### Technical quick-reference table

| Symptom | Test | Interpretation |
| --- | --- | --- |
| Local only | Ping gateway | VLAN or gateway issue |
| IP works, name fails | DNS query | Resolver or record issue |
| Duplicate IP | ARP changes | Check address allocation |
| No lease | DHCP exchange | Relay or scope issue |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>A DHCP client self-assigns 169.254.12.4. What should be investigated first?</summary>

**Answer:** DHCP reachability

Check VLAN membership, trunk allowances, STP state, IP address, mask, gateway and route table. Duplicate addresses cause intermittent reachability. APIPA suggests a DHCP failure or unavailable server. Isolate scope before changing configuration.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: no available dynamic leases remain in the configured scope?</summary>

**Answer:** DHCP pool exhaustion

DHCP pool exhaustion: No available dynamic leases remain in the configured scope. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: host can reach local subnet but sends remote traffic toward wrong next hop?</summary>

**Answer:** Incorrect gateway

Incorrect gateway: Host can reach local subnet but sends remote traffic toward wrong next hop. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: two devices claim the same address causing intermittent delivery?</summary>

**Answer:** Duplicate IP

Duplicate IP: Two devices claim the same address causing intermittent delivery. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: switch port places a host in the wrong broadcast domain?</summary>

**Answer:** Incorrect VLAN

Incorrect VLAN: Switch port places a host in the wrong broadcast domain. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: router lacks a matching route for otherwise unknown destinations?</summary>

**Answer:** Missing default route

Missing default route: Router lacks a matching route for otherwise unknown destinations. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>A host at 192.168.10.20/24 uses gateway 192.168.20.1. Local peers respond but remote networks fail. What is wrong?</summary>

**Answer:** Gateway is outside the local subnet

A conventional IPv4 host needs a reachable next hop on its local subnet.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Incorrect gateway?</summary>

**Answer:** Host can reach local subnet but sends remote traffic toward wrong next hop

Incorrect gateway refers to host can reach local subnet but sends remote traffic toward wrong next hop. The alternatives instead describe DHCP pool exhaustion, Duplicate IP, Incorrect VLAN.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Duplicate IP?</summary>

**Answer:** Two devices claim the same address causing intermittent delivery

Duplicate IP refers to two devices claim the same address causing intermittent delivery. The alternatives instead describe DHCP pool exhaustion, Incorrect gateway, Incorrect VLAN.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Incorrect VLAN?</summary>

**Answer:** Switch port places a host in the wrong broadcast domain

Incorrect VLAN refers to switch port places a host in the wrong broadcast domain. The alternatives instead describe DHCP pool exhaustion, Incorrect gateway, Duplicate IP.

</details>

<details class="hr-qa" markdown="1">
<summary>A host reaches peers in its own subnet but cannot reach any remote subnet. Its configured gateway is outside its local prefix. What should be corrected?</summary>

**Answer:** Default gateway address

A conventional gateway must be reachable on the local link; the other settings do not repair next-hop reachability.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: prevents new clients obtaining leases when pool is full?</summary>

**Answer:** DHCP exhaustion

DHCP exhaustion: Prevents new clients obtaining leases when pool is full; Wrong default gateway: Prevents off-subnet access despite local connectivity; VLAN mismatch: Places endpoints in unintended broadcast domains; Duplicate IP: Causes conflicting address ownership and intermittent reachability.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes DHCP exhaustion from the alternatives?</summary>

**Answer:** Prevents new clients obtaining leases when pool is full

DHCP exhaustion: Prevents new clients obtaining leases when pool is full; Wrong default gateway: Prevents off-subnet access despite local connectivity; VLAN mismatch: Places endpoints in unintended broadcast domains; Duplicate IP: Causes conflicting address ownership and intermittent reachability.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: prevents off-subnet access despite local connectivity?</summary>

**Answer:** Wrong default gateway

DHCP exhaustion: Prevents new clients obtaining leases when pool is full; Wrong default gateway: Prevents off-subnet access despite local connectivity; VLAN mismatch: Places endpoints in unintended broadcast domains; Duplicate IP: Causes conflicting address ownership and intermittent reachability.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Wrong default gateway from the alternatives?</summary>

**Answer:** Prevents off-subnet access despite local connectivity

DHCP exhaustion: Prevents new clients obtaining leases when pool is full; Wrong default gateway: Prevents off-subnet access despite local connectivity; VLAN mismatch: Places endpoints in unintended broadcast domains; Duplicate IP: Causes conflicting address ownership and intermittent reachability.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: places endpoints in unintended broadcast domains?</summary>

**Answer:** VLAN mismatch

DHCP exhaustion: Prevents new clients obtaining leases when pool is full; Wrong default gateway: Prevents off-subnet access despite local connectivity; VLAN mismatch: Places endpoints in unintended broadcast domains; Duplicate IP: Causes conflicting address ownership and intermittent reachability.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes VLAN mismatch from the alternatives?</summary>

**Answer:** Places endpoints in unintended broadcast domains

DHCP exhaustion: Prevents new clients obtaining leases when pool is full; Wrong default gateway: Prevents off-subnet access despite local connectivity; VLAN mismatch: Places endpoints in unintended broadcast domains; Duplicate IP: Causes conflicting address ownership and intermittent reachability.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: causes conflicting address ownership and intermittent reachability?</summary>

**Answer:** Duplicate IP

DHCP exhaustion: Prevents new clients obtaining leases when pool is full; Wrong default gateway: Prevents off-subnet access despite local connectivity; VLAN mismatch: Places endpoints in unintended broadcast domains; Duplicate IP: Causes conflicting address ownership and intermittent reachability.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Duplicate IP from the alternatives?</summary>

**Answer:** Causes conflicting address ownership and intermittent reachability

DHCP exhaustion: Prevents new clients obtaining leases when pool is full; Wrong default gateway: Prevents off-subnet access despite local connectivity; VLAN mismatch: Places endpoints in unintended broadcast domains; Duplicate IP: Causes conflicting address ownership and intermittent reachability.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes Wrong default gateway for a task that requires: prevents new clients obtaining leases when pool is full. Which alternative is the better match?</summary>

**Answer:** DHCP exhaustion

DHCP exhaustion: Prevents new clients obtaining leases when pool is full; Wrong default gateway: Prevents off-subnet access despite local connectivity; VLAN mismatch: Places endpoints in unintended broadcast domains; Duplicate IP: Causes conflicting address ownership and intermittent reachability.

</details>

<details class="hr-qa" markdown="1">
<summary>A host reaches local peers but no remote networks; its gateway is wrong — which answer best fits?</summary>

**Answer:** Correct default gateway

Correct default gateway is the best match for this situation. Check local address, mask, gateway, VLAN, DHCP and DNS separately. A duplicate IP may cause intermittent ARP changes. A missing VLAN on a trunk isolates that VLAN. STP changes can interrupt forwarding. Routing loops consume TTL; wrong default routes break remote reachability. Exhausted DHCP pools affect new leases.

</details>

<details class="hr-qa" markdown="1">
<summary>A host reaches remote IPs but cannot resolve names — which answer best fits?</summary>

**Answer:** Investigate DNS

Investigate DNS is the best match for this situation. Check local address, mask, gateway, VLAN, DHCP and DNS separately. A duplicate IP may cause intermittent ARP changes. A missing VLAN on a trunk isolates that VLAN. STP changes can interrupt forwarding. Routing loops consume TTL; wrong default routes break remote reachability. Exhausted DHCP pools affect new leases.

</details>

<details class="hr-qa" markdown="1">
<summary>New clients fail leases while existing clients work and pool is full — which answer best fits?</summary>

**Answer:** DHCP exhaustion

DHCP exhaustion is the best match for this situation. Check local address, mask, gateway, VLAN, DHCP and DNS separately. A duplicate IP may cause intermittent ARP changes. A missing VLAN on a trunk isolates that VLAN. STP changes can interrupt forwarding. Routing loops consume TTL; wrong default routes break remote reachability. Exhausted DHCP pools affect new leases.

</details>

<details class="hr-qa" markdown="1">
<summary>Two hosts use the same static address — which answer best fits?</summary>

**Answer:** Duplicate IP conflict

Duplicate IP conflict is the best match for this situation. Check local address, mask, gateway, VLAN, DHCP and DNS separately. A duplicate IP may cause intermittent ARP changes. A missing VLAN on a trunk isolates that VLAN. STP changes can interrupt forwarding. Routing loops consume TTL; wrong default routes break remote reachability. Exhausted DHCP pools affect new leases.

</details>

<details class="hr-qa" markdown="1">
<summary>Only VLAN 40 fails across a trunk; allowed list omits 40 — which answer best fits?</summary>

**Answer:** Correct trunk allowed VLANs

Correct trunk allowed VLANs is the best match for this situation. Check local address, mask, gateway, VLAN, DHCP and DNS separately. A duplicate IP may cause intermittent ARP changes. A missing VLAN on a trunk isolates that VLAN. STP changes can interrupt forwarding. Routing loops consume TTL; wrong default routes break remote reachability. Exhausted DHCP pools affect new leases.

</details>

<details class="hr-qa" markdown="1">
<summary>A host has /16 mask but intended subnet is /24 — which answer best fits?</summary>

**Answer:** Correct subnet mask

Correct subnet mask is the best match for this situation. Check local address, mask, gateway, VLAN, DHCP and DNS separately. A duplicate IP may cause intermittent ARP changes. A missing VLAN on a trunk isolates that VLAN. STP changes can interrupt forwarding. Routing loops consume TTL; wrong default routes break remote reachability. Exhausted DHCP pools affect new leases.

</details>

<details class="hr-qa" markdown="1">
<summary>Traceroute repeatedly shows the same routers until TTL expires — which answer best fits?</summary>

**Answer:** Investigate routing loop

Investigate routing loop is the best match for this situation. Check local address, mask, gateway, VLAN, DHCP and DNS separately. A duplicate IP may cause intermittent ARP changes. A missing VLAN on a trunk isolates that VLAN. STP changes can interrupt forwarding. Routing loops consume TTL; wrong default routes break remote reachability. Exhausted DHCP pools affect new leases.

</details>

<details class="hr-qa" markdown="1">
<summary>A switch port is administratively down — which answer best fits?</summary>

**Answer:** Verify intended configuration before enabling

Verify intended configuration before enabling is the best match for this situation. Check local address, mask, gateway, VLAN, DHCP and DNS separately. A duplicate IP may cause intermittent ARP changes. A missing VLAN on a trunk isolates that VLAN. STP changes can interrupt forwarding. Routing loops consume TTL; wrong default routes break remote reachability. Exhausted DHCP pools affect new leases.

</details>

<details class="hr-qa" markdown="1">
<summary>A client self-assigns link-local IPv4 after DHCP timeout — which answer best fits?</summary>

**Answer:** Investigate DHCP path and scope

Investigate DHCP path and scope is the best match for this situation. Check local address, mask, gateway, VLAN, DHCP and DNS separately. A duplicate IP may cause intermittent ARP changes. A missing VLAN on a trunk isolates that VLAN. STP changes can interrupt forwarding. Routing loops consume TTL; wrong default routes break remote reachability. Exhausted DHCP pools affect new leases.

</details>

<details class="hr-qa" markdown="1">
<summary>A newly connected redundant switch link causes broadcast storm — which answer best fits?</summary>

**Answer:** Investigate layer-2 loop and STP

Investigate layer-2 loop and STP is the best match for this situation. Check local address, mask, gateway, VLAN, DHCP and DNS separately. A duplicate IP may cause intermittent ARP changes. A missing VLAN on a trunk isolates that VLAN. STP changes can interrupt forwarding. Routing loops consume TTL; wrong default routes break remote reachability. Exhausted DHCP pools affect new leases.

</details>


### Visual learning

- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)

<a id="objective-5-4"></a>

## 5.4 — Performance troubleshooting

### Technical distinctions

- **Latency:** Measures delay across a path.
- **Jitter:** Measures variation in packet delay.
- **Packet loss:** Measures packets failing to reach destination.
- **Congestion:** Occurs when offered traffic exceeds available forwarding capacity.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


Latency measures delay; jitter measures variation in delay; loss measures missing packets; throughput measures achieved rate. Congestion, interference and retransmissions reduce performance. Compare counters and measurements with baselines.


### Deep dive — Performance reasoning

Latency is delay, jitter is delay variation, loss is missing packets, throughput is delivered rate. Congestion causes queues and drops; errors suggest physical problems. Wireless interference reduces effective airtime. Compare baseline, utilization, errors and application timing; avoid assuming high bandwidth guarantees low latency.

**Hands-on verification:** Measure RTT and loss, compare interface queues and utilization, then repeat after a controlled change.

**Reference for further study:** RFC 3393.

[Practice this objective](../practice/?objective=5.4) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| QoS | Quality of service; traffic classification and treatment |
| DSCP | Differentiated services code point; IP traffic marking |
| RTT | Round trip time; elapsed time for request and response |

### Technical quick-reference table

| Metric | Meaning | Diagnostic |
| --- | --- | --- |
| Latency | Delay | Compare baseline RTT |
| Jitter | Delay variation | Inspect voice quality |
| Loss | Missing packets | Check congestion and errors |
| Throughput | Delivered rate | Compare capacity and application limits |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>Which metric most directly describes variation in packet arrival delay?</summary>

**Answer:** Jitter

Latency measures delay; jitter measures variation in delay; loss measures missing packets; throughput measures achieved rate. Congestion, interference and retransmissions reduce performance. Compare counters and measurements with baselines.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: offered traffic exceeds available forwarding capacity?</summary>

**Answer:** Congestion

Congestion: Offered traffic exceeds available forwarding capacity. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: elapsed time for data to travel between points?</summary>

**Answer:** Latency

Latency: Elapsed time for data to travel between points. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: actual achieved data transfer rate?</summary>

**Answer:** Throughput

Throughput: Actual achieved data transfer rate. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: nearby wireless channels share spectrum and interfere?</summary>

**Answer:** Channel overlap

Channel overlap: Nearby wireless channels share spectrum and interfere. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: client fails to transition smoothly between access points?</summary>

**Answer:** Roaming issue

Roaming issue: Client fails to transition smoothly between access points. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Voice packets arrive with delays varying from 10 to 110 ms despite negligible loss. Which metric is the issue?</summary>

**Answer:** Jitter

Jitter measures variation in packet delay and can disrupt real-time audio.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Latency?</summary>

**Answer:** Elapsed time for data to travel between points

Latency refers to elapsed time for data to travel between points. The alternatives instead describe Congestion, Throughput, Channel overlap.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Throughput?</summary>

**Answer:** Actual achieved data transfer rate

Throughput refers to actual achieved data transfer rate. The alternatives instead describe Congestion, Latency, Channel overlap.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Channel overlap?</summary>

**Answer:** Nearby wireless channels share spectrum and interfere

Channel overlap refers to nearby wireless channels share spectrum and interfere. The alternatives instead describe Congestion, Latency, Throughput.

</details>

<details class="hr-qa" markdown="1">
<summary>A WAN link reaches capacity during backups and voice delay rises. Which change most directly protects voice during congestion?</summary>

**Answer:** QoS prioritization

QoS schedules delay-sensitive traffic preferentially; the alternatives do not control congested queues.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: measures delay across a path?</summary>

**Answer:** Latency

Latency: Measures delay across a path; Jitter: Measures variation in packet delay; Packet loss: Measures packets failing to reach destination; Congestion: Occurs when offered traffic exceeds available forwarding capacity.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Latency from the alternatives?</summary>

**Answer:** Measures delay across a path

Latency: Measures delay across a path; Jitter: Measures variation in packet delay; Packet loss: Measures packets failing to reach destination; Congestion: Occurs when offered traffic exceeds available forwarding capacity.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: measures variation in packet delay?</summary>

**Answer:** Jitter

Latency: Measures delay across a path; Jitter: Measures variation in packet delay; Packet loss: Measures packets failing to reach destination; Congestion: Occurs when offered traffic exceeds available forwarding capacity.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Jitter from the alternatives?</summary>

**Answer:** Measures variation in packet delay

Latency: Measures delay across a path; Jitter: Measures variation in packet delay; Packet loss: Measures packets failing to reach destination; Congestion: Occurs when offered traffic exceeds available forwarding capacity.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: measures packets failing to reach destination?</summary>

**Answer:** Packet loss

Latency: Measures delay across a path; Jitter: Measures variation in packet delay; Packet loss: Measures packets failing to reach destination; Congestion: Occurs when offered traffic exceeds available forwarding capacity.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Packet loss from the alternatives?</summary>

**Answer:** Measures packets failing to reach destination

Latency: Measures delay across a path; Jitter: Measures variation in packet delay; Packet loss: Measures packets failing to reach destination; Congestion: Occurs when offered traffic exceeds available forwarding capacity.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: occurs when offered traffic exceeds available forwarding capacity?</summary>

**Answer:** Congestion

Latency: Measures delay across a path; Jitter: Measures variation in packet delay; Packet loss: Measures packets failing to reach destination; Congestion: Occurs when offered traffic exceeds available forwarding capacity.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes Congestion from the alternatives?</summary>

**Answer:** Occurs when offered traffic exceeds available forwarding capacity

Latency: Measures delay across a path; Jitter: Measures variation in packet delay; Packet loss: Measures packets failing to reach destination; Congestion: Occurs when offered traffic exceeds available forwarding capacity.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes Jitter for a task that requires: measures delay across a path. Which alternative is the better match?</summary>

**Answer:** Latency

Latency: Measures delay across a path; Jitter: Measures variation in packet delay; Packet loss: Measures packets failing to reach destination; Congestion: Occurs when offered traffic exceeds available forwarding capacity.

</details>

<details class="hr-qa" markdown="1">
<summary>Voice packets arrive with highly variable delay — which answer best fits?</summary>

**Answer:** Jitter

Jitter is the best match for this situation. Latency is delay, jitter is delay variation, loss is missing packets, throughput is delivered rate. Congestion causes queues and drops; errors suggest physical problems. Wireless interference reduces effective airtime. Compare baseline, utilization, errors and application timing; avoid assuming high bandwidth guarantees low latency.

</details>

<details class="hr-qa" markdown="1">
<summary>A WAN link runs near capacity and output drops rise — which answer best fits?</summary>

**Answer:** Congestion

Congestion is the best match for this situation. Latency is delay, jitter is delay variation, loss is missing packets, throughput is delivered rate. Congestion causes queues and drops; errors suggest physical problems. Wireless interference reduces effective airtime. Compare baseline, utilization, errors and application timing; avoid assuming high bandwidth guarantees low latency.

</details>

<details class="hr-qa" markdown="1">
<summary>A transfer achieves 80 Mbps on a 100 Mbps link — which answer best fits?</summary>

**Answer:** Throughput is 80 Mbps

Throughput is 80 Mbps is the best match for this situation. Latency is delay, jitter is delay variation, loss is missing packets, throughput is delivered rate. Congestion causes queues and drops; errors suggest physical problems. Wireless interference reduces effective airtime. Compare baseline, utilization, errors and application timing; avoid assuming high bandwidth guarantees low latency.

</details>

<details class="hr-qa" markdown="1">
<summary>A ping round trip takes 150 ms — which answer best fits?</summary>

**Answer:** Round-trip latency

Round-trip latency is the best match for this situation. Latency is delay, jitter is delay variation, loss is missing packets, throughput is delivered rate. Congestion causes queues and drops; errors suggest physical problems. Wireless interference reduces effective airtime. Compare baseline, utilization, errors and application timing; avoid assuming high bandwidth guarantees low latency.

</details>

<details class="hr-qa" markdown="1">
<summary>A test sends 100 packets and receives 95 — which answer best fits?</summary>

**Answer:** 5 percent loss

5 percent loss is the best match for this situation. Latency is delay, jitter is delay variation, loss is missing packets, throughput is delivered rate. Congestion causes queues and drops; errors suggest physical problems. Wireless interference reduces effective airtime. Compare baseline, utilization, errors and application timing; avoid assuming high bandwidth guarantees low latency.

</details>

<details class="hr-qa" markdown="1">
<summary>A Wi-Fi channel has high utilization from neighboring APs — which answer best fits?</summary>

**Answer:** Investigate airtime contention

Investigate airtime contention is the best match for this situation. Latency is delay, jitter is delay variation, loss is missing packets, throughput is delivered rate. Congestion causes queues and drops; errors suggest physical problems. Wireless interference reduces effective airtime. Compare baseline, utilization, errors and application timing; avoid assuming high bandwidth guarantees low latency.

</details>

<details class="hr-qa" markdown="1">
<summary>A link has low utilization but rising CRC errors — which answer best fits?</summary>

**Answer:** Investigate physical corruption

Investigate physical corruption is the best match for this situation. Latency is delay, jitter is delay variation, loss is missing packets, throughput is delivered rate. Congestion causes queues and drops; errors suggest physical problems. Wireless interference reduces effective airtime. Compare baseline, utilization, errors and application timing; avoid assuming high bandwidth guarantees low latency.

</details>

<details class="hr-qa" markdown="1">
<summary>A server responds slowly despite fast network RTT — which answer best fits?</summary>

**Answer:** Investigate application/server timing

Investigate application/server timing is the best match for this situation. Latency is delay, jitter is delay variation, loss is missing packets, throughput is delivered rate. Congestion causes queues and drops; errors suggest physical problems. Wireless interference reduces effective airtime. Compare baseline, utilization, errors and application timing; avoid assuming high bandwidth guarantees low latency.

</details>

<details class="hr-qa" markdown="1">
<summary>A voice class needs priority during verified congestion — which answer best fits?</summary>

**Answer:** Appropriate QoS policy

Appropriate QoS policy is the best match for this situation. Latency is delay, jitter is delay variation, loss is missing packets, throughput is delivered rate. Congestion causes queues and drops; errors suggest physical problems. Wireless interference reduces effective airtime. Compare baseline, utilization, errors and application timing; avoid assuming high bandwidth guarantees low latency.

</details>

<details class="hr-qa" markdown="1">
<summary>A speed test is slow only during scheduled backups — which answer best fits?</summary>

**Answer:** Compare traffic flows and schedule or shape backups

Compare traffic flows and schedule or shape backups is the best match for this situation. Latency is delay, jitter is delay variation, loss is missing packets, throughput is delivered rate. Congestion causes queues and drops; errors suggest physical problems. Wireless interference reduces effective airtime. Compare baseline, utilization, errors and application timing; avoid assuming high bandwidth guarantees low latency.

</details>


### Visual learning

- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)

<a id="objective-5-5"></a>

## 5.5 — Diagnostic tools

### Technical distinctions

- **traceroute:** Reveals responding hops toward a destination.
- **nslookup:** Queries DNS records.
- **tcpdump:** Captures packets for protocol inspection.
- **ipconfig:** Displays Windows IP configuration.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).


Ping tests ICMP reachability; traceroute reveals responding hops; nslookup or dig queries DNS; ipconfig or ip displays addressing; netstat or ss shows sockets. Cisco show interfaces reveals counters; show ip route shows routes. Use scanners only on authorized systems.

[Related completed lab](/network-portfolio/videos/lab-6-1-8-open-ports-netstat-wireshark/)


### Deep dive — Tool selection

Ping tests ICMP reachability but filtering can hide responses. Traceroute reveals responding hops, not necessarily the exact return path. ipconfig/ip addr show addressing; arp/ip neigh show neighbor mappings; netstat/ss show sockets; dig/nslookup query DNS. Packet analyzers inspect protocols. LLDP/CDP reveal adjacent devices. Cable and optical tools test physical media.

**Hands-on verification:** Run ipconfig /all, ping gateway, tracert, nslookup and netstat on a lab host; record what each proves and cannot prove.

**Reference for further study:** RFC 792; RFC 1035.

[Practice this objective](../practice/?objective=5.5) · [Interactive exercises](../exercises/)


### Acronyms and definitions

| Term | Meaning and purpose |
| --- | --- |
| LLDP | Link layer discovery protocol; neighbor advertisement |
| CDP | Cisco discovery protocol; Cisco neighbor discovery |
| PCAP | Packet capture; captured network traffic |

### Technical quick-reference table

| Tool | Purpose | Example |
| --- | --- | --- |
| ping | Reachability and RTT | ping gateway |
| traceroute/tracert | Path visibility | Identify responding hops |
| nslookup/dig | DNS query | Check record |
| netstat/ss | Socket state | Identify listeners |
| tcpdump/Wireshark | Packet inspection | Filter by host or protocol |

### Question and answer review

<details class="hr-qa" markdown="1">
<summary>Which command directly queries DNS records?</summary>

**Answer:** nslookup

Ping tests ICMP reachability; traceroute reveals responding hops; nslookup or dig queries DNS; ipconfig or ip displays addressing; netstat or ss shows sockets. Cisco show interfaces reveals counters; show ip route shows routes. Use scanners only on authorized systems.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: traces an unidentified copper cable to its termination?</summary>

**Answer:** Toner

Toner: Traces an unidentified copper cable to its termination. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: visible light helps locate breaks or bends in fiber?</summary>

**Answer:** Visual fault locator

Visual fault locator: Visible light helps locate breaks or bends in fiber. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: inspect learned MAC addresses and associated switch ports on Cisco IOS?</summary>

**Answer:** show mac address-table

show mac address-table: Inspect learned MAC addresses and associated switch ports on Cisco IOS. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: capture and inspect packets from a command-line interface?</summary>

**Answer:** tcpdump

tcpdump: Capture and inspect packets from a command-line interface. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>Which term best matches this networking requirement or observation: measure nearby wireless channels and signal conditions?</summary>

**Answer:** Wi-Fi analyzer

Wi-Fi analyzer: Measure nearby wireless channels and signal conditions. The other choices describe different technologies or conditions and do not match this defining characteristic.

</details>

<details class="hr-qa" markdown="1">
<summary>A Windows host reaches a server by IP but not by hostname. Which tool directly tests DNS resolution?</summary>

**Answer:** nslookup

nslookup queries DNS and helps distinguish name resolution from basic IP reachability.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes Visual fault locator?</summary>

**Answer:** Visible light helps locate breaks or bends in fiber

Visual fault locator refers to visible light helps locate breaks or bends in fiber. The alternatives instead describe Toner, show mac address-table, tcpdump.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes show mac address-table?</summary>

**Answer:** Inspect learned MAC addresses and associated switch ports on Cisco IOS

show mac address-table refers to inspect learned MAC addresses and associated switch ports on Cisco IOS. The alternatives instead describe Toner, Visual fault locator, tcpdump.

</details>

<details class="hr-qa" markdown="1">
<summary>Which statement accurately describes tcpdump?</summary>

**Answer:** Capture and inspect packets from a command-line interface

tcpdump refers to capture and inspect packets from a command-line interface. The alternatives instead describe Toner, Visual fault locator, show mac address-table.

</details>

<details class="hr-qa" markdown="1">
<summary>A Windows client resolves a hostname but TCP 443 connections fail. Which command directly tests that destination port?</summary>

**Answer:** Test-NetConnection host.example -Port 443

Test-NetConnection can test TCP reachability; ipconfig displays settings, arp displays neighbor mappings and hostname identifies the local system.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: reveals responding hops toward a destination?</summary>

**Answer:** traceroute

traceroute: Reveals responding hops toward a destination; nslookup: Queries DNS records; tcpdump: Captures packets for protocol inspection; ipconfig: Displays Windows IP configuration.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes traceroute from the alternatives?</summary>

**Answer:** Reveals responding hops toward a destination

traceroute: Reveals responding hops toward a destination; nslookup: Queries DNS records; tcpdump: Captures packets for protocol inspection; ipconfig: Displays Windows IP configuration.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: queries DNS records?</summary>

**Answer:** nslookup

traceroute: Reveals responding hops toward a destination; nslookup: Queries DNS records; tcpdump: Captures packets for protocol inspection; ipconfig: Displays Windows IP configuration.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes nslookup from the alternatives?</summary>

**Answer:** Queries DNS records

traceroute: Reveals responding hops toward a destination; nslookup: Queries DNS records; tcpdump: Captures packets for protocol inspection; ipconfig: Displays Windows IP configuration.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: captures packets for protocol inspection?</summary>

**Answer:** tcpdump

traceroute: Reveals responding hops toward a destination; nslookup: Queries DNS records; tcpdump: Captures packets for protocol inspection; ipconfig: Displays Windows IP configuration.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes tcpdump from the alternatives?</summary>

**Answer:** Captures packets for protocol inspection

traceroute: Reveals responding hops toward a destination; nslookup: Queries DNS records; tcpdump: Captures packets for protocol inspection; ipconfig: Displays Windows IP configuration.

</details>

<details class="hr-qa" markdown="1">
<summary>Which concept matches this requirement: displays Windows IP configuration?</summary>

**Answer:** ipconfig

traceroute: Reveals responding hops toward a destination; nslookup: Queries DNS records; tcpdump: Captures packets for protocol inspection; ipconfig: Displays Windows IP configuration.

</details>

<details class="hr-qa" markdown="1">
<summary>Which description best distinguishes ipconfig from the alternatives?</summary>

**Answer:** Displays Windows IP configuration

traceroute: Reveals responding hops toward a destination; nslookup: Queries DNS records; tcpdump: Captures packets for protocol inspection; ipconfig: Displays Windows IP configuration.

</details>

<details class="hr-qa" markdown="1">
<summary>A colleague proposes nslookup for a task that requires: reveals responding hops toward a destination. Which alternative is the better match?</summary>

**Answer:** traceroute

traceroute: Reveals responding hops toward a destination; nslookup: Queries DNS records; tcpdump: Captures packets for protocol inspection; ipconfig: Displays Windows IP configuration.

</details>

<details class="hr-qa" markdown="1">
<summary>A Windows host needs its assigned gateway and DNS settings displayed — which answer best fits?</summary>

**Answer:** ipconfig /all

ipconfig /all is the best match for this situation. Ping tests ICMP reachability but filtering can hide responses. Traceroute reveals responding hops, not necessarily the exact return path. ipconfig/ip addr show addressing; arp/ip neigh show neighbor mappings; netstat/ss show sockets; dig/nslookup query DNS. Packet analyzers inspect protocols. LLDP/CDP reveal adjacent devices. Cable and optical tools test physical media.

</details>

<details class="hr-qa" markdown="1">
<summary>A Linux host needs its neighbor cache displayed — which answer best fits?</summary>

**Answer:** ip neigh

ip neigh is the best match for this situation. Ping tests ICMP reachability but filtering can hide responses. Traceroute reveals responding hops, not necessarily the exact return path. ipconfig/ip addr show addressing; arp/ip neigh show neighbor mappings; netstat/ss show sockets; dig/nslookup query DNS. Packet analyzers inspect protocols. LLDP/CDP reveal adjacent devices. Cable and optical tools test physical media.

</details>

<details class="hr-qa" markdown="1">
<summary>A technician needs responding hops toward a destination — which answer best fits?</summary>

**Answer:** traceroute or tracert

traceroute or tracert is the best match for this situation. Ping tests ICMP reachability but filtering can hide responses. Traceroute reveals responding hops, not necessarily the exact return path. ipconfig/ip addr show addressing; arp/ip neigh show neighbor mappings; netstat/ss show sockets; dig/nslookup query DNS. Packet analyzers inspect protocols. LLDP/CDP reveal adjacent devices. Cable and optical tools test physical media.

</details>

<details class="hr-qa" markdown="1">
<summary>A technician needs DNS MX records — which answer best fits?</summary>

**Answer:** dig MX or nslookup type MX

dig MX or nslookup type MX is the best match for this situation. Ping tests ICMP reachability but filtering can hide responses. Traceroute reveals responding hops, not necessarily the exact return path. ipconfig/ip addr show addressing; arp/ip neigh show neighbor mappings; netstat/ss show sockets; dig/nslookup query DNS. Packet analyzers inspect protocols. LLDP/CDP reveal adjacent devices. Cable and optical tools test physical media.

</details>

<details class="hr-qa" markdown="1">
<summary>A technician needs active TCP sockets on Linux — which answer best fits?</summary>

**Answer:** ss

ss is the best match for this situation. Ping tests ICMP reachability but filtering can hide responses. Traceroute reveals responding hops, not necessarily the exact return path. ipconfig/ip addr show addressing; arp/ip neigh show neighbor mappings; netstat/ss show sockets; dig/nslookup query DNS. Packet analyzers inspect protocols. LLDP/CDP reveal adjacent devices. Cable and optical tools test physical media.

</details>

<details class="hr-qa" markdown="1">
<summary>A technician needs packet-level TCP handshake evidence — which answer best fits?</summary>

**Answer:** Wireshark or tcpdump

Wireshark or tcpdump is the best match for this situation. Ping tests ICMP reachability but filtering can hide responses. Traceroute reveals responding hops, not necessarily the exact return path. ipconfig/ip addr show addressing; arp/ip neigh show neighbor mappings; netstat/ss show sockets; dig/nslookup query DNS. Packet analyzers inspect protocols. LLDP/CDP reveal adjacent devices. Cable and optical tools test physical media.

</details>

<details class="hr-qa" markdown="1">
<summary>A technician needs adjacent switch identity via standards-based discovery — which answer best fits?</summary>

**Answer:** LLDP

LLDP is the best match for this situation. Ping tests ICMP reachability but filtering can hide responses. Traceroute reveals responding hops, not necessarily the exact return path. ipconfig/ip addr show addressing; arp/ip neigh show neighbor mappings; netstat/ss show sockets; dig/nslookup query DNS. Packet analyzers inspect protocols. LLDP/CDP reveal adjacent devices. Cable and optical tools test physical media.

</details>

<details class="hr-qa" markdown="1">
<summary>A technician needs Cisco neighbor information — which answer best fits?</summary>

**Answer:** show cdp neighbors

show cdp neighbors is the best match for this situation. Ping tests ICMP reachability but filtering can hide responses. Traceroute reveals responding hops, not necessarily the exact return path. ipconfig/ip addr show addressing; arp/ip neigh show neighbor mappings; netstat/ss show sockets; dig/nslookup query DNS. Packet analyzers inspect protocols. LLDP/CDP reveal adjacent devices. Cable and optical tools test physical media.

</details>

<details class="hr-qa" markdown="1">
<summary>A technician needs switch interface error counters — which answer best fits?</summary>

**Answer:** show interfaces

show interfaces is the best match for this situation. Ping tests ICMP reachability but filtering can hide responses. Traceroute reveals responding hops, not necessarily the exact return path. ipconfig/ip addr show addressing; arp/ip neigh show neighbor mappings; netstat/ss show sockets; dig/nslookup query DNS. Packet analyzers inspect protocols. LLDP/CDP reveal adjacent devices. Cable and optical tools test physical media.

</details>

<details class="hr-qa" markdown="1">
<summary>A technician needs locate an unlabeled copper cable among many — which answer best fits?</summary>

**Answer:** Tone generator and probe

Tone generator and probe is the best match for this situation. Ping tests ICMP reachability but filtering can hide responses. Traceroute reveals responding hops, not necessarily the exact return path. ipconfig/ip addr show addressing; arp/ip neigh show neighbor mappings; netstat/ss show sockets; dig/nslookup query DNS. Packet analyzers inspect protocols. LLDP/CDP reveal adjacent devices. Cable and optical tools test physical media.

</details>


### Visual learning

- [Infrastructure — Passive TAP vs Port Mirroring"
](/network-portfolio/study-diagrams/passive-tap-vs-port-mirroring/)
- [Infrastructure — Cisco Discovery Protocol"
](/network-portfolio/study-diagrams/cisco-discovery-protocol/)
- [Browse portfolio study diagrams](/network-portfolio/study-diagrams/)


<style>.hr-qa{border:1px solid #2563a6;border-radius:8px;padding:.65rem;margin:.5rem 0}.hr-qa summary{cursor:pointer;font-weight:600}</style>
