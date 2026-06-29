---
layout: post
title: "Technical Communication | Initial GitHub Site Setup"
lab_title: "Initial GitHub Site Setup"

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
video: ""
pdf: ""
diagram: ""

protocols: []

---

In this lab, I demonstrate how to resolve a common issue where local changes are not reflected on GitHub. The goal is to ensure that the contents of a local project folder completely replace the remote repository and successfully publish to GitHub Pages.
<!--more-->
---

### Problem Scenario

* Local files were updated successfully
* `git add` and `git commit` were run
* Changes did **not appear on GitHub**
* GitHub Pages build showed an error:

  > "The log was not found. It may have been deleted based on retention settings."

---

### Objective

Force the local repository to overwrite the remote `main` branch and trigger a successful GitHub Pages deployment.

---

### Prerequisites

* Git installed on local machine
* GitHub account and repository created
* Local project folder ready

---

### Step 1: Navigate to Local Project Folder

Open a terminal and move into your project directory:

```bash
cd path/to/your/local/folder
```

---

### Step 2: Configure Git Identity

Ensure Git is properly configured:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

Verify configuration:

```bash
git config --list
```

---

### Step 3: Initialize Git Repository

If the folder is not already a Git repository:

```bash
git init
```

---

### Step 4: Connect to GitHub Repository

Add your remote repository:

```bash
git remote add origin https://github.com/<username>/<repository>.git
```

Verify the connection:

```bash
git remote -v
```

If the remote already exists, update it:

```bash
git remote set-url origin https://github.com/<username>/<repository>.git
```

---

### Step 5: Stage All Files

Prepare all files for commit:

```bash
git add .
```

---

### Step 6: Commit Changes

Use a descriptive commit message:

```bash
git commit -m "updated blogs, homepage, added first blog entries, ready for assignments, labs and bible study"
```

---

### Step 7: Force Push to GitHub

Push changes and overwrite the remote `main` branch:

```bash
git push origin main --force
```

#### Important Note:

* The `--force` flag replaces the remote repository with local content
* Use with caution in collaborative environments

---

### Step 8: Verify Deployment

1. Navigate to your GitHub repository
2. Confirm updated files are visible
3. Open GitHub Pages site:

   ```
   https://<username>.github.io/<repository>/
   ```
4. Allow 1–5 minutes for the site to rebuild

---

### Key Concepts Learned

* Difference between local and remote repositories
* Importance of pushing commits to GitHub
* How to resolve sync issues using force push
* Basic Git workflow: add → commit → push
* GitHub Pages deployment process

---

### Troubleshooting Tips

* If changes don’t appear:

  * Ensure you are pushing to the correct branch (`main`)
  * Verify remote URL with `git remote -v`
* If commit fails:

  * Check Git identity configuration
* If Pages doesn’t update:

  * Wait a few minutes and refresh
  * Confirm Pages is enabled in repository settings

---

### Reflection

This lab demonstrates a real-world GitHub issue and its resolution. Understanding how to properly sync local and remote repositories is essential for developers, especially when deploying live web content using GitHub Pages.


---
---
---

## 🔗 Navigation

* **[HOME](/)**
* [Network+ Portfolio](/network-portfolio/)
  * [Formative Modules](/network-portfolio/formative-modules/)
  * [Video Walkthroughs](/network-portfolio/videos/)
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* [Bible Study](/bible-study/)
* [About the Portfolio](/zabout-the-portfolio/)

---
---
---

