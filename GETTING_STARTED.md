# Getting Started with Git and GitHub 🌱

Welcome! This guide will help you set up Git and make your first contribution to this repository.

## Table of Contents

- [Installing Git](#installing-git)
- [Configuring Git](#configuring-git)
- [Understanding Basic Concepts](#understanding-basic-concepts)
- [Creating a GitHub Account](#creating-a-github-account)
- [Your First Contribution](#your-first-contribution)

## Installing Git

### Windows
1. Download Git from https://git-scm.com/download/win
2. Run the installer with default settings
3. Open "Git Bash" to verify: `git --version`

### macOS
1. Open Terminal
2. Install using Homebrew: `brew install git`
   - Or download from https://git-scm.com/download/mac
3. Verify installation: `git --version`

### Linux
```bash
# Debian/Ubuntu
sudo apt-get update
sudo apt-get install git

# Fedora
sudo dnf install git

# Verify
git --version
```

## Configuring Git

After installing Git, configure your identity:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

**Important**: Use the same email as your GitHub account!

Optional but recommended settings:

```bash
# Set default branch name to 'main'
git config --global init.defaultBranch main

# Enable colorful output
git config --global color.ui auto

# Set your default editor (example: VS Code)
git config --global core.editor "code --wait"
```

Verify your configuration:

```bash
git config --list
```

## Understanding Basic Concepts

### What is Git?

Git is a **version control system** that tracks changes in your files over time. Think of it as a super-powered "undo" button for your entire project!

### Key Concepts

- **Repository (Repo)**: A folder tracked by Git containing your project and its history
- **Commit**: A snapshot of your project at a specific point in time
- **Branch**: A parallel version of your repository (allows you to work independently)
- **Remote**: A version of your repository hosted on the internet (like GitHub)
- **Clone**: Creating a local copy of a remote repository
- **Pull**: Getting updates from a remote repository
- **Push**: Sending your local commits to a remote repository
- **Fork**: Creating your own copy of someone else's repository
- **Pull Request (PR)**: Proposing changes to be merged into the main project

### Basic Git Workflow

```
1. Clone a repository    →  Get a copy on your computer
2. Create a branch       →  Make a new workspace for your changes
3. Make changes          →  Edit files
4. Stage changes         →  Mark files to be committed
5. Commit changes        →  Save a snapshot
6. Push to remote        →  Upload your commits
7. Create Pull Request   →  Propose merging your changes
```

## Creating a GitHub Account

1. Go to https://github.com/signup
2. Follow the signup process
3. Verify your email address
4. Set up your profile (add a profile picture and bio!)

### Setting up SSH (Optional but Recommended)

SSH allows you to connect to GitHub without entering your password each time.

1. Generate an SSH key:
```bash
ssh-keygen -t ed25519 -C "your.email@example.com"
```

2. Start the SSH agent:
```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

3. Copy your public key:
```bash
# Linux/macOS
cat ~/.ssh/id_ed25519.pub

# Windows (Git Bash)
cat ~/.ssh/id_ed25519.pub
```

4. Add the SSH key to your GitHub account:
   - Go to GitHub Settings → SSH and GPG keys → New SSH key
   - Paste your public key
   - Save

## Your First Contribution

Now you're ready to make your first contribution! Follow these steps:

### 1. Fork the Repository

1. Go to this repository on GitHub
2. Click the "Fork" button in the top-right corner
3. This creates a copy of the repository in your GitHub account

### 2. Clone Your Fork

```bash
# Replace YOUR-USERNAME with your GitHub username
git clone https://github.com/YOUR-USERNAME/LBMC_tutorial_collaborative_git.git

# Navigate into the repository
cd LBMC_tutorial_collaborative_git
```

### 3. Create a Branch

```bash
# Create and switch to a new branch
git checkout -b add-my-name

# Or using newer Git syntax
git switch -c add-my-name
```

**Branch naming tips:**
- Use descriptive names: `add-john-doe`, `fix-typo-readme`, `update-resources`
- Use lowercase and hyphens
- Keep it short but meaningful

### 4. Make Your Changes

Open `CONTRIBUTORS.md` and add your name:

```markdown
- Your Name - @your-github-username
```

### 5. Stage and Commit Your Changes

```bash
# Check what files changed
git status

# Add the file to staging
git add CONTRIBUTORS.md

# Commit with a descriptive message
git commit -m "Add [Your Name] to contributors"
```

**Good commit messages:**
- ✅ "Add John Doe to contributors list"
- ✅ "Fix typo in README.md"
- ✅ "Update Git installation instructions"

**Bad commit messages:**
- ❌ "update"
- ❌ "fixes"
- ❌ "asdfasdf"

### 6. Push Your Changes

```bash
# Push your branch to your fork
git push origin add-my-name
```

### 7. Create a Pull Request

1. Go to your fork on GitHub
2. Click "Compare & pull request"
3. Add a title and description explaining your changes
4. Click "Create pull request"

Congratulations! 🎉 You've made your first contribution!

## What's Next?

Now that you've got the basics down, continue to [TUTORIAL.md](TUTORIAL.md) for more advanced exercises and practice scenarios.

## Common Commands Cheat Sheet

```bash
# Check repository status
git status

# View commit history
git log
git log --oneline --graph

# Create a new branch
git checkout -b branch-name

# Switch between branches
git checkout branch-name
# or
git switch branch-name

# Pull latest changes
git pull

# Add files to staging
git add filename
git add .                    # Add all changes

# Commit changes
git commit -m "Message"

# Push changes
git push origin branch-name

# View differences
git diff                     # Unstaged changes
git diff --staged            # Staged changes

# Undo changes (careful!)
git checkout -- filename     # Discard unstaged changes
git reset HEAD filename      # Unstage changes
```

## Troubleshooting

### "Permission denied" error when pushing
- Make sure you've forked the repository
- Check that you're pushing to your fork, not the original repository
- Verify your SSH keys or GitHub credentials

### "Merge conflict" when pulling
- Don't panic! This is normal in collaborative work
- Git will mark the conflicting areas in your files
- Edit the files to resolve conflicts
- Stage and commit the resolved files

### Lost work?
- Git rarely loses data! Try `git reflog` to find lost commits
- Before doing anything destructive, make a backup branch

## Need Help?

- Check [RESOURCES.md](RESOURCES.md) for more detailed guides
- Open an issue on this repository
- Ask in your team chat

---

**Ready for more?** Continue to [TUTORIAL.md](TUTORIAL.md) for hands-on exercises!
