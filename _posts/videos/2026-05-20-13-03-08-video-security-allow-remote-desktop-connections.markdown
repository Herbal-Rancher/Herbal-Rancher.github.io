---
layout: post
title: "Security | Allow Remote Desktop Connections"
lab_title: "Allow Remote Desktop Connections"

lesson: "13.3"
lesson_id: "13.03.08"
sort_order: "130308"

categories: [portfolio, videos]

category: security
category_display: Security

subcategory: remote-access
subcategory_display: Remote Access

content_type: video
content_type_display: Assignment Video

tags:
  - remote-desktop
  - rdp
  - windows-administration
  - remote-access
  - network-security
  - network-plus

permalink: /network-portfolio/videos/lab-13-3-8-allow-remote-desktop-connections/
status: complete

video_id: "wh2vpkIDdJs"
video_url: "https://www.youtube.com/watch?v=wh2vpkIDdJs"
thumbnail: "https://img.youtube.com/vi/wh2vpkIDdJs/hqdefault.jpg"
---

## Overview

This video walkthrough explores how to allow authorized Remote Desktop connections on Windows systems, verify connectivity, and apply secure remote administration practices.

<!--more-->

---

## Video Walkthrough

Watch the complete walkthrough:

<a href="{{ page.video_url }}" target="_blank" rel="noopener noreferrer">
  <img src="{{ page.thumbnail }}"
       alt="{{ page.title }}"
       style="width:420px; border-radius:8px;">
</a>

---

# Lab 13.3.8 — Allow Remote Desktop Connections

> Companion study guide for my TestOut lab walkthrough. This is an independently written learning resource, **not** a reproduction of TestOut's proprietary lab instructions. Exact screens, options, and required settings depend on the lab version and Windows edition.

## Learning objectives

- Explain the purpose of Remote Desktop Protocol (RDP) and secure remote administration.
- Enable Remote Desktop on a supported Windows host in an authorized lab.
- Identify account permissions, Network Level Authentication (NLA), and firewall requirements.
- Verify reachability separately from authentication and session success.
- Troubleshoot common RDP connection failures without exposing RDP to the public internet.

## Core concepts

| Concept | Meaning |
| --- | --- |
| RDP | Protocol for interacting with a remote Windows desktop |
| TCP 3389 | Default RDP listening port; deployments can change it |
| Network Level Authentication (NLA) | Requires authentication before establishing a full remote desktop session |
| Windows Defender Firewall | Controls inbound access to the RDP service |
| User authorization | Only permitted accounts should be able to sign in remotely |
| VPN or secure access gateway | Preferred controlled access path for remote connections across untrusted networks |

**Important:** Windows Home editions generally cannot act as an incoming Remote Desktop host using the built-in Microsoft RDP host feature. They can usually connect *to* supported hosts.

## Suggested hands-on workflow

1. **Record the baseline.** Identify the target Windows edition, hostname, IPv4 address, network profile, and whether Remote Desktop is already enabled.
2. **Confirm authorization.** Use a lab host you administer and an account permitted to access it.
3. **Enable Remote Desktop.** On a supported Windows version, open **Settings → System → Remote Desktop** and turn on Remote Desktop. The precise path may vary by Windows version.
4. **Review authentication.** Keep Network Level Authentication enabled where supported and confirm the intended account is authorized for remote sign-in.
5. **Review firewall rules.** Confirm the appropriate Remote Desktop inbound rules are enabled and scoped to approved networks or management hosts. Avoid opening unrestricted inbound access.
6. **Verify network reachability.** From an authorized client, test the target address and TCP port before attempting a session.
7. **Connect.** Launch Remote Desktop Connection (`mstsc`) from the client, enter the approved host name or IP address, and authenticate using authorized credentials.
8. **Document results.** Record successful or failed connection, relevant error messages, and any corrective actions. Redact usernames, addresses, and other sensitive details before publishing.
9. **Restore lab state.** Disable remote access or revert settings if the exercise requires cleanup.

## Example commands and checks

These are **reference examples**, not guaranteed exact steps for the TestOut simulation. Replace placeholders with values from your authorized lab.

On a Windows client, inspect addressing:

```powershell
ipconfig /all
```

Test reachability to the default RDP port:

```powershell
Test-NetConnection -ComputerName <AUTHORIZED_HOST> -Port 3389
```

On the Windows host, inspect relevant firewall rules:

```powershell
Get-NetFirewallRule -DisplayGroup "Remote Desktop" |
  Select-Object DisplayName, Enabled, Direction, Action
```

Inspect whether the host is listening on the default port:

```powershell
Get-NetTCPConnection -LocalPort 3389 -State Listen -ErrorAction SilentlyContinue
```

Open the Remote Desktop client:

```text
mstsc
```

A successful port test means the TCP port is reachable; it does **not** prove the credentials are valid or that a remote desktop session can be established.

## Verification checklist

- [ ] Windows host edition supports incoming Remote Desktop connections
- [ ] Remote Desktop is enabled on the intended host
- [ ] Intended user is authorized for remote access
- [ ] NLA is enabled where supported
- [ ] Firewall access is limited to approved sources
- [ ] Client can reach the host over the required network path
- [ ] Remote session connects and authenticates successfully
- [ ] Test results and corrective actions are documented
- [ ] Lab changes are retained or reverted as required

## Troubleshooting prompts

| Symptom | Check |
| --- | --- |
| Host unreachable | IPv4 address, routing, VPN, host power, network connection |
| TCP 3389 inaccessible | RDP service, firewall rules, port configuration, security filtering |
| Authentication fails | Credentials, account permissions, NLA compatibility, account restrictions |
| Remote Desktop option missing | Windows edition and administrative privileges |
| Works locally but not remotely | VPN, gateway, firewall scope, network segmentation |
| Connection drops | Link stability, latency, host resource usage, session policy |

## Security and operational notes

- Do not expose RDP directly to the public internet; use a VPN, secure gateway, or approved zero-trust access solution.
- Restrict access to specific authorized accounts and management networks.
- Use strong authentication, MFA where supported by the access architecture, and timely patching.
- Keep NLA enabled where supported and monitor remote logon events.
- Disable Remote Desktop when it is not needed.

## CompTIA Network+ review questions

1. What is the purpose of RDP, and what port does it use by default?
2. How does NLA improve the security of a remote desktop connection?
3. Why can a successful TCP port test still be followed by an RDP sign-in failure?
4. How do host firewall rules differ from network routing requirements?
5. Why is a VPN or secure access gateway preferable to public RDP exposure?

## Lab reflection

- **Initial state:** _Document the host and connectivity baseline._
- **Configuration performed:** _Summarize approved changes._
- **Verification evidence:** _Record observed connection and authentication results._
- **Issue encountered:** _Describe any failure and its root cause._
- **Lesson learned:** _Explain what this exercise reinforced about remote access security._

---
---
---

## 🔗 Navigation

* [Home](/)
* [Network+ Portfolio](/network-portfolio/)
  * [Formative Modules](/network-portfolio/formative-modules/)
  * **[VIDEOS](/network-portfolio/videos/)**
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* [Trading+](/trading/)
* [Bible Study](/bible-study/)
* [About the Portfolio](/about/)

---
---
---
