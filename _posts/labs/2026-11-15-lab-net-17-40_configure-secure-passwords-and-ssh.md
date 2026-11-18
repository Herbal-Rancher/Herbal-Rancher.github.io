---
layout: post
title: "Lab 40 | Cisco Networking Labs - Configure Secure Passwords and SSH"
lab_title: "Configure Secure Passwords and SSH"

lesson: "17.0"
lesson_id: "17.40.00"
sort_order: "174000"

categories:
  - portfolio
  - videos

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: network-implementation
subcategory_display: Network Implementation

content_type: video
content_type_display: Video

tags:
  - packet-tracer
  - ssh
  - device-hardening
  - passwords
  - router
  - switch

topics:
  - router-hardening
  - switch-hardening
  - ssh-management

tools:
  - cisco-packet-tracer
  - cisco-ios-cli
  - ssh-client

protocols:
  - IPv4
  - SSH

status: complete

video_id: ""
video_url: ""
thumbnail: ""

completed_lab: ""
lab_pdf: ""
permalink: /network-portfolio/videos/17-40-configure-secure-passwords-and-ssh/
diagram: ""
---

## Overview

Prepare a Cisco router and switch for secure management in a Packet Tracer deployment scenario. Configure management addressing, local authentication, password controls, SSH access, and restrictions on unused switch ports.

<!--more-->

---

## Preconditions

![Packet Tracer Lab 40 - Configure Secure Passwords and SSH - Preconditions](/assets/images/packet-tracer/cisco-lab-topology-Module-17-Lab-40.png)

---

## Skills Practiced

- Configure router and switch management addressing
- Apply password and login controls
- Generate keys and enable SSH-only remote management
- Disable unused switch ports and verify remote access

---

## Video Walkthrough

This lab is documented as a written exercise; no video walkthrough is planned.

{% if page.video_id != "" %}
<iframe width="560" height="315" src="https://www.youtube.com/embed/{{ page.video_id }}" title="{{ page.title }}" frameborder="0" allowfullscreen></iframe>
{% endif %}

---

## Completed Lab Documentation

- Note: [Completed Lab PDF may be available upon request]

---

## Key Observations

Device hardening combines multiple protections: local credentials, controlled management access, login restrictions, session timeouts, and reducing unused access points. A secure configuration must also be saved and tested.

### Activity Focus

1. Configure RTA and PCA addressing and apply basic router security controls.
2. Enable SSH management with local authentication and verify connectivity.
3. Configure SW1 management settings and secure unused interfaces.

### Notes

The educational activity specifies 1024-bit RSA keys for Packet Tracer scoring. This is a lab requirement, not a recommended production key size.

---

## Validation

Confirm SSH access to RTA and SW1 as appropriate, saved configurations, and disabled unused ports.

___
___
___

## Module 17 — Lab 40: Configure Secure Passwords and SSH Study Guide

> Cisco Packet Tracer command reference for **RTA**, **SW1**, and **PCA**. Commands below use example lab-only credentials. Replace them with passwords you can remember. Do not reuse these passwords on real devices.

___
___
___

## Quick answer: Step 1(g)

At the `RTA(config)#` prompt, type:

```cisco
enable secret SunShineDay2027
```

This protects privileged EXEC mode (`enable`). It is **not** the SSH account password. The command must be entered in **global configuration mode**.

## Addressing table

| Device | Interface | IPv4 address | Subnet mask | Default gateway |
|---|---|---|---|---|
| RTA | GigabitEthernet0/0 | 172.16.1.1 | 255.255.255.0 | N/A |
| PCA | NIC | 172.16.1.10 | 255.255.255.0 | 172.16.1.1 |
| SW1 | VLAN 1 (SVI) | 172.16.1.2 | 255.255.255.0 | 172.16.1.1 |

**Example lab credentials**

- Router enable secret: `SunShineDay2027`
- Router SSH username: `netadmin`
- Router SSH password: `RouterSSH2027!`
- Switch enable secret: `SwitchEnable2027!`
- Switch SSH username: `netadmin`
- Switch SSH password: `SwitchSSH2027!`

All example passwords are at least 10 characters. These are **illustrative**, not production credentials.

## IOS modes and prompt reference

| Prompt | Mode | How to enter |
|---|---|---|
| `RTA>` | User EXEC | Initial console login |
| `RTA#` | Privileged EXEC | `enable` |
| `RTA(config)#` | Global configuration | `configure terminal` |
| `RTA(config-if)#` | Interface configuration | `interface g0/0` |
| `RTA(config-line)#` | Line configuration | `line vty 0 4` |

Use `exit` to return one level; use `end` or **Ctrl+Z** to return to privileged EXEC mode.

## Step 1: Secure router RTA

### 1(a) Configure PCA's IPv4 settings

In Packet Tracer, select **PCA → Desktop → IP Configuration** and set:

```text
IPv4 address:    172.16.1.10
Subnet mask:     255.255.255.0
Default gateway: 172.16.1.1
```

### 1(b) Connect to the router console

Use the light-blue console cable from **PCA RS-232** to **RTA Console**. Select **PCA → Desktop → Terminal**, accept default terminal settings, and press Enter if needed. The console is used for initial setup; SSH will be tested later through **PCA → Desktop → Command Prompt**.

### 1(c–o) Full router command sequence

Enter these commands one line at a time. The `RTA#` and `RTA(config)#` prompts shown elsewhere in this guide are **not** typed as part of a command.

```cisco
enable
configure terminal
hostname RTA
interface gigabitEthernet 0/0
 ip address 172.16.1.1 255.255.255.0
 no shutdown
exit
service password-encryption
security passwords min-length 10
enable secret SunShineDay2027
no ip domain-lookup
ip domain-name CCNA.com
username netadmin secret RouterSSH2027!
crypto key generate rsa
```

At the RSA modulus prompt, enter:

```text
How many bits in the modulus [512]: 1024
```

Then finish:

```cisco
ip ssh version 2
login block-for 180 attempts 4 within 120
line vty 0 4
 transport input ssh
 login local
 exec-timeout 6 0
exit
end
copy running-config startup-config
```

Press Enter to accept the default destination filename when saving.

**Packet Tracer grading notes:** The lab requires the domain name `CCNA.com` with exactly that capitalization and **1024-bit** RSA keys. On production networks, 1024-bit RSA is obsolete; use a stronger supported key length, generally at least 2048 bits. `ip ssh version 2` is an additional security command that may already be the default on your device.

**Syntax note:** Cisco IOS commonly uses `security passwords min-length 10` (plural `passwords`). If the activity's example uses `security password min-length 10`, follow the syntax accepted by your device and check with `security ?` or `security passwords ?`.

**VTY coverage:** This lab specifies `line vty 0 4`. If `show line` reveals additional VTY lines (such as 5–15), configure them consistently as well if the activity requires **all** VTY lines. Some Packet Tracer models expose only 0–4.

### 1(p) Test SSH from PCA

Open **PCA → Desktop → Command Prompt** (not Terminal). Verify reachability and start SSH:

```text
ping 172.16.1.1
ssh -l netadmin 172.16.1.1
```

When prompted, enter `RouterSSH2027!`. If you see `RTA>`, the SSH login worked. To enter privileged EXEC mode:

```cisco
enable
```

Enter `SunShineDay2027` when prompted. The password will not display as you type.

## Step 2: Secure switch SW1

Select **SW1 → CLI**. The switch's management address is assigned to **interface VLAN 1**, not to an individual physical switch port.

### 2(b–n) Full switch command sequence

```cisco
enable
configure terminal
hostname SW1
interface vlan 1
 ip address 172.16.1.2 255.255.255.0
 no shutdown
exit
ip default-gateway 172.16.1.1
interface range fastEthernet 0/2-24, gigabitEthernet 0/2
 shutdown
exit
service password-encryption
enable secret SwitchEnable2027!
no ip domain-lookup
ip domain-name CCNA.com
username netadmin secret SwitchSSH2027!
crypto key generate rsa
```

At the modulus prompt, enter:

```text
How many bits in the modulus [512]: 1024
```

Then finish:

```cisco
ip ssh version 2
line vty 0 4
 transport input ssh
 login local
 exec-timeout 6 0
exit
end
copy running-config startup-config
```

**Leave FastEthernet0/1 and GigabitEthernet0/1 enabled** as specified in the lab. The VLAN 1 SVI typically needs at least one active port in VLAN 1 for its line protocol to come up. If additional VTY lines exist, check whether they also need SSH-only configuration.

### Test switch management and SSH

From **PCA → Desktop → Command Prompt**:

```text
ping 172.16.1.2
ssh -l netadmin 172.16.1.2
```

Enter `SwitchSSH2027!` when prompted. If you reach `SW1>`, switch SSH works. Use `enable` and `SwitchEnable2027!` to enter privileged EXEC mode.

## Command explanations

| Command | Why it matters |
|---|---|
| `hostname RTA` / `hostname SW1` | Sets device identity and helps form the RSA key name |
| `interface g0/0` | Selects the router's LAN interface |
| `interface vlan 1` | Selects the switch virtual management interface (SVI) |
| `ip address ...` | Assigns the device an IPv4 address |
| `no shutdown` | Administratively enables an interface |
| `ip default-gateway 172.16.1.1` | Sets the Layer 2 switch's gateway for off-subnet management |
| `interface range ...` | Selects multiple physical ports for one configuration change |
| `shutdown` | Administratively disables unused ports |
| `service password-encryption` | Applies reversible obfuscation to supported plaintext configuration passwords; **not strong encryption** |
| `security passwords min-length 10` | Enforces a minimum length for subsequently configured passwords on supporting IOS versions |
| `enable secret ...` | Stores a hashed privileged EXEC password |
| `no ip domain-lookup` | Prevents mistyped commands from triggering DNS hostname lookups |
| `ip domain-name CCNA.com` | Sets domain name used in the RSA key identity |
| `username ... secret ...` | Creates a local account with a hashed password for SSH authentication |
| `crypto key generate rsa` | Generates RSA keys needed by the SSH server |
| `ip ssh version 2` | Requests SSH version 2 |
| `login block-for 180 attempts 4 within 120` | Blocks login attempts for 180 seconds after 4 failures within 120 seconds |
| `line vty 0 4` | Selects remote terminal lines 0 through 4 |
| `transport input ssh` | Allows SSH but disallows Telnet on those lines |
| `login local` | Uses locally defined usernames and passwords for VTY login |
| `exec-timeout 6 0` | Ends idle EXEC sessions after 6 minutes, 0 seconds |
| `copy running-config startup-config` | Saves running settings in NVRAM for reboot persistence |

## Verification checklist

Run these in privileged EXEC mode (`RTA#` or `SW1#`):

```cisco
show ip interface brief
show running-config
show startup-config
show ip ssh
show ssh
show crypto key mypubkey rsa
show line
```

Some commands vary by Packet Tracer device model and IOS implementation. Use `show ?` to discover supported commands.

Confirm:

- [ ] PCA is `172.16.1.10/24`, gateway `172.16.1.1`.
- [ ] RTA G0/0 is `172.16.1.1/24` and up/up.
- [ ] SW1 VLAN 1 is `172.16.1.2/24` and up/up.
- [ ] SW1 default gateway is `172.16.1.1`.
- [ ] SW1 F0/2–F0/24 and G0/2 are administratively down.
- [ ] Router has a 10-character minimum, login blocking, and 6-minute VTY timeout.
- [ ] Both devices have an enable secret, local SSH user, and RSA keys.
- [ ] Both devices use `CCNA.com` and SSH-only VTY transport.
- [ ] PCA can ping and SSH to RTA and SW1.
- [ ] Both configurations are saved to startup-config.

## Troubleshooting

| Symptom | Likely cause | What to check |
|---|---|---|
| `RTA(config)#` command is rejected | Wrong mode or command syntax | Use `?` for help; check `security passwords min-length 10` |
| `enable secret` does not work | Password entered incorrectly or you are not at `>` | Run `enable` at `RTA>`; enter the exact secret, case-sensitive |
| `crypto key generate rsa` fails | Missing hostname or domain name | Check `hostname` and `ip domain-name CCNA.com` |
| RSA generation asks for modulus | Expected interactive step | Type `1024`, then Enter |
| SSH connection refused | SSH server/keys missing or VTY disallows SSH | Check `show ip ssh`, RSA keys, `transport input ssh` |
| SSH says authentication failed | Wrong SSH username/password or missing `login local` | Verify `username ... secret ...` and VTY configuration |
| Ping to RTA fails | Wrong IP, subnet, cable, or shutdown interface | Check PCA IP and `show ip interface brief` |
| Ping to SW1 fails | VLAN 1 SVI down or physical link/VLAN issue | Check `show ip interface brief`, active VLAN 1 ports, and cables |
| Switch SSH fails but router SSH works | Switch SVI/SSH configuration incomplete | Verify switch IP, active VLAN 1, RSA keys, local user, and VTY settings |
| Device unexpectedly rejects logins | Router login-blocking rule triggered | Wait 180 seconds after the blocking condition; verify credentials |
| Settings disappear after reboot | Running config not saved | Use `copy running-config startup-config` |

## Security concepts to remember for Network+

**Console vs SSH:** Console access is a direct out-of-band connection for initial configuration; SSH is encrypted remote CLI access over an IP network.

**Authentication vs authorization:** `login local` checks identity against local accounts. `enable secret` separately protects access to privileged EXEC commands. Neither alone creates a complete role-based authorization design.

**Hashing vs encryption:** `secret` stores a one-way password hash. `service password-encryption` uses weak reversible encoding for applicable plaintext passwords; do not treat it as secure credential storage.

**Least privilege and attack surface:** Disabling unused ports, turning off Telnet, using strong credentials, and setting idle timeouts reduce exposure. In real deployments, also consider AAA, management ACLs, current crypto algorithms, and dedicated management VLANs.

**SSH prerequisites:** Reachable management IP + hostname + domain name + RSA keys + SSH-enabled VTY + local user authentication.

---

*Lab-specific reference based on the supplied Module 17 Lab 40 instructions. Packet Tracer syntax and available interfaces can vary by device image.*


---

# Integrated Study Companion: VTY, SSH, and Local Authentication

This section expands on Step 1(m) and Step 2(l). Use the complete lab commands above for execution, then this section for review.

## The three commands to memorize

| Command | What it means | Question it answers |
|---|---|---|
| `line vty 0 15` | Enter configuration for virtual terminal lines | Where do remote sessions enter? |
| `transport input ssh` | Allow SSH, not Telnet, on those lines | Which remote access protocol is allowed? |
| `login local` | Authenticate against the device's local username database | How is the user authenticated? |

**Memory cue: LINE → TRANSPORT → LOGIN** (where, how, who).

## Before VTY SSH can work

On SW1, make sure these prerequisites are present:

```cisco
hostname SW1
interface vlan 1
 ip address 172.16.1.2 255.255.255.0
 no shutdown
exit
ip default-gateway 172.16.1.1
ip domain-name CCNA.com
username netadmin secret MySecurePass2027!
crypto key generate rsa
```

When Packet Tracer prompts for RSA modulus size, enter `1024` **for this lab**. For modern production deployments, prefer RSA 2048 bits or stronger where supported. VLAN 1's SVI is only operational if the VLAN is active and at least one associated switch port is up and forwarding.

Optionally force SSH version 2 if supported:

```cisco
ip ssh version 2
```

## Passwords are different

- `enable secret ...` protects privileged EXEC mode (`SW1#`).
- `username netadmin secret ...` creates the credentials used by `login local` for SSH.
- `service password-encryption` only reversibly obscures certain plaintext passwords; it is **not** a substitute for `secret`.

## How to test from PCA

PCA addressing: `172.16.1.10 /24`, gateway `172.16.1.1`.

From PCA's **Desktop → Command Prompt**:

```text
ping 172.16.1.2
ssh -l netadmin 172.16.1.2
```

Enter the password from the SW1 `username ... secret ...` command, **not** the `enable secret` password. The Packet Tracer SSH syntax uses a lowercase `-l` (letter L).

## Verify and troubleshoot

On SW1:

```cisco
show ip interface brief
show running-config | section line vty
show running-config | include username
show ip ssh
show crypto key mypubkey rsa
```

If `| section` or `show crypto key` is unsupported by your Packet Tracer device, use `show running-config` or `show ip ssh` instead.

| Symptom | What to check |
|---|---|
| SSH connection refused | `transport input ssh`, RSA keys, SSH support |
| Authentication fails | `login local`, exact username, local user's password |
| Ping fails | PCA IP/mask, SW1 VLAN 1 IP, active switch ports, cabling |
| VTY range rejected | Try `line vty 0 4`, then `line vty 5 15` if available |
| Locked out | Use the console connection to recover, if still accessible |

## Quick self-test

1. What does VTY stand for? **Virtual Teletype.**
2. What command limits remote access to SSH? **`transport input ssh`.**
3. What command checks locally configured users? **`login local`.**
4. What command sets a six-minute idle timeout? **`exec-timeout 6 0`.**
5. Does SSH use `enable secret` for initial login? **No; with `login local`, it uses the local username and its secret.**
6. Why use SSH instead of Telnet? **SSH encrypts the management session.**



## Active recall practice

Without looking above, write the commands to select all VTY lines, restrict incoming remote access to SSH, authenticate against locally configured users, and disconnect idle sessions after six minutes. Then check your answers against Step 2(l–m).


---
---
---

## 🔗 Navigation

* [Home](/)
* [Network+ Portfolio](/network-portfolio/)
  * **[FORMATIVE MODULES](/network-portfolio/formative-modules/)**
  * [Video Walkthroughs](/network-portfolio/videos/)
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* [Trading+](/trading/)
* [Bible Study](/bible-study/)
* [About the Portfolio](/about/)

---
---
---
