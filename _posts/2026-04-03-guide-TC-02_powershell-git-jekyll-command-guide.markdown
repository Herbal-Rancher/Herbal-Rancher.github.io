---
layout: post
title: "Technical Communication | PowerShell, Git, and Jekyll Commands"
lab_title: "PowerShell, Git, and Jekyll Commands"

lesson: "10.0" 
lesson_id: "01.02.00"
sort_order: "010200"

categories: [portfolio, guides]

category: technical-communication
category_display: Technical Communication

subcategory: Reference-Guides
subcategory_display: Reference Guides

content_type: guide
content_type_display: Guide

sort_order: "900002"

tags:
  - switch-security
  - switch-security
  - github-pages
  - jekyll
  - git
  - troubleshooting
  - setup
  - reference-guide

permalink: /network-portfolio/guides/powershell-git-jekyll-commands/
status: complete

topics:
  - router-configuration
  - routing-tables
  - connectivity-testing

tools: 
  - cisco-packet-tracer
  
date: 2026-04-03 09:14:11 -0700
video: ""
pdf: ""
diagram: ""

protocols: []

---

This page provides a structured command reference for managing a local Jekyll site, validating changes, and publishing updates to GitHub Pages.
<!--more-->
---

## Navigate to Project
```powershell 
cd C:\Users\herba\Herbal-Rancher.github.io
```

---

## Check Repository Status
```powershell 
git status 
git branch 
git remote -v
```
---

## Sync With GitHub
```powershell 
 git checkout main 
 git pull --rebase origin main
```
---

## Start Local Jekyll Server
```powershell 
bundle exec jekyll serve --baseurl ""
```
Open in browser:
```powershell
http://localhost:4000
```
Stop server:
```powershell
Ctrl + C
```
---

## Editing Workflow

1. Start the local server
2. Edit content files (_posts, pages, layouts, assets)
3. Save changes
4. Refresh browser
5. Repeat until output is correct

---

## Stage Changes
```powershell 
git add .
```
Specific files or folders:
```powershell 
git add _posts 
git add assets 
git add Gemfile.lock
```
---

## Commit Changes
```powershell 
git commit -m "Update site content"
```
---

## Push to GitHub
```powershell 
git push origin main
```
---

## Full Daily Workflow
Change to local github directory , check status, pull latest changes, start server, edit files, validate output, stage changes, commit, and push to GitHub:
```powershell 
cd C:\Users\herba\Herbal-Rancher.github.io 
git status 
git pull --rebase origin main 
bundle exec jekyll serve --baseurl "" 
git add . 
git commit -m "Update site content" 
git push origin main
```
---

## Fix Push Rejected
```powershell 
git pull --rebase origin main 
git push origin main
```
If conflicts occur:
```powershell 
git status
```
# resolve files manually
```powershell 
git add . 
git rebase --continue 
git push origin main
```
---

## View Recent Commits
```powershell 
git log --oneline -5
```
---

## Undo Local Changes
```powershell 
git restore .
```
Undo one file:
```powershell 
git restore filename.md
```
---

## Unstage Files
```powershell 
git restore --staged .
```
---

## Check Repo Location
```powershell 
git rev-parse --show-toplevel
```
---

## Install Dependencies
```powershell 
bundle install
```
---

## Update Gems
```powershell 
bundle update 
bundle update github-pages
```
---

## Build Site Without Serving
```powershell 
bundle exec jekyll build
```
---

## GitHub Actions Platform Fix
```powershell 
bundle lock --add-platform x86_64-linux 
git add Gemfile.lock 
git commit -m "Add Linux platform for GitHub Actions" 
git push origin main
```
---

## Port Already in Use
```powershell 
bundle exec jekyll serve --baseurl "" --port 4001
```
---

## Restart Server if Not Updating

Ctrl + C
```powershell 
bundle exec jekyll serve --baseurl ""
```
---

## Workflow Summary

Pull → Serve → Edit → Validate → Commit → Push


---
---
---

## 🔗 Navigation

* **[HOME](/)**
* [Network+ Portfolio](/network-portfolio/)
  * [Formative Modules](/network-portfolio/formative-modules/)
  * [Video Walkthroughs](/network-portfolio/videos/)
  * [Study Diagrams](/network-portfolio/study-diagrams/)
* [Bible Study](/network-portfolio/bible-study/)
* [Behind the Portfolio](/network-portfolio/behind-the-portfolio/)

---
---
---
