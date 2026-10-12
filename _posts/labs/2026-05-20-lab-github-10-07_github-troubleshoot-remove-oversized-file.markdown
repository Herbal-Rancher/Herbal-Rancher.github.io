---
layout: post
title: "Technical Communication | Remove Oversized Files from Git History"
lab_title: "Remove Oversized Files from Git History"

lesson: "10.0"
lesson_id: "10.07.00"
sort_order: "100700"

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

permalink: /network-portfolio/labs/module-10-0/remove-oversized-files-from-git-history/
status: complete

topics:

- github-pages
- website-deployment
- static-site-hosting
- jekyll
- deployment-workflow
- troubleshooting

tools:

- github
- git
- visual-studio-code
- jekyll

date: 2026-10-12 06:15:00 -0700

video_id: ""
video_url: ""
thumbnail: ""

pdf: ""
diagram: ""

protocols: []

---

# Git & GitHub Troubleshooting: Removing Oversized Files

## Overview

GitHub rejects individual files larger than 100 MB in a standard Git repository. An oversized file can prevent a push even after it has been deleted from the working directory because Git preserves files in commit history.

The solution depends on whether the oversized file has already been pushed to GitHub.

## Scenario 1: The Oversized File Has NOT Been Pushed

**Situation:** GitHub rejects a push because an oversized file exists in one or more local commits that have not yet been uploaded.

### Step 1: Inspect the repository

```powershell
git status
git log --oneline -5
```

- `git status` checks whether the working tree has uncommitted changes.
- `git log --oneline -5` displays the five most recent commits.

### Step 2: Check whether the file is currently tracked

```powershell
git ls-files "path/to/oversized-file.mp4"
```

No output means the file is not currently tracked at that path. However, it may still exist in earlier commits.

### Step 3: Search the unpushed history

```powershell
git rev-list --objects origin/main..main | Select-String "oversized-file.mp4"
```

This PowerShell command searches the objects referenced by local commits that are not reachable from `origin/main`.

### Step 4: Rebuild the local commits

If the local commits contain all the changes you intend to publish, and the oversized file is confined to those unpushed commits, you can rebuild the changes from the remote baseline.

```powershell
git reset --soft origin/main
git commit -m "Update project and remove oversized file"
git push origin main
```

**How this works:**

- `git reset --soft origin/main` moves the local branch to the remote baseline while preserving the changes in the index.
- `git commit` creates a new commit from those staged changes.
- `git push` uploads the new commit history to GitHub.

**Important:** Review the staged changes before committing. This method rewrites the local commit sequence, so use it only when you understand which commits will be replaced and have confirmed that the intended changes are preserved.

---

## Scenario 2: The Oversized File HAS Already Been Pushed

**Situation:** The oversized file exists in GitHub’s commit history. Deleting it and committing the deletion does not remove the original file from earlier commits.

### Step 1: Remove the file from the working directory

For example, in PowerShell:

```powershell
Remove-Item "path/to/oversized-file.mp4"
```

If you need to retain the file on your computer, move it outside the repository instead.

### Step 2: Commit the deletion

```powershell
git add -A
git commit -m "Remove oversized file"
```

This removes the file from the latest version of the project, but **does not remove it from earlier commits**. A push can still be rejected if the oversized object remains in the history being uploaded.

### Step 3: Remove the file from Git history

Use Git’s history-rewriting tool, `git-filter-repo`, to remove the file from all affected commits.

After installing `git-filter-repo`, run the following from the repository root, replacing the example path with the file’s actual repository-relative path:

```powershell
git filter-repo --path "path/to/oversized-file.mp4" --invert-paths
```

This rewrites repository history to exclude that path. If the file was renamed or stored under multiple paths, each relevant path must be addressed.

**Important precautions:**

- Back up the repository before rewriting history.
- Coordinate with collaborators because commit IDs change when history is rewritten.
- `git-filter-repo` may remove the `origin` remote as a safety measure. Check with `git remote -v` and re-add the correct remote URL if necessary.
- If the file was already pushed, updating GitHub will generally require a force push of the rewritten branch. Coordinate first if others use the branch.

### Step 4: Push the rewritten history

After verifying the rewritten history and confirming the correct remote:

```powershell
git push --force-with-lease origin main
```

`--force-with-lease` is safer than a plain `--force` because it checks that the remote branch has not changed unexpectedly. It can still overwrite remote history, so use it only when you understand the consequences and have coordinated with collaborators.

**Note:** Rewriting history removes the file from the branch history being rewritten, but copies may remain in other branches, tags, forks, or cached references until those are addressed separately.

---

## What I Learned

- **Git tracks history, not just current files.** Deleting a file from the project does not automatically remove it from previous commits.
- **The working tree and commit history are different.** A clean `git status` does not guarantee that a push will succeed.
- **GitHub evaluates the objects being pushed.** An oversized file in an earlier commit can cause a rejection even if a newer commit deletes it.
- **The solution depends on whether the file was pushed.** Local, unpushed commits can sometimes be rebuilt; already-pushed files generally require history rewriting to remove the oversized object from the affected history.
- **Protect your work before changing history.** Inspect the commits, verify the intended changes, and back up the repository before performing destructive or history-rewriting operations.

### Key Takeaway

When GitHub rejects a push because of an oversized file, first determine whether the file exists in the current working tree, the unpushed commit history, or history already published to GitHub. Diagnose the location before choosing a solution. This avoids unnecessary history changes and helps protect your work.

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
