---
layout: post
title: "Push Latest Updates to GitHub Repository"
lesson: 1.0
order: 1.5
categories: [portfolio, blog, walkthroughs]
date: 2026-04-12 11:12:12 -0200
tags: [github-pages, jekyll, git, troubleshooting, setup, branching, workflow]
permalink: /portfolio/walkthroughs/lesson-1-0/walkthroughs-1-5/
---

definitely need something better than this title, but for now, this is the walkthrough for how to update your local repository with the latest changes from GitHub before you start working on your next blog post. This is an important step to ensure that you are working with the most up-to-date version of your project and to avoid any potential conflicts when you push your changes back to GitHub.	

---
<!--more-->
### Step 1 — Make sure you're in your project folder
```bash
cd path/to/your/repo
```
---

### Step 2 — Check your current status and branch
```bash
git status
git branch
```
Ensure you are on: ** main **

If NOT on main:
```bash
git checkout main
```
---

### Step 3 — Pull latest from GitHub to avoids overwrite conflicts

```bash
git pull origin main
```
This avoids overwrite conflicts.

### Step 4 - Then continue your normal workflow

```bash
git add .
git commit -m "updated lesson and walkthrough format, added content for all areas"
git push origin main
```
---

### Why This Matters

* Prevents overwriting remote changes
* Keeps your workflow consistent
* Ensures accurate version control
* Aligns with **GitHub Flow best practices**

---

### 🔗 Navigation

* **[Formative Lessons](/portfolio/formative-lessons/)**
* **[Walkthroughs](/portfolio/walkthroughs/)**
* **[Network+ Portfolio](/portfolio/)**
* **[Home](/)**

---
