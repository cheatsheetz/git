# Git Cheat Sheet

Essential Git commands for version control and collaboration.

---

## Table of Contents
- [Basic Commands](#basic-commands)
- [Branching](#branching)
- [Remote Repositories](#remote-repositories)
- [History & Information](#history--information)
- [Stashing](#stashing)
- [Undoing Changes](#undoing-changes)
- [Configuration](#configuration)
- [Advanced Operations](#advanced-operations)

---

## Basic Commands

| Command | Description | Example |
|---------|-------------|---------|
| `git init` | Initialize repository | `git init` |
| `git clone <url>` | Clone repository | `git clone https://github.com/user/repo.git` |
| `git add <file>` | Stage changes | `git add README.md` |
| `git add .` | Stage all changes | `git add .` |
| `git commit -m "message"` | Commit staged changes | `git commit -m "Add new feature"` |
| `git commit -am "message"` | Stage and commit | `git commit -am "Fix bug"` |
| `git status` | Show working tree status | `git status` |
| `git diff` | Show unstaged changes | `git diff` |
| `git diff --staged` | Show staged changes | `git diff --staged` |

## Branching

| Command | Description | Example |
|---------|-------------|---------|
| `git branch` | List branches | `git branch` |
| `git branch <name>` | Create branch | `git branch feature-xyz` |
| `git checkout <branch>` | Switch branch | `git checkout main` |
| `git checkout -b <branch>` | Create and switch | `git checkout -b feature-abc` |
| `git switch <branch>` | Switch branch (modern) | `git switch main` |
| `git switch -c <branch>` | Create and switch (modern) | `git switch -c feature-def` |
| `git merge <branch>` | Merge branch | `git merge feature-xyz` |
| `git branch -d <branch>` | Delete branch | `git branch -d feature-xyz` |
| `git branch -D <branch>` | Force delete branch | `git branch -D broken-feature` |

## Remote Repositories

| Command | Description | Example |
|---------|-------------|---------|
| `git remote -v` | List remotes | `git remote -v` |
| `git remote add <name> <url>` | Add remote | `git remote add origin https://github.com/user/repo.git` |
| `git fetch` | Fetch from remote | `git fetch` |
| `git fetch <remote>` | Fetch from specific remote | `git fetch upstream` |
| `git pull` | Fetch and merge | `git pull` |
| `git pull <remote> <branch>` | Pull specific branch | `git pull origin main` |
| `git push` | Push to remote | `git push` |
| `git push <remote> <branch>` | Push to specific remote/branch | `git push origin feature-xyz` |
| `git push -u origin <branch>` | Push and set upstream | `git push -u origin feature-abc` |

## History & Information

| Command | Description | Example |
|---------|-------------|---------|
| `git log` | Show commit history | `git log` |
| `git log --oneline` | Compact log | `git log --oneline` |
| `git log --graph` | Visual history | `git log --graph --oneline --all` |
| `git show <commit>` | Show commit details | `git show abc123` |
| `git blame <file>` | Show line authors | `git blame README.md` |
| `git ls-files` | List tracked files | `git ls-files` |

## Stashing

| Command | Description | Example |
|---------|-------------|---------|
| `git stash` | Stash changes | `git stash` |
| `git stash push -m "message"` | Stash with message | `git stash push -m "WIP: new feature"` |
| `git stash list` | List stashes | `git stash list` |
| `git stash pop` | Apply and drop stash | `git stash pop` |
| `git stash apply` | Apply stash (keep) | `git stash apply` |
| `git stash drop` | Delete stash | `git stash drop stash@{0}` |
| `git stash clear` | Delete all stashes | `git stash clear` |

## Undoing Changes

| Command | Description | Example |
|---------|-------------|---------|
| `git checkout -- <file>` | Discard file changes | `git checkout -- README.md` |
| `git restore <file>` | Discard file changes (modern) | `git restore README.md` |
| `git reset <file>` | Unstage file | `git reset README.md` |
| `git reset --hard` | Reset to last commit | `git reset --hard` |
| `git reset --hard <commit>` | Reset to specific commit | `git reset --hard abc123` |
| `git revert <commit>` | Create revert commit | `git revert abc123` |
| `git clean -f` | Remove untracked files | `git clean -f` |
| `git clean -fd` | Remove untracked files/dirs | `git clean -fd` |

## Configuration

| Command | Description | Example |
|---------|-------------|---------|
| `git config --global user.name "Name"` | Set global username | `git config --global user.name "John Doe"` |
| `git config --global user.email "email"` | Set global email | `git config --global user.email "john@example.com"` |
| `git config --list` | Show all config | `git config --list` |
| `git config <key>` | Show config value | `git config user.name` |

## Advanced Operations

### Rebasing
- `git rebase <branch>` - Rebase current branch onto another
- `git rebase -i <commit>` - Interactive rebase
- `git rebase --continue` - Continue rebase after resolving conflicts

### Cherry-picking
- `git cherry-pick <commit>` - Apply specific commit
- `git cherry-pick <commit1>..<commit2>` - Apply range of commits

### Tagging
- `git tag` - List tags
- `git tag <name>` - Create lightweight tag
- `git tag -a <name> -m "message"` - Create annotated tag
- `git push origin <tag>` - Push tag to remote

---

## Resources
- [Git Documentation](https://git-scm.com/doc)
- [Git Book](https://git-scm.com/book)
- [GitHub Git Handbook](https://guides.github.com/introduction/git-handbook/)

---
*Originally compiled from various sources. Contributions welcome!*