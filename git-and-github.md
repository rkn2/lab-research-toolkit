# Git and GitHub

Git is a version control system — it tracks changes to files over time and lets multiple people work on the same project without overwriting each other's work. GitHub is a website that hosts Git repositories and makes collaboration easier.

The lab's code, website, and resources (including this toolkit) all live on GitHub. You need to know the basics.

**Jump to:**
- [Core Concepts](#core-concepts)
- [Getting Started](#getting-started)
- [The Basic Daily Workflow](#the-basic-daily-workflow)
- [Essential Commands](#essential-commands)
- [Writing Good Commit Messages](#writing-good-commit-messages)
- [What to Put in Git (and What Not To)](#what-to-put-in-git-and-what-not-to)
- [GitHub for Collaboration](#github-for-collaboration)
- [Learning More](#learning-more)

---

## Core Concepts

**Repository (repo):** A folder tracked by Git. Every project has one.

**Commit:** A saved snapshot of your changes. Think of it as a checkpoint you can always return to.

**Branch:** A parallel version of the repo. You make changes on a branch without affecting the main version until you are ready.

**Push / Pull:** Push sends your local commits to GitHub. Pull brings changes from GitHub down to your machine.

**Clone:** Download a copy of a repo from GitHub to your computer.

---

## Getting Started

**Install Git:**
- Mac: Git is usually pre-installed. Check by running `git --version` in Terminal.
- If not installed: download from git-scm.com or install via Homebrew (`brew install git`)

**Configure your identity** (do this once):
```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

**Clone a repo:**
```bash
git clone https://github.com/rkn2/repo-name.git
```

---

## The Basic Daily Workflow

```bash
# See what has changed
git status

# Stage the files you want to commit
git add filename.py
# Or stage everything changed
git add .

# Commit with a message describing what you did
git commit -m "Add damage classification function"

# Push to GitHub
git push
```

---

## Essential Commands

| Command | What it does |
|---|---|
| `git status` | Show what has changed since last commit |
| `git log` | Show commit history |
| `git diff` | Show exactly what changed line by line |
| `git pull` | Get latest changes from GitHub |
| `git add <file>` | Stage a file for committing |
| `git commit -m "message"` | Save a snapshot with a description |
| `git push` | Send commits to GitHub |
| `git checkout -b branch-name` | Create and switch to a new branch |

---

## Writing Good Commit Messages

A commit message should complete the sentence: *"If applied, this commit will..."*

**Good:**
- `Add tornado damage classification model`
- `Fix off-by-one error in GPR depth calculation`
- `Update figure 3 to use consistent color scale`

**Not useful:**
- `update`
- `fix stuff`
- `changes`

You will thank yourself when you need to find something in the history six months later.

---

## What to Put in Git (and What Not To)

**Put in Git:**
- Code and scripts
- LaTeX files and `.bib` files
- Markdown documentation
- Small configuration files

**Do not put in Git:**
- Large data files (use DesignSafe, Google Drive, or a data repository instead)
- Compiled outputs (PDFs, `.pyc` files)
- Credentials or API keys — never commit passwords or tokens
- Jupyter notebook outputs if the notebooks are large (clear outputs before committing)

Use a `.gitignore` file to tell Git to automatically ignore certain file types.

---

## GitHub for Collaboration

When working with Rebecca or labmates on a shared repo:

1. **Pull before you start working** — always run `git pull` first to get the latest version
2. **Use branches for new features or experiments** — don't work directly on `main`
3. **Open a Pull Request** when your branch is ready — this lets Rebecca review before merging
4. **Communicate about conflicts** — if two people edited the same file, Git will flag a merge conflict; don't panic, just talk it through

---

## Learning More

- **Interactive tutorial:** learngitbranching.js.org — visual, hands-on, highly recommended
- **GitHub Docs:** docs.github.com — comprehensive reference
- **Pro Git book:** git-scm.com/book — free, thorough, worth reading the first few chapters
