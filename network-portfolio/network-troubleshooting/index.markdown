---
layout: page
permalink: /network-portfolio/network-troubleshooting-checklist/
nav_exclude: true
---

---
---
---


# Network Troubleshooting Checklist

**A systematic, CompTIA-inspired field guide for IT support technicians**

Use this checklist for workstation, network, and application incidents. Follow the six-step process, skipping tests that do not apply. Record evidence before changing production configurations. This is an independent study aid, not an official CompTIA publication.

> **Print options:** Use your browser's **Print → Save as PDF** or print on paper. Select **Blank worksheet** below for a clean copy to fill in; use **Worked example** to see how the process applies to a sample incident.

<div class="no-print" markdown="1">

**[Print blank worksheet](#blank-incident-worksheet)** · **[View worked example](#worked-example)** · **[Command reference](#quick-command-reference)**

</div>

## Incident details

| Field | Entry |
|---|---|
| Ticket / incident ID | __________________________ |
| Date and time | __________________________ |
| Technician | __________________________ |
| User / department | __________________________ |
| Device / location | __________________________ |
| Affected service | __________________________ |
| Business impact / priority | __________________________ |

## Step 1 — Identify the problem

- [ ] Record symptoms, error messages, and when the problem started.
- [ ] Determine whether the issue is constant or intermittent.
- [ ] Identify affected users, devices, locations, and services.
- [ ] Compare an affected device with a working device.
- [ ] Ask about recent changes to equipment, software, or configurations.
- [ ] Review alerts, incident history, and network documentation.
- [ ] Assess business impact and assign priority.

**Observations:** ______________________________________________

## Step 2 — Establish a theory of probable cause

Work from simple, likely causes toward complex ones. Use the OSI model to guide your investigation.

- [ ] **Layer 1 — Physical:** Power, cabling, connectors, link LEDs, speed/duplex, errors.
- [ ] **Layer 2 — Data link:** Switch ports, VLANs, MAC learning, loops, port security.
- [ ] **Layer 3 — Network:** IP address/prefix, gateway, DHCP, routing, ACLs.
- [ ] **Layer 4 — Transport:** TCP/UDP ports, reachability, firewall rules.
- [ ] **Layers 5–7 — Services/applications:** DNS, authentication, server status, application logs.
- [ ] **Security:** Suspicious traffic, endpoint alerts, unauthorized changes.

**Leading theory and reason:** __________________________________

## Step 3 — Test the theory

- [ ] Select a test that can confirm or disprove the theory.
- [ ] Capture the initial result and expected result.
- [ ] Isolate the affected device, link, network segment, or service.
- [ ] Compare with a known-working system when possible.
- [ ] If the theory is not supported, revise it and test again.
- [ ] Escalate when outside your access, authority, or expertise.

**Test / result / conclusion:** ___________________________________

## Step 4 — Plan and implement a solution

- [ ] Identify the correction supported by evidence.
- [ ] Assess business impact and possible side effects.
- [ ] Obtain authorization and follow change procedures.
- [ ] Back up configurations and prepare rollback steps as appropriate.
- [ ] Apply the correction and monitor for unintended effects.
- [ ] For suspected attacks, preserve evidence and follow incident response procedures.

**Change made / approval / rollback:** __________________________

## Step 5 — Verify full functionality

- [ ] Repeat the test that originally demonstrated the problem.
- [ ] Confirm the user can complete the original task.
- [ ] Check connectivity, service access, and performance as applicable.
- [ ] Review interface counters, logs, and monitoring for continuing errors.
- [ ] Confirm related services still work.
- [ ] Monitor for recurrence when appropriate.

**Verification / user confirmation:** _____________________________

## Step 6 — Document findings and outcomes

- [ ] Record the confirmed root cause, or state if undetermined.
- [ ] Record tests, evidence, corrective actions, and outcomes.
- [ ] Update diagrams, configuration records, or knowledge base as needed.
- [ ] Note preventive actions and follow-up ownership.
- [ ] Close or escalate the ticket following company procedures.

**Resolution / follow-up:** ______________________________________

## Quick command reference

| Goal | Example command or tool | Important note |
|---|---|---|
| Windows IP configuration | `ipconfig /all` | Check address, gateway, DNS, DHCP. |
| Local TCP/IP stack | `ping 127.0.0.1` | Loopback only; does not prove network access. |
| Gateway reachability | `ping <gateway-IP>` | ICMP may be blocked. |
| Route path | `tracert <destination>` (Windows), `traceroute <destination>` (Linux/macOS) | Nonresponding hops do not always indicate failure. |
| DNS lookup | `nslookup <hostname>` | Compare expected and returned address. |
| TCP port | `Test-NetConnection <host> -Port <port>` (PowerShell) | TCP connectivity is not proof of application health. |
| ARP cache | `arp -a` | Useful for local IPv4 neighbor information. |
| Windows routes | `route print` | Check default and specific routes. |
| Cisco interfaces | `show interfaces` | Check errors, speed, duplex, status. |
| Cisco VLANs | `show vlan brief` | Availability depends on platform. |
| Cisco routing | `show ip route` | Check expected routes and gateway of last resort. |
| Throughput | `iperf3` | Requires controlled test endpoints. |
| Packet analysis | Wireshark | Capture only with authorization. |

## Quick decision guide

| Symptom | Start here |
|---|---|
| No connection | Power → cable/Wi-Fi → link → IP configuration |
| Local network works, remote subnet fails | Gateway → VLAN → routing → ACLs |
| IP works, hostname fails | DNS settings → resolver → records |
| Server reachable, app unavailable | Port → firewall → service → authentication/logs |
| Slow or intermittent | Cable/errors → speed/duplex → loss/congestion → server performance |
| Suspicious traffic or changes | Logs/alerts → preserve evidence → security escalation |

**Reminder:** A successful ping does not establish that an application is healthy. A failed ping does not necessarily mean the destination is down.

---

## Blank incident worksheet

*Print this section by itself for a fresh incident. The checkboxes and lines are intentionally blank.*

**Ticket:** __________________ **Date/time:** __________________

**Technician:** __________________ **Priority:** _______________

**Affected users/devices/services:** ____________________________

### 1. Identify
- [ ] Symptoms and error messages recorded
- [ ] Scope and impact determined
- [ ] Recent changes and known-good comparison checked

**Notes:** ______________________________________________________

_______________________________________________________________

### 2. Establish a theory
- [ ] Physical (L1)  - [ ] Switching (L2)  - [ ] IP/routing (L3)
- [ ] Ports/firewall (L4)  - [ ] Application/service (L5–7)  - [ ] Security

**Theory:** _____________________________________________________

_______________________________________________________________

### 3. Test
- [ ] Diagnostic test selected and run
- [ ] Result recorded and theory confirmed or revised

**Command/test:** _______________________________________________

**Result:** _____________________________________________________

### 4. Correct
- [ ] Impact reviewed and approval obtained if required
- [ ] Backup/rollback considered
- [ ] Approved correction applied

**Action:** _____________________________________________________

### 5. Verify
- [ ] Original failure retested
- [ ] User confirms normal service
- [ ] Other services checked

**Evidence:** ___________________________________________________

### 6. Document
- [ ] Root cause or uncertainty recorded
- [ ] Resolution and follow-up recorded
- [ ] Ticket closed or escalated

**Outcome / next owner:** _______________________________________



---

## Worked example

**Incident:** Employees in one department cannot open internal webmail, but coworkers elsewhere can.

1. **Identify:** Interview affected employees; confirm their devices share a switch/VLAN and the problem began after a network change.
2. **Theory:** The department's VLAN may lack a permitted path to the mail server.
3. **Test:** Verify IP/gateway, compare DNS results, test the mail server's TCP 443 port, and review the relevant switch, routing, and firewall configurations. Record actual results before deciding.
4. **Correct:** If an incorrect ACL is confirmed, obtain approval and restore the intended rule using change control.
5. **Verify:** Retest webmail access and confirm unaffected services still operate.
6. **Document:** Record the actual configuration error, approved change, verification evidence, and preventive recommendation.

*This is a hypothetical example, not a report of a completed repair.*

---

**Core workflow:** **Identify → Establish theory → Test → Correct → Verify → Document**

*CompTIA-inspired educational checklist. Always follow your organization's change-management, security, and incident-response policies.*


---
---
---

## 🔗 Navigation

* [Home](/)
* [Network Portfolio](/network-portfolio/)
  * [Formative Modules](/network-portfolio/formative-modules/)
  * [Videos](/network-portfolio/videos/)
  * [Study Diagrams](/network-portfolio/study-diagrams/)
  * [Test Readiness Lab](/test-readiness-lab/)
  * **[NETWORK TROUBLESHOOTING CHECKLIST](/network-portfolio/network-troubleshooting-checklist/)**
* [Trading+](/trading/)
* [Bible Study](/bible-study/)
* [About the Portfolio](/about/)

---
---
---