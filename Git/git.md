# Git

## What is Git?

Git is a distributed version control system. It records changes in files so that previous versions can be inspected and recovered. It also helps multiple people work on the same project.

## Git and GitHub

- **Git** is the version control tool that runs on a computer.
- **GitHub** is an online platform for hosting Git repositories and collaborating.

Git can be used locally without an internet connection. GitHub's online features require connectivity.

## How Git works

Git mainly uses three areas:

1. **Working directory:** files that are being edited.
2. **Staging area:** changes selected for the next commit.
3. **Repository:** committed project history.

The normal workflow is:

`Edit files → git add → git commit → git push`

## Installation

- Windows: download Git from [git-scm.com](https://git-scm.com/downloads).
- Ubuntu/Debian: `sudo apt update` then `sudo apt install git`.
- macOS with Homebrew: `brew install git`.

Check installation with:

```bash
git --version
```

## Configure Git

```bash
git config --global user.name "Student Name"
git config --global user.email "student@example.com"
git config --global --list
```

These settings identify the author of commits. They do not log in to GitHub.

## Create a repository

```bash
mkdir my-project
cd my-project
git init
```

## Basic workflow

```bash
git status
git add .
git status
git commit -m "Add project files"
git log --oneline
```

- `git status`: shows changed, staged, and untracked files.
- `git add`: stages changes.
- `git commit`: records staged changes.
- `git log`: shows commit history.

## Branches

A branch is a separate line of development.

```bash
git branch
git branch feature-login
git switch feature-login
git switch -c docs-update
git switch main
git merge feature-login
```

## Remote repositories

```bash
git remote add origin REPOSITORY_URL
git remote -v
git push -u origin main
git clone REPOSITORY_URL
git fetch origin
git pull
```

- `git push` uploads local commits.
- `git fetch` downloads remote updates without integrating them into the current branch.
- `git pull` fetches and integrates remote changes.
- `git clone` creates a local copy of a remote repository.

## Other useful commands

```bash
git diff
git diff --staged
git diff HEAD
git ls-files
git restore --staged main.c
git restore main.c
git revert COMMIT_ID
git mv old.c new.c
git rm old.c
git tag
git show v1.0.0
git rebase main
```

Be careful: `git restore main.c` discards unstaged changes to that file. Inspect your work before using it.

## Best practices

- Commit changes regularly.
- Write clear commit messages.
- Use descriptive branch names.
- Review changes before committing.
- Test changes before merging.
- Do not commit passwords, tokens, or private keys.
- Use a README to explain the project.

## What I learned

I learned how Git tracks project changes, creates commits, manages branches, and connects local work to remote repositories.
