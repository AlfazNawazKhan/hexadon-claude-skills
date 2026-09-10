---
name: github-mastery
description: Comprehensive guide and workflow to master Git and GitHub from beginner fundamentals to advanced pro capabilities. Use this skill whenever the user asks about Git version control, GitHub workflows, repository creation, branching, pull requests, resolving merge conflicts, GitHub Actions, open source contributions, or profile setup—even if they don't explicitly name a specific command.
---

# GitHub Mastery Skill

Follow this structured workflow to guide users through mastering Git and GitHub from foundational concepts to advanced production practices.

## Workflow & Learning Path

### Phase 1: Core Concepts & Setup (Beginner)
1. **Version Control Fundamentals:**
   - Explain the three zones: Working Directory, Staging Area, and Local Repository.
   - Differentiate Git (local VCS) from GitHub (cloud hosting and collaboration platform).
2. **Account Setup & Security:**
   - Enable Two-Factor Authentication (2FA) via `Settings → Password and authentication`.
   - Save recovery codes in a secure password manager.
   - Create a Profile README repository named after the account username containing a `README.md` file.
3. **Essential Configuration:**
   - Configure user identity:
     ```bash
     git config --global user.name "Your Name"
     git config --global user.email "your.email@example.com"
     ```
   - Verify configuration with `git config --list`.

---

### Phase 2: Local Project Development (Intermediate)
1. **Repository Initialization:**
   - Initialize a local project: `git init`.
   - Check workspace state: `git status`.
   - Ignore untracked or system files by creating a `.gitignore` file.
2. **Staging & Committing:**
   - Stage changes: `git add <filename>` or `git add .`.
   - Save snapshot: `git commit -m "Descriptive commit message"`.
   - View commit history: `git log` or `git show`.

---

### Phase 3: The GitHub Flow & Collaboration (Pro Workflow)
1. **Branching Strategy:**
   - Create and switch to a feature branch:
     ```bash
     git switch -c feature-branch-name
     # or git checkout -b feature-branch-name
     ```
   - Keep the `main` branch protected; avoid committing directly to `main`.
2. **Pushing to Remote & Pull Requests (PRs):**
   - Connect local repo to remote: `git remote add origin <URL>`.
   - Upload branch: `git push origin feature-branch-name`.
   - Open a Pull Request on GitHub with a clear title, description, and issue linkage (e.g., `Closes #42`).
3. **Review & Merging:**
   - Review code diffs and comments before merging.
   - Merge PR into `main` branch on GitHub.
   - Pull remote updates locally: `git pull origin main`.
4. **Resolving Merge Conflicts:**
   - Identify conflict markers when concurrent changes touch the same lines.
   - Choose changes to keep, stage resolved files (`git add .`), and commit resolution (`git commit -m "resolve merge conflict"`).
5. **Branch Cleanup:**
   - Delete local branch: `git branch -d feature-branch-name`.
   - Delete remote branch: `git push origin --delete feature-branch-name`.

---

### Phase 4: Advanced Features & Automation (Expert)
1. **CI/CD with GitHub Actions:**
   - Define workflow automation files in `.github/workflows/main.yml`.
   - Trigger automated testing, linting, and deployment on `push` or `pull_request` events.
2. **Security & Vulnerability Scanning:**
   - Enable Dependabot for automated dependency updates.
   - Enable Secret Scanning to detect accidentally committed API keys and tokens.
   - Enable CodeQL for static application security testing.
3. **Hosting with GitHub Pages:**
   - Deploy static sites directly from repository settings (`Settings → Pages → Deploy from branch`).
4. **Open Source Contribution Protocol:**
   - Fork external repository to personal account.
   - Clone forked repo, create feature branch, make changes, and push.
   - Submit PR from forked branch back to original repository.
   - Filter issues by `good first issue` label to start contributing.

---

## Command Quick Reference Table
| Command | Action |
| --- | --- |
| `git init` | Initialize a new Git repository |
| `git clone <url>` | Copy a remote repository locally |
| `git status` | Check working tree and staging state |
| `git add .` | Stage all modified and new files |
| `git commit -m "msg"` | Save snapshot to local repo history |
| `git switch -c <branch>` | Create and switch to new branch |
| `git push origin <branch>` | Upload local branch commits to GitHub |
| `git pull origin <branch>` | Fetch and merge remote changes locally |
