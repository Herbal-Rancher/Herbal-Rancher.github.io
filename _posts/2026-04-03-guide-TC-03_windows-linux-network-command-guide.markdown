---
layout: post
title: "Technical Communication | Windows & Linux Network Administration Commands"
lab_title: "Windows & Linux Network Administration Commands"

lesson: "TC.03" 
lesson_id: "01.03.00"
sort_order: "010300"

categories: [portfolio, guides]

category: technical-communication
category_display: Technical Communication

subcategory: Reference-Guides
subcategory_display: Reference Guides

content_type: guide
content_type_display: Guide


tags:
  - windows
  - linux
  - networking
  - cybersecurity
  - command-reference
  - troubleshooting

permalink: /network-portfolio/guides/windows-linux-network-commands/
status: complete

date: 2026-04-03 09:13:11 -0700
video: ""
pdf: ""
diagram: ""

tools:
  - ipconfig
  - ip
  - ping
  - traceroute
  - tracert
  - nslookup
  - dig
  - netstat
  - ss
  - tcpdump

protocols:
  - DNS
  - DHCP
  - ICMP
  - TCP
  - UDP
  - ARP

topics:
  - network-administration
  - cybersecurity
  - troubleshooting
  - windows-linux-command-conversion
  - incident-response

---

# IP Configuration

| Task | Windows | Linux |
|--------|---------|---------|
| Show IP configuration | `ipconfig` | `ip addr` |
| Detailed configuration | `ipconfig /all` | `ip addr && ip route` |
| Release DHCP lease | `ipconfig /release` | `dhclient -r` |
| Renew DHCP lease | `ipconfig /renew` | `dhclient` |
| Display hostname | `hostname` | `hostname` |
| Display IP only | `hostname -I` | `hostname -I` |

---

# Network Interfaces

| Task | Windows | Linux |
|--------|---------|---------|
| View adapters | `Get-NetAdapter` | `ip link` |
| Enable adapter | `Enable-NetAdapter` | `ip link set up` |
| Disable adapter | `Disable-NetAdapter` | `ip link set down` |
| Interface statistics | `netstat -e` | `ip -s link` |

---

# Routing

| Task | Windows | Linux |
|--------|---------|---------|
| View routing table | `route print` | `ip route` |
| Add route | `route add` | `ip route add` |
| Delete route | `route delete` | `ip route del` |
| View default gateway | `ipconfig` | `ip route` |

---

# DNS

| Task | Windows | Linux |
|--------|---------|---------|
| Query DNS | `nslookup` | `nslookup` |
| Alternative DNS lookup | N/A | `dig` |
| View DNS servers | `ipconfig /all` | `cat /etc/resolv.conf` |
| Flush DNS cache | `ipconfig /flushdns` | `resolvectl flush-caches` |

---

# Connectivity Testing

| Task | Windows | Linux |
|--------|---------|---------|
| Ping host | `ping` | `ping` |
| Trace route | `tracert` | `traceroute` |
| Path analysis | `pathping` | `mtr` |
| Test TCP port | `Test-NetConnection` | `nc` |

---

# Active Connections

| Task | Windows | Linux |
|--------|---------|---------|
| View connections | `netstat -ano` | `ss -tulnp` |
| Listening ports | `netstat -an` | `ss -l` |
| Show processes | `tasklist` | `ps aux` |
| Kill process | `taskkill /PID` | `kill` |

---

# Network Shares

| Task | Windows | Linux |
|--------|---------|---------|
| View shares | `net share` | `showmount -e` |
| Map drive | `net use` | `mount` |
| View sessions | `net session` | `smbstatus` |

---

# User Administration

| Task | Windows | Linux |
|--------|---------|---------|
| Current user | `whoami` | `whoami` |
| List users | `net user` | `cat /etc/passwd` |
| Add user | `net user /add` | `useradd` |
| Change password | `net user` | `passwd` |
| Group membership | `net localgroup` | `groups` |

---

# System Information

| Task | Windows | Linux |
|--------|---------|---------|
| System information | `systeminfo` | `uname -a` |
| OS version | `winver` | `cat /etc/os-release` |
| Running processes | `tasklist` | `ps aux` |
| Running services | `services.msc` | `systemctl` |

---

# Log Analysis

| Task | Windows | Linux |
|--------|---------|---------|
| Security logs | Event Viewer | `/var/log/auth.log` |
| System logs | Event Viewer | `/var/log/syslog` |
| View logs | `Get-EventLog` | `journalctl` |
| Real-time logs | Event Viewer | `tail -f` |

---

# Packet Capture

| Task | Windows | Linux |
|--------|---------|---------|
| Packet capture | `pktmon` | `tcpdump` |
| Protocol analysis | Wireshark | Wireshark |
| Capture interface list | `pktmon list` | `tcpdump -D` |

---

# Security Investigation

| Task | Windows | Linux |
|--------|---------|---------|
| Open ports | `netstat -ano` | `ss -tulnp` |
| ARP table | `arp -a` | `arp -a` |
| DNS cache | `ipconfig /displaydns` | `resolvectl statistics` |
| Active sessions | `query user` | `who` |
| Logged-in users | `query user` | `w` |

---

# File System Analysis

| Task | Windows | Linux |
|--------|---------|---------|
| List files | `dir` | `ls -la` |
| Change directory | `cd` | `cd` |
| Copy file | `copy` | `cp` |
| Move file | `move` | `mv` |
| Delete file | `del` | `rm` |
| Search files | `dir /s` | `find` |

---

# Cybersecurity Incident Response

## Identify Active Connections

Windows

```powershell
netstat -ano
````

Linux

```bash
ss -tulnp
```

---

## Determine Process Using Port 443

Windows

```powershell
netstat -ano | findstr :443
tasklist
```

Linux

```bash
ss -tulnp | grep 443
```

---

## Review ARP Table

Windows

```powershell
arp -a
```

Linux

```bash
arp -a
```

---

## Check DNS Resolution

Windows

```powershell
nslookup google.com
```

Linux

```bash
nslookup google.com
```

---

# Top 20 Commands Every Network Administrator Should Know

```text
ipconfig
ip addr
ip route
ping
tracert
traceroute
pathping
mtr
nslookup
dig
netstat
ss
arp
route
hostname
whoami
tcpdump
wireshark
systemctl
journalctl
```

---

# Top 20 Commands Every Cybersecurity Analyst Should Know

```text
netstat
ss
tcpdump
wireshark
nslookup
dig
arp
tasklist
ps aux
whoami
who
w
journalctl
tail
find
grep
systemctl
route
ip route
ping
```

---

# Key Takeaways

Modern Linux networking relies primarily on the `ip` command suite (`ip addr`, `ip route`, and `ip link`) while Windows relies heavily on `ipconfig`, `route`, and PowerShell networking cmdlets.

For troubleshooting, the most commonly used commands are:

```text
ipconfig
ip addr
ping
nslookup
tracert
traceroute
netstat
ss
arp
tcpdump
```

Mastering these commands provides a strong foundation for Network+, Security+, CCNA, Linux administration, SOC analyst work, and incident response investigations.

```
```


---
---
---

## 🔗 Navigation

* **[HOME](/)**
* [Network+ Portfolio](/network-portfolio/)
  * [Formative Lessons](/network-portfolio/formative-lessons/)
  * [Lab Walkthroughs](/network-portfolio/labs/)
  * [Video Walkthroughs](/network-portfolio/videos/)
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* [Bible Study](/network-portfolio/Bible-Study/)
* [Behind the Portfolio](/network-portfolio/behind-the-portfolio/)

---
---
---
