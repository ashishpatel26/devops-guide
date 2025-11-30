# Git Cheat Sheet

Git is a distributed version control system.

## Configuration

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

## Basic Commands

| Command | Description |
| :--- | :--- |
| `git init` | Initialize a new repository |
| `git clone <url>` | Clone an existing repository |
| `git status` | Check the status of files |
| `git add .` | Stage all changes |
| `git commit -m "msg"` | Commit staged changes |
| `git push origin main` | Push changes to remote |
| `git pull` | Pull changes from remote |

## Branching

```bash
# Create a new branch
git checkout -b feature-branch

# Switch to a branch
git checkout main

# Merge branch into current branch
git merge feature-branch
```

## Undoing Changes

```bash
# Discard changes in working directory
git checkout -- <file>

# Unstage a file
git reset HEAD <file>
```