---
description: Create a pull request for a GitHub Pages Jekyll site repo
---

# Create Pull Request Workflow

Use this workflow when the user wants to submit their current changes to GitHub.
Read `.agent/skills/create-pr/SKILL.md` before starting.

## Steps

1. **Check branch** — Verify if the user is on a feature branch or `main`.
   ```powershell
   git branch --show-current
   ```
   If on `main`, ask if they want to create a new branch first.

2. **Stage changes** — Show the user what is about to be staged.
   ```powershell
   git status
   ```
   // turbo
   Stage the changes:
   ```powershell
   git add .
   ```

3. **Commit changes** — Create a commit with a descriptive message following the skill guidelines.
   // turbo
   ```powershell
   git commit -m "Feat: [describe changes]"
   ```

4. **Push to GitHub** — Push the current branch to the remote repository.
   // turbo
   ```powershell
   $branch = git branch --show-current; git push origin $branch
   ```

5. **Generate PR Link** — Construct the GitHub URL and present it to the user.
   The link should be: `https://github.com/{github.owner}/{github.repo}/compare/{git.main_branch}...[BRANCH_NAME]`

6. **Finalize** — Inform the user that the changes are pushed and they can complete the PR using the link provided.
