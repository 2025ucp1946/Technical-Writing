# Git Commands Reference

This page collects the Git commands covered in the Git and GitHub lecture slides. Run commands in a terminal or Git Bash from the correct project folder.

## 1. Installation and configuration

| Command | Purpose |
|---|---|
| `git --version` | Check the installed Git version. |
| `git config --global user.name "Student Name"` | Set the commit author name. |
| `git config --global user.email "student@example.com"` | Set the commit author email. |
| `git config --global --list` | Show Git configuration. |

## 2. Create and inspect repositories

| Command | Purpose |
|---|---|
| `mkdir my-project` | Create a folder. |
| `cd my-project` | Move into the folder. |
| `git init` | Initialize a Git repository. |
| `git status` | Show repository status. |

## 3. Add and commit changes

| Command | Purpose |
|---|---|
| `git add main.py` | Stage one file. |
| `git add .` | Stage changes in the current directory. |
| `git add file1.py file2.py` | Stage selected files. |
| `git add *.py` | Stage matching Python files. |
| `git commit -m "Add main program"` | Create a commit. |
| `git log` | Show full commit history. |
| `git log --oneline` | Show compact commit history. |

## 4. Compare and inspect files

| Command | Purpose |
|---|---|
| `git diff` | Show unstaged changes. |
| `git diff --staged` | Show staged changes. |
| `git diff HEAD` | Compare tracked changes with the current commit. |
| `git ls-files` | List files known to Git's index. |

## 5. Ignore, rename, remove, and undo

| Command | Purpose |
|---|---|
| `git mv old.py new.py` | Rename or move a tracked file. |
| `git rm old.py` | Remove a tracked file and stage the removal. |
| `git restore --staged main.py` | Unstage a file but keep its working changes. |
| `git restore main.py` | Discard unstaged changes to a tracked file. |
| `git revert COMMIT_ID` | Create a new commit that reverses an earlier commit. |

**Warning:** `git restore main.py` can discard work. Check `git diff` before running it. Use `git revert` when you need to reverse a commit while preserving history.

## 6. Connect to GitHub

| Command | Purpose |
|---|---|
| `git remote add origin REPOSITORY_URL` | Add a remote named origin. |
| `git remote -v` | List remote URLs. |
| `git branch -M main` | Rename the current branch to main. |
| `git push -u origin main` | Push main and set its upstream. |
| `git clone REPOSITORY_URL` | Copy a remote repository locally. |
| `git fetch origin` | Download remote updates without integrating them. |
| `git pull` | Fetch and integrate updates into the current branch. |

## 7. Branches and collaboration

| Command | Purpose |
|---|---|
| `git branch` | List local branches. |
| `git branch feature-login` | Create a branch. |
| `git switch feature-login` | Switch to a branch. |
| `git switch main` | Switch to main. |
| `git switch -c feature-login` | Create and switch to a new branch. |
| `git merge feature-login` | Merge feature-login into the current branch. |
| `git rebase main` | Replay the current branch's commits on top of main. |

To merge a feature branch into main:

```bash
git switch main
git merge feature-login
```

To rebase a feature branch on main:

```bash
git switch feature-login
git rebase main
```

Rebase rewrites commit identities. Avoid rebasing shared commits unless everyone understands the effect.

## 8. Tags

| Command | Purpose |
|---|---|
| `git tag` | List tags. |
| `git tag -a v1.0.0 -m "Version 1.0.0"` | Create an annotated tag. |
| `git show v1.0.0` | Show tag information. |
| `git push origin v1.0.0` | Push a tag to the remote. |

## 9. Complete workflow example

```bash
mkdir calculator
cd calculator
git init

git status
git add .
git status
git commit -m "Add initial calculator"
git log --oneline

git branch -M main
git remote add origin REPOSITORY_URL
git push -u origin main

git switch -c feature-subtraction
# Edit the project files
git add .
git commit -m "Add subtraction feature"
git push -u origin feature-subtraction
```

Then open GitHub, create a pull request from `feature-subtraction` into `main`, review it, and merge it.

After the pull request is merged:

```bash
git switch main
git pull origin main
```

## 10. Useful folder and file commands from the lecture exercise

```bash
mkdir calculator
cd calculator
```

The lecture also uses `echo` to create a quick file in a terminal:

```bash
echo "print(2 + 3)" > main.py
```

## Important reminders

- Replace `REPOSITORY_URL` with the actual repository URL.
- Check `git status` often.
- Commit related changes together.
- Resolve merge conflicts by editing the affected files, removing conflict markers, staging the resolved files, and completing the merge.
- Never commit passwords, API keys, or private tokens.


## 11. Sample command outputs

These are example outputs to help you recognize what Git displays. Your branch name, file names, commit IDs, and Git version may be different.

### Check Git version

Command:

\`\`\`bash
git --version
\`\`\`

Example output:

\`\`\`text
git version 2.45.1
\`\`\`

### Initialize a repository

Command:

\`\`\`bash
git init
\`\`\`

Example output:

\`\`\`text
Initialized empty Git repository in .../my-project/.git/
\`\`\`

### Check status before staging

Command:

\`\`\`bash
git status
\`\`\`

Example output:

\`\`\`text
On branch master
No commits yet
Untracked files:
  main.py
nothing added to commit but untracked files present
\`\`\`

### Stage a file

Commands:

\`\`\`bash
git add main.py
git status
\`\`\`

Example output:

\`\`\`text
On branch master
No commits yet
Changes to be committed:
  new file: main.py
\`\`\`

### Commit changes

Command:

\`\`\`bash
git commit -m "Add main program"
\`\`\`

Example output:

\`\`\`text
[master (root-commit) a1b2c3d] Add main program
 1 file changed, 5 insertions(+)
 create mode 100644 main.py
\`\`\`

The commit ID above is only an example.

### View commit history

Command:

\`\`\`bash
git log --oneline
\`\`\`

Example output:

\`\`\`text
a1b2c3d Add main program
\`\`\`

### View configured remote

Command:

\`\`\`bash
git remote -v
\`\`\`

Example output:

\`\`\`text
origin  https://github.com/USERNAME/REPOSITORY.git (fetch)
origin  https://github.com/USERNAME/REPOSITORY.git (push)
\`\`\`

### Push to GitHub

Command:

\`\`\`bash
git push -u origin main
\`\`\`

Example output after a successful push:

\`\`\`text
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Writing objects: 100% (5/5), done.
To https://github.com/USERNAME/REPOSITORY.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
\`\`\`

The number of objects and progress messages depend on the repository.

### Create and switch to a branch

Command:

\`\`\`bash
git switch -c feature-login
\`\`\`

Example output:

\`\`\`text
Switched to a new branch 'feature-login'
\`\`\`

### Merge a branch

Commands:

\`\`\`bash
git switch main
git merge feature-login
\`\`\`

Example output when Git can merge automatically:

\`\`\`text
Updating a1b2c3d..d4e5f6a
Fast-forward
 login.py | 2 ++
 1 file changed, 2 insertions(+)
\`\`\`

If the same lines were changed differently, Git may stop and report a merge conflict. Edit the affected file, remove conflict markers, stage the resolved file with \`git add\`, and complete the merge.

### Pull changes

Command:

\`\`\`bash
git pull origin main
\`\`\`

Example output when the local branch is already up to date:

\`\`\`text
From https://github.com/USERNAME/REPOSITORY
 * branch            main       -> FETCH_HEAD
Already up to date.
\`\`\`

### Create and push a tag

Commands:

\`\`\`bash
git tag -a v1.0.0 -m "Version 1.0.0"
git push origin v1.0.0
\`\`\`

Expected result: Git creates the tag locally and sends it to the remote repository. The tag can then be used to identify that version on GitHub.

## 12. Complete mini example and expected result

Run these commands in a new folder:

\`\`\`bash
mkdir calculator
cd calculator
git init
echo "print(10 + 5)" > main.py
git status
git add main.py
git commit -m "Add calculator"
git log --oneline
\`\`\`

The program file contains:

\`\`\`python
print(10 + 5)
\`\`\`

If you run the Python file with \`python main.py\`, the program output is:

\`\`\`text
15
\`\`\`

The Git commit records the file; Git does not run the Python program.

**Remember:** The outputs in this reference are illustrative examples, not guaranteed exact terminal text. Git may display slightly different wording or progress information on your computer.
