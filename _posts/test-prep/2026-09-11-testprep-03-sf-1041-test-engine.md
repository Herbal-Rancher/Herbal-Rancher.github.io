---
layout: page
title: "SF 1041 Networks Core | Test Engine"
date: 2026-09-10 14:00:00 -0700
permalink: /network-portfolio/sf-1041-network-exam-prep/test-engine/
categories:
  - portfolio
  - study-tools
  - networking
tags:
  - sf-1041
  - network-engineer
  - practice-test
  - eigrp
  - vlan
  - 802-1x
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
<div class="sf1041-app">
  <div class="sf1041-hero">
    <p class="eyebrow">TIER 3 • PRACTICE ENGINE</p>
    <h1>1041 Networks Core Test Engine</h1>
    <p class="lede">178 original questions built for review → test → identify weakness → retest → repeat.</p>
    <div class="notice">
      <strong>Study-use notice:</strong> These are original practice questions created for this learning portfolio. They are not City of San Francisco exam questions and are not copied from commercial practice banks.
    </div>
  </div>

  <div class="exam-facts">
    <div><strong>178</strong><span>question bank</span></div>
    <div><strong>25</strong><span>City Simulation</span></div>
    <div><strong>60 min</strong><span>simulation timer</span></div>
    <div><strong>→</strong><span>forward-only simulation</span></div>
  </div>

  <div class="engine">
    <h2>Choose a Practice Mode</h2>
    <p class="muted">Progress is stored only in this browser with localStorage. If the browser storage is cleared or you use another device/browser, saved progress will not follow automatically.</p>

    <div class="controls">
      <label>Mode
        <select id="mode">
          <option value="quick">Quick Drill — 10</option>
          <option value="city">City Simulation — 25 / 60 min / forward only</option>
          <option value="challenge">Readiness Challenge — 40 / 75 min</option>
          <option value="focus">Focused Review — selected domain</option>
          <option value="missed">Retest Missed</option>
        </select>
      </label>

      <label>Domain
        <select id="domain">
          <option value="all">All domains</option>
          <option value="routing">Routing & EIGRP</option>
          <option value="switching">Switching & VLANs</option>
          <option value="wireless">Secure Wireless & 802.1X</option>
          <option value="security">Firewalls & Security</option>
          <option value="services">Services, Tools & Monitoring</option>
          <option value="troubleshooting">Troubleshooting</option>
          <option value="documentation">MFP & Documentation</option>
        </select>
      </label>

      <button id="startBtn" type="button">Start / Restart</button>
      <button id="resetStatsBtn" type="button" class="secondary">Reset Saved Progress</button>
    </div>

    <div id="dashboard" class="dashboard"></div>

    <section id="quiz" class="quiz hidden" aria-live="polite">
      <div class="quiz-top">
        <div id="progress"></div>
        <div id="timer"></div>
      </div>
      <div id="domainBadge" class="badge"></div>
      <h3 id="questionText"></h3>
      <div id="answers" class="answers"></div>
      <div id="feedback" class="feedback hidden"></div>
      <div class="actions">
        <button id="submitBtn" type="button">Submit Answer</button>
        <button id="nextBtn" type="button" class="hidden">Next Question →</button>
      </div>
    </section>

    <section id="results" class="results hidden"></section>
  </div>

  <details class="troubleshoot">
    <summary>Engine Troubleshooting</summary>
    <h3>If the page loads but buttons do not work</h3>
    <ul>
      <li>Open the browser developer console and look for a JavaScript error.</li>
      <li>Confirm the entire script block at the bottom of this Markdown file is present after the last edit.</li>
      <li>Confirm your Jekyll theme allows inline JavaScript in page content.</li>
    </ul>

    <h3>If saved progress disappears</h3>
    <ul>
      <li>The engine uses browser <code>localStorage</code>.</li>
      <li>Progress is specific to the browser/device and can be erased by clearing site data.</li>
    </ul>

    <h3>If navigation returns 404</h3>
    <ul>
      <li>Confirm the three <code>permalink</code> values match the links used in the navigation.</li>
      <li>If your local site uses a different base path, update the three navigation links consistently.</li>
    </ul>

    <h3>If a question appears incorrect</h3>
    <ul>
      <li>Search this file for the question ID shown in the source bank, such as <code>r13</code> or <code>sec20</code>.</li>
      <li>Each question has one <code>c</code> value representing the zero-based correct-answer index.</li>
      <li>The explanation is stored in the same question object under <code>e</code>.</li>
    </ul>
  </details>
</div>

<style>
.sf1041-app { max-width: 980px; margin: 0 auto; }
.sf1041-hero { padding: 1.25rem 0 .5rem; }
.eyebrow { font-size: .78rem; letter-spacing: .08em; font-weight: 700; opacity: .72; }
.lede { font-size: 1.08rem; line-height: 1.6; }
.notice { border-left: 4px solid currentColor; padding: .8rem 1rem; margin: 1rem 0; background: rgba(127,127,127,.08); }
.exam-facts { display: grid; grid-template-columns: repeat(4,1fr); gap: .7rem; margin: 1rem 0 1.5rem; }
.exam-facts div { border: 1px solid rgba(127,127,127,.35); border-radius: 12px; padding: .8rem; text-align: center; }
.exam-facts strong { display:block; font-size: 1.35rem; }
.exam-facts span { font-size: .78rem; opacity: .75; }
.engine { border-top: 3px solid currentColor; padding-top: 1rem; }
.controls { display:flex; flex-wrap:wrap; gap:.8rem; align-items:end; margin:1rem 0; }
.controls label { display:flex; flex-direction:column; gap:.3rem; font-size:.85rem; font-weight:600; }
select, button { font:inherit; }
select { padding:.65rem; border-radius:8px; border:1px solid rgba(127,127,127,.45); background:inherit; color:inherit; }
button { padding:.7rem 1rem; border-radius:8px; border:1px solid currentColor; cursor:pointer; font-weight:700; }
button.secondary { background:transparent; color:inherit; }
.dashboard { display:grid; grid-template-columns:repeat(auto-fit,minmax(150px,1fr)); gap:.65rem; margin:1rem 0 1.2rem; }
.stat { border:1px solid rgba(127,127,127,.3); border-radius:10px; padding:.7rem; }
.stat strong { display:block; font-size:1.2rem; }
.quiz, .results, .troubleshoot { border:1px solid rgba(127,127,127,.35); border-radius:12px; padding:1.1rem; margin-top:1rem; }
.quiz-top { display:flex; justify-content:space-between; gap:1rem; font-weight:700; }
.badge { display:inline-block; margin:.9rem 0 .2rem; padding:.22rem .55rem; border:1px solid rgba(127,127,127,.4); border-radius:999px; font-size:.75rem; }
.answers { display:grid; gap:.6rem; margin:1rem 0; }
.answer { display:flex; gap:.65rem; align-items:flex-start; border:1px solid rgba(127,127,127,.3); border-radius:10px; padding:.75rem; cursor:pointer; }
.answer:hover { background:rgba(127,127,127,.08); }
.feedback { margin:1rem 0; padding:.9rem; border-radius:10px; background:rgba(127,127,127,.10); line-height:1.55; }
.actions { display:flex; gap:.7rem; }
.hidden { display:none !important; }
.muted { opacity:.78; }
.results table { width:100%; border-collapse:collapse; margin-top:1rem; }
.results th,.results td { text-align:left; padding:.45rem; border-bottom:1px solid rgba(127,127,127,.25); }
.troubleshoot summary { cursor:pointer; font-weight:700; }
@media (max-width:650px){
  .exam-facts { grid-template-columns:repeat(2,1fr); }
  .controls { align-items:stretch; }
  .controls label, .controls button { width:100%; }
}
</style>

<script>
/*
========================================================
SF 1041 NETWORKS CORE TEST ENGINE
Troubleshooting map:
1) QUESTION BANK       -> const QUESTIONS
2) DOMAIN LABELS       -> const domainNames
3) LOCAL STORAGE       -> loadStats / saveStats
4) TEST BUILDING       -> buildSet
5) QUESTION DISPLAY    -> render
6) ANSWER PROCESSING   -> submit
7) RESULTS             -> finish
========================================================
*/
(() => {
  const QUESTIONS = [{"id": "r1", "d": "routing", "q": "A router has two static routes to 10.20.0.0/16. The primary route uses administrative distance 1 and the backup uses administrative distance 200. What is the purpose of the second route?", "a": ["Provide a floating static backup route", "Load-balance all traffic equally", "Replace longest-prefix matching", "Advertise the route with EIGRP"], "c": 0, "e": "A static route with a higher administrative distance can remain less preferred until the lower-AD route disappears; this is commonly called a floating static route."}, {"id": "r2", "d": "routing", "q": "Which EIGRP term identifies the current best next-hop route to a destination?", "a": ["Designated router", "Successor", "Feasible successor", "Area border router"], "c": 1, "e": "In EIGRP, the successor is the current best loop-free route. A feasible successor is a qualified backup."}, {"id": "r3", "d": "routing", "q": "Which algorithm is most closely associated with EIGRP path calculation and loop-free convergence?", "a": ["SPF", "DUAL", "Bellman-Ford only", "CSMA/CD"], "c": 1, "e": "EIGRP uses the Diffusing Update Algorithm (DUAL)."}, {"id": "r4", "d": "routing", "q": "A router learns the same prefix from internal EIGRP and OSPF. Using common default administrative distances, which route is preferred?", "a": ["OSPF because 110 is lower than 90", "EIGRP because 90 is lower than 110", "Both are always installed equally", "The route with the highest metric"], "c": 1, "e": "Administrative distance compares route sources. Internal EIGRP commonly uses AD 90; OSPF uses 110, so EIGRP is preferred when prefix length is equal."}, {"id": "r5", "d": "routing", "q": "Which routing protocol is primarily used to exchange routes between autonomous systems on the public Internet?", "a": ["RIP", "OSPF", "BGP", "STP"], "c": 2, "e": "BGP is the path-vector exterior gateway protocol used for interdomain routing."}, {"id": "r6", "d": "routing", "q": "Which protocol is a link-state interior gateway protocol that calculates shortest paths using cost?", "a": ["OSPF", "RIP", "BGP", "ARP"], "c": 0, "e": "OSPF is a link-state IGP and uses cost as its routing metric."}, {"id": "r7", "d": "routing", "q": "A /30 IPv4 subnet is traditionally useful for which situation?", "a": ["A LAN needing 254 hosts", "A point-to-point link needing two usable host addresses", "A wireless guest network", "A VLAN needing 62 hosts"], "c": 1, "e": "A /30 provides four addresses: network, two usable hosts, and broadcast."}, {"id": "r8", "d": "routing", "q": "A router has routes 10.0.0.0/8 and 10.10.20.0/24. A packet is destined for 10.10.20.55. Which route is selected first?", "a": ["10.0.0.0/8 because it was learned first", "10.10.20.0/24 because it is the longest prefix match", "Whichever has the higher administrative distance", "The default route"], "c": 1, "e": "Routers first prefer the most specific matching route—the route with the longest prefix."}, {"id": "r9", "d": "routing", "q": "RIP primarily uses which metric?", "a": ["Cost", "Hop count", "Bandwidth-delay composite only", "Path attributes"], "c": 1, "e": "RIP uses hop count and treats 16 hops as unreachable."}, {"id": "r10", "d": "routing", "q": "A host is 192.168.10.70/26. Which network contains the host?", "a": ["192.168.10.0/26", "192.168.10.64/26", "192.168.10.128/26", "192.168.10.192/26"], "c": 1, "e": "A /26 has blocks of 64 addresses: .0, .64, .128, .192. Address .70 belongs to 192.168.10.64/26."}, {"id": "r11", "d": "routing", "q": "What is the primary purpose of a default route?", "a": ["Reach destinations not matched by a more specific route", "Replace ARP on a LAN", "Assign addresses to clients", "Prevent switching loops"], "c": 0, "e": "The default route is used when the routing table has no more-specific destination match."}, {"id": "r12", "d": "routing", "q": "Which EIGRP concept describes a loop-free backup path that satisfies the feasibility condition?", "a": ["Feasible successor", "Root port", "Default gateway", "Designated router"], "c": 0, "e": "A feasible successor is a qualified loop-free backup route in EIGRP."}, {"id": "s1", "d": "switching", "q": "Two switches must carry VLANs 10, 20, and 30 across one Ethernet link. What should that link normally be configured as?", "a": ["Access port", "802.1Q trunk", "Routed port with DHCP", "Port mirror"], "c": 1, "e": "An 802.1Q trunk carries traffic for multiple VLANs over one physical link."}, {"id": "s2", "d": "switching", "q": "A workstation connected to an access port should normally send Ethernet frames for its VLAN in what form?", "a": ["Tagged with every VLAN", "Untagged on the access link", "Encapsulated in GRE", "Encrypted with IPsec"], "c": 1, "e": "Endpoint access links are normally untagged; the switch associates the port with the configured access VLAN."}, {"id": "s3", "d": "switching", "q": "What problem is Spanning Tree Protocol designed to prevent?", "a": ["IP address exhaustion", "Layer 2 switching loops", "DNS cache poisoning", "Wireless interference"], "c": 1, "e": "STP creates a loop-free logical Layer 2 topology when redundant physical paths exist."}, {"id": "s4", "d": "switching", "q": "Why would two physical switch links be placed in an LACP EtherChannel?", "a": ["To create one logical link for redundancy and aggregate capacity", "To assign DHCP leases", "To create an IPsec tunnel", "To provide DNS failover"], "c": 0, "e": "LACP negotiates link aggregation, combining compatible links into one logical channel."}, {"id": "s5", "d": "switching", "q": "A PC was moved to a new desk. It can reach the Internet and a local printer but cannot reach servers available only to its department. What should be checked first?", "a": ["The monitor cable", "The access VLAN assignment on the new switchport", "The DNS root hints", "The WAN BGP ASN"], "c": 1, "e": "A wrong access VLAN can place the user in a network that has general connectivity but lacks access to department-specific resources."}, {"id": "s6", "d": "switching", "q": "What is an SVI on a managed switch?", "a": ["A logical Layer 3 interface associated with a VLAN", "A physical fiber transceiver", "A wireless antenna type", "A spanning-tree timer"], "c": 0, "e": "A Switch Virtual Interface is a logical interface for a VLAN and can provide management or routing functions depending on the switch."}, {"id": "s7", "d": "switching", "q": "A switchport connects an IP phone with a PC attached through the phone. Which design best supports separation of voice and data?", "a": ["Disable VLANs on the port", "Use a data access VLAN plus a voice VLAN", "Make the PC a trunk", "Assign both devices the same static public IP"], "c": 1, "e": "A voice VLAN allows the phone's voice traffic to be separated while the attached PC uses the data access VLAN."}, {"id": "s8", "d": "switching", "q": "What is the native VLAN on an 802.1Q trunk used for?", "a": ["Traffic sent untagged on that trunk", "Only multicast traffic", "Only voice traffic", "The STP root bridge address"], "c": 0, "e": "On an 802.1Q trunk, the native VLAN is the VLAN whose frames are normally transmitted untagged."}, {"id": "s9", "d": "switching", "q": "A new redundant cable between two switches causes a broadcast storm and widespread instability. Which control is most directly relevant?", "a": ["STP/RSTP", "DHCP relay", "RADIUS", "NAT"], "c": 0, "e": "A Layer 2 loop can cause broadcast storms; STP/RSTP is designed to block redundant paths as needed."}, {"id": "s10", "d": "switching", "q": "Which table does a Layer 2 switch consult to forward a unicast Ethernet frame?", "a": ["ARP table only", "MAC address table", "DNS cache", "Routing information base only"], "c": 1, "e": "A Layer 2 switch forwards frames based on destination MAC addresses learned in its MAC address table."}, {"id": "w1", "d": "wireless", "q": "In 802.1X, what role does a wireless access point or Ethernet switch usually perform?", "a": ["Supplicant", "Authenticator", "Certificate authority", "DNS resolver"], "c": 1, "e": "The client is the supplicant, the AP/switch is the authenticator, and a service such as RADIUS commonly acts as the authentication server."}, {"id": "w2", "d": "wireless", "q": "Which service is commonly used as the centralized authentication server for enterprise 802.1X access?", "a": ["RADIUS", "DHCP", "NTP", "TFTP"], "c": 0, "e": "RADIUS commonly supplies AAA services for 802.1X enterprise network authentication."}, {"id": "w3", "d": "wireless", "q": "Employees should authenticate to Wi-Fi with individual company credentials instead of a shared wireless password. Which approach best fits?", "a": ["WPA2/WPA3 Enterprise with 802.1X", "Open Wi-Fi with MAC filtering only", "WEP", "A single WPA2-Personal PSK"], "c": 0, "e": "Enterprise Wi-Fi uses 802.1X/EAP with centralized identity rather than one pre-shared key for everyone."}, {"id": "w4", "d": "wireless", "q": "A microwave causes intermittent Wi-Fi failures near a break room. Which band is most likely affected?", "a": ["2.4 GHz", "5 GHz only", "6 GHz only", "60 GHz"], "c": 0, "e": "Microwave ovens can interfere with 2.4 GHz Wi-Fi."}, {"id": "w5", "d": "wireless", "q": "Which set represents the commonly used non-overlapping 20 MHz channels in the 2.4 GHz band in the United States?", "a": ["1, 6, 11", "2, 7, 12", "36, 40, 44", "149, 153, 157"], "c": 0, "e": "Channels 1, 6, and 11 are the classic non-overlapping 20 MHz choices in 2.4 GHz in the U.S."}, {"id": "w6", "d": "wireless", "q": "Visitors must accept an acceptable-use policy before getting temporary Internet access. What is the most appropriate wireless feature?", "a": ["Captive portal", "STP", "LACP", "Port mirroring"], "c": 0, "e": "Captive portals commonly present terms, sign-in, or temporary access workflows to guests."}, {"id": "w7", "d": "wireless", "q": "A user can roam through a building while remaining on the same wireless network served by several APs. What design concept enables this?", "a": ["Extended service set with coordinated APs", "Ad hoc networking only", "A point-to-point bridge only", "NAT overload"], "c": 0, "e": "An extended service set uses multiple APs to provide a common WLAN across a larger area and supports roaming."}, {"id": "w8", "d": "wireless", "q": "Which 802.1X component runs on the endpoint requesting network access?", "a": ["Supplicant", "Authenticator", "RADIUS proxy only", "Root bridge"], "c": 0, "e": "The endpoint software/device requesting access is the supplicant."}, {"id": "sec1", "d": "security", "q": "After a firewall change, users cannot reach an HTTPS server. What should be verified first in the relevant firewall policy?", "a": ["That TCP 443 is permitted from the required source to the server", "That STP priority is 32768", "That DHCP option 6 is disabled", "That the wireless channel is 11"], "c": 0, "e": "Firewall troubleshooting starts with the intended flow: source, destination, protocol, port, direction, action, and rule order."}, {"id": "sec2", "d": "security", "q": "Which remote management protocol provides encrypted command-line access to network devices?", "a": ["Telnet", "SSH", "TFTP", "SNMPv1"], "c": 1, "e": "SSH encrypts the management session; Telnet sends session contents in plaintext."}, {"id": "sec3", "d": "security", "q": "What is the key advantage of out-of-band management during a production network outage?", "a": ["It uses an independent management path", "It automatically fixes routing loops", "It eliminates authentication", "It converts copper to fiber"], "c": 0, "e": "OOB management is intentionally separated from the production data path, so administrators may still reach devices during production failures."}, {"id": "sec4", "d": "security", "q": "Which IPsec component provides confidentiality through encryption of the protected payload?", "a": ["AH", "ESP", "ARP", "GRE alone"], "c": 1, "e": "ESP provides encryption and can also provide integrity/authentication. AH does not provide confidentiality."}, {"id": "sec5", "d": "security", "q": "Why segment operational-technology or sensitive systems into dedicated VLANs/security zones?", "a": ["To reduce unnecessary access and lateral movement", "To eliminate the need for routing", "To guarantee zero packet loss", "To replace authentication"], "c": 0, "e": "Segmentation limits which systems can directly communicate and supports policy enforcement between zones."}, {"id": "sec6", "d": "security", "q": "A passive IDS needs to inspect copies of traffic traversing a switch without sitting inline. Which switch feature is appropriate?", "a": ["Port mirroring/SPAN", "DHCP snooping only", "LACP", "Native VLAN"], "c": 0, "e": "Port mirroring copies selected traffic to a monitoring port where a passive IDS can inspect it."}, {"id": "sec7", "d": "security", "q": "Which security principle is best represented by allowing a help-desk group only the network permissions needed for its assigned duties?", "a": ["Least privilege", "Open access", "Implicit trust", "Broadcast forwarding"], "c": 0, "e": "Least privilege limits access to the minimum necessary for the role."}, {"id": "sec8", "d": "security", "q": "What is the best reason to disable unused switchports?", "a": ["Reduce unauthorized physical network access opportunities", "Increase DNS cache size", "Improve BGP convergence", "Change the subnet mask"], "c": 0, "e": "Unused active ports can provide unauthorized access if someone connects a device; disabling them reduces attack surface."}, {"id": "svc1", "d": "services", "q": "A Windows client has an address beginning with 169.254 and cannot reach remote networks. What is the leading suspicion?", "a": ["DHCP lease failure", "Correct static addressing", "A working default route", "A valid public address"], "c": 0, "e": "169.254.0.0/16 is IPv4 link-local/APIPA space and often indicates the client could not obtain a DHCP lease."}, {"id": "svc2", "d": "services", "q": "Which DNS record identifies the mail server responsible for receiving mail for a domain?", "a": ["A", "CNAME", "MX", "PTR"], "c": 2, "e": "MX records identify mail exchangers for a domain."}, {"id": "svc3", "d": "services", "q": "Which DNS record creates an alias from one hostname to another hostname?", "a": ["CNAME", "MX", "PTR", "NS only"], "c": 0, "e": "CNAME is the canonical-name alias record."}, {"id": "svc4", "d": "services", "q": "Why is NTP especially important when a SIEM correlates logs from many network devices?", "a": ["Consistent timestamps make event timelines reliable", "It assigns VLAN IDs", "It encrypts every log", "It replaces syslog"], "c": 0, "e": "Event correlation depends on aligned clocks so timestamps from different devices can be compared accurately."}, {"id": "svc5", "d": "services", "q": "Which SNMP version is preferred when authentication and encryption of management traffic are required?", "a": ["SNMPv1", "SNMPv2c", "SNMPv3", "All versions provide the same security"], "c": 2, "e": "SNMPv3 supports security features including authentication and privacy/encryption."}, {"id": "svc6", "d": "services", "q": "You can ping a web server but need to test whether TCP ports 80 and 443 are reachable. Which tool is best suited among these choices?", "a": ["nmap", "arp", "nslookup", "hostname"], "c": 0, "e": "A port scanner such as nmap can test whether specific TCP/UDP ports are reachable/open; ping alone tests ICMP reachability."}, {"id": "svc7", "d": "services", "q": "Which command-line tool is most directly used to query DNS records?", "a": ["nslookup or dig", "traceroute only", "arp only", "show spanning-tree only"], "c": 0, "e": "nslookup and dig query DNS and help distinguish name-resolution problems from general IP connectivity problems."}, {"id": "svc8", "d": "services", "q": "What is the primary role of a SIEM compared with a simple syslog collector?", "a": ["Correlate and analyze events across multiple sources", "Assign IP addresses", "Switch Ethernet frames", "Provide wireless encryption"], "c": 0, "e": "A SIEM ingests events and adds correlation, analysis, detection, and investigation capabilities."}, {"id": "svc9", "d": "services", "q": "A router must forward DHCP broadcasts from a client VLAN to a DHCP server on another subnet. What feature is commonly required?", "a": ["DHCP relay/IP helper", "STP root guard", "Port mirroring", "NAT64 only"], "c": 0, "e": "DHCP relay (often configured as an IP helper on Cisco devices) forwards DHCP requests across routed boundaries."}, {"id": "svc10", "d": "services", "q": "A VoIP call becomes choppy whenever users upload large files. What network feature is most directly used to prioritize voice traffic?", "a": ["QoS", "ARP inspection", "Port mirroring", "DNSSEC"], "c": 0, "e": "QoS can classify and prioritize latency-sensitive traffic such as voice during congestion."}, {"id": "t1", "d": "troubleshooting", "q": "A workstation is physically connected, but neither the NIC nor switchport shows a link light. Which issue should be investigated before DNS or the default gateway?", "a": ["Layer 1/port state", "MX records", "BGP path selection", "NTP offset"], "c": 0, "e": "No link light points first to physical connectivity, transceiver/cabling, NIC, or an administratively disabled port."}, {"id": "t2", "d": "troubleshooting", "q": "A user can ping 8.8.8.8 but cannot browse to example.com by name. Which service should be tested next?", "a": ["DNS", "STP", "LACP", "PoE"], "c": 0, "e": "Successful IP reachability with failed hostname access strongly suggests a name-resolution problem."}, {"id": "t3", "d": "troubleshooting", "q": "A PC can ping its own IP address but cannot ping its default gateway. Other PCs in the same VLAN work. What should you check early?", "a": ["Local mask/VLAN/port and Layer 2 path", "Internet BGP advertisements first", "MX record", "NTP stratum"], "c": 0, "e": "The failure is local to the host or its access path; verify addressing, VLAN membership, link, ARP, and switchport state before chasing WAN issues."}, {"id": "t4", "d": "troubleshooting", "q": "You changed a switch configuration to fix a problem. What should happen before closing the ticket?", "a": ["Verify full functionality and document the result", "Delete all logs", "Change unrelated settings", "Skip validation if ping succeeds once"], "c": 0, "e": "Troubleshooting is not complete until the solution is validated, preventive measures are considered, and findings/actions are documented."}, {"id": "t5", "d": "troubleshooting", "q": "Which tool is most useful for discovering where along a routed path packets stop or take an unexpected route?", "a": ["traceroute/tracert", "arp only", "whoami", "format"], "c": 0, "e": "Traceroute/tracert reveals the sequence of routed hops toward a destination."}, {"id": "t6", "d": "troubleshooting", "q": "Users in one VLAN cannot reach a server in another VLAN, but hosts within each VLAN communicate normally. Which area becomes a primary focus?", "a": ["Inter-VLAN routing and Layer 3 policy", "Keyboard drivers", "Wireless channel width only", "Local printer toner"], "c": 0, "e": "Intra-VLAN success with inter-VLAN failure points toward routing, SVI/subinterface state, gateway configuration, ACLs, or firewall policy."}, {"id": "t7", "d": "troubleshooting", "q": "A web application is slow, and you need to determine the actual routed path taken to the server. Which tool is the best first choice?", "a": ["traceroute/tracert", "nslookup", "arp", "show vlan only"], "c": 0, "e": "Traceroute/tracert maps the Layer 3 path and can reveal asymmetric, unexpected, or high-latency hops."}, {"id": "t8", "d": "troubleshooting", "q": "A DHCP scope is exhausted after many new users arrive. What is the most direct corrective action?", "a": ["Increase available addresses or redesign the scope/subnet", "Change every switch to a trunk", "Disable DNS", "Lower STP priority"], "c": 0, "e": "If the scope has no leases available, expand the available address pool or redesign addressing as appropriate."}, {"id": "t9", "d": "troubleshooting", "q": "A theory says the firewall is blocking a service. What is the strongest next action?", "a": ["Test the theory with a targeted connectivity or rule/log check", "Immediately replace the core switch", "Change several unrelated settings", "Document the issue as resolved"], "c": 0, "e": "After establishing a theory, test it with the least disruptive evidence-gathering action before implementing broader changes."}, {"id": "t10", "d": "troubleshooting", "q": "A workstation moved to another subnet can reach IP addresses but an internal hostname resolves to an old address only on that workstation. What should you inspect?", "a": ["Local DNS cache/hosts file and resolver settings", "STP root bridge only", "EtherChannel hashing", "Power supply redundancy"], "c": 0, "e": "A client-specific name-resolution error points to local caching, hosts-file overrides, or resolver configuration before an enterprise-wide DNS failure."}, {"id": "d1", "d": "documentation", "q": "A network printer should keep the same IPv4 address while still receiving its configuration from DHCP. What is a clean solution?", "a": ["DHCP reservation tied to the printer MAC address", "APIPA", "Random address selection", "A different VLAN every reboot"], "c": 0, "e": "A DHCP reservation gives the device a predictable address while retaining centralized DHCP management."}, {"id": "d2", "d": "documentation", "q": "A multifunction printer is reachable by IP but users cannot print by hostname. Which component should be checked first?", "a": ["DNS/name resolution", "STP root priority", "EIGRP feasible successor", "LACP system priority"], "c": 0, "e": "If IP connectivity works but name-based access fails, test DNS records, suffix/search settings, and client resolution."}, {"id": "d3", "d": "documentation", "q": "Which information is most valuable in a logical network topology diagram?", "a": ["Subnets, VLANs, routing relationships, and logical connections", "Desk colors", "Employee vacation dates", "Printer paper size only"], "c": 0, "e": "Logical diagrams document how networks, VLANs, subnets, routes, and services relate independent of exact physical placement."}, {"id": "d4", "d": "documentation", "q": "Before changing a production firewall rule, which documentation practice best supports rollback?", "a": ["Record the current rule/configuration and the intended change", "Delete the old configuration immediately", "Rely on memory", "Change several rules at once without notes"], "c": 0, "e": "Capturing the current state and exact proposed change creates a rollback path and improves auditability."}, {"id": "d5", "d": "documentation", "q": "After resolving an intermittent network outage, what should the ticket include?", "a": ["Symptoms, evidence, root cause, change made, validation, and outcome", "Only 'fixed'", "Only the user's name", "A list of unrelated commands"], "c": 0, "e": "Good operational documentation preserves the evidence trail and allows others to understand, reproduce, and audit the resolution."}, {"id": "d6", "d": "documentation", "q": "A networked MFP is placed in a new VLAN and can reach devices in its subnet but not its print server on another subnet. Which setting should be verified first on the MFP?", "a": ["Default gateway and subnet mask", "Paper tray size", "Toner percentage", "Display brightness"], "c": 0, "e": "Communication beyond the local subnet depends on correct IP addressing, subnet mask, and default gateway."}, {"id": "d7", "d": "documentation", "q": "Which change-management approach minimizes risk during a network repair?", "a": ["Make the minimum necessary change, validate, and document", "Make every possible improvement at once", "Skip the baseline", "Avoid rollback planning"], "c": 0, "e": "Small, controlled changes make cause/effect easier to assess and reduce collateral impact."}, {"id": "d8", "d": "documentation", "q": "Which item belongs in a physical topology diagram rather than only a logical topology?", "a": ["Rack/device locations and physical cable links", "DNS CNAME purpose", "EIGRP metric formula only", "User password policy"], "c": 0, "e": "Physical diagrams capture hardware placement and physical cabling; logical diagrams focus on traffic and network relationships."}, {"id": "r13", "d": "routing", "q": "A router has 10.10.0.0/16 learned by OSPF and 10.10.10.0/24 learned by RIP. Which route is used for traffic to 10.10.10.50?", "a": ["The OSPF route because OSPF has a lower administrative distance", "The RIP route because /24 is a longer prefix match", "Both routes are ignored", "The default route"], "c": 1, "e": "Longest-prefix match is evaluated before administrative distance. The /24 route is more specific than /16."}, {"id": "r14", "d": "routing", "q": "What does administrative distance measure?", "a": ["Trustworthiness of a route source", "Number of Layer 2 hops", "Interface bandwidth only", "Wireless signal strength"], "c": 0, "e": "Administrative distance ranks the relative trustworthiness of routes learned from different sources."}, {"id": "r15", "d": "routing", "q": "Which command output would be most useful for verifying which route a Cisco router will use to reach a remote subnet?", "a": ["show ip route", "show vlan brief", "show mac address-table", "show cdp neighbors"], "c": 0, "e": "The routing table shows installed routes, next hops, route sources, and prefix lengths."}, {"id": "r16", "d": "routing", "q": "A route marked with code D in a Cisco IPv4 routing table was most likely learned by which protocol?", "a": ["EIGRP", "OSPF", "RIP", "BGP"], "c": 0, "e": "Cisco routing tables commonly use D to identify EIGRP-learned routes."}, {"id": "r17", "d": "routing", "q": "A route marked with code O in a Cisco IPv4 routing table was learned by which protocol?", "a": ["OSPF", "EIGRP", "RIP", "BGP"], "c": 0, "e": "Cisco routing tables use O for OSPF routes."}, {"id": "r18", "d": "routing", "q": "Two routers running EIGRP are directly connected but never become neighbors. Which item should be checked early?", "a": ["Whether the EIGRP autonomous system/process parameters match and interfaces can communicate", "Whether both switches use the same STP root priority", "Whether DNS has an MX record", "Whether the clients use APIPA"], "c": 0, "e": "EIGRP peers require compatible EIGRP configuration and Layer 3 reachability on the shared link."}, {"id": "r19", "d": "routing", "q": "What is convergence in dynamic routing?", "a": ["The time until routers agree on current reachable paths after a topology change", "The process of assigning MAC addresses", "The encryption of routing updates", "The creation of VLAN trunks"], "c": 0, "e": "Convergence describes the network reaching a consistent routing state after changes."}, {"id": "r20", "d": "routing", "q": "Which route is represented by 0.0.0.0/0 in IPv4?", "a": ["Default route", "Loopback route", "Multicast route", "Broadcast route"], "c": 0, "e": "0.0.0.0/0 matches any IPv4 destination not matched by a more specific route."}, {"id": "r21", "d": "routing", "q": "A router interface is configured 172.16.8.126/25. Which address is the broadcast address for that subnet?", "a": ["172.16.8.127", "172.16.8.255", "172.16.8.126", "172.16.8.1"], "c": 0, "e": "A /25 splits the /24 into .0-.127 and .128-.255. .126 is in the first subnet, whose broadcast is .127."}, {"id": "r22", "d": "routing", "q": "Which subnet mask corresponds to /27?", "a": ["255.255.255.224", "255.255.255.240", "255.255.255.192", "255.255.255.248"], "c": 0, "e": "A /27 has 27 network bits, producing 255.255.255.224."}, {"id": "r23", "d": "routing", "q": "A router has a directly connected route and an OSPF route to the same exact prefix. Which is normally preferred?", "a": ["The directly connected route", "The OSPF route", "Whichever has more hops", "Whichever was learned last"], "c": 0, "e": "Directly connected routes have the strongest preference and are installed when the connected interface is up/up."}, {"id": "r24", "d": "routing", "q": "Which statement best describes a routing metric?", "a": ["A value a routing protocol uses to compare candidate paths", "A password used to authenticate users", "A VLAN identifier", "A switchport error counter"], "c": 0, "e": "Metrics are protocol-specific path values such as cost, hop count, or composite metrics."}, {"id": "s11", "d": "switching", "q": "Which command is most useful for quickly checking access VLAN assignments on Cisco switchports?", "a": ["show vlan brief", "show ip route", "show arp", "show clock"], "c": 0, "e": "show vlan brief displays VLANs and associated access ports."}, {"id": "s12", "d": "switching", "q": "Which command is most useful for checking whether a Cisco switchport is operating as an access port or trunk?", "a": ["show interfaces switchport", "show users", "show ip protocols", "show ntp associations"], "c": 0, "e": "show interfaces switchport displays administrative/operational mode and VLAN information."}, {"id": "s13", "d": "switching", "q": "A trunk between two switches carries VLAN 10 but not VLAN 30. VLAN 30 exists on both switches. What should be checked next?", "a": ["Whether VLAN 30 is allowed on the trunk", "Whether the DNS server has a PTR record", "Whether EIGRP AD is 90", "Whether the printer has toner"], "c": 0, "e": "A trunk can restrict its allowed VLAN list; a missing VLAN there blocks its traffic across the link."}, {"id": "s14", "d": "switching", "q": "What is the primary purpose of a switch MAC address table?", "a": ["Map learned source MAC addresses to switch interfaces", "Map hostnames to IP addresses", "Map IP addresses to DNS servers", "Store routing protocol metrics"], "c": 0, "e": "Switches learn source MAC addresses and associate them with ingress ports for Layer 2 forwarding."}, {"id": "s15", "d": "switching", "q": "A switch receives a frame for an unknown unicast destination MAC. What does it normally do within that VLAN?", "a": ["Flood it out eligible ports except the ingress port", "Discard it immediately", "Send it only to the default gateway", "Convert it to multicast"], "c": 0, "e": "Unknown unicast frames are flooded within the VLAN until the destination MAC is learned."}, {"id": "s16", "d": "switching", "q": "Why is a native VLAN mismatch on an 802.1Q trunk undesirable?", "a": ["Untagged traffic can be placed into different VLANs on each end", "It increases fiber attenuation", "It disables DNS", "It changes EIGRP metrics"], "c": 0, "e": "If trunk ends disagree on the native VLAN, untagged frames may be interpreted as belonging to different VLANs."}, {"id": "s17", "d": "switching", "q": "Which STP value is used first when electing the root bridge?", "a": ["Lowest bridge ID", "Highest MAC address", "Highest interface bandwidth", "Lowest IP address"], "c": 0, "e": "STP elects the switch with the lowest bridge ID, which includes bridge priority and MAC-related information."}, {"id": "s18", "d": "switching", "q": "What is the purpose of PortFast on an appropriate access port?", "a": ["Allow an edge port to transition to forwarding quickly", "Create an EtherChannel", "Encrypt switch traffic", "Route between VLANs"], "c": 0, "e": "PortFast is intended for edge ports and avoids normal STP listening/learning delays; it should not be used casually on switch-to-switch links."}, {"id": "s19", "d": "switching", "q": "Which technology should be used to bundle multiple parallel Ethernet links into one logical connection between switches?", "a": ["EtherChannel/link aggregation", "NAT", "RADIUS", "DNSSEC"], "c": 0, "e": "Link aggregation combines compatible links, and LACP can negotiate the bundle."}, {"id": "s20", "d": "switching", "q": "A Layer 2 switch has no IP address on its physical access ports. How can it still be remotely managed by IP?", "a": ["Configure a management SVI with an IP address and appropriate default gateway", "Assign an IP address to every access port", "Use only a MAC address over the Internet", "Enable RIP on every workstation"], "c": 0, "e": "Layer 2 managed switches commonly use an SVI for IP-based management."}, {"id": "s21", "d": "switching", "q": "What happens when two endpoints are accidentally configured with the same IPv4 address on one VLAN?", "a": ["Intermittent connectivity and ARP conflicts can occur", "STP elects a new root", "The switch forms an EtherChannel", "RADIUS disables both users automatically"], "c": 0, "e": "Duplicate IPv4 addresses can cause conflicting ARP mappings and unstable connectivity."}, {"id": "s22", "d": "switching", "q": "Which VLAN design most directly limits a broadcast to one logical group of switchports?", "a": ["Separate the devices into a dedicated VLAN", "Put all devices in VLAN 1", "Disable STP", "Use one large flat subnet"], "c": 0, "e": "Each VLAN is a separate Layer 2 broadcast domain."}, {"id": "s23", "d": "switching", "q": "A switchport is administratively down. Which Cisco configuration command is generally needed under the interface to enable it?", "a": ["no shutdown", "ip route", "router eigrp", "service password-encryption"], "c": 0, "e": "no shutdown administratively enables the interface."}, {"id": "w9", "d": "wireless", "q": "What is EAP primarily used for in an 802.1X enterprise authentication design?", "a": ["Carry authentication methods between the supplicant and authentication infrastructure", "Assign VLAN tags to trunks", "Replace IP routing", "Provide DHCP leases"], "c": 0, "e": "EAP is the framework used by 802.1X to support authentication methods."}, {"id": "w10", "d": "wireless", "q": "In an 802.1X wired deployment, which device typically acts as the authenticator?", "a": ["Access switch", "DNS server", "DHCP client", "Web proxy"], "c": 0, "e": "On wired networks, the switchport commonly controls access as the 802.1X authenticator."}, {"id": "w11", "d": "wireless", "q": "Which Wi-Fi security approach is weakest and considered obsolete?", "a": ["WEP", "WPA3-Enterprise", "WPA2-Enterprise", "802.1X with EAP"], "c": 0, "e": "WEP is obsolete and cryptographically weak."}, {"id": "w12", "d": "wireless", "q": "A high-density office has many modern clients. Which Wi-Fi generation is particularly designed to improve efficiency in dense environments?", "a": ["802.11ax / Wi-Fi 6", "802.11b", "802.11a only", "802.11g only"], "c": 0, "e": "802.11ax includes features designed to improve efficiency and capacity in dense deployments."}, {"id": "w13", "d": "wireless", "q": "Users near the edge of an AP's coverage area have low throughput and frequent retries. What is the most likely category of issue?", "a": ["Weak signal / signal degradation", "Incorrect MX record", "STP root election", "EIGRP feasible successor"], "c": 0, "e": "Low signal-to-noise ratio near the edge of coverage commonly causes retries and reduced rates."}, {"id": "w14", "d": "wireless", "q": "What does an omnidirectional antenna generally do?", "a": ["Radiates energy broadly around the antenna in the horizontal plane", "Focuses nearly all energy in one narrow direction", "Encrypts wireless frames", "Assigns DHCP addresses"], "c": 0, "e": "Omnidirectional antennas provide broad surrounding coverage rather than a narrow focused beam."}, {"id": "w15", "d": "wireless", "q": "A point-to-point wireless bridge must span two buildings. Which antenna type is usually preferred?", "a": ["Directional antenna", "Omnidirectional antenna", "NFC antenna", "Bluetooth-only antenna"], "c": 0, "e": "Directional antennas focus RF energy toward the remote endpoint and are common for point-to-point links."}, {"id": "w16", "d": "wireless", "q": "What is a major security weakness of relying only on MAC filtering for Wi-Fi admission?", "a": ["MAC addresses can be observed and spoofed", "MAC addresses are encrypted by DNS", "It prevents all roaming", "It requires fiber"], "c": 0, "e": "MAC filtering is not strong identity authentication because MAC addresses can be learned and impersonated."}, {"id": "w17", "d": "wireless", "q": "Which device can centrally manage configuration for many enterprise access points?", "a": ["Wireless LAN controller", "Layer 1 hub", "Patch panel", "Passive tap"], "c": 0, "e": "A wireless LAN controller can centralize policy, configuration, and coordination for managed APs."}, {"id": "w18", "d": "wireless", "q": "Why might an administrator steer capable clients from 2.4 GHz toward 5 GHz?", "a": ["Reduce congestion on 2.4 GHz and use additional spectrum", "Because 5 GHz always travels farther", "Because 2.4 GHz cannot use WPA2", "Because 5 GHz requires no authentication"], "c": 0, "e": "Band steering can help distribute clients and reduce pressure on crowded 2.4 GHz spectrum."}, {"id": "w19", "d": "wireless", "q": "A company wants per-user wireless authentication and dynamic policy assignment. Which combination is most aligned with that goal?", "a": ["802.1X + RADIUS", "WEP + hidden SSID", "Open Wi-Fi + MAC filtering only", "Ad hoc mode + DHCP"], "c": 0, "e": "802.1X with RADIUS supports centralized user/device authentication and can return authorization attributes."}, {"id": "w20", "d": "wireless", "q": "Which factor most directly influences whether two nearby 2.4 GHz APs interfere with each other?", "a": ["Channel overlap and RF energy", "DNS TTL", "Routing administrative distance", "Printer queue name"], "c": 0, "e": "Overlapping channels and RF energy in the same area are major sources of co-channel/adjacent-channel interference."}, {"id": "sec9", "d": "security", "q": "A firewall rule allows TCP 443 from any source when only a small administration subnet needs access. What principle should guide the correction?", "a": ["Least privilege", "Maximum broadcast scope", "Open trust", "First-hop redundancy"], "c": 0, "e": "Restrict the rule to the minimum source, destination, service, and access required."}, {"id": "sec10", "d": "security", "q": "Which AAA function determines what an authenticated user is permitted to do?", "a": ["Authorization", "Authentication", "Accounting", "Address resolution"], "c": 0, "e": "Authentication verifies identity; authorization determines permitted actions; accounting records activity."}, {"id": "sec11", "d": "security", "q": "Which AAA function records user activity for auditing or billing?", "a": ["Accounting", "Authentication", "Authorization", "Address translation"], "c": 0, "e": "Accounting tracks session and usage information."}, {"id": "sec12", "d": "security", "q": "What is the purpose of an ACL applied to routed traffic?", "a": ["Permit or deny traffic based on defined packet criteria", "Elect an STP root bridge", "Resolve hostnames", "Negotiate LACP"], "c": 0, "e": "ACLs enforce traffic policy using fields such as source/destination addresses, protocols, and ports."}, {"id": "sec13", "d": "security", "q": "Why is rule order important in many firewall and ACL implementations?", "a": ["Earlier matching rules may determine the action before later rules are evaluated", "Rules are sorted only by VLAN number", "DNS rewrites rule order", "STP controls firewall order"], "c": 0, "e": "Many policy engines evaluate rules top-down or by precedence; an earlier match can shadow a later rule."}, {"id": "sec14", "d": "security", "q": "Which protocol should replace Telnet for remote administration of a router over an IP network?", "a": ["SSH", "FTP", "TFTP", "HTTP"], "c": 0, "e": "SSH provides encrypted remote terminal access."}, {"id": "sec15", "d": "security", "q": "What is a screened subnet/DMZ commonly used for?", "a": ["Place externally accessible services in a controlled network segment", "Create a wireless mesh", "Assign DHCP reservations", "Prevent all routing"], "c": 0, "e": "A DMZ isolates public-facing services from more trusted internal networks."}, {"id": "sec16", "d": "security", "q": "A company wants to block unauthorized personal devices from obtaining normal network access on wired and wireless ports using identity-based access control. Which technology is a strong fit?", "a": ["802.1X/NAC", "NTP", "STP", "NAT overload"], "c": 0, "e": "802.1X and NAC can enforce authentication and policy before granting normal network access."}, {"id": "sec17", "d": "security", "q": "Which version of SNMP avoids relying only on plaintext-style community strings and supports stronger security?", "a": ["SNMPv3", "SNMPv1", "SNMPv2c", "All are equivalent"], "c": 0, "e": "SNMPv3 adds authenticated and privacy-capable management security."}, {"id": "sec18", "d": "security", "q": "What is the main difference between an IDS and an IPS?", "a": ["An IDS detects/alerts, while an IPS can be inline and block traffic", "An IDS routes packets and an IPS assigns IP addresses", "An IDS is wireless-only", "There is no difference"], "c": 0, "e": "IDS is generally monitoring/detection oriented; IPS is commonly inline and can actively prevent malicious traffic."}, {"id": "sec19", "d": "security", "q": "Which attack can occur when an attacker sends forged ARP messages to associate the attacker's MAC address with another host's IP?", "a": ["ARP poisoning", "DNS zone transfer", "Tailgating", "VLAN pruning"], "c": 0, "e": "ARP poisoning manipulates ARP mappings and can enable interception or disruption on a local network."}, {"id": "sec20", "d": "security", "q": "Which Layer 2 attack attempts to force a switch to flood frames by exhausting its MAC address table?", "a": ["MAC flooding", "Smurf attack", "DNS poisoning", "Route summarization"], "c": 0, "e": "MAC flooding attempts to overflow the CAM/MAC table so traffic may be flooded more broadly."}, {"id": "sec21", "d": "security", "q": "What security control limits the number or identity of MAC addresses learned on a switch access port?", "a": ["Port security", "OSPF", "NTP", "PAT"], "c": 0, "e": "Switch port security can restrict learned/allowed MAC addresses and define violation actions."}, {"id": "sec22", "d": "security", "q": "A remote branch connects to headquarters across the public Internet and needs confidentiality for site-to-site traffic. Which solution is most appropriate?", "a": ["IPsec site-to-site VPN", "GRE without encryption", "Open HTTP tunnel", "STP"], "c": 0, "e": "IPsec site-to-site VPNs provide protected communication between networks across untrusted transport."}, {"id": "sec23", "d": "security", "q": "Which concept separates management traffic from user data traffic to reduce exposure and improve control?", "a": ["Management network/VLAN segmentation", "Broadcast amplification", "Open guest access", "Flat addressing"], "c": 0, "e": "A dedicated management network or VLAN isolates administrative access from ordinary user traffic."}, {"id": "svc11", "d": "services", "q": "Which DHCP message sequence is commonly summarized as DORA?", "a": ["Discover, Offer, Request, Acknowledge", "Detect, Open, Route, Accept", "Discover, Operate, Relay, Assign", "Drop, Observe, Retry, Alert"], "c": 0, "e": "The common IPv4 DHCP lease sequence is Discover, Offer, Request, Acknowledge."}, {"id": "svc12", "d": "services", "q": "Which DNS record maps an IPv4 hostname to an address?", "a": ["A", "AAAA", "MX", "PTR"], "c": 0, "e": "An A record maps a name to an IPv4 address."}, {"id": "svc13", "d": "services", "q": "Which DNS record maps a hostname to an IPv6 address?", "a": ["AAAA", "A", "MX", "CNAME only"], "c": 0, "e": "AAAA records map names to IPv6 addresses."}, {"id": "svc14", "d": "services", "q": "Which DNS record is used for reverse lookup from IP address to hostname?", "a": ["PTR", "MX", "A", "SOA"], "c": 0, "e": "PTR records support reverse DNS mappings."}, {"id": "svc15", "d": "services", "q": "A DNS record was changed but many clients still receive the old value. Which setting most directly affects how long resolvers may cache the old record?", "a": ["TTL", "STP priority", "MTU", "Duplex"], "c": 0, "e": "DNS TTL defines how long a cached record can remain valid before refresh."}, {"id": "svc16", "d": "services", "q": "Which protocol commonly transports centralized log messages from network devices?", "a": ["Syslog", "ARP", "ICMP only", "STP"], "c": 0, "e": "Syslog is widely used for centralized event and log messages."}, {"id": "svc17", "d": "services", "q": "Which monitoring approach should be established so future utilization spikes can be recognized as abnormal?", "a": ["Performance baseline", "Random cable changes", "Disable logging", "Clear all counters every hour"], "c": 0, "e": "A baseline defines normal performance and utilization so deviations can be detected."}, {"id": "svc18", "d": "services", "q": "Which protocol is primarily used to synchronize device clocks?", "a": ["NTP", "SNMP", "SMTP", "SFTP"], "c": 0, "e": "NTP synchronizes clocks across networked systems."}, {"id": "svc19", "d": "services", "q": "Which command would show the local ARP cache on many systems?", "a": ["arp -a", "nslookup", "traceroute", "hostname"], "c": 0, "e": "arp -a is commonly used to display current IPv4 ARP mappings."}, {"id": "svc20", "d": "services", "q": "Which tool can capture and inspect packets to verify whether a TCP handshake or DNS response is actually occurring?", "a": ["Packet analyzer such as tcpdump/Wireshark", "Text editor", "Calculator", "Print spooler"], "c": 0, "e": "Packet capture tools reveal protocol exchanges and are valuable when higher-level symptoms are ambiguous."}, {"id": "svc21", "d": "services", "q": "What does NAT/PAT commonly allow in an IPv4 enterprise network?", "a": ["Multiple internal private hosts to communicate externally using fewer public addresses", "A switch to prevent loops", "A DNS server to resolve MX records", "An AP to authenticate with EAP"], "c": 0, "e": "NAT translates addresses; PAT commonly lets many private hosts share a public address by tracking transport-layer ports."}, {"id": "svc22", "d": "services", "q": "Which protocol is best associated with checking basic IP reachability using echo requests and replies?", "a": ["ICMP", "SMTP", "LDAP", "SIP"], "c": 0, "e": "ping uses ICMP echo requests/replies for basic reachability testing."}, {"id": "t11", "d": "troubleshooting", "q": "A user reports 'the network is down.' What is the best first action?", "a": ["Clarify symptoms, scope, timing, and affected services", "Replace the router immediately", "Reconfigure all VLANs", "Delete the ticket"], "c": 0, "e": "Start by defining the problem: who/what is affected, what changed, when it began, and what still works."}, {"id": "t12", "d": "troubleshooting", "q": "Only one workstation is affected while nearby users on the same switch are working. What does this suggest?", "a": ["Start with the endpoint and its access port before assuming a network-wide outage", "Replace the core router first", "Change the WAN provider", "Readdress every VLAN"], "c": 0, "e": "A single-host scope points first to local configuration, cabling, NIC, switchport, or endpoint-specific policy."}, {"id": "t13", "d": "troubleshooting", "q": "Every user in one VLAN lost connectivity immediately after a trunk change. What should be inspected first?", "a": ["Trunk status and allowed/native VLAN configuration", "All client keyboards", "Public DNS root servers", "Printer drivers"], "c": 0, "e": "A change affecting one entire VLAN across a trunk strongly points to trunk/VLAN configuration."}, {"id": "t14", "d": "troubleshooting", "q": "A client has correct IP, mask, DNS, and link status but the configured default gateway address is wrong. Which symptom is most likely?", "a": ["Local-subnet communication may work while remote networks fail", "Nothing on the local subnet will ever work", "DNS automatically fixes routing", "The switch will elect a new root"], "c": 0, "e": "The default gateway is required to reach destinations outside the local subnet."}, {"id": "t15", "d": "troubleshooting", "q": "A switch interface shows many CRC/FCS errors. Which category should be investigated?", "a": ["Physical link problems such as cabling, interference, or duplex issues", "DNS aliases", "EIGRP autonomous system only", "Printer permissions"], "c": 0, "e": "CRC/FCS errors indicate corrupted Ethernet frames and often point to physical-layer or link-negotiation problems."}, {"id": "t16", "d": "troubleshooting", "q": "A user can reach a server by hostname and IP but the application on TCP 8443 fails. What should be tested next?", "a": ["Whether TCP 8443 is listening and permitted through any firewall", "Whether DHCP DORA is working", "Whether STP is enabled on every access port", "Whether the user has an MX record"], "c": 0, "e": "General IP and DNS connectivity are working; focus next on the target service, port, and filtering path."}, {"id": "t17", "d": "troubleshooting", "q": "A router interface is administratively down. What will a Cisco show interface status commonly indicate?", "a": ["Administratively down/down", "Up/up", "Up/down only because of DNS", "Forwarding/blocking"], "c": 0, "e": "An interface shut by configuration is reported as administratively down."}, {"id": "t18", "d": "troubleshooting", "q": "After implementing a fix, which action best verifies the root problem is actually solved?", "a": ["Reproduce the original workflow and confirm expected end-to-end service", "Only confirm the device powers on", "Clear logs without testing", "Assume success because the configuration saved"], "c": 0, "e": "Validation should test the original symptom and the required end-to-end functionality."}, {"id": "t19", "d": "troubleshooting", "q": "A route exists to a destination, but packets fail only after a new ACL was applied. Which evidence is most useful next?", "a": ["ACL hit counters/logs and a targeted traffic test", "DNS MX records", "STP root priority", "Printer queue status"], "c": 0, "e": "The timing and scope point to policy filtering; counters and targeted tests can confirm whether the ACL is matching the flow."}, {"id": "t20", "d": "troubleshooting", "q": "A device can ping its gateway but cannot ping a remote destination. Which layer should be investigated next?", "a": ["Routing/path beyond the local gateway", "Local link light only", "Keyboard layout", "Printer toner"], "c": 0, "e": "Gateway reachability confirms the local subnet path; next inspect routing and downstream policy/path."}, {"id": "t21", "d": "troubleshooting", "q": "A wireless user has excellent signal strength but poor performance during busy hours only. What should be considered?", "a": ["Channel utilization/congestion", "A bad default gateway solely because signal is strong", "A failed cable on every AP", "An MX record"], "c": 0, "e": "Strong signal does not guarantee available airtime; congestion and interference can reduce throughput."}, {"id": "t22", "d": "troubleshooting", "q": "Which sequence best reflects a disciplined troubleshooting approach?", "a": ["Identify → theorize → test → plan → implement → verify → document", "Implement → guess → document → identify", "Replace everything → test later", "Document → close → investigate"], "c": 0, "e": "A structured methodology reduces unnecessary changes and produces a traceable result."}, {"id": "t23", "d": "troubleshooting", "q": "A server is reachable from the same VLAN but not from a different VLAN. The gateway interfaces are up. Which control should be reviewed next?", "a": ["Inter-VLAN routing policy such as ACL/firewall rules", "The server monitor resolution", "The wireless SSID name", "Printer paper settings"], "c": 0, "e": "If gateway interfaces are operational, Layer 3 policy between VLANs becomes a likely cause."}, {"id": "d9", "d": "documentation", "q": "Which document should show which switchport a server is physically connected to?", "a": ["Physical topology / port map", "DNS zone file only", "Routing protocol database only", "Wireless heat map only"], "c": 0, "e": "Physical topology and port-map documentation records physical device and cable relationships."}, {"id": "d10", "d": "documentation", "q": "Which document should most clearly show VLAN IDs, subnets, gateways, and routed relationships?", "a": ["Logical network topology", "Building evacuation map", "Hardware purchase receipt", "Printer toner log"], "c": 0, "e": "Logical topology captures Layer 2/3 relationships independent of exact physical placement."}, {"id": "d11", "d": "documentation", "q": "What is the best reason to record validation steps after a network change?", "a": ["Provide evidence the intended service works and make future troubleshooting repeatable", "Increase broadcast traffic", "Avoid backups", "Replace monitoring"], "c": 0, "e": "Validation records show what was tested and what successful behavior looked like."}, {"id": "d12", "d": "documentation", "q": "A troubleshooting runbook should be written primarily so that another technician can do what?", "a": ["Follow a repeatable sequence of checks and actions", "Memorize every password", "Ignore change control", "Bypass documentation"], "c": 0, "e": "Runbooks turn operational knowledge into a repeatable procedure."}, {"id": "d13", "d": "documentation", "q": "What should a rollback plan contain?", "a": ["The steps and information needed to return to the known-good prior state", "Only the new configuration", "Only the user's phone number", "A list of unrelated upgrades"], "c": 0, "e": "Rollback planning defines how to restore the prior stable state if the change fails."}, {"id": "d14", "d": "documentation", "q": "A network printer's address was changed. Which records may need updating so users and monitoring systems continue to find it reliably?", "a": ["DNS, DHCP reservation or IPAM, and device documentation as applicable", "STP root bridge only", "BGP ASN only", "Wireless channel plan only"], "c": 0, "e": "Address changes should be reflected consistently in relevant naming, addressing, monitoring, and inventory documentation."}, {"id": "d15", "d": "documentation", "q": "Which practice makes configuration troubleshooting easiest after several changes?", "a": ["Record each controlled change with timestamp, reason, and validation result", "Batch many unrelated changes without notes", "Delete the previous configuration", "Rely on memory"], "c": 0, "e": "A clear change history makes it easier to correlate symptoms with specific modifications and roll back safely."}];

  /* Advanced layer: closer distractors and multi-clue scenarios. */
  const ADVANCED_QUESTIONS = [
    {id:"r25",d:"routing",q:"A router has 10.40.0.0/16 via OSPF, 10.40.8.0/24 via internal EIGRP, and 10.40.8.128/25 as a static route with AD 200. Which route forwards a packet to 10.40.8.150?",a:["The OSPF /16 because its AD is lower than 200","The EIGRP /24 because internal EIGRP has AD 90","The static /25 because it is the longest prefix match","All three are load-balanced because they overlap"],c:2,e:"The static /25 is the most specific match. Prefix length is considered before administrative distance.",x:"OSPF and EIGRP would matter only if the competing routes had the same prefix length. Overlapping routes are not automatically load-balanced."},
    {id:"r26",d:"routing",q:"An EIGRP neighbor remains listed, but a destination has no route in the routing table. The topology table shows the destination as active. What is the best interpretation?",a:["The route is stable and forwarding normally","EIGRP is searching for a replacement and awaiting query replies","The neighbor relationship must have failed completely","A feasible successor was installed immediately"],c:1,e:"An active EIGRP route is undergoing recomputation and query processing; passive is the normal stable state.",x:"A neighbor can remain established while one destination is active. If a usable feasible successor had been installed immediately, extended querying might not be needed."},
    {id:"r27",d:"routing",q:"Two equal-prefix EIGRP routes are available. Route A has lower delay but a slower minimum-bandwidth link; Route B has higher delay but faster links. What should the technician use to determine the selected path?",a:["Hop count only","The composite EIGRP metric using bandwidth and delay by default","Administrative distance because both routes are EIGRP","The route learned most recently"],c:1,e:"EIGRP compares its composite metric, classically based on minimum bandwidth and cumulative delay by default.",x:"Administrative distance compares different route sources, not two routes from the same EIGRP process. EIGRP does not choose by recency or hop count alone."},
    {id:"r28",d:"routing",q:"A branch router has a primary dynamic route and a static backup route, but both are installed simultaneously for the same prefix. What is the most precise correction?",a:["Increase the backup static route's administrative distance above the dynamic route","Decrease the static route's prefix length by one in every case","Increase the dynamic protocol's metric","Add a second default gateway to each workstation"],c:0,e:"A floating static route must have a higher administrative distance than the preferred dynamic route for the same prefix.",x:"Changing prefix length changes route specificity and may affect different traffic. A protocol metric does not override a competing route source's administrative distance."},

    {id:"s24",d:"switching",q:"Users in VLAN 30 communicate locally on both switches, but traffic for VLAN 30 cannot cross the inter-switch link. VLANs 10 and 20 cross normally. What should be checked first?",a:["Whether VLAN 30 is allowed on the trunk","Whether STP is disabled globally","Whether every VLAN uses a different native VLAN","Whether the users have public IP addresses"],c:0,e:"A selective single-VLAN failure across an otherwise working trunk strongly suggests that VLAN is missing from the allowed list or trunk path.",x:"A broad STP failure would normally affect more than one VLAN or link. Native-VLAN differences and public addressing do not best explain this selective symptom."},
    {id:"s25",d:"switching",q:"Four links are intended to form an LACP EtherChannel. Three bundle successfully; one is suspended. Which action is best first?",a:["Compare the suspended port's speed, duplex, trunk, native, and allowed-VLAN settings with the channel","Enable PortFast on all four inter-switch ports","Change LACP active to passive on both ends","Delete the VLAN database"],c:0,e:"One failed member amid three working members points to an interface compatibility mismatch.",x:"PortFast is inappropriate for a normal switch-to-switch bundle. Passive/passive prevents negotiation, and deleting VLANs creates a wider outage."},
    {id:"s26",d:"switching",q:"An access port with PortFast receives BPDUs after someone connects an unmanaged switch. Which control most directly protects the topology?",a:["Root guard on every routed interface","BPDU Guard on the edge port","DHCP snooping on the trunk","LACP passive mode"],c:1,e:"BPDU Guard can err-disable a PortFast edge port when an unexpected BPDU appears.",x:"Root guard addresses unexpected superior BPDUs but BPDU Guard is the direct edge-port protection described. DHCP snooping and LACP solve different problems."},
    {id:"s27",d:"switching",q:"An IP phone works, but the PC connected through the phone receives an address from the wrong department. What is the best switchport check?",a:["Data access VLAN assignment while preserving the voice VLAN","Native VLAN on the WAN router","STP root priority on the core","EIGRP variance"],c:0,e:"The phone and attached PC can use separate voice and data VLAN assignments on the same access port.",x:"The phone working narrows the problem to the data side of the port. WAN routing, root election, and EIGRP do not directly assign the PC's local VLAN."},

    {id:"w21",d:"wireless",q:"A wireless client associates to the correct SSID and reaches the 802.1X authenticator, but the RADIUS server reports an unknown issuing CA. What should be corrected first?",a:["The client's certificate trust chain or certificate deployment","The AP's RF channel width","The DHCP lease duration","The trunk's STP cost"],c:0,e:"An unknown issuing CA is a certificate trust problem in the EAP authentication path.",x:"Association already works, so RF is not the leading issue. DHCP occurs after access authorization, and STP cost does not repair certificate validation."},
    {id:"w22",d:"wireless",q:"802.1X authentication succeeds, but the client is placed in the guest VLAN instead of the employee VLAN. Which component should be examined first?",a:["RADIUS authorization attributes and policy","The user's wireless signal strength","The DNS TTL","The EIGRP hello interval"],c:0,e:"Successful authentication with incorrect access indicates an authorization or dynamic-VLAN assignment problem.",x:"Signal affects radio performance, not the assigned role after authentication. DNS and EIGRP do not normally choose the 802.1X authorization VLAN."},
    {id:"w23",d:"wireless",q:"A warehouse scanner cannot run an 802.1X supplicant but still requires restricted network access. Which approach is most appropriate?",a:["MAB with a tightly restricted authorization profile","A shared administrator account with full access","Disable authentication for the entire WLAN","Use MAC filtering as proof of strong identity"],c:0,e:"MAB can accommodate non-802.1X devices, but it should receive narrowly limited access because MAC identity is spoofable.",x:"The alternatives grant excessive trust or incorrectly treat a MAC address as strong identity."},
    {id:"w24",d:"wireless",q:"Users have strong RSSI but high latency and low throughput only at noon. Which measurement is most useful next?",a:["Channel utilization and retransmission rate","DNS MX priority","EIGRP feasible distance","Printer spool size"],c:0,e:"Strong signal can coexist with congestion or interference; airtime utilization and retries test that theory.",x:"The time-of-day pattern and healthy signal point toward shared RF capacity, not routing metrics, mail records, or printing."},

    {id:"sec24",d:"security",q:"A technician adds a narrow permit rule below a broad deny rule. Traffic remains blocked. What is the best explanation?",a:["The broad rule matches first and shadows the later permit","The permit needs a higher TCP port number","Stateful firewalls ignore rule order","NAT automatically converts denies to permits"],c:0,e:"Ordered policies commonly stop at the first match, so a broad earlier deny can shadow a specific later permit.",x:"Port magnitude is irrelevant, statefulness does not eliminate policy order, and NAT does not override access policy."},
    {id:"sec25",d:"security",q:"A passive IDS must inspect traffic between a server VLAN and the firewall without becoming an inline failure point. Which design is best?",a:["Feed the IDS from a SPAN/mirror port or network tap","Place the IDS as the default gateway","Replace the firewall with the IDS","Configure the IDS as the DHCP relay"],c:0,e:"A mirror port or tap provides a copy of traffic to a passive sensor without putting it inline.",x:"Making the IDS a gateway changes it into a critical path device. IDS and firewall/DHCP-relay functions are not interchangeable."},
    {id:"sec26",d:"security",q:"Administrators need centralized command authorization and a reliable record of commands entered on routers. Which service is generally the closer fit?",a:["TACACS+","RADIUS for wireless client access","SNMPv2c","NTP"],c:0,e:"TACACS+ is commonly favored for network-device administration and granular command authorization/accounting.",x:"RADIUS is strongly associated with network access, SNMPv2c is monitoring/management, and NTP provides time synchronization."},
    {id:"sec27",d:"security",q:"An inbound firewall rule permits HTTPS to a public address, but the internal web server never receives the connection. Routing is correct and the firewall logs show the permit. What should be verified next?",a:["Destination NAT/port-forward translation to the internal server","STP root election on the user access switch","The client's DHCP reservation","The server's DNS PTR record"],c:0,e:"Permitting traffic to a public address does not by itself translate that traffic to the private server.",x:"The firewall permit and correct routing narrow the issue to translation or service delivery; the other options do not map the public destination to the server."},

    {id:"svc23",d:"services",q:"Clients on one new VLAN receive no DHCP lease, while existing VLANs work. The DHCP server has an available scope for the new subnet. What should be verified first?",a:["DHCP relay/IP helper on the new VLAN interface","DNS recursion on the client","SNMP trap destination","NTP stratum"],c:0,e:"DHCP discovery broadcasts do not cross a router without a relay; a new routed VLAN needs the appropriate helper configuration.",x:"The scope exists and other VLANs work, so the missing subnet-specific relay is more likely than unrelated DNS, SNMP, or NTP settings."},
    {id:"svc24",d:"services",q:"A user can resolve internal names and ping Internet IP addresses but cannot resolve public names. Which test best isolates the problem?",a:["Query the configured resolver for a public name and compare recursion/forwarder behavior","Renew the switch's STP election","Change the workstation's VLAN without testing","Clear the router's EIGRP neighbors"],c:0,e:"The evidence isolates the failure to external DNS recursion or forwarding, not general IP or internal DNS.",x:"The alternatives disturb functioning Layer 2 or routing components without testing the service that the symptoms isolate."},
    {id:"svc25",d:"services",q:"Monitoring graphs show high interface utilization, but users report normal performance. What is the best next step?",a:["Compare against the established baseline and examine errors, drops, latency, and business impact","Replace the interface immediately","Assume the graph proves an outage","Disable monitoring to remove the alert"],c:0,e:"Utilization alone is not failure evidence; compare it with normal patterns and corroborating performance indicators.",x:"Immediate replacement or declaring an outage is premature, while disabling monitoring removes useful evidence."},
    {id:"svc26",d:"services",q:"SNMP polling succeeds, but urgent device events never reach the monitoring server. Which path should be investigated?",a:["Device-to-manager traps/informs, commonly UDP 162","Manager-to-device polling, commonly UDP 161 only","DNS zone transfers over TCP 53","DHCP client broadcasts over UDP 68"],c:0,e:"Polling and unsolicited notifications use different exchanges; traps commonly target UDP 162 on the manager.",x:"Successful polling already demonstrates the UDP 161 query path. DNS and DHCP are unrelated to SNMP notifications."},

    {id:"t24",d:"troubleshooting",q:"After an ACL change, only return traffic for one application fails. Forward packets reach the server. What evidence is most valuable before editing the ACL again?",a:["A bidirectional packet capture plus ACL counters on the return path","A list of DNS aliases only","The access switch's STP root ID only","The client's wallpaper settings"],c:0,e:"Bidirectional capture and policy counters show whether replies exist, where they stop, and which rule matches.",x:"The symptom is path- and policy-specific; the other evidence does not test the failing return flow."},
    {id:"t25",d:"troubleshooting",q:"One workstation cannot connect, but moving its cable to a known-good port restores service. The original port has link and rising CRC errors. What is the best next action?",a:["Test or replace the cable and inspect physical termination before changing routing","Rebuild the DNS zone","Change the enterprise EIGRP AS","Create a new wireless SSID"],c:0,e:"A known-good port restores service and CRC errors implicate the original physical path or termination.",x:"Routing and DNS are disproved by success on the alternate port; wireless configuration is unrelated."},
    {id:"t26",d:"troubleshooting",q:"A host reaches its gateway and a remote server by IP, but HTTPS fails by name with a certificate-name warning. Which explanation best fits?",a:["DNS may resolve to the wrong host or the certificate does not cover the requested name","The local switchport must be administratively down","The default gateway is missing","EIGRP has no route to the server"],c:0,e:"IP reachability and the TLS name warning isolate the issue to naming/certificate identity rather than basic connectivity.",x:"A down port, missing gateway, or absent route would prevent the successful IP connection already observed."},
    {id:"t27",d:"troubleshooting",q:"A change restored connectivity, but the technician cannot explain why and has not reproduced the original workflow. What should happen next?",a:["Verify the original end-to-end function, check for side effects, and document evidence","Close the incident because ping works once","Make additional unrelated changes","Erase logs to prevent confusion"],c:0,e:"A defensible resolution requires validation of the reported service, side-effect checks, and documentation.",x:"One ping is narrower than the original workflow, unrelated changes increase risk, and logs preserve rather than obstruct evidence."},

    {id:"d16",d:"documentation",q:"A switch replacement is planned. Which document set most directly reduces restoration risk?",a:["Current configuration backup, physical port map, VLAN/trunk map, validation plan, and rollback criteria","Only the purchase receipt","Only a logical diagram without port details","Only a list of user names"],c:0,e:"Replacement requires both configuration state and physical/logical mappings, followed by validation and rollback guidance.",x:"Each alternative omits critical implementation or recovery information."},
    {id:"d17",d:"documentation",q:"An MFP prints successfully but scan-to-email stopped after a mail-security change. What should be checked first?",a:["SMTP relay policy, authentication, TLS requirements, and certificate trust","The printer's paper tray","The switch's EIGRP feasible successor","The user's browser cache"],c:0,e:"Printing and scan-to-email use different services; a mail-security change points to SMTP authentication, encryption, or relay policy.",x:"The alternatives do not explain why only the email function changed after a mail-policy modification."},
    {id:"d18",d:"documentation",q:"A procedure says only 'update the firewall and test it.' What is the most important improvement before implementation?",a:["Add exact changes, affected flows, prerequisites, risk, validation, and rollback steps","Add more decorative formatting","Remove the maintenance window","Omit the current configuration"],c:0,e:"A usable method of procedure must make the change controlled, reproducible, testable, and reversible.",x:"Appearance is secondary, and removing timing or baseline information increases operational risk."},
    {id:"d19",d:"documentation",q:"Two diagrams disagree about a server's VLAN. What is the best immediate response?",a:["Verify the live configuration and approved source of truth, then correct the stale artifact through change control","Choose the newer-looking diagram without checking","Change the server to match both diagrams","Delete all diagrams"],c:0,e:"Conflicting documentation should be reconciled against authoritative live and approved records before configuration changes.",x:"Guessing or changing production to satisfy stale documentation can create an outage; deleting records removes useful history."}
  ];
  QUESTIONS.push(...ADVANCED_QUESTIONS);

  const domainNames = {
    routing: "Routing & EIGRP",
    switching: "Switching & VLANs",
    wireless: "Secure Wireless & 802.1X",
    security: "Firewalls & Security",
    services: "Services, Tools & Monitoring",
    troubleshooting: "Troubleshooting",
    documentation: "MFP & Documentation"
  };

  const $ = id => document.getElementById(id);

  const state = {
    set: [],
    index: 0,
    score: 0,
    answered: false,
    mode: "quick",
    secondsLeft: 3600,
    timerId: null,
    responses: []
  };

  // ---------- LOCAL STORAGE ----------
  function loadStats(){
    try {
      return JSON.parse(localStorage.getItem("sf1041Stats")) ||
        {attempts:0, correct:0, total:0, missed:[], domains:{}};
    } catch(e){
      return {attempts:0, correct:0, total:0, missed:[], domains:{}};
    }
  }

  function saveStats(stats){
    localStorage.setItem("sf1041Stats", JSON.stringify(stats));
  }

  // ---------- HELPERS ----------
  function shuffle(arr){
    const a = [...arr];
    for(let i=a.length-1;i>0;i--){
      const j = Math.floor(Math.random()*(i+1));
      [a[i],a[j]] = [a[j],a[i]];
    }
    return a;
  }

  function dashboard(){
    const s = loadStats();
    const pct = s.total ? Math.round(100*s.correct/s.total) : 0;
    const missedCount = (s.missed || []).length;

    $("dashboard").innerHTML = [
      `<div class="stat"><span>Lifetime accuracy</span><strong>${pct}%</strong></div>`,
      `<div class="stat"><span>Questions answered</span><strong>${s.total || 0}</strong></div>`,
      `<div class="stat"><span>Saved missed</span><strong>${missedCount}</strong></div>`,
      `<div class="stat"><span>Completed sets</span><strong>${s.attempts || 0}</strong></div>`
    ].join("");
  }

  // ---------- TEST BUILDING ----------
  function buildSet(){
    state.mode = $("mode").value;
    let pool = [...QUESTIONS];
    const domain = $("domain").value;

    if(state.mode === "focus" && domain !== "all"){
      pool = pool.filter(q => q.d === domain);
    }

    if(state.mode === "missed"){
      const missedIds = new Set(loadStats().missed || []);
      pool = pool.filter(q => missedIds.has(q.id));

      if(!pool.length){
        alert("No saved missed questions yet. Complete a drill first.");
        return false;
      }
    }

    pool = shuffle(pool);

    const requestedCount =
      state.mode === "city" ? 25 :
      state.mode === "challenge" ? 40 :
      state.mode === "quick" ? 10 :
      pool.length;

    state.set = pool.slice(0, Math.min(requestedCount, pool.length));
    state.index = 0;
    state.score = 0;
    state.answered = false;
    state.responses = [];
    state.secondsLeft = state.mode === "challenge" ? 4500 : 3600;

    return true;
  }

  function start(){
    clearInterval(state.timerId);
    if(!buildSet()) return;

    $("results").classList.add("hidden");
    $("quiz").classList.remove("hidden");

    if(state.mode === "city" || state.mode === "challenge"){
      tick();
      state.timerId = setInterval(() => {
        state.secondsLeft--;
        tick();
        if(state.secondsLeft <= 0){
          clearInterval(state.timerId);
          finish(true);
        }
      }, 1000);
    } else {
      $("timer").textContent = "";
    }

    render();
  }

  function tick(){
    const minutes = Math.floor(state.secondsLeft/60);
    const seconds = state.secondsLeft % 60;
    $("timer").textContent =
      `Time ${minutes}:${String(seconds).padStart(2,"0")}`;
  }

  // ---------- QUESTION DISPLAY ----------
  function render(){
    const q = state.set[state.index];

    if(!q){
      finish(false);
      return;
    }

    state.answered = false;

    $("progress").textContent =
      `Question ${state.index+1} of ${state.set.length}`;

    $("domainBadge").textContent =
      `${domainNames[q.d]} • ${q.id.toUpperCase()}`;

    $("questionText").textContent = q.q;
    $("feedback").classList.add("hidden");
    $("feedback").innerHTML = "";
    $("submitBtn").classList.remove("hidden");
    $("nextBtn").classList.add("hidden");

    const shuffledAnswers =
      shuffle(q.a.map((text, originalIndex) => ({
        text,
        originalIndex
      })));

    $("answers").innerHTML =
      shuffledAnswers.map((item, displayIndex) =>
        `<label class="answer">
          <input type="radio" name="answer" value="${item.originalIndex}">
          <span><strong>${String.fromCharCode(65+displayIndex)}.</strong> ${item.text}</span>
        </label>`
      ).join("");
  }

  // ---------- ANSWER PROCESSING ----------
  function submit(){
    if(state.answered) return;

    const chosen =
      document.querySelector('input[name="answer"]:checked');

    if(!chosen){
      alert("Choose the best answer before continuing.");
      return;
    }

    state.answered = true;

    const q = state.set[state.index];
    const selected = Number(chosen.value);
    const correct = selected === q.c;

    if(correct) state.score++;

    state.responses.push({
      id: q.id,
      d: q.d,
      correct,
      selected
    });

    $("feedback").innerHTML =
      `<strong>${correct ? "Correct." : "Not quite."}</strong>
      ${q.e}
      <br><br>
      <strong>Best answer:</strong> ${q.a[q.c]}
      ${q.x ? `<br><br><strong>Why the alternatives are weaker:</strong> ${q.x}` : ""}
      <br><br><strong>Concept to retain:</strong> ${domainNames[q.d]}`;

    $("feedback").classList.remove("hidden");
    $("submitBtn").classList.add("hidden");
    $("nextBtn").classList.remove("hidden");
  }

  function next(){
    if(!state.answered) return;

    state.index++;

    if(state.index >= state.set.length){
      finish(false);
    } else {
      render();
    }
  }

  // ---------- RESULTS ----------
  function finish(timedOut){
    clearInterval(state.timerId);
    $("quiz").classList.add("hidden");

    const stats = loadStats();
    stats.attempts = (stats.attempts || 0) + 1;

    for(const response of state.responses){
      stats.total = (stats.total || 0) + 1;

      if(response.correct){
        stats.correct = (stats.correct || 0) + 1;
      }

      stats.domains = stats.domains || {};
      stats.domains[response.d] =
        stats.domains[response.d] || {correct:0,total:0};

      stats.domains[response.d].total++;

      if(response.correct){
        stats.domains[response.d].correct++;
      }

      const missed = new Set(stats.missed || []);

      if(response.correct){
        missed.delete(response.id);
      } else {
        missed.add(response.id);
      }

      stats.missed = [...missed];
    }

    saveStats(stats);
    dashboard();

    const answered = state.responses.length;
    const pct = answered ?
      Math.round(100*state.score/answered) : 0;

    const domainRows =
      Object.keys(domainNames).map(domain => {
        const responses =
          state.responses.filter(r => r.d === domain);

        if(!responses.length) return "";

        const correct =
          responses.filter(r => r.correct).length;

        return `<tr>
          <td>${domainNames[domain]}</td>
          <td>${correct}/${responses.length}</td>
          <td>${Math.round(100*correct/responses.length)}%</td>
        </tr>`;
      }).join("");

    $("results").innerHTML =
      `<h2>${timedOut ? "Time Expired" : "Set Complete"}</h2>
      <p><strong>Score: ${state.score}/${answered} (${pct}%)</strong></p>
      <p>${
        pct >= 90 ?
        "High-confidence practice result. Confirm it across several fresh mixed sets and keep missed concepts sharp." :
        pct >= 85 ?
        "Strong result. Review the weakest domain and retest missed questions before relying on this level." :
        pct >= 75 ?
        "Developing readiness. Review the weakest domain, then repeat a fresh mixed set." :
        "Important gaps remain. Use the domain breakdown to study narrowly, then retest missed concepts."
      }</p>
      <table>
        <thead>
          <tr>
            <th>Domain</th>
            <th>Correct</th>
            <th>Accuracy</th>
          </tr>
        </thead>
        <tbody>${domainRows}</tbody>
      </table>
      <p class="muted">
        Demanding study standard: aim for 90% or higher across several fresh mixed sets. This is a readiness indicator only, not an estimate or guarantee of the City's passing score.
      </p>`;

    $("results").classList.remove("hidden");
  }

  // ---------- EVENT WIRING ----------
  $("startBtn").addEventListener("click", start);
  $("submitBtn").addEventListener("click", submit);
  $("nextBtn").addEventListener("click", next);

  $("resetStatsBtn").addEventListener("click", () => {
    if(confirm("Clear all saved practice progress and missed-question history?")){
      localStorage.removeItem("sf1041Stats");
      dashboard();
    }
  });

  $("mode").addEventListener("change", () => {
    $("domain").disabled = $("mode").value !== "focus";
  });

  $("domain").disabled = true;
  dashboard();
})();
</script>



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