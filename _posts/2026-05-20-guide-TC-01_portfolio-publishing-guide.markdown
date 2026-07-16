---
layout: post
title: "Technical Communication | Portfolio Publishing Guide"
lab_title: "Portfolio Publishing Guide"

lesson: "10.0" 
lesson_id: "10.00.10"
sort_order: "100010"

categories: [portfolio, guides]

category: technical-communication
category_display: Technical Communication

subcategory: Reference-Guides
subcategory_display: Reference Guides

content_type: guide
content_type_display: Guide


permalink: /network-portfolio/guides/portfolio-publishing-guide/

status: complete

topics: [markdown, yaml, liquid, jekyll, github-pages, technical-writing, documentation, portfolio-development, information-architecture]

tools: [Markdown, Jekyll, GitHub, GitHub-Pages, Liquid, VS-Code]

---

# Portfolio Publishing Guide

This guide serves as the central reference for creating, organizing, publishing, and maintaining content throughout my technical portfolio.

It documents the standards used for metadata, Markdown, Jekyll, Liquid, GitHub Pages, content organization, and publishing workflows.

<!--more-->

---

# Metadata Standard

All content should use the same metadata structure regardless of whether the content is a lab, assessment, guide, diagram, study, project, or video.

## Required Fields

```yaml
lesson_id:
title:

category:
category_display:

subcategory:
subcategory_display:

content_type:
content_type_display:

topics:
tools:

status:
sort_order:
permalink:
```

---

# Example Front Matter

```yaml
---
layout: post

title: "Use PowerShell Remote Management"

lesson_id: "13.3.9"

category: systems-administration
category_display: Systems Administration

subcategory: remote-administration
subcategory_display: Remote Administration

content_type: lab
content_type_display: Lab

sort_order: "133009"

status: complete

topics: [remote-administration, powershell-remoting, remote-management, windows-administration]

tools: [PowerShell, Windows]
---
```

---

# Portfolio Taxonomy

## Networking Fundamentals

Subcategories:

* TCP/IP
* DHCP Configuration
* DHCP Troubleshooting
* DNS Administration
* DNS Troubleshooting
* Network Troubleshooting

---

## Infrastructure

Subcategories:

* Switch Security
* Switch Configuration
* Switch Monitoring
* Routing
* Wireless
* Network Services

---

## Security

Subcategories:

* Reconnaissance
* Packet Analysis
* Attack Techniques
* Security Monitoring

---

## Systems Administration

Subcategories:

* Remote Administration
* Windows Administration
* Linux Administration

---

## Technical Communication

Subcategories:

* Markdown & Jekyll
* GitHub
* Portfolio Development
* Technical Writing

---

# Content Types

```yaml
content_type: lab
content_type_display: Lab
```

```yaml
content_type: assessment
content_type_display: Assessment
```

```yaml
content_type: guide
content_type_display: Guide
```

```yaml
content_type: diagram
content_type_display: Diagram
```

```yaml
content_type: project
content_type_display: Project
```

```yaml
content_type: study
content_type_display: Study
```

---

# Markdown Reference

## Headings

Syntax:

```
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
```

Result:

# Heading 1

## Heading 2

### Heading 3

#### Heading 4

---

## Text Formatting

### Italic

Syntax:

```
*italic text*
```

Result:

*italic text*

### Bold

Syntax:

```
**bold text**
```

Result:

**bold text**

### Bold and Italic

Syntax:

```
***bold and italic text***
```

Result:

***bold and italic text***

---

## Lists

### Unordered

Syntax:

```
- Item One
- Item Two
- Item Three
```

Result:

* Item One
* Item Two
* Item Three

### Ordered

Syntax:

```
1. First
2. Second
3. Third
```

Result:

1. First
2. Second
3. Third


---

# Links

## Internal Link

### Syntax

```
[Video Gallery](/)
```

### Result

[Video Gallery](/network-portfolio/videos/)

---

## External Link

### Syntax

```
[Herbal Rancher GitHub](https://github.com/Herbal-Rancher)
```

### Result

[Herbal Rancher GitHub](https://github.com/Herbal-Rancher)

---

# Images

## Standard Image

### Syntax

```
![Alt Text](/assets/images/study-diagrams/top-network-ports-for-compTIA-network-exam-prep-diagram-chatgpt-rendered-image.png)
```

### Result
![Alt Text](/assets/images/study-diagrams/top-network-ports-for-compTIA-network-exam-prep-diagram-chatgpt-rendered-image.png)

---

## Clickable Image

### Syntax

```
[![Thumbnail](/assets/images/study-diagrams/top-network-ports-for-compTIA-network-exam-prep-diagram-chatgpt-rendered-image.png)](https://herbal-rancher.github.io/)
```
### Result

[![Thumbnail](/assets/images/study-diagrams/top-network-ports-for-compTIA-network-exam-prep-diagram-chatgpt-rendered-image.png)](https://herbal-rancher.github.io/)

---

## Inline Code

Syntax:

```
Use `ipconfig` to view configuration.
```

Result:

Use `ipconfig` to view configuration.

---

## Code Block

Syntax:

````text
```powershell
ipconfig /all
ping 192.168.0.1
```
````

Result:

```powershell
ipconfig /all
ping 192.168.0.1
```

---

# Liquid Reference

## Variables

```liquid
{{ page.title }}
{{ page.url }}
{{ site.posts.size }}
```

---

## Conditions

```liquid
{% if page.category %}
{{ page.category }}
{% endif %}
```

---

## Assignments

```liquid
{% assign posts = site.posts %}
```

```liquid
{% assign category_posts = posts | where: "category", category %}
```

---

## Loops

```liquid
{% for post in site.posts %}
{{ post.title }}
{% endfor %}
```

---

# Learning Journey Loop Pattern

## Category Order

```liquid
{% assign category_order = "networking-fundamentals|infrastructure|security|systems-administration|technical-communication" | split: "|" %}
```

## Category Display

```liquid
{% assign category_display = category_posts | map: "category_display" | compact | first %}
```

## Subcategory Display

```liquid
{% assign subcategory_display = subcategory_posts | map: "subcategory_display" | compact | first %}
```

---

# Publishing Checklist

* Verify title
* Verify lesson_id
* Verify category
* Verify subcategory
* Verify content_type
* Verify permalink
* Verify sort_order
* Verify topics
* Verify tools
* Verify internal links
* Verify images
* Verify GitHub commit
* Verify local build
* Verify published page

---

# Site Architecture

* Home
* Learning Journey
* Video Gallery
* Guides
* Labs
* Assessments
* Diagrams

The Home page serves as the visitor entry point.

The Learning Journey page serves as the primary portfolio roadmap.

Individual content pages provide the evidence supporting each skill, concept, project, and study area.

---

# Key Takeaways

Technical communication is more than writing.

It includes documentation, information architecture, discoverability, maintainability, organization, automation, and knowledge sharing.

Consistent metadata enables the portfolio to scale while remaining organized, searchable, and easy to maintain.


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
