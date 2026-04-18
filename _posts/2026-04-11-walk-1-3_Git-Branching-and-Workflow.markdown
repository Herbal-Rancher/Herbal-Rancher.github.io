---
layout: post
title: "Git Branching and Workflow"
lesson: 1.0
order: 1.3
categories: [portfolio, blog, walkthroughs]
date: 2026-04-11 11:13:14 -0200
tags: [github-pages, jekyll, git, troubleshooting, setup, branching, workflow]
permalink: /portfolio/walkthroughs/lesson-1-0/walkthroughs-1-3/
---

This walkthrough documents the transition from a **basic Git workflow** to a more **structured, industry-standard branching workflow**.

It builds on previous walkthroughs and establishes a repeatable process for safely updating and deploying changes to a GitHub Pages site.

---
<!--more-->
## Overview

In earlier work, changes were committed directly to the `main` branch. While effective for quick updates, this approach carries risk as projects grow.

This walkthrough introduces:

* Feature branches
* Controlled merges
* Safer deployment practices

The goal is to align with **real-world development workflows**.

---

### Why Branching Matters

Branching allows you to:

* Work on new features without breaking the live site
* Test changes before deployment
* Organize work into manageable units
* Maintain a clean and stable `main` branch

---

### Branching Strategy Used

This project uses a **feature branching model**:

* `main` → Production (live GitHub Pages site)
* `feature/*` → Development work

Example:

```
feature/formative-lessons-index
feature/walkthrough-2-update
```

---

### Step-by-Step Workflow

#### 1. Start from Main

Always begin by ensuring your local `main` branch is up to date:

```bash
git checkout main
git pull origin main
```

---

#### 2. Create a Feature Branch

Create a new branch for your work:

```bash
git checkout -b feature/<feature-name>
```

Example:

```bash
git checkout -b feature/formative-lessons-index
```

---

#### 3. Make Changes Locally

Update files, create pages, or modify content.

---

#### 4. Stage and Commit Changes

```bash
git add .
git commit -m "added formative lessons index page"
```

---

#### 5. Push Branch to GitHub

```bash
git push origin feature/<feature-name>
```

---

#### 6. Merge into Main

Option A: GitHub (Recommended)

1. Open your repository on GitHub
2. Click **Compare & Pull Request**
3. Review changes
4. Click **Merge Pull Request**

Option B: Command Line

```bash
git checkout main
git pull origin main
git merge feature/<feature-name>
git push origin main
```

---

#### 7. Clean Up Branch (Optional)

```bash
git branch -d feature/<feature-name>
```

---

### Deployment Behavior

GitHub Pages deploys from the `main` branch.

Only merged changes will:

* Trigger a build
* Appear on the live site

---

### When to Use Branches

Use branches when:

* Adding new pages
* Updating layouts or structure
* Testing new features
* Working on larger updates

Direct commits to `main` are acceptable for:

* Minor text edits
* Small fixes

---

### Lessons Learned

* Branching reduces risk during development
* Keeping `main` stable ensures consistent deployments
* GitHub Pull Requests provide visibility and control
* Structured workflows improve scalability

---

### Outcome

* Adopted a professional Git workflow
* Improved reliability of deployments
* Established a repeatable process for future updates

---

### Quick Reference: Branching Commands

#### Create and Switch to Branch

```bash
git checkout -b feature/<name>
```

#### Stage and Commit

```bash
git add .
git commit -m "message"
```

#### Push Branch

```bash
git push origin feature/<name>
```

#### Merge to Main (CLI)

```bash
git checkout main
git pull origin main
git merge feature/<name>
git push origin main
```

#### Delete Branch

```bash
git branch -d feature/<name>
```

---

### Next Steps

* Apply this workflow to all future portfolio updates
* Use branching for Wireshark lab documentation
* Expand into advanced Git workflows (rebasing, tagging, CI/CD)

---

### 🔗 Navigation

* **[Formative Lessons](/portfolio/formative-lessons/)**
* **[Walkthroughs](/portfolio/walkthroughs/)**
* **[Network+ Portfolio](/portfolio/)**
* **[Home](/)**

---

