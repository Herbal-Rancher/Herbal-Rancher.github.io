---
layout: page
title: Network+ Objective Review
permalink: /network-portfolio/network-plus/review/
---

[Study Center](/network-portfolio/network-plus/) · [Practice](/network-portfolio/network-plus/practice/) · [Test Readiness Lab](/test-readiness-lab/)

Starter reference notes; expand each objective during the study cycle. These original notes are not exhaustive.

<a id="objective-1-1"></a>

## 1.1 — OSI and encapsulation

Udemy section: 3

Application data is carried by TCP segments or UDP datagrams, then IP packets, then link-layer frames. Routers replace link-layer headers at each routed hop; IP addresses normally persist absent NAT. TCP ports identify endpoints, not physical interfaces. TLS does not fit perfectly into one OSI layer.

<a id="objective-1-2"></a>

## 1.2 — Network appliances

Udemy section: 4

Switches learn source MAC addresses and forward frames; routers choose IP routes. A stateful firewall tracks connections; IDS alerts while IPS can block. NAS exposes file shares; SAN exposes block storage. Load balancers distribute requests and proxies mediate connections.

<a id="objective-1-3"></a>

## 1.3 — Cloud networking

Udemy section: 13

IaaS exposes virtual infrastructure, PaaS manages the runtime, SaaS delivers an application. A virtual private cloud isolates logical networks; route tables and security rules control connectivity. Public, private and hybrid deployment models differ from service models.

<a id="objective-1-4"></a>

## 1.4 — Protocols and ports

Udemy section: 6

TCP provides ordered reliable delivery; UDP does not guarantee delivery. DNS uses UDP and TCP 53; DHCPv4 uses UDP 67/68; SSH and SFTP use TCP 22; HTTPS commonly uses TCP 443 or UDP 443 for HTTP/3. ICMP and GRE use IP protocol numbers rather than transport ports.

[Related portfolio exercise](/network-portfolio/videos/lab-6-1-7-tcp-three-way-handshake/)

<a id="objective-1-5"></a>

## 1.5 — Media and transceivers

Udemy section: 7

Copper Ethernet uses electrical signaling; fiber uses light. Single-mode fiber supports long distances; multimode commonly serves shorter links. Match transceiver wavelength, fiber type and link budget. DAC is useful for short rack connections. T568A and T568B specify pair placement.

<a id="objective-1-6"></a>

## 1.6 — Topologies and architectures

Udemy section: 2 (unconfirmed)

Star networks centralize connections; mesh provides multiple paths. Spine-leaf designs connect each leaf to each spine to provide predictable east-west paths. Three-tier campus designs separate access, distribution and core. Point-to-point links join two endpoints.

<a id="objective-1-7"></a>

## 1.7 — IPv4 addressing and subnetting

Udemy section: 5

IPv4 uses 32 bits. A /26 leaves six host bits: 64 addresses and normally 62 usable hosts. Network boundaries increment by 64 in the final octet. RFC1918 ranges are 10/8, 172.16/12 and 192.168/16; 169.254/16 is link-local. Longest prefix matching determines route specificity.

[Related portfolio exercise](/network-portfolio/videos/16-31-implement-subnetted-ipv6-addressing-scheme/)

<a id="objective-1-8"></a>

## 1.8 — Modern networking and IPv6

Udemy section: 8

SDN separates control decisions from forwarding; VXLAN encapsulates Layer 2 over Layer 3. Zero trust evaluates access explicitly; SASE combines network and security services. Infrastructure as code makes configuration repeatable. IPv6 uses 128-bit addresses, NDP and typically /64 LAN prefixes; dual stack runs both IP versions.

[Related portfolio exercise](/network-portfolio/videos/17-38-ipv6-neighbor-discovery/)

<a id="objective-2-1"></a>

## 2.1 — Routing

Udemy section: 9

Routers choose longest matching prefixes before comparing route preferences for identical prefixes. OSPF is link-state, BGP is path-vector, EIGRP is advanced distance-vector. NAT changes addresses; PAT multiplexes flows using ports. A floating static route has a less preferred administrative distance.

<a id="objective-2-2"></a>

## 2.2 — Switching

Udemy section: 10

Access ports normally carry one VLAN; trunks carry multiple VLANs using 802.1Q tags. STP prevents Layer 2 loops; LACP negotiates link aggregation. A Layer 3 interface or router is needed to route between VLANs. MTU mismatch can impair traffic.

<a id="objective-2-3"></a>

## 2.3 — Wireless

Udemy section: 11

Wi-Fi shares radio airtime. Channel width, interference, signal strength and client density affect performance. WPA3 provides modern authentication and encryption options; enterprise authentication commonly uses 802.1X. A site survey helps determine coverage and channel reuse.

<a id="objective-2-4"></a>

## 2.4 — Physical installation

Udemy section: 12

Plan rack space, power, cooling, grounding, cable paths and physical access. UPS supplies temporary power; PDU distributes power. Label both cable ends and document patch-panel mappings. Verify environmental limits and redundancy.

<a id="objective-3-1"></a>

## 3.1 — Documentation and change management

Udemy section: 15

Maintain physical and logical diagrams, IPAM, inventories, baselines and configuration backups. Changes require impact analysis, approval, validation and rollback planning. Track end-of-life and end-of-support separately.

<a id="objective-3-2"></a>

## 3.2 — Monitoring

Udemy section: 16

SNMP polls counters and receives notifications; syslog records events; flow telemetry summarizes conversations; packet captures show packet detail. Baselines distinguish normal variation from anomalies. SIEM correlates logs across sources.

[Related portfolio exercise](/network-portfolio/formative-modules/lesson-18-0/summative-network-monitoring-tcp-udp-communications-lab-43/)

<a id="objective-3-3"></a>

## 3.3 — Disaster recovery

Udemy section: 17

RPO is acceptable data loss measured in time; RTO is the target restoration time. Hot sites are more ready than cold sites. Redundancy reduces single points of failure but does not replace backups. Test recovery plans and validate restored services.

<a id="objective-3-4"></a>

## 3.4 — IP services

Udemy section: 14

DHCPv4 uses Discover, Offer, Request, Acknowledge. Relays forward requests across routed boundaries. DNS A and AAAA records map names to IPv4 and IPv6; PTR supports reverse lookup. NTP synchronizes clocks. IPv6 SLAAC uses router advertisements.

[Related portfolio exercise](/network-portfolio/labs/module-6-0/lab-6-6-6-use-nslookup/)

<a id="objective-3-5"></a>

## 3.5 — Access and management

Udemy section: 18

SSH protects remote CLI sessions; HTTPS protects web management. Out-of-band management uses a separate access path. VPNs provide protected tunnels; split tunneling routes only selected traffic through them. Restrict management access to authorized networks.

[Related portfolio exercise](/network-portfolio/videos/17-40-configure-secure-passwords-and-ssh/)

<a id="objective-4-1"></a>

## 4.1 — Security concepts

Udemy section: 19

Confidentiality prevents unauthorized disclosure; integrity protects correctness; availability keeps services usable. Authentication establishes identity, authorization grants access, accounting records activity. PKI binds identities to public keys using certificates. Least privilege limits access.

<a id="objective-4-2"></a>

## 4.2 — Network attacks

Udemy section: 20

ARP spoofing can redirect local traffic; rogue DHCP can supply false settings; DNS poisoning corrupts name resolution. DDoS exhausts resources; social engineering targets people. Investigate anomalies with logs and packet evidence; use segmentation and validated controls.

<a id="objective-4-3"></a>

## 4.3 — Network defense

Udemy section: 21

Disable unused services and ports, patch devices, restrict management, use ACLs and segmentation. 802.1X authenticates network access using a supplicant, authenticator and authentication server. MAC filtering alone is weak because addresses can be spoofed.

<a id="objective-5-1"></a>

## 5.1 — Troubleshooting methodology

Udemy section: 22

Identify the problem, establish a theory, test it, plan a solution, implement or escalate, verify functionality and preventive measures, document outcomes. If testing disproves a theory, establish a new one. Assess change impact before implementation.

[Existing troubleshooting workspace](/network-portfolio/network-troubleshooting-checklist/) (six-step presentation; planning and implementation are combined there).

<a id="objective-5-2"></a>

## 5.2 — Physical troubleshooting

Udemy section: 23

Check link state, cable seating, interface counters, speed and duplex, optics and power. CRC errors may indicate physical corruption. A cable certifier validates standards; a toner traces copper; an optical power meter measures received light.

<a id="objective-5-3"></a>

## 5.3 — Common network issues

Udemy section: 24

Check VLAN membership, trunk allowances, STP state, IP address, mask, gateway and route table. Duplicate addresses cause intermittent reachability. APIPA suggests a DHCP failure or unavailable server. Isolate scope before changing configuration.

<a id="objective-5-4"></a>

## 5.4 — Performance troubleshooting

Udemy section: 25

Latency measures delay; jitter measures variation in delay; loss measures missing packets; throughput measures achieved rate. Congestion, interference and retransmissions reduce performance. Compare counters and measurements with baselines.

<a id="objective-5-5"></a>

## 5.5 — Diagnostic tools

Udemy section: 26

Ping tests ICMP reachability; traceroute reveals responding hops; nslookup or dig queries DNS; ipconfig or ip displays addressing; netstat or ss shows sockets. Cisco show interfaces reveals counters; show ip route shows routes. Use scanners only on authorized systems.

[Related portfolio exercise](/network-portfolio/videos/lab-6-1-8-open-ports-netstat-wireshark/)

