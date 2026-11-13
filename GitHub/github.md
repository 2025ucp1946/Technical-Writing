# GitHub

## What is GitHub?

GitHub is an online platform for hosting Git repositories. It helps developers share projects, review changes, and collaborate.

## Main features

- **Repositories:** store project files and history.
- **Issues:** report bugs and track tasks.
- **Pull requests:** propose changes for review.
- **Projects:** organize and track work.
- **Releases:** publish versions of a project.
- **Actions:** automate workflows.

## Create a repository

1. Sign in at [GitHub](https://github.com/).
2. Select **New repository**.
3. Enter a repository name.
4. Choose public or private visibility.
5. Optionally add a README and a .gitignore file.
6. Select **Create repository**.

A public repository can be viewed by anyone. A private repository is limited to people who have access.

## README file

A README introduces the project. It can contain:

- Project name and purpose.
- Topics covered.
- Instructions for using the project.
- Useful links and examples.

## Upload a local project

Run these commands in the project folder. Replace the URL with your own repository URL.

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin REPOSITORY_URL
git push -u origin main
```

## Clone a repository

```bash
git clone REPOSITORY_URL
```

This downloads the repository and its history to your computer.

## Branches and pull requests

1. Create a branch for your work.
2. Make changes and commit them.
3. Push the branch to GitHub.
4. Open a pull request.
5. Review the changes.
6. Merge the pull request when it is ready.

## Fork vs clone

- **Fork:** creates a separate hosted copy under another GitHub account or namespace.
- **Clone:** creates a local copy on your computer.

## Security

- Never share passwords or personal access tokens.
- Do not commit API keys or private keys.
- Use repository permissions carefully.
- Remember that adding a secret to .gitignore does not remove it from Git history if it was already committed.

## What I learned

I learned how to create repositories, upload projects, use README files, work with branches, and collaborate using pull requests.


## Practical example: publish a project

Assume a local folder named \`my-project\` contains a file named \`hello.txt\`.

Run:

\`\`\`bash
cd my-project
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/USERNAME/my-project.git
git push -u origin main
\`\`\`

Replace \`USERNAME\` and the repository name with your own GitHub details.

Expected result on GitHub:

- A repository named \`my-project\` is visible in your account.
- The \`hello.txt\` file appears in the file list.
- The commit message \`Initial commit\` appears in the commit history.
- The default branch is \`main\`.

## Example: create and merge a pull request

Suppose I want to add a file called \`notes.txt\`.

Run locally:

\`\`\`bash
git switch -c add-notes
echo "My project notes" > notes.txt
git add notes.txt
git commit -m "Add project notes"
git push -u origin add-notes
\`\`\`

Then on GitHub:

1. Open the repository.
2. Select **Compare & pull request** (if shown), or open the **Pull requests** tab and select **New pull request**.
3. Set the base branch to \`main\` and compare branch to \`add-notes\`.
4. Create and review the pull request.
5. Select **Merge pull request** when ready.

Expected result: \`notes.txt\` is included in the \`main\` branch after the pull request is merged. On your computer, update your local main branch with:

\`\`\`bash
git switch main
git pull origin main
\`\`\`

## Example: create an Issue

A sample issue could be:

\`\`\`text
Title: Correct spelling in README
Description: The project README contains a spelling mistake.
\`\`\`

Expected result: GitHub creates an issue page where team members can discuss and track the task.
