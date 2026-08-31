---
layout: post
title: "Technical Communication | Set Up a GitHub Pages Site"
lab_title: "Set Up a GitHub Pages Site"

lesson: "10.0"
lesson_id: "10.01.00"
sort_order: "100100"

categories: [portfolio, labs]

category: technical-communication
category_display: Technical Communication

subcategory: github
subcategory_display: GitHub

content_type: lab
content_type_display: Lab

tags: 
  - github-pages
  - jekyll
  - git
  - troubleshooting
  - setup
  - branching
  - workflow

permalink: /network-portfolio/labs/module-1-0/initial-github-site-setup/
status: complete

topics:
  - router-configuration
  - routing-tables
  - connectivity-testing

tools: 
  - cisco-packet-tracer
  
date: 2026-04-03 01:11:11 -0100

video_id: "zwGWxiwK79o"
video_url: "https://www.youtube.com/watch?v=zwGWxiwK79o"
thumbnail: "https://img.youtube.com/vi/zwGWxiwK79o/hqdefault.jpg"

pdf: ""
diagram: ""

protocols: []

---


# Initial GitHub Site Setup

## Overview

This guide documents the initial setup process used to create my GitHub Pages portfolio. The goal is to build a professional documentation site that grows alongside my Network+, Cybersecurity, Trading Journey, and Bible Study learning paths.

Rather than simply storing files, the site serves as a living portfolio that demonstrates technical knowledge, documentation skills, and continuous learning.

---

## Objectives

After completing this guide, you should have:

- A GitHub account
- A public repository
- GitHub Pages enabled
- A local development environment
- Jekyll running locally
- Visual Studio Code configured
- Git installed
- Git connected to GitHub
- Your first published website

---

# Prerequisites

Install the following software before beginning:

- Git
- GitHub account
- Visual Studio Code
- Ruby
- RubyGems
- Bundler
- Jekyll

---

# Step 1 – Create a GitHub Repository

1. Sign in to GitHub.
2. Click **New Repository**.
3. Choose a repository name.
4. Select **Public**.
5. Initialize the repository (optional).
6. Create the repository.

---

# Step 2 – Clone the Repository

Open Git Bash or a terminal.

```bash
git clone https://github.com/<username>/<repository>.git
```

Change into the project directory.

```bash
cd <repository>
```

---

# Step 3 – Install Jekyll

Install Bundler.

```bash
gem install bundler
```

Install Jekyll.

```bash
gem install jekyll
```

Create a new Jekyll site inside the repository.

```bash
jekyll new .
```

Install project dependencies.

```bash
bundle install
```

---

# Step 4 – Run the Local Website

Start the local server.

```bash
bundle exec jekyll serve
```

Open your browser.

```
http://localhost:4000
```

Every time you save a page, Jekyll automatically rebuilds the site.

---

# Step 5 – Enable GitHub Pages

Within your GitHub repository:

1. Open **Settings**.
2. Select **Pages**.
3. Under **Build and Deployment**, choose:
   - Deploy from Branch
   - Branch: **main**
   - Folder: **/(root)**
4. Save.

GitHub will build your website automatically after each push.

Your website will be available at:

```
https://username.github.io/repository/
```

---

# Step 6 – Configure the Site

Edit the `_config.yml` file.

Typical settings include:

```yaml
title: Herbal Rancher
description: Professional Learning Portfolio
baseurl: ""
url: "https://username.github.io"
theme: minima
```

As your portfolio grows, additional settings may include:

- Collections
- Plugins
- Navigation
- Defaults
- Markdown options
- Syntax highlighting

---

# Step 7 – Organize the Project

A recommended folder structure:

```
.
├── _data/
├── _includes/
├── _layouts/
├── _posts/
├── assets/
│   ├── css/
│   ├── images/
│   └── pdf/
├── network+
├── trading
├── bible-study
├── about
├── index.md
└── _config.yml
```

As your documentation expands, organize related pages into logical sections instead of placing everything in one folder.

---

# Step 8 – Git Workflow

Check repository status.

```bash
git status
```

Stage all changes.

```bash
git add .
```

Commit your work.

```bash
git commit -m "Describe your changes"
```

Push to GitHub.

```bash
git push origin main
```

GitHub Pages will automatically rebuild the site after each successful push.

---

# Troubleshooting

## Localhost Works but GitHub Displays a 404

Possible causes include:

- Incorrect permalink
- Wrong folder location
- Incorrect capitalization
- File not committed
- GitHub Pages build failure

Remember:

Windows is **not** case-sensitive.

GitHub Pages **is** case-sensitive.

For example:

```
Networking.md
```

is different from

```
networking.md
```

---

## YAML Errors

Always verify the front matter.

```yaml
---
layout: page
title: Example
permalink: /example/
---
```

Common issues include:

- Missing `---`
- Incorrect indentation
- Missing colon
- Missing quotation marks when needed

---

## Broken Links

Check:

- Folder names
- File names
- Permalinks
- Navigation links
- Relative vs. absolute paths

---

## GitHub Pages Build Errors

If the site does not update:

1. Open the repository.
2. Select **Actions**.
3. Review the latest workflow.
4. Correct any reported errors.
5. Commit and push again.

---

# Best Practices

- Test locally before pushing.
- Keep filenames lowercase.
- Use descriptive page titles.
- Maintain consistent permalinks.
- Organize content into logical sections.
- Commit frequently.
- Write meaningful commit messages.
- Document your learning as you progress.

---

# Lessons Learned

Building a GitHub Pages website is an excellent way to demonstrate technical skills while documenting your learning journey.

Over time, this portfolio can evolve into a professional knowledge base containing:

- Study guides
- Network diagrams
- Packet Tracer labs
- Troubleshooting documentation
- Knowledge articles
- Video walkthroughs
- Career projects
- Certification preparation
- Personal learning resources

Consistent documentation not only reinforces technical knowledge but also creates a portfolio that showcases practical experience to future employers and collaborators.

---

# Related Resources

- Git Installation
- GitHub Basics
- GitHub Pages
- Markdown Fundamentals
- Jekyll Basics
- Visual Studio Code
- Portfolio Organization
- Documentation Standards
- Creating Your First Page
- Publishing Updates to GitHub

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