---
layout: post
title: "Lab 6.6.5 - Explore nslookup"
lab_title: "Explore nslookup"

lesson: "04.0"
lesson_id: "06.06.05"
sort_order: "040605"

categories: [portfolio, labs]

category: networking-fundamentals
category_display: Networking Fundamentals

subcategory: dhcp-dns
subcategory_display: DHCP & DNS

content_type: lab
content_type_display: Lab

topics:
  - dns
  - nslookup
  - name-resolution
  - dns-queries
  - dns-troubleshooting

tools:
  - Nslookup
  - DNS
  - Windows-Terminal
  - ping

tags:
  - dns
  - nslookup
  - name-resolution
  - dns-troubleshooting
  - windows
  - terminal
  - networking
  - network-diagnostics
  - network-plus
  - testout

permalink: /network-portfolio/labs/module-6-0/lab-6-6-5/
status: complete


video: ""
video_id: "3fJ-T0xGQ5E"
video_url: "https://youtu.be/3fJ-T0xGQ5E"
thumbnail: "https://img.youtube.com/vi/3fJ-T0xGQ5E/hqdefault.jpg"

pdf: ""
diagram: ""

protocols: [DNS]
---

## Overview

In this lab, I explore the `nslookup` command-line utility to investigate Domain Name System (DNS) resolution, verify hostname-to-IP address mappings, and troubleshoot name resolution issues within a TCP/IP networking environment.

The focus is on interpreting DNS query results, identifying the DNS server answering a query, and distinguishing DNS failures from broader network connectivity problems.

---

## Video Walkthrough

Watch the complete walkthrough:

<a href="{{ page.video_url }}" target="_blank" rel="noopener noreferrer">
  <img src="{{ page.thumbnail }}"
       alt="{{ page.title }}"
       style="width:420px; border-radius:8px;">
</a>

---

## Learning objectives

- Explore the `nslookup` utility.
- Query DNS servers for hostname resolution.
- Verify hostname-to-IP address mappings.
- Interpret DNS responses.
- Identify the DNS server used for a lookup.
- Practice DNS troubleshooting with command-line tools.

## Key concepts

| Concept | Explanation |
| --- | --- |
| DNS | Translates domain names into IP addresses and supports other resource-record lookups. |
| `nslookup` | Command-line utility for querying DNS servers. |
| Forward lookup | Resolves a hostname to an IP address, commonly using A or AAAA records. |
| Reverse lookup | Attempts to resolve an IP address to a hostname using PTR records. |
| DNS server | Responds to DNS queries, often through a configured recursive resolver. |
| DNS response | Contains an answer or an error/status useful for troubleshooting. |

## Suggested hands-on workflow

1. **Record the baseline.** Note the device, interfaces, addressing, current configuration, and intended outcome.
2. **Plan the change.** Identify dependencies, permissions, and a rollback approach.
3. **Perform the lab task.** Compare DNS answers, record types, and configured resolvers.
4. **Verify.** Check the resulting configuration or packet evidence and test the expected behavior.
5. **Document.** Capture redacted screenshots/output, observations, issues, and resolution.
6. **Restore or save.** Save only approved changes; otherwise revert the lab environment.

## Command reference

The following are general study examples, not a transcript of the exact TestOut lab environment.

```powershell
nslookup example.com
nslookup -type=A example.com
nslookup -type=AAAA example.com
nslookup -type=MX example.com
nslookup example.com 8.8.8.8
```

### Interactive mode

```text
nslookup
> set type=A
> example.com
> set type=AAAA
> example.com
> exit
```

## Troubleshooting workflow

1. Confirm the hostname is spelled correctly.
2. Query the hostname with `nslookup` and record the responding DNS server.
3. Inspect returned IP addresses or DNS error messages.
4. Compare results with a known alternative DNS resolver when appropriate and permitted.
5. Test IP connectivity separately to distinguish DNS issues from routing or connectivity failures.
6. Record the evidence and any configuration changes.

## Common results to recognize

- **Successful answer:** The DNS server returns one or more relevant resource records.
- **NXDOMAIN / non-existent domain:** The queried name does not exist according to the DNS response.
- **Timeout:** The query did not receive a response within the allowed time; check reachability, filtering, or DNS service availability.
- **SERVFAIL:** The DNS server could not complete the query; further investigation may be needed.


## Security and operational notes

DNS response is not the same as application reachability.

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