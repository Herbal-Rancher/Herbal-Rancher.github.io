---
layout: post
title: "Technical Communication | Clone a GitHub Repository"
lab_title: "Clone a GitHub Repository"

lesson: "10.0"
lesson_id: "10.02.00"
sort_order: "100200"

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
  - github-desktop
  - git-bash
  - repository
  - clone
  - local-development
  - workflow

permalink: /network-portfolio/labs/module-10-0/clone-github-repository/
status: complete

topics:
  - repository-cloning
  - local-development
  - version-control

tools:
  - git
  - github
  - visual-studio-code

date: 2026-04-03 01:11:11 -0100

video_id: ""
video_url: ""
thumbnail: ""

pdf: ""
diagram: ""

protocols: []

---

## Overview

This lab demonstrates how to create a local development project by cloning an existing GitHub repository. Cloning downloads the complete repository, including its commit history, branches, and files, allowing development to occur locally while maintaining synchronization with the remote repository.

This workflow is the foundation for nearly every software development, documentation, and GitHub Pages project.

---

## Objectives

By completing this lab you will be able to:

- Locate an existing GitHub repository.
- Copy the repository clone URL.
- Clone a repository using Git.
- Open the project in Visual Studio Code.
- Verify the repository was cloned successfully.
- Confirm the remote repository connection.

---

## Prerequisites

Before beginning this lab, ensure you have:

- Git installed
- A GitHub account
- Visual Studio Code
- Git Bash (or another terminal)
- Access to an existing GitHub repository

---

## Lab Steps

### Step 1 – Open GitHub

Navigate to the repository you want to work with.

Select **Code** and copy the HTTPS repository URL.

Example:

```text
https://github.com/username/repository-name.git
```

---

### Step 2 – Open Git Bash

Navigate to the directory where you want to store your local projects.

Example:

```bash
cd ~/Documents/GitHub
```

---

### Step 3 – Clone the Repository

Execute the clone command.

```bash
git clone https://github.com/username/repository-name.git
```

Git downloads the complete repository to your local computer.

---

### Step 4 – Navigate into the Repository

```bash
cd repository-name
```

---

### Step 5 – Verify the Repository

Confirm Git recognizes the repository.

```bash
git status
```

A successful clone should display a clean working tree.

Example output:

```text
On branch main

Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

---

### Step 6 – Verify the Remote Repository

Display the configured remote repository.

```bash
git remote -v
```

Example:

```text
origin https://github.com/username/repository-name.git (fetch)

origin https://github.com/username/repository-name.git (push)
```

---

### Step 7 – Open the Project

Launch Visual Studio Code.

```bash
code .
```

Alternatively, open the project folder manually using **File → Open Folder**.

---

## Validation

Verify the following:

- Repository cloned successfully.
- All project files downloaded.
- Git recognizes the repository.
- Remote origin configured correctly.
- Project opens successfully in Visual Studio Code.

---

## Common Issues

### Repository Not Found

Possible causes include:

- Incorrect repository URL
- Private repository access denied
- Authentication failure

---

### Permission Denied

Verify:

- GitHub account permissions
- SSH or HTTPS authentication
- Repository ownership

---

### Existing Folder Already Exists

If the destination folder already exists:

- Delete the existing folder.
- Choose a different location.
- Clone using a different folder name.

---

### Git Command Not Recognized

Verify Git is installed.

```bash
git --version
```

If Git is not installed, download and install Git before continuing.

---

## Skills Practiced

- Git
- GitHub
- Repository Cloning
- Local Development
- Version Control
- Visual Studio Code
- Git Workflow

---

## Lessons Learned

Cloning a repository creates a complete local copy of a GitHub project while preserving its version history.

Working locally allows changes to be tested before committing and pushing updates back to the remote repository. This workflow supports safe development, easier troubleshooting, and collaboration with other developers.

Understanding how to clone, verify, and manage repositories is a foundational Git skill used throughout software development, documentation projects, and GitHub Pages websites.

---

## Related Labs

- 10.01.00 – Initial GitHub Site Setup
- 10.03.00 – Create Your First Markdown Page
- 10.04.00 – Commit and Push Changes
- 10.05.00 – GitHub Pages Deployment

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

