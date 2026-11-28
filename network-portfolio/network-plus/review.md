---
layout: page
hr_theme: network
title: Network+ Objective Review
permalink: /network-portfolio/network-plus/review/
---

[Study Center](/network-portfolio/network-plus/) · [Practice](/network-portfolio/network-plus/practice/) · [Test Readiness Lab](/test-readiness-lab/)

v0.6 technical review: concept contrasts, deployment reasoning, hands-on verification and further reading for all 25 objectives. Not an exhaustive exam syllabus.

<a id="objective-1-1"></a>

## 1.1 — OSI and encapsulation

### Technical distinctions

- **Physical layer:** Signal encoding and bit transmission.
- **Data link layer:** MAC addressing and frame delivery.
- **Network layer:** Logical addressing and routing.
- **Transport layer:** End-to-end port multiplexing and reliability.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 3

Application data is carried by TCP segments or UDP datagrams, then IP packets, then link-layer frames. Routers replace link-layer headers at each routed hop; IP addresses normally persist absent NAT. TCP ports identify endpoints, not physical interfaces. TLS does not fit perfectly into one OSI layer.


### Deep dive — Encapsulation and forwarding

A switch uses destination MAC addresses within a VLAN; a router uses destination IP prefixes between networks. TCP sequence numbers support ordered delivery; UDP has no built-in retransmission. Session and presentation functions include dialogue management and representation, though real protocols span layers.

**Hands-on verification:** Capture a ping on both sides of a router and compare Ethernet addresses, IP addresses and TTL.

**Reference for further study:** RFC 8200.

[Practice this objective](../practice/?objective=1.1) · [Interactive exercises](../exercises/)

<a id="objective-1-2"></a>

## 1.2 — Network appliances

### Technical distinctions

- **Stateful firewall:** Tracks connection state to enforce policy.
- **IDS:** Alerts on suspicious traffic without inline blocking.
- **Load balancer:** Distributes client requests among healthy servers.
- **SAN:** Provides block-level storage access.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 4

Switches learn source MAC addresses and forward frames; routers choose IP routes. A stateful firewall tracks connections; IDS alerts while IPS can block. NAS exposes file shares; SAN exposes block storage. Load balancers distribute requests and proxies mediate connections.


### Deep dive — Appliance placement

A proxy terminates or mediates application connections; a load balancer distributes requests. A CDN caches content near consumers. QoS prioritizes traffic under contention, and TTL limits forwarding lifetime. Wireless controllers coordinate AP configuration. Virtual appliances perform similar functions in software.

**Hands-on verification:** Draw a client-to-web-server path including firewall, load balancer and backend; label where each decision occurs.

**Reference for further study:** RFC 1812.

[Practice this objective](../practice/?objective=1.2) · [Interactive exercises](../exercises/)

<a id="objective-1-3"></a>

## 1.3 — Cloud networking

### Technical distinctions

- **IaaS:** Customer manages guest operating systems.
- **PaaS:** Provider manages runtime and underlying infrastructure.
- **SaaS:** Customer consumes a hosted application.
- **Private endpoint:** Accesses a cloud service through private addressing.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 13

IaaS exposes virtual infrastructure, PaaS manages the runtime, SaaS delivers an application. A virtual private cloud isolates logical networks; route tables and security rules control connectivity. Public, private and hybrid deployment models differ from service models.


### Deep dive — Cloud paths and responsibility

A VPC is a logical network with subnets and routing. Internet gateways provide internet paths; NAT gateways commonly allow outbound connections from private IPv4 subnets. Security groups and subnet ACLs differ by provider; verify statefulness. Elasticity adjusts capacity with demand, while scalability is the ability to grow. NFV implements network functions in software.

**Hands-on verification:** Sketch public and private subnets; trace an outbound update and an inbound web request separately.

**Reference for further study:** NIST SP 800-145.

[Practice this objective](../practice/?objective=1.3) · [Interactive exercises](../exercises/)

<a id="objective-1-4"></a>

## 1.4 — Protocols and ports

### Technical distinctions

- **DNS:** Resolves names using port 53.
- **SSH:** Encrypted remote shell on TCP 22.
- **SNMP:** Queries device management data on UDP 161.
- **NTP:** Synchronizes clocks using UDP 123.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 6

TCP provides ordered reliable delivery; UDP does not guarantee delivery. DNS uses UDP and TCP 53; DHCPv4 uses UDP 67/68; SSH and SFTP use TCP 22; HTTPS commonly uses TCP 443 or UDP 443 for HTTP/3. ICMP and GRE use IP protocol numbers rather than transport ports.

[Related portfolio exercise](/network-portfolio/videos/lab-6-1-7-tcp-three-way-handshake/)


### Deep dive — Service flows

TCP establishes connections; UDP sends datagrams. DNS uses UDP and TCP 53; DHCP uses UDP 67/68. SSH/SFTP use TCP 22; HTTPS normally TCP 443 (HTTP/3 uses QUIC over UDP). SMTP submission commonly uses 587 with STARTTLS, implicit TLS 465. IPsec ESP protects payloads, AH authenticates without encryption, IKE negotiates security associations. GRE alone does not encrypt.

**Hands-on verification:** Use a capture to identify source ephemeral ports and destination service ports; distinguish TCP SYN from UDP.

**Reference for further study:** IANA service name registry.

[Practice this objective](../practice/?objective=1.4) · [Interactive exercises](../exercises/)

<a id="objective-1-5"></a>

## 1.5 — Media and transceivers

### Technical distinctions

- **Single-mode fiber:** Long-distance optical links with narrow core.
- **Multimode fiber:** Shorter optical links with multiple propagation modes.
- **Twinax DAC:** Short direct copper connection between compatible ports.
- **Cat 6A:** Balanced copper supporting 10GBASE-T up to 100 meters.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 7

Copper Ethernet uses electrical signaling; fiber uses light. Single-mode fiber supports long distances; multimode commonly serves shorter links. Match transceiver wavelength, fiber type and link budget. DAC is useful for short rack connections. T568A and T568B specify pair placement.


### Deep dive — Media engineering

Single-mode fiber supports long optical paths; multimode is common for shorter links. Match wavelength, fiber type, connector and supported speed at both ends. DAC is useful for short rack links. Copper Ethernet distance depends on the standard; typical balanced twisted-pair channels are 100 m. Plenum rating concerns fire/smoke requirements, not speed.

**Hands-on verification:** Read transceiver labels and compare both ends before replacing a link; inspect and clean fiber using approved procedures.

**Reference for further study:** IEEE 802.3.

[Practice this objective](../practice/?objective=1.5) · [Interactive exercises](../exercises/)

<a id="objective-1-6"></a>

## 1.6 — Topologies and architectures

### Technical distinctions

- **Spine-leaf:** Predictable east-west paths through spine switches.
- **Star:** Endpoints connect to a central device.
- **Mesh:** Multiple alternate paths between nodes.
- **Three-tier:** Access distribution and core layers.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 2 (unconfirmed)

Star networks centralize connections; mesh provides multiple paths. Spine-leaf designs connect each leaf to each spine to provide predictable east-west paths. Three-tier campus designs separate access, distribution and core. Point-to-point links join two endpoints.


### Deep dive — Topology and traffic

A three-tier campus separates access, distribution and core. A collapsed core combines distribution and core. Spine-leaf fabrics connect each leaf to every spine, supporting predictable east-west paths. Mesh improves path redundancy but adds links and management. North-south traffic crosses a network boundary; east-west moves among internal workloads.

**Hands-on verification:** Draw a campus and a spine-leaf fabric; trace traffic between two servers and from a client to the internet.

**Reference for further study:** RFC 7938.

[Practice this objective](../practice/?objective=1.6) · [Interactive exercises](../exercises/)

<a id="objective-1-7"></a>

## 1.7 — IPv4 addressing and subnetting

### Technical distinctions

- **RFC 1918:** Private IPv4 address space not globally routed.
- **APIPA:** Self-assigned IPv4 link-local address in 169.254/16.
- **CIDR:** Prefix length describes network bits.
- **VLSM:** Different prefix lengths allocate different subnet sizes.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 5

IPv4 uses 32 bits. A /26 leaves six host bits: 64 addresses and normally 62 usable hosts. Network boundaries increment by 64 in the final octet. RFC1918 ranges are 10/8, 172.16/12 and 192.168/16; 169.254/16 is link-local. Longest prefix matching determines route specificity.

[Related portfolio exercise](/network-portfolio/videos/16-31-implement-subnetted-ipv6-addressing-scheme/)


### Deep dive — IPv4 calculations

CIDR prefixes identify network bits; the remaining bits identify addresses. For ordinary /30 or larger LAN subnets, usable hosts are 2^(32-prefix)-2; /31 point-to-point links are a special case. VLSM assigns different prefix sizes. Private ranges are 10/8, 172.16/12 and 192.168/16; 169.254/16 is link-local. Classful ranges are historical, not modern route selection.

**Hands-on verification:** Allocate largest VLSM subnet first, align boundaries, then verify no overlap. Practice /25 through /30 in the exercise lab.

**Reference for further study:** RFC 4632.

[Practice this objective](../practice/?objective=1.7) · [Interactive exercises](../exercises/)

<a id="objective-1-8"></a>

## 1.8 — Modern networking and IPv6

### Technical distinctions

- **SD-WAN:** Policy-driven selection across WAN transports.
- **VXLAN:** Encapsulates layer-two segments over an IP underlay.
- **Zero trust:** Explicit verification and least privilege without implicit network trust.
- **IPv6 SLAAC:** Host forms addresses using advertised prefixes.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 8

SDN separates control decisions from forwarding; VXLAN encapsulates Layer 2 over Layer 3. Zero trust evaluates access explicitly; SASE combines network and security services. Infrastructure as code makes configuration repeatable. IPv6 uses 128-bit addresses, NDP and typically /64 LAN prefixes; dual stack runs both IP versions.

[Related portfolio exercise](/network-portfolio/videos/17-38-ipv6-neighbor-discovery/)


### Deep dive — Programmable networks and IPv6

SDN separates control logic from forwarding; SD-WAN selects paths based on policy and application needs. VXLAN carries layer-2 frames over IP overlays. SASE combines WAN and cloud security capabilities; SSE focuses on security services. Zero trust requires explicit policy decisions. IaC uses versioned desired state and detects drift. IPv6 transition uses dual stack, tunneling or NAT64 as appropriate.

**Hands-on verification:** Compare a desired configuration in Git with actual device state; review a diff before deploying. Practice hexadecimal /64 increments.

**Reference for further study:** RFC 7348; RFC 6146.

[Practice this objective](../practice/?objective=1.8) · [Interactive exercises](../exercises/)

<a id="objective-2-1"></a>

## 2.1 — Routing

### Technical distinctions

- **OSPF:** Link-state routing within an autonomous system.
- **BGP:** Policy-based path-vector routing between autonomous systems.
- **PAT:** Multiple private hosts share a public address using ports.
- **FHRP:** Provides a redundant virtual default gateway.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 9

Routers choose longest matching prefixes before comparing route preferences for identical prefixes. OSPF is link-state, BGP is path-vector, EIGRP is advanced distance-vector. NAT changes addresses; PAT multiplexes flows using ports. A floating static route has a less preferred administrative distance.


### Deep dive — Routing decisions

Forwarding uses longest prefix first. For competing routes to the same prefix, administrative distance selects the source and protocol metrics select paths within a protocol. OSPF uses link state, EIGRP uses DUAL, BGP exchanges policy-based reachability. NAT translates addresses; PAT also distinguishes flows by ports. FHRP provides a shared gateway IP.

**Hands-on verification:** Inspect show ip route and compare a /24 with a default route; test gateway failover in a lab.

**Reference for further study:** RFC 2328; RFC 4271.

[Practice this objective](../practice/?objective=2.1) · [Interactive exercises](../exercises/)

<a id="objective-2-2"></a>

## 2.2 — Switching

### Technical distinctions

- **802.1Q:** Tags Ethernet frames to identify VLANs.
- **RSTP:** Converges loop-free switched topology rapidly.
- **LACP:** Negotiates aggregation of compatible links.
- **Voice VLAN:** Separates voice traffic from ordinary access data.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 10

Access ports normally carry one VLAN; trunks carry multiple VLANs using 802.1Q tags. STP prevents Layer 2 loops; LACP negotiates link aggregation. A Layer 3 interface or router is needed to route between VLANs. MTU mismatch can impair traffic.


### Deep dive — Switch configuration

Access ports associate endpoints with one data VLAN; trunks carry tagged VLANs and may carry native untagged traffic. An SVI provides a logical layer-3 interface. STP blocks redundant layer-2 paths; LACP negotiates bundles. MTU mismatch can cause drops. Voice VLANs separate phone traffic.

**Hands-on verification:** Use show vlan brief, show interfaces trunk, show spanning-tree and show etherchannel summary; verify both ends.

**Reference for further study:** IEEE 802.1Q.

[Practice this objective](../practice/?objective=2.2) · [Interactive exercises](../exercises/)

<a id="objective-2-3"></a>

## 2.3 — Wireless

### Technical distinctions

- **WPA3-Personal:** Uses SAE for password-based wireless authentication.
- **WPA2-Enterprise:** Uses 802.1X authentication with an authentication server.
- **Directional antenna:** Concentrates radio energy toward a specific area.
- **Channel planning:** Reduces interference by coordinating frequency use.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 11

Wi-Fi shares radio airtime. Channel width, interference, signal strength and client density affect performance. WPA3 provides modern authentication and encryption options; enterprise authentication commonly uses 802.1X. A site survey helps determine coverage and channel reuse.


### Deep dive — Wireless design

2.4 GHz generally reaches farther but has fewer nonoverlapping channels; 5 and 6 GHz offer more capacity subject to regulations and client support. WPA3 uses stronger authentication modes; enterprise Wi-Fi commonly uses 802.1X. Channel width trades capacity for interference exposure. Survey coverage, SNR and channel utilization.

**Hands-on verification:** Survey RSSI and SNR at client locations; compare channel utilization before changing power or channel width.

**Reference for further study:** IEEE 802.11.

[Practice this objective](../practice/?objective=2.3) · [Interactive exercises](../exercises/)

<a id="objective-2-4"></a>

## 2.4 — Physical installation

### Technical distinctions

- **UPS:** Provides temporary power during an outage.
- **PDU:** Distributes electrical power to rack equipment.
- **Patch panel:** Terminates and organizes permanent cabling.
- **Hot aisle:** Collects warm exhaust from equipment racks.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 12

Plan rack space, power, cooling, grounding, cable paths and physical access. UPS supplies temporary power; PDU distributes power. Label both cable ends and document patch-panel mappings. Verify environmental limits and redundancy.


### Deep dive — Installation constraints

MDF and IDF organize distribution; patch panels provide termination. Calculate PoE demand against switch budget and UPS capacity against load/runtime. Maintain airflow, temperature, humidity and grounding per code. Use labels, cable management and physical access control.

**Hands-on verification:** Inventory rack power, PoE class, uplink type and UPS runtime; verify against manufacturer ratings.

**Reference for further study:** IEEE 802.3.

[Practice this objective](../practice/?objective=2.4) · [Interactive exercises](../exercises/)

<a id="objective-3-1"></a>

## 3.1 — Documentation and change management

### Technical distinctions

- **Baseline:** Records normal behavior for later comparison.
- **Change approval:** Authorizes planned modifications before implementation.
- **IPAM:** Tracks address allocations and utilization.
- **Logical diagram:** Shows VLANs subnets and routing relationships.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 15

Maintain physical and logical diagrams, IPAM, inventories, baselines and configuration backups. Changes require impact analysis, approval, validation and rollback planning. Track end-of-life and end-of-support separately.


### Deep dive — Operational records

Physical and logical diagrams serve different purposes. IPAM records address allocation; inventory records assets and lifecycle. Baselines describe expected behavior. Change management defines scope, approval, validation and rollback. Configuration backups should be secured and tested. EOL and EOS dates guide replacement.

**Hands-on verification:** Draft a VLAN change with prechecks, rollback triggers, maintenance window and postchecks.

**Reference for further study:** NIST SP 800-128.

[Practice this objective](../practice/?objective=3.1) · [Interactive exercises](../exercises/)

<a id="objective-3-2"></a>

## 3.2 — Monitoring

### Technical distinctions

- **SNMPv3:** Supports authenticated and encrypted management messages.
- **Flow records:** Summarize conversations and traffic volume.
- **Syslog:** Collects timestamped device event messages.
- **Packet capture:** Records individual frames or packets for inspection.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 16

SNMP polls counters and receives notifications; syslog records events; flow telemetry summarizes conversations; packet captures show packet detail. Baselines distinguish normal variation from anomalies. SIEM correlates logs across sources.

[Related portfolio exercise](/network-portfolio/formative-modules/lesson-18-0/summative-network-monitoring-tcp-udp-communications-lab-43/)


### Deep dive — Monitoring evidence

SNMP polls counters and receives notifications; v3 supports authentication and privacy. Flow telemetry summarizes conversations, while packet capture provides packet detail. Syslog centralizes events; synchronized time enables correlation. Baselines and thresholds should reflect normal patterns and alert severity.

**Hands-on verification:** Compare interface errors, utilization and flow data during a reported slowdown; correlate timestamps.

**Reference for further study:** RFC 3411; RFC 5424.

[Practice this objective](../practice/?objective=3.2) · [Interactive exercises](../exercises/)

<a id="objective-3-3"></a>

## 3.3 — Disaster recovery

### Technical distinctions

- **RPO:** Maximum tolerable data loss measured in time.
- **RTO:** Target time to restore a service.
- **Hot site:** Recovery location with ready infrastructure.
- **Cold site:** Recovery location requiring substantial setup.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 17

RPO is acceptable data loss measured in time; RTO is the target restoration time. Hot sites are more ready than cold sites. Redundancy reduces single points of failure but does not replace backups. Test recovery plans and validate restored services.


### Deep dive — Recovery planning

RPO is tolerable data loss measured in time; RTO is target restoration time. MTTR measures repair/recovery duration; MTBF measures operating time between failures. Hot sites are ready sooner than cold sites. HA reduces interruption but does not replace backups. Test restores and failover.

**Hands-on verification:** Design a recovery exercise with explicit RPO/RTO and verify restored data, not merely backup completion.

**Reference for further study:** NIST SP 800-34.

[Practice this objective](../practice/?objective=3.3) · [Interactive exercises](../exercises/)

<a id="objective-3-4"></a>

## 3.4 — IP services

### Technical distinctions

- **DHCP relay:** Forwards DHCP requests across routed boundaries.
- **AAAA record:** Maps a hostname to an IPv6 address.
- **PTR record:** Supports reverse DNS lookup.
- **Router advertisement:** Communicates IPv6 prefixes and default router information.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 14

DHCPv4 uses Discover, Offer, Request, Acknowledge. Relays forward requests across routed boundaries. DNS A and AAAA records map names to IPv4 and IPv6; PTR supports reverse lookup. NTP synchronizes clocks. IPv6 SLAAC uses router advertisements.

[Related portfolio exercise](/network-portfolio/labs/module-6-0/lab-6-6-6-use-nslookup/)


### Deep dive — Address and name services

DHCPv4 uses discover, offer, request, acknowledge; relays forward requests across routed boundaries. IPv6 router advertisements supply default-router information and may enable SLAAC; DHCPv6 can supply addresses or other options. DNS A/AAAA map names, PTR reverses, MX directs mail, CNAME aliases. NTP aligns time.

**Hands-on verification:** Inspect ipconfig /all or ip addr, query A/AAAA/MX with nslookup or dig, then compare gateway reachability.

**Reference for further study:** RFC 2131; RFC 4861; RFC 1035.

[Practice this objective](../practice/?objective=3.4) · [Interactive exercises](../exercises/)

<a id="objective-3-5"></a>

## 3.5 — Access and management

### Technical distinctions

- **SSH:** Encrypted command-line remote administration.
- **Console:** Local management independent of production IP connectivity.
- **API:** Programmatic access to management functions.
- **Jump host:** Controlled intermediary for administrative access.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 18

SSH protects remote CLI sessions; HTTPS protects web management. Out-of-band management uses a separate access path. VPNs provide protected tunnels; split tunneling routes only selected traffic through them. Restrict management access to authorized networks.

[Related portfolio exercise](/network-portfolio/videos/17-40-configure-secure-passwords-and-ssh/)


### Deep dive — Management paths

In-band management shares production connectivity; out-of-band uses a separate path such as console or dedicated management network. SSH protects CLI traffic; HTTPS protects web administration. APIs enable automation but require scoped credentials and audit. Console access is useful when IP configuration is broken.

**Hands-on verification:** Compare console, SSH and web access; verify management ACLs and retain a recovery path before changes.

**Reference for further study:** RFC 4251.

[Practice this objective](../practice/?objective=3.5) · [Interactive exercises](../exercises/)

<a id="objective-4-1"></a>

## 4.1 — Security concepts

### Technical distinctions

- **Least privilege:** Grants only permissions needed for a task.
- **MFA:** Requires authentication factors from different categories.
- **PKI:** Uses certificates and trust chains to bind identities to keys.
- **Encryption:** Protects confidentiality of data using cryptographic keys.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 19

Confidentiality prevents unauthorized disclosure; integrity protects correctness; availability keeps services usable. Authentication establishes identity, authorization grants access, accounting records activity. PKI binds identities to public keys using certificates. Least privilege limits access.


### Deep dive — Security foundations

Confidentiality limits disclosure, integrity protects against unauthorized modification, availability supports access. Authentication verifies identity, authorization grants permissions, accounting records activity. PKI binds identities to public keys through certificates. Segmentation and least privilege reduce exposure; physical controls and data classification complement logical controls.

**Hands-on verification:** Map a management login to authentication, authorization and accounting; inspect certificate hostname, issuer and expiry.

**Reference for further study:** NIST SP 800-207.

[Practice this objective](../practice/?objective=4.1) · [Interactive exercises](../exercises/)

<a id="objective-4-2"></a>

## 4.2 — Network attacks

### Technical distinctions

- **ARP poisoning:** Falsifies IPv4 neighbor mappings.
- **Rogue DHCP:** Supplies unauthorized client network settings.
- **Evil twin:** Imitates a legitimate wireless access point.
- **DDoS:** Overwhelms resources using distributed traffic sources.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 20

ARP spoofing can redirect local traffic; rogue DHCP can supply false settings; DNS poisoning corrupts name resolution. DDoS exhausts resources; social engineering targets people. Investigate anomalies with logs and packet evidence; use segmentation and validated controls.


### Deep dive — Attack recognition

Spoofing falsifies identity information; ARP poisoning can redirect local IPv4 traffic. Rogue DHCP may supply malicious gateway or DNS settings. Evil twin APs imitate trusted Wi-Fi. DoS exhausts resources; DDoS uses distributed sources. Social engineering targets human decisions. VLAN hopping crosses intended layer-2 boundaries. Validate evidence before attribution.

**Hands-on verification:** In an isolated lab, compare legitimate ARP and DHCP messages with a prepared anomalous capture; do not attack production systems.

**Reference for further study:** NIST SP 800-61.

[Practice this objective](../practice/?objective=4.2) · [Interactive exercises](../exercises/)

<a id="objective-4-3"></a>

## 4.3 — Network defense

### Technical distinctions

- **802.1X:** Controls port access through identity authentication.
- **ACL:** Permits or denies traffic using defined match rules.
- **Screened subnet:** Isolates externally accessible services from internal networks.
- **NAC:** Evaluates endpoint access policy and posture.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 21

Disable unused services and ports, patch devices, restrict management, use ACLs and segmentation. 802.1X authenticates network access using a supplicant, authenticator and authentication server. MAC filtering alone is weak because addresses can be spoofed.


### Deep dive — Defense deployment

Use explicit ACL policy, segmentation, secure management, patching and disable unused services. 802.1X controls port access; RADIUS commonly supports network access authentication, TACACS+ commonly supports device administration. DHCP snooping and dynamic ARP inspection mitigate specific local threats when correctly configured. DMZs isolate exposed services; NAC can assess endpoint compliance.

**Hands-on verification:** Build a management-only ACL in a lab; test permitted and denied flows and preserve console recovery.

**Reference for further study:** IEEE 802.1X.

[Practice this objective](../practice/?objective=4.3) · [Interactive exercises](../exercises/)

<a id="objective-5-1"></a>

## 5.1 — Troubleshooting methodology

### Technical distinctions

- **Identify problem:** Collect symptoms scope and recent changes.
- **Test theory:** Use evidence to confirm or reject suspected cause.
- **Verify functionality:** Confirm service restoration and check side effects.
- **Document findings:** Record cause actions and outcome for future reference.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 22

Identify the problem, establish a theory, test it, plan a solution, implement or escalate, verify functionality and preventive measures, document outcomes. If testing disproves a theory, establish a new one. Assess change impact before implementation.

[Existing troubleshooting workspace](/network-portfolio/network-troubleshooting-checklist/) (six-step presentation; planning and implementation are combined there).


### Deep dive — Evidence-driven troubleshooting

Identify scope and symptoms, establish a probable cause, test the theory, plan and implement a fix, verify full functionality and document findings. Escalate when evidence or authorization is insufficient. Change one variable at a time and use rollback plans. Verify with affected users and monitoring.

**Hands-on verification:** Use the portfolio checklist to record observations, hypotheses, test results, fix and verification for a simulated outage.

**Reference for further study:** CompTIA N10-009 objective 5.1.

[Practice this objective](../practice/?objective=5.1) · [Interactive exercises](../exercises/)

<a id="objective-5-2"></a>

## 5.2 — Physical troubleshooting

### Technical distinctions

- **Wire map tester:** Detects incorrect conductor pin assignments.
- **OTDR:** Locates optical fiber faults by reflected light.
- **CRC errors:** Indicate frames failing integrity checks.
- **Duplex mismatch:** Can cause collisions and poor throughput on Ethernet.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 23

Check link state, cable seating, interface counters, speed and duplex, optics and power. CRC errors may indicate physical corruption. A cable certifier validates standards; a toner traces copper; an optical power meter measures received light.


### Deep dive — Physical diagnostics

CRC/FCS errors can indicate corrupted frames from cabling, optics or duplex issues. Check link state, speed, duplex, error trends and transceiver compatibility. Cable testers identify wire faults; certification validates performance; optical power meters measure light. PoE budget and standards must match device demand.

**Hands-on verification:** Compare show interfaces counters before and after a known-good cable swap; avoid looking into optical connectors.

**Reference for further study:** IEEE 802.3.

[Practice this objective](../practice/?objective=5.2) · [Interactive exercises](../exercises/)

<a id="objective-5-3"></a>

## 5.3 — Common network issues

### Technical distinctions

- **DHCP exhaustion:** Prevents new clients obtaining leases when pool is full.
- **Wrong default gateway:** Prevents off-subnet access despite local connectivity.
- **VLAN mismatch:** Places endpoints in unintended broadcast domains.
- **Duplicate IP:** Causes conflicting address ownership and intermittent reachability.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 24

Check VLAN membership, trunk allowances, STP state, IP address, mask, gateway and route table. Duplicate addresses cause intermittent reachability. APIPA suggests a DHCP failure or unavailable server. Isolate scope before changing configuration.


### Deep dive — Service isolation

Check local address, mask, gateway, VLAN, DHCP and DNS separately. A duplicate IP may cause intermittent ARP changes. A missing VLAN on a trunk isolates that VLAN. STP changes can interrupt forwarding. Routing loops consume TTL; wrong default routes break remote reachability. Exhausted DHCP pools affect new leases.

**Hands-on verification:** Test loopback, local gateway, remote IP and DNS name in sequence; compare a working host on the same VLAN.

**Reference for further study:** RFC 5227.

[Practice this objective](../practice/?objective=5.3) · [Interactive exercises](../exercises/)

<a id="objective-5-4"></a>

## 5.4 — Performance troubleshooting

### Technical distinctions

- **Latency:** Measures delay across a path.
- **Jitter:** Measures variation in packet delay.
- **Packet loss:** Measures packets failing to reach destination.
- **Congestion:** Occurs when offered traffic exceeds available forwarding capacity.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 25

Latency measures delay; jitter measures variation in delay; loss measures missing packets; throughput measures achieved rate. Congestion, interference and retransmissions reduce performance. Compare counters and measurements with baselines.


### Deep dive — Performance reasoning

Latency is delay, jitter is delay variation, loss is missing packets, throughput is delivered rate. Congestion causes queues and drops; errors suggest physical problems. Wireless interference reduces effective airtime. Compare baseline, utilization, errors and application timing; avoid assuming high bandwidth guarantees low latency.

**Hands-on verification:** Measure RTT and loss, compare interface queues and utilization, then repeat after a controlled change.

**Reference for further study:** RFC 3393.

[Practice this objective](../practice/?objective=5.4) · [Interactive exercises](../exercises/)

<a id="objective-5-5"></a>

## 5.5 — Diagnostic tools

### Technical distinctions

- **traceroute:** Reveals responding hops toward a destination.
- **nslookup:** Queries DNS records.
- **tcpdump:** Captures packets for protocol inspection.
- **ipconfig:** Displays Windows IP configuration.

**Apply:** Explain how each concept differs from the other three, then identify a real deployment where it is appropriate. [Practice and retest](/network-portfolio/network-plus/practice/).

Udemy section: 26

Ping tests ICMP reachability; traceroute reveals responding hops; nslookup or dig queries DNS; ipconfig or ip displays addressing; netstat or ss shows sockets. Cisco show interfaces reveals counters; show ip route shows routes. Use scanners only on authorized systems.

[Related portfolio exercise](/network-portfolio/videos/lab-6-1-8-open-ports-netstat-wireshark/)


### Deep dive — Tool selection

Ping tests ICMP reachability but filtering can hide responses. Traceroute reveals responding hops, not necessarily the exact return path. ipconfig/ip addr show addressing; arp/ip neigh show neighbor mappings; netstat/ss show sockets; dig/nslookup query DNS. Packet analyzers inspect protocols. LLDP/CDP reveal adjacent devices. Cable and optical tools test physical media.

**Hands-on verification:** Run ipconfig /all, ping gateway, tracert, nslookup and netstat on a lab host; record what each proves and cannot prove.

**Reference for further study:** RFC 792; RFC 1035.

[Practice this objective](../practice/?objective=5.5) · [Interactive exercises](../exercises/)

