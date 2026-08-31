---
layout: post
title: "Technical Communication | Update a Local Repository from GitHub"
lab_title: "Update a Local Repository from GitHub"

lesson: "10.0"
lesson_id: "10.04.00"
sort_order: "100400"

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
- repository
- git-pull
- synchronization
- version-control
- troubleshooting
- workflow

permalink: /network-portfolio/labs/module-10-0/update-local-project-from-github/
status: complete

topics:

- repository-synchronization
- remote-repositories
- git-pull
- local-repository-management
- version-control-workflow

tools:

- git
- github
- visual-studio-code
- terminal

date: 2026-04-03 04:14:14 -0700

video_id: ""
video_url: ""
thumbnail: ""

pdf: ""
diagram: ""

protocols: []

---

Before beginning a new blog post, lab walkthrough, or site update, confirm that the local repository contains the latest changes from GitHub.

Updating the local project first helps prevent missing files, duplicate work, merge conflicts, and accidental overwrites.

<!--more-->

---

## Overview

A GitHub project normally exists in two locations:

* The **remote repository** stored on GitHub
* The **local repository** stored on the computer

This walkthrough demonstrates how to update the local `main` branch before beginning new work.

---

## Quick Workflow

For a clean repository, use:

```bash
git switch main
git status
git fetch origin
git pull --ff-only origin main
git status
```

A successful update should end with:

```text
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

---

## Prerequisites

Before beginning, confirm that:

* Git is installed
* The repository has already been cloned
* The project is connected to GitHub
* You have access to the repository
* A terminal or Visual Studio Code is available

---

## Step 1 — Open the Local Repository

Navigate to the project folder.

```bash
cd path/to/repository
```

Example:

```bash
cd ~/Documents/GitHub/herbal-rancher.github.io
```

You can also open the project in Visual Studio Code and use the integrated terminal.

---

## Step 2 — Check the Current Branch

Display the available local branches.

```bash
git branch
```

The active branch is marked with an asterisk.

```text
* main
  feature/navigation-update
```

Switch to `main` when needed.

```bash
git switch main
```

---

## Step 3 — Check for Local Changes

Run:

```bash
git status
```

The safest condition before pulling is:

```text
nothing to commit, working tree clean
```

If files have been changed, commit or temporarily store them before continuing.

### Commit Completed Work

```bash
git add .
git commit -m "Save local work before updating repository"
```

### Temporarily Store Unfinished Work

```bash
git stash
```

Restore the changes later with:

```bash
git stash pop
```

---

## Step 4 — Retrieve Remote Information

Fetch the latest repository information from GitHub.

```bash
git fetch origin
```

This updates Git's knowledge of the remote repository without changing the local project files.

Check the status again.

```bash
git status
```

Git may report that the branch is:

* Up to date
* Behind the remote branch
* Ahead of the remote branch
* Diverged from the remote branch

---

## Step 5 — Pull the Latest Changes

Update the local `main` branch.

```bash
git pull --ff-only origin main
```

The `--ff-only` option updates the branch only when Git can move it forward without creating an unexpected merge commit.

For a basic workflow, this command is also commonly used:

```bash
git pull origin main
```

---

## Step 6 — Verify the Update

Run:

```bash
git status
```

A successfully synchronized repository should display:

```text
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

---

## Step 7 — Test the Updated Site

For a Jekyll project, run:

```bash
bundle exec jekyll serve
```

Open:

```text
http://localhost:4000
```

Confirm that:

* The site builds successfully
* Pages display correctly
* Navigation links work
* No YAML or Liquid errors appear
* Recent GitHub updates are present

Stop the local server with:

```text
Ctrl + C
```

---

## Step 8 — Begin New Work

After updating `main`, create a feature branch.

```bash
git switch -c feature/<feature-name>
```

Example:

```bash
git switch -c feature/github-lab-update
```

Make and test the required changes before committing them.

---

## Troubleshooting

### Local Changes Would Be Overwritten

Git may prevent the pull when local files have been changed.

Commit the work:

```bash
git add .
git commit -m "Save local changes before pull"
git pull --ff-only origin main
```

Or temporarily store it:

```bash
git stash
git pull --ff-only origin main
git stash pop
```

---

### The Branch Has Diverged

Review the repository history.

```bash
git log --oneline --graph --decorate --all
```

Do not force-push or reset the branch until you understand which commits need to be preserved.

A possible workflow is:

```bash
git pull --rebase origin main
```

Resolve any conflicts before continuing.

---

### Incorrect Branch Is Active

Check the current branch.

```bash
git branch
```

Switch to `main`.

```bash
git switch main
```

Then retrieve the latest changes.

```bash
git pull --ff-only origin main
```

---

### Remote Changes Do Not Appear

Refresh all remote branch information.

```bash
git fetch --all --prune
```

Then check the repository again.

```bash
git status
```

---

### GitHub Authentication Fails

Verify the remote repository address.

```bash
git remote -v
```

Confirm that:

* The repository URL is correct
* Your GitHub account has access
* Your saved credentials are valid
* Your personal access token has not expired

---

## Validation

Verify that:

* The correct repository was opened
* The active branch is `main`
* Local changes were committed or stashed
* Remote information was fetched
* The latest changes were pulled
* The local branch matches `origin/main`
* The updated site was tested locally
* New work began from an updated branch

---

## Skills Practiced

* Git branch management
* Local and remote repository synchronization
* Fetching and pulling changes
* Working-directory review
* Stashing unfinished work
* Jekyll testing
* Version-control troubleshooting
* Feature-branch creation

---

## Lessons Learned

* Update the local repository before beginning new work.
* `git fetch` checks for remote changes without modifying local files.
* `git pull` retrieves and integrates remote changes.
* `git pull --ff-only` helps prevent unexpected merge commits.
* Local work should be committed or stashed before pulling.
* A clean and current `main` branch is the best starting point for a feature branch.

---

## Outcome

* Updated the local `main` branch from GitHub
* Verified that the local and remote repositories matched
* Tested the updated Jekyll site
* Prepared a current feature branch for new work
* Established a repeatable repository-update workflow

---

## Quick Reference

```bash
git switch main
git status
git fetch origin
git pull --ff-only origin main
git status
git switch -c feature/<feature-name>
```

---

## Related Labs

* 10.01.00 — Initial GitHub Site Setup
* 10.02.00 — Create Local Project from GitHub Repository
* 10.03.00 — Git Branching and Workflow


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