---
layout: post
title: "Quick Reference Guide: Git Commands"
lesson: 1.0
order: 1.9
categories: [portfolio, walkthroughs, network]
date: 2026-04-14 11:14:11 -0700
tags: [github-pages, jekyll, git, troubleshooting, setup, reference-guide]
permalink: /portfolio/walkthroughs/lesson-1-0/walkthroughs-1-9/
---

This section provides a quick reference guide for common Git commands used throughout this walkthrough and future blog updates.

---

#### 1. Initial Setup – Basic Git Workflow
```bash
git add .
git commit -m "initial commit"
git push origin main
```
---
<!--more-->
#### 2. Sync Local Repository with GitHub (Start Here for New Work)

```bash
git checkout main
git pull origin main
git status
```
---
#### 3. Branch Mismatch Fix (gh-website → main)


```bash
git checkout -b main
git merge gh-website
git push origin main --force
```
---

#### 4. Incorrect Remote Repository URL Fix

```bash
git remote set-url origin https://github.com/<username>/<repository>.git
```
---

#### 5. Push Blocked by Email Privacy Settings Fix

```bash
git commit --amend --reset-author
git push origin main --force
```
---

#### 6. Dependency Fix (GitHub Pages Compatibility)
```bash
gem "github-pages", "~> 228", group: :jekyll_plugins
```
---

#### 7. Clean Gemfile
```bash
source "https://rubygems.org"
gem "github-pages", "~> 228", group: :jekyll_plugins
```

---

#### 8. Deployment Command
```bash
git push origin main --force
```
---

#### 9. Add New Blog Post Workflow
```bash
git add .
git commit -m "add new blog post"
git push origin main
```
---

### 🔗 Navigation

* **[Formative Lessons](/portfolio/formative-lessons/)**
* **[Walkthroughs](/portfolio/walkthroughs/)**
* **[Network+ Portfolio](/portfolio/)**
* **[Home](/)**

---
