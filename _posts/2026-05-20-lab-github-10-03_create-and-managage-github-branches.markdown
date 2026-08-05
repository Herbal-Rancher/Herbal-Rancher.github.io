---
layout: post
title: "Technical Communication | Create and Manage Git Branches"
lab_title: "Create and Manage Git Branches"

lesson: "10.0"
lesson_id: "10.03.00"
sort_order: "100300"

categories: [portfolio, labs]

category: technical-communication
category_display: Technical Communication

subcategory: github
subcategory_display: GitHub

content_type: lab
content_type_display: Lab

tags:

- github
- git
- branching
- feature-branches
- pull-requests
- version-control
- deployment
- workflow

permalink: /network-portfolio/labs/module-10-0/git-branching-and-workflow/
status: complete

topics:

- git-branching
- feature-branch-workflow
- pull-requests
- branch-merging
- github-pages-deployment

tools:

- git
- github
- visual-studio-code

date: 2026-04-03 03:13:14 -0200

video_id: ""
video_url: ""
thumbnail: ""

pdf: ""
diagram: ""

protocols: []

---

This walkthrough documents the transition from a **basic Git workflow** to a more **structured, industry-standard branching workflow**.

It builds on previous labs and establishes a repeatable process for safely updating and deploying changes to a GitHub Pages site.

<!--more-->

---

## Overview

In earlier work, changes were committed directly to the `main` branch. While this approach is effective for quick updates, it can introduce risk as a project grows.

This walkthrough introduces:

* Feature branches
* Controlled merges
* Pull requests
* Safer deployment practices

The goal is to align the project with common real-world development workflows.

---

## Why Branching Matters

Branching allows you to:

* Work on new features without disrupting the live site
* Test changes before deployment
* Organize work into manageable units
* Review changes before merging
* Maintain a clean and stable `main` branch

---

## Branching Strategy Used

This project uses a **feature-branch workflow**:

* `main` — Production branch used for the live GitHub Pages site
* `feature/*` — Temporary branches used for development work

Examples:

```text
feature/formative-modules-index
feature/walkthrough-update
feature/navigation-fix
```

Each feature branch should focus on one related change or group of changes.

---

## Step-by-Step Workflow

### Step 1 — Start from Main

Before creating a branch, switch to the local `main` branch and retrieve the latest version from GitHub.

```bash
git checkout main
git pull origin main
```

This reduces the chance of creating a new branch from outdated files.

---

### Step 2 — Create a Feature Branch

Create and switch to a new branch.

```bash
git checkout -b feature/<feature-name>
```

Example:

```bash
git checkout -b feature/formative-modules-index
```

Use a short, descriptive branch name that explains the purpose of the work.

---

### Step 3 — Make Changes Locally

Update files, create pages, correct links, or modify site content within the feature branch.

Use the following command to verify the active branch and review changed files:

```bash
git status
```

---

### Step 4 — Test the Changes

For a Jekyll site, run the local development server before committing the changes.

```bash
bundle exec jekyll serve
```

Review the site at:

```text
http://localhost:4000
```

Confirm that:

* New pages display correctly
* Links work
* Permalinks are correct
* Layouts render properly
* No Jekyll build errors appear

---

### Step 5 — Stage and Commit Changes

Stage the updated files.

```bash
git add .
```

Create a descriptive commit.

```bash
git commit -m "Add formative lessons index page"
```

A useful commit message briefly explains what changed.

---

### Step 6 — Push the Feature Branch

Push the branch to GitHub.

```bash
git push origin feature/<feature-name>
```

Example:

```bash
git push origin feature/formative-modules-index
```

The branch is now available in the remote GitHub repository.

---

### Step 7 — Create a Pull Request

Using GitHub:

1. Open the repository.
2. Select **Compare & pull request**.
3. Confirm that the feature branch will merge into `main`.
4. Review the changed files.
5. Add a clear pull request title and description.
6. Select **Create pull request**.
7. Review the pull request.
8. Select **Merge pull request** when the changes are ready.

A pull request provides an opportunity to review changes before they affect the live site.

---

### Step 8 — Merge Using the Command Line

A feature branch can also be merged locally.

```bash
git checkout main
git pull origin main
git merge feature/<feature-name>
git push origin main
```

Example:

```bash
git checkout main
git pull origin main
git merge feature/formative-modules-index
git push origin main
```

---

### Step 9 — Delete the Completed Branch

After the branch has been successfully merged, delete the local branch.

```bash
git branch -d feature/<feature-name>
```

Example:

```bash
git branch -d feature/formative-modules-index
```

To delete the remote branch:

```bash
git push origin --delete feature/<feature-name>
```

Deleting completed branches helps keep the repository organized.

---

## Deployment Behavior

GitHub Pages deploys the published site from the configured production branch.

For this project, the production branch is:

```text
main
```

Changes made on a feature branch do not appear on the live site until they are merged into `main`.

After a successful merge, GitHub Pages will:

* Start a new build
* Process the Jekyll site
* Deploy the updated files
* Publish the changes to the live website

The deployment status can be reviewed under the repository's **Actions** tab.

---

## When to Use a Branch

Use a feature branch when:

* Adding new pages
* Updating navigation
* Changing layouts
* Modifying site structure
* Testing new features
* Updating multiple related files
* Making changes that could affect the live site

Direct commits to `main` may be appropriate for:

* Minor spelling corrections
* Small formatting fixes
* Simple text updates
* Low-risk changes that can be quickly verified

Using a branch is still the safer option whenever there is uncertainty.

---

## Validation

Verify the following before completing the lab:

* The local `main` branch was updated.
* A feature branch was created.
* Changes were completed on the feature branch.
* The site was tested locally.
* Changes were committed.
* The feature branch was pushed to GitHub.
* A pull request was created or the branch was merged locally.
* The changes were merged into `main`.
* The GitHub Pages deployment completed successfully.
* The completed branch was deleted when no longer needed.

---

## Troubleshooting

### Changes Were Made on the Wrong Branch

Check the current branch:

```bash
git branch
```

The active branch is marked with an asterisk.

```text
* feature/formative-modules-index
  main
```

---

### Branch Is Behind Main

Update `main`, then merge it into the feature branch.

```bash
git checkout main
git pull origin main
git checkout feature/<feature-name>
git merge main
```

Resolve any conflicts before continuing.

---

### Merge Conflict

Git identifies the files containing conflicts.

Open the affected files and look for conflict markers:

```text
<<<<<<< HEAD
Current branch content
=======
Incoming branch content
>>>>>>> feature/<feature-name>
```

Choose the correct content, remove the conflict markers, and then complete the merge.

```bash
git add .
git commit -m "Resolve merge conflict"
```

---

### Branch Was Not Pushed

Push the branch to GitHub.

```bash
git push origin feature/<feature-name>
```

---

### GitHub Pages Did Not Update

Verify that:

* The feature branch was merged into `main`
* The latest commit appears on `main`
* The GitHub Actions workflow completed successfully
* The Jekyll build did not report an error
* The page permalink matches the published link
* File and folder capitalization is correct

---

## Skills Practiced

* Git branching
* Feature-branch workflows
* Repository management
* Pull requests
* Branch merging
* Local testing
* GitHub Pages deployment
* Version control
* Troubleshooting

---

## Lessons Learned

* Branching reduces the risk of disrupting the live site.
* A stable `main` branch supports reliable deployments.
* Feature branches separate unfinished work from production content.
* Pull requests provide visibility and an opportunity to review changes.
* Local testing helps identify problems before deployment.
* Completed branches should be removed when they are no longer needed.
* Structured Git workflows make projects easier to maintain as they grow.

---

## Outcome

* Adopted a structured Git branching workflow
* Improved the reliability of GitHub Pages deployments
* Established a repeatable process for testing and reviewing changes
* Practiced creating, pushing, merging, and deleting feature branches
* Improved repository organization and version-control practices

---

## Quick Reference

### Update Main

```bash
git checkout main
git pull origin main
```

### Create and Switch to a Feature Branch

```bash
git checkout -b feature/<name>
```

### Review Changes

```bash
git status
```

### Stage and Commit

```bash
git add .
git commit -m "Describe the completed change"
```

### Push the Feature Branch

```bash
git push origin feature/<name>
```

### Merge into Main

```bash
git checkout main
git pull origin main
git merge feature/<name>
git push origin main
```

### Delete the Local Branch

```bash
git branch -d feature/<name>
```

### Delete the Remote Branch

```bash
git push origin --delete feature/<name>
```

---

## Related Labs

* 10.01.00 — Initial GitHub Site Setup
* 10.02.00 — Create Local Project from GitHub Repository
* 10.04.00 — Commit and Push Changes
* 10.05.00 — GitHub Pages Deployment


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

