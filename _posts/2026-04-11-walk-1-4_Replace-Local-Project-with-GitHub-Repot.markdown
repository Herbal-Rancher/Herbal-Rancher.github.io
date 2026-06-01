---
layout: post
title: "Lab 4: Update Local Project With GitHub Latest Repository"

lesson: "1.0"
lab: "1.4"
sort_order: "010400"

categories: [portfolio, labs]
tags: [github-pages, jekyll, git, troubleshooting, setup, branching, workflow]
permalink: /portfolio/labs/module-1-0/update-local-project-with-github-latest-repository/
status: complete

date: 2026-04-11 11:14:14 -0200
video: ""
pdf: ""
diagram: ""

tools: []
protocols: []
topics: []
---

Before starting a new blog post or walkthrough, it’s important to ensure your **local repository matches the latest version on GitHub**.

This prevents conflicts, missing updates, or accidental overwrites.
<!--more-->
---

### Step 1: Check Current Branch
```bash
git branch
```
Ensure you are on:  main

If not:
```bash
git checkout main
```
---

### Step 2: Pull Latest Changes from GitHub

```bash
git pull origin main
```

This ensures your local repository includes:

* Latest commits
* Any fixes made directly on GitHub
* Updated site configuration

---

### Step 3: Verify Clean Working Directory

```bash
git status
```

You should see:

```bash
nothing to commit, working tree clean
```
---

### Step 4: Start Your Next Blog Post

Create your new file inside `_posts/`, for example:

```bash
_posts/2026-04-06-next-walkthrough.md
```

Then continue your normal workflow:

```bash
git add .
git commit -m "add walkthrough 3 blog post"
git push origin main
```
---

### Why This Matters

* Prevents overwriting remote changes
* Keeps your workflow consistent
* Ensures accurate version control
* Aligns with **[GitHub Flow best practices](https://guides.github.com/introduction/flow/)**


---
---
---

## 🔗 Navigation

* **[HOME](/)**
* [Network+ Portfolio](/portfolio/)
  * [Formative Lessons](/portfolio/formative-lessons/)
  * [Lab Walkthroughs](/portfolio/labs/)
  * [Video Walkthroughs](/portfolio/videos/)
  * [Study Diagrams](/portfolio/study-diagrams/)
* [zBible Study](/zBible-Study/)
* [About Me](/about/)

---
---
---