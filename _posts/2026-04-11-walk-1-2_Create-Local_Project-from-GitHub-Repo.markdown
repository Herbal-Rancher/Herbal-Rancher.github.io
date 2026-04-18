---
layout: post
title: "Creating a Local Project From My Remote GitHub Repository"
lesson: 1.0
order: 1.2
categories: [portfolio, blog, walkthroughs]
date: 2026-04-11 11:12:14 -0200
tags: [github-pages, jekyll, git, troubleshooting, setup]
permalink: /portfolio/walkthroughs/lesson-1-0/walkthroughs-1-2/
---

In this walkthrough, I document the process of configuring and deploying my GitHub Pages blog for the first time. While the initial setup seemed straightforward, I encountered several real-world issues involving Git, branching, authentication, and dependency management.

This post outlines both the setup process and the troubleshooting steps required to successfully publish my site.

---
<!--more-->
### Objective

* Configure a local Jekyll-based project
* Push the project to GitHub
* Deploy the site using GitHub Pages
* Resolve any errors preventing deployment

---

### Initial Setup

I began by:

* Creating a GitHub repository for my site
* Copying my project files into a local directory
* Initializing Git and connecting to the remote repository

#### Basic Git Workflow

```bash
git add .
git commit -m "initial commit"
git push origin main
```

At this point, I expected my site to appear on GitHub Pages—but it didn’t.

---

### Issues Encountered & Resolutions

#### 1. Branch Mismatch (`gh-website` vs `main`)

**Issue:**
My changes were committed to a branch called `gh-website`, but GitHub Pages was configured to use `main`.

**Fix:**

```bash
git checkout -b main
git merge gh-website
git push origin main --force
```

---

#### 2. Incorrect Remote Repository URL

**Issue:**
Git could not find my repository due to an incorrectly formatted remote URL.

**Fix:**

```bash
git remote set-url origin https://github.com/<username>/<repository>.git
```

---

#### 3. Push Blocked by Email Privacy Settings

**Issue:**
GitHub rejected my push because my commit exposed a private email address.

**Fix:**

* Updated Git config to use GitHub’s noreply email
* Amended the commit:

```bash
git commit --amend --reset-author
git push origin main --force
```

---

#### 4. Bundler and Ruby Version Conflict

**Issue:**
The build failed because Bundler version 4.x required Ruby 3.2+, while GitHub Pages uses Ruby 3.1.6.

**Fix:**

* Removed `Gemfile.lock`
* Avoided explicitly setting incompatible Bundler versions

---

#### 5. Outdated `github-pages` Gem

**Issue:**
The project was using an outdated version of the `github-pages` gem, causing compatibility issues.

**Fix:**
Updated the `Gemfile`:

```ruby
source "https://rubygems.org"

gem "github-pages", "~> 228", group: :jekyll_plugins
```

---

#### 6. Jekyll Version Conflict

**Issue:**
I manually specified Jekyll 4.x, but GitHub Pages requires Jekyll 3.9.x.

**Fix:**
Removed the Jekyll dependency entirely and allowed GitHub Pages to manage it.

---

### Final Working Configuration

#### Clean `Gemfile`

```ruby
source "https://rubygems.org"

gem "github-pages", "~> 228", group: :jekyll_plugins
```

#### Deployment Command

```bash
git push origin main --force
```

---

### Key Lessons Learned

* GitHub Pages manages its own dependencies—avoid overriding them
* Branch selection matters (`main` vs others)
* `Gemfile.lock` can cause hidden conflicts
* Git commit identity must align with GitHub privacy settings
* Many deployment issues are not code-related, but configuration-related

---

### Outcome

After resolving these issues, my GitHub Pages site built successfully and published my blog content. This process provided valuable experience in debugging real-world deployment and configuration problems.

---

### Next Steps

* Add more blog entries and content
* Record a full video walkthrough of this process
* Expand documentation for additional labs and assignments
* Continue refining Git and deployment workflows

---

### Reflection

This experience reinforced the importance of understanding both development and deployment workflows. Troubleshooting these issues improved my confidence in using Git, GitHub, and static site deployment tools.

---

### 🔗 Navigation

* **[Formative Lessons](/portfolio/formative-lessons/)**
* **[Walkthroughs](/portfolio/walkthroughs/)**
* **[Network+ Portfolio](/portfolio/)**
* **[Home](/)**

---