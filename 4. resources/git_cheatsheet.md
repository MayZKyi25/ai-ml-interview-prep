# Git Cheat Sheet

Quick Git commands for this repo.

---

## Daily Workflow

| Step | Command | Meaning |
|---|---|---|
| 1 | `git status` | Check what changed |
| 2 | `git add .` | Stage all changes |
| 3 | `git commit -m "message"` | Save changes locally |
| 4 | `git push` | Upload to GitHub |

Example:

```bash
git status
git add .
git commit -m "Add count words practice"
git push
```

---

## Basic Commands

| Command | Meaning |
|---|---|
| `pwd` | Show current folder |
| `ls` | List files and folders |
| `git status` | Show Git changes |
| `git log --oneline` | Show commit history |
| `git diff` | Show unstaged changes |
| `git diff --staged` | Show staged changes |

---

## Add Files

| Command | Meaning |
|---|---|
| `git add .` | Add all changed files |
| `git add README.md` | Add one file |
| `git add folder/file.py` | Add one specific file |

---

## Commit

```bash
git commit -m "Add Two Sum solution"
```

A commit saves your staged changes locally.

Good messages:

```text
Add count words practice
Add LeetCode 1 Two Sum solution
Update README structure
Add ML fundamentals notes
```

Avoid:

```text
update
fix
stuff
```

---

## Push to GitHub

| Command | Meaning |
|---|---|
| `git push` | Push commits to GitHub |
| `git push -u origin main` | First push to GitHub |

---

## Pull from GitHub

```bash
git pull
```

Downloads latest changes from GitHub.

Use this after editing files directly on GitHub.

---

## Remote Repo

| Command | Meaning |
|---|---|
| `git remote -v` | Show GitHub repo link |
| `git remote add origin URL` | Connect to GitHub |
| `git remote set-url origin URL` | Change GitHub repo link |

For this repo:

```bash
git remote set-url origin https://github.com/MayZKyi25/ai-ml-interview-prep.git
```

---

## Branch Commands

| Command | Meaning |
|---|---|
| `git branch` | Show branches |
| `git branch -M main` | Rename branch to main |
| `git checkout -b branch-name` | Create new branch |
| `git switch main` | Switch to main |
| `git merge branch-name` | Merge branch into current branch |
| `git branch -d branch-name` | Delete local branch |

---

## Move / Rename Files

```bash
git mv old_name.py new_name.py
```

Example:

```bash
git mv resources/template.py templates/problem_template.py
git mv "1. python_review" python_foundations
git mv "2. dsa_leetcode" dsa_leetcode
git mv "3. ml_concepts_review" ml_fundamentals
git mv "4. resources" resources
```

Then commit:

```bash
git commit -m "Move problem template"
```

---

## Delete Files

```bash
git rm old_file.py
git commit -m "Remove old file"
```

---

## Undo Staging

| Command | Meaning |
|---|---|
| `git restore --staged README.md` | Unstage one file |
| `git restore --staged .` | Unstage all files |

This does not delete your changes.

---

## Undo Local Changes 

| Command | Meaning |
|---|---|
| `git restore README.md` | Undo changes in one file |
| `git restore .` | Undo all local changes |

Only use this when you are sure.

---

## Python `.gitignore`

```text
__pycache__/
*.py[cod]
.venv/
venv/
.env
.DS_Store
.vscode/
.ipynb_checkpoints/
```

| Item | Meaning |
|---|---|
| `__pycache__/` | Python auto files |
| `.venv/`, `venv/` | Virtual environments |
| `.env` | Secret variables |
| `.DS_Store` | Mac system file |
| `.vscode/` | VS Code settings |

---

## Common Git Pitfalls

| Pitfall | Wrong | Correct |
|---|---|---|
| Creating a file | `mkdir file.py` | `touch file.py` |
| Pushing without commit | `git add .` then `git push` | `git add .` → `git commit` → `git push` |
| Wrong folder | Start typing commands anywhere | Run `pwd` first |

---

## Mental Model

| Area | Meaning |
|---|---|
| Working folder | Your actual files |
| Staging area | Files selected for commit |
| Commit | Saved snapshot |
| GitHub | Online backup and portfolio |

Flow:

```text
edit files → git add → git commit → git push
```

---

## For This Repo

```bash
cd ~/Desktop/ai-ml-interview-prep
git status
git add .
git commit -m "Update AI ML interview prep repo"
git push
```

