---
layout: post
title: "Technical Communication | Deploy a GitHub Pages Website"
lab_title: "Deploy a GitHub Pages Website"

lesson: "10.0"
lesson_id: "10.06.00"
sort_order: "100600"

categories: [portfolio, labs]

category: technical-communication
category_display: Technical Communication

subcategory: github
subcategory_display: GitHub

content_type: lab
content_type_display: Lab

tags:

- github
- github-pages
- jekyll
- deployment
- static-website
- publishing
- workflow
- troubleshooting

permalink: /network-portfolio/labs/module-10-0/deploy-a-github-pages-website/
status: complete

topics:

- github-pages
- website-deployment
- static-site-hosting
- jekyll
- deployment-workflow

tools:

- github
- git
- visual-studio-code
- jekyll

date: 2026-04-03 06:15:00 -0700

video_id: ""
video_url: ""
thumbnail: ""

pdf: ""
diagram: ""

protocols: []

---

After committing and pushing your changes to GitHub, the final step is deploying the updated website using GitHub Pages.

GitHub Pages automatically builds and publishes static websites directly from a GitHub repository, making it an excellent platform for portfolios, documentation, and project websites.

<!--more-->

---

## Overview

This walkthrough demonstrates how to:

* Configure GitHub Pages
* Select the deployment source
* Publish a Jekyll website
* Monitor the deployment process
* Verify the live website
* Troubleshoot common deployment issues

---

## Prerequisites

Before beginning, confirm that:

* A GitHub repository exists.
* The project has been committed and pushed.
* GitHub Pages is enabled for the repository.
* The website builds successfully on your local computer.

---

## Quick Workflow

```text
Update Project
      ↓
Commit Changes
      ↓
Push to GitHub
      ↓
GitHub Pages Builds Site
      ↓
Verify Live Website
```

---

## Step 1 — Open the Repository

Log in to GitHub and open the repository you want to publish.

---

## Step 2 — Open GitHub Pages Settings

Navigate to:

**Settings → Pages**

Locate the **Build and deployment** section.

---

## Step 3 — Configure the Deployment Source

Select:

* **Source:** Deploy from a branch
* **Branch:** `main`
* **Folder:** `/ (root)`

Save the settings.

GitHub will begin building the website automatically.

---

## Step 4 — Push Future Updates

After making changes locally:

```bash
git add .
git commit -m "Describe your changes"
git push origin main
```

Every successful push to the deployment branch automatically starts a new GitHub Pages build.

---

## Step 5 — Monitor the Deployment

Open the repository's **Actions** tab.

A successful deployment typically progresses through:

1. Checkout repository
2. Build Jekyll site
3. Publish website

Wait until the workflow completes successfully.

---

## Step 6 — Verify the Live Website

Open the published website.

Example:

```text
https://username.github.io/repository-name/
```

Verify that:

* The home page loads.
* Navigation links work.
* Images display correctly.
* CSS styles load.
* New pages appear.
* Updated content is visible.

---

## Validation

Verify that:

* GitHub Pages is enabled.
* The deployment completed successfully.
* No workflow errors occurred.
* The website loads correctly.
* Navigation functions properly.
* Recent updates appear on the live site.

---

## Troubleshooting

### 404 Page

Possible causes include:

* Incorrect permalink
* Incorrect folder name
* Capitalization mismatch
* Page was not committed
* Deployment still in progress

---

### Changes Don't Appear

Verify:

* The changes were committed.
* The changes were pushed.
* The deployment completed successfully.
* Refresh the browser to clear cached content if necessary.

---

### Build Failed

Review the **Actions** workflow for errors.

Common causes include:

* YAML syntax errors
* Invalid front matter
* Liquid syntax errors
* Missing layout files

---

### Images Do Not Display

Confirm that:

* Image paths are correct.
* File names match exactly.
* Capitalization is consistent.
* Images were committed and pushed.

---

### CSS Is Missing

Check:

* `baseurl` and `url` settings in `_config.yml`
* Asset paths
* Theme configuration

---

## Skills Practiced

* GitHub Pages configuration
* Static website deployment
* Jekyll publishing
* Build monitoring
* Website validation
* Deployment troubleshooting

---

## Lessons Learned

* GitHub Pages automatically publishes static websites from a GitHub repository.
* Every successful push can trigger a new deployment.
* Local testing reduces deployment errors.
* Repository organization and consistent file naming improve reliability.
* Reviewing deployment logs helps identify build problems quickly.

---

## Outcome

* Configured GitHub Pages
* Published a Jekyll website
* Verified the live deployment
* Confirmed website functionality
* Practiced a complete deployment workflow

---

## Quick Reference

```text
Update Project
      ↓
git add .
      ↓
git commit -m "Describe your changes"
      ↓
git push origin main
      ↓
GitHub Pages builds automatically
      ↓
Verify the live website
```

---

## Related Labs

* 10.01.00 — Set Up a GitHub Pages Site
* 10.02.00 — Clone a GitHub Repository
* 10.03.00 — Create and Manage Git Branches
* 10.04.00 — Update a Local Repository from GitHub
* 10.05.00 — Push Local Changes to GitHub

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
