---
layout: post
title: "Technical Communication | Use PowerShell Remote Management"
lab_title: "Use PowerShell Remote Management"

lesson: "02.0"
lesson_id: "13.03.09"
sort_order: "130309"

categories: [portfolio, videos]

category: systems-administration
category_display: Systems Administration

subcategory: remote-administration
subcategory_display: Remote Administration

content_type: video
content_type_display: Assignment Video


tags:
  - powershell
  - remote-management
  - security
  - administration

permalink: /network-portfolio/videos/lab-13-3-9-powershell-remote-management/
status: complete

video_id: "AkQEJt5Gz3o"
video_url: "https://youtu.be/AkQEJt5Gz3o"
thumbnail: "https://img.youtube.com/vi/AkQEJt5Gz3o/hqdefault.jpg"

topics:
  - remote-administration
  - remote-management
  - windows-administration
  - powershell-scripting

tools:
  - powershell
  - windows-remote-management

protocols: []

---

## Overview

This no-narration video walkthrough demonstrates PowerShell Remote Management configuration and administration techniques within a Windows networking environment.
<!--more-->

## Video Walkthrough

Watch the complete walkthrough:

<a href="{{ page.video_url }}" target="_blank" rel="noopener noreferrer">
  <img src="{{ page.thumbnail }}"
       alt="{{ page.title }}"
       style="width:420px; border-radius:8px;">
</a>

---

# Lab 13.3.9 — Use PowerShell Remote Management

> Companion study guide for my TestOut lab walkthrough. This is an independently written learning resource, **not** a reproduction of TestOut's proprietary lab instructions. Exact steps and available commands depend on the Windows version, permissions, and lab environment.

## Learning objectives

- Explain how PowerShell remoting differs from Remote Desktop Protocol (RDP).
- Identify the role of Windows Remote Management (WinRM) and authentication.
- Configure remoting where authorized, establish sessions, and run commands remotely.
- Verify connectivity, permissions, and firewall rules.
- Troubleshoot common failures without weakening security unnecessarily.

## Core concepts

| Concept | Explanation |
| --- | --- |
| PowerShell remoting | Run PowerShell commands or interactive sessions on a remote Windows host. |
| WinRM | Windows implementation of the WS-Management protocol, used by Windows PowerShell remoting. |
| `Enter-PSSession` | Start an interactive session to one remote host. |
| `Invoke-Command` | Run a command or script block on one or more remote hosts. |
| `New-PSSession` | Create a reusable remote session. |
| Authentication | Usually Kerberos in an Active Directory domain; other methods require deliberate configuration. |
| Transport | Default WinRM HTTP listener typically uses TCP **5985**; HTTPS typically uses TCP **5986**. HTTP transport does **not** imply that authenticated PowerShell message content is sent in plaintext. |

## Lab preparation

1. Identify the **management computer** and **target computer**; record their names and IP addresses.
2. Confirm you have authorization and suitable administrator or remoting permissions on the target.
3. Check whether the computers are domain-joined or in a workgroup; authentication differs.
4. Use an elevated PowerShell window on the target for setup commands where required.
5. Avoid exposing WinRM directly to the public internet. Prefer a trusted management network or VPN.

## Guided configuration and verification

### Step 1 — Check basic network connectivity

On the management computer, substitute your actual target hostname:

```powershell
Resolve-DnsName TARGET-PC
Test-Connection TARGET-PC -Count 2
Test-NetConnection TARGET-PC -Port 5985
```

**Interpretation:** DNS resolution and ICMP reachability are useful diagnostics but do not prove that PowerShell remoting is enabled. Port connectivity is another separate test.

### Step 2 — Enable remoting on the target (only if required)

Run **as administrator** on the target:

```powershell
Enable-PSRemoting -Force
Get-Service WinRM
Get-WSManInstance winrm/config/listener -Enumerate
```

`Enable-PSRemoting` configures WinRM and relevant firewall exceptions; behavior can depend on Windows edition, network profile, and policy. On Windows client systems, a Public network profile may require a profile change or appropriately restricted configuration. Do **not** broadly open the firewall as a shortcut.

### Step 3 — Test the remoting service

From the management computer:

```powershell
Test-WSMan TARGET-PC
```

A successful WS-Management response confirms the endpoint is responding; it does **not** prove that your account is authorized to run remote commands.

### Step 4 — Open an interactive remote session

```powershell
Enter-PSSession -ComputerName TARGET-PC
hostname
Get-Date
Get-Service WinRM
Exit-PSSession
```

The remote prompt should identify the target computer. `Exit-PSSession` returns to your local shell.

### Step 5 — Run a one-time remote command

```powershell
Invoke-Command -ComputerName TARGET-PC -ScriptBlock {
    hostname
    Get-ComputerInfo | Select-Object CsName, WindowsProductName
}
```

This runs the script block on the target and returns the results to the local console.

### Step 6 — Create and close a reusable session

```powershell
$session = New-PSSession -ComputerName TARGET-PC
Invoke-Command -Session $session -ScriptBlock { Get-Service WinRM }
Get-PSSession
Remove-PSSession -Session $session
```

Close sessions when finished. Do not leave elevated sessions open unnecessarily.

## Authentication and security notes

- In an Active Directory domain, Kerberos is typically preferred when properly configured.
- In a workgroup or when connecting by IP address, Kerberos may not be available. Use a properly configured HTTPS listener with a trusted certificate or other approved authentication arrangement.
- Avoid setting `TrustedHosts` to `*`; it broadens which remote endpoints the client will trust for certain authentication flows and does not itself authenticate the server.
- Follow least privilege and use approved administrative accounts. Avoid embedding passwords in scripts.
- WinRM over HTTP normally uses message-level encryption after authentication; HTTPS additionally protects the transport and supports server certificate validation.
- PowerShell 7 also supports SSH-based remoting, which is a different transport and configuration path from classic WinRM examples above.

## Troubleshooting reference

| Symptom | What to check | Useful command |
| --- | --- | --- |
| Hostname not found | DNS records, spelling, network configuration | `Resolve-DnsName TARGET-PC` |
| Port 5985 unreachable | Routing, firewall, WinRM listener | `Test-NetConnection TARGET-PC -Port 5985` |
| WSMan connection failure | WinRM service and listener on target | `Get-Service WinRM` / `Test-WSMan TARGET-PC` |
| Access denied | Account permissions, authentication, endpoint authorization | `whoami` |
| Kerberos error | Domain membership, DNS, SPN, clock synchronization | `klist` |
| Public-profile firewall issue | Network profile and scoped WinRM firewall rules | `Get-NetConnectionProfile` |
| HTTPS certificate error | Certificate validity, hostname match, trust chain | Inspect listener/certificate configuration |

**Troubleshooting sequence:** physical/network connectivity → name resolution → TCP reachability → WinRM service/listener → authentication → authorization → command execution.

## Verification checklist

- [ ] Target host and management host identified
- [ ] Target resolves to the expected address
- [ ] WinRM service and listener verified
- [ ] Appropriate firewall access confirmed
- [ ] Remote session successfully established
- [ ] Remote command returned the expected hostname/output
- [ ] Session closed after testing
- [ ] Security settings reviewed and documented

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