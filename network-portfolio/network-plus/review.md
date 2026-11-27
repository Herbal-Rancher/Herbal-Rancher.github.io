---
layout: page
hr_theme: network
title: Network+ Objective Review
permalink: /network-portfolio/network-plus/review/
---

[Study Center](/network-portfolio/network-plus/) · [Practice](/network-portfolio/network-plus/practice/) · [Test Readiness Lab](/test-readiness-lab/)

Expanded reference notes with concept contrasts and practical review. Not an exhaustive exam syllabus.

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

