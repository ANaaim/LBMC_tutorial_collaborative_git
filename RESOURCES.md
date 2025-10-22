# Git & GitHub Resources 📚

A curated collection of resources to help you master Git and GitHub. These resources complement the hands-on exercises in this repository.

## Table of Contents

- [Official Documentation](#official-documentation)
- [Interactive Tutorials](#interactive-tutorials)
- [Video Tutorials](#video-tutorials)
- [Cheat Sheets](#cheat-sheets)
- [Books](#books)
- [Tools & Extensions](#tools--extensions)
- [Advanced Topics](#advanced-topics)
- [Common Issues & Solutions](#common-issues--solutions)

---

## Official Documentation

- **[Git Documentation](https://git-scm.com/doc)** - The official Git documentation
- **[GitHub Docs](https://docs.github.com)** - Comprehensive GitHub guides
- **[Git Reference](https://git-scm.com/docs)** - Complete command reference
- **[Pro Git Book](https://git-scm.com/book/en/v2)** - Free online book covering Git in depth

## Interactive Tutorials

- **[Learn Git Branching](https://learngitbranching.js.org/)** - Visual, interactive Git tutorial
- **[GitHub Learning Lab](https://lab.github.com/)** - Hands-on courses for GitHub
- **[Codecademy Git Course](https://www.codecademy.com/learn/learn-git)** - Beginner-friendly course
- **[Git Immersion](https://gitimmersion.com/)** - A guided tour through Git fundamentals
- **[Visualizing Git](https://git-school.github.io/visualizing-git/)** - See Git commands in action

## Video Tutorials

- **[Git & GitHub for Beginners](https://www.youtube.com/watch?v=RGOj5yH7evk)** - Crash course by freeCodeCamp
- **[Git Tutorial for Beginners](https://www.youtube.com/watch?v=8JJ101D3knE)** - By Programming with Mosh
- **[GitHub for Noobs](https://www.youtube.com/watch?v=1h9_cB9mPT8)** - Simple introduction to GitHub

## Cheat Sheets

### Essential Git Commands

#### Setup & Config
```bash
git config --global user.name "Your Name"
git config --global user.email "email@example.com"
git config --list                    # View all settings
```

#### Creating & Cloning
```bash
git init                             # Initialize a new repository
git clone <url>                      # Clone a remote repository
```

#### Basic Workflow
```bash
git status                           # Check status
git add <file>                       # Stage a file
git add .                            # Stage all changes
git commit -m "message"              # Commit with message
git push origin <branch>             # Push to remote
git pull                             # Pull latest changes
```

#### Branching
```bash
git branch                           # List branches
git branch <name>                    # Create branch
git checkout <branch>                # Switch branch
git checkout -b <branch>             # Create and switch
git switch <branch>                  # Switch branch (newer)
git switch -c <branch>               # Create and switch (newer)
git merge <branch>                   # Merge branch
git branch -d <branch>               # Delete branch
```

#### Viewing History
```bash
git log                              # View commit history
git log --oneline                    # Compact log
git log --graph                      # Visual graph
git log --oneline --graph --all      # Complete visual history
git diff                             # Show unstaged changes
git diff --staged                    # Show staged changes
git show <commit>                    # Show specific commit
```

#### Undoing Changes
```bash
git checkout -- <file>               # Discard unstaged changes
git reset HEAD <file>                # Unstage file
git reset --soft HEAD~1              # Undo last commit, keep changes
git reset --hard HEAD~1              # Undo last commit, discard changes (CAREFUL!)
git revert <commit>                  # Create new commit that undoes changes
```

#### Remote Repositories
```bash
git remote -v                        # List remotes
git remote add origin <url>          # Add remote
git fetch origin                     # Fetch from remote
git push origin <branch>             # Push branch
git pull origin <branch>             # Pull branch
```

#### Stashing
```bash
git stash                            # Stash changes
git stash list                       # List stashes
git stash apply                      # Apply latest stash
git stash pop                        # Apply and remove latest stash
git stash drop                       # Delete latest stash
```

### GitHub-Specific Workflow

```bash
# Fork workflow
1. Fork repo on GitHub
2. git clone <your-fork-url>
3. git remote add upstream <original-repo-url>
4. git checkout -b feature-branch
5. # Make changes
6. git add .
7. git commit -m "Description"
8. git push origin feature-branch
9. # Create PR on GitHub

# Keeping fork updated
git fetch upstream
git checkout main
git merge upstream/main
git push origin main
```

## Books

- **[Pro Git](https://git-scm.com/book/en/v2)** by Scott Chacon (Free online)
- **[Version Control with Git](https://www.oreilly.com/library/view/version-control-with/9781492091189/)** by Jon Loeliger
- **[Git Pocket Guide](https://www.oreilly.com/library/view/git-pocket-guide/9781449327507/)** by Richard E. Silverman

## Tools & Extensions

### Git GUIs
- **[GitKraken](https://www.gitkraken.com/)** - Beautiful Git client
- **[SourceTree](https://www.sourcetreeapp.com/)** - Free Git GUI by Atlassian
- **[GitHub Desktop](https://desktop.github.com/)** - Official GitHub client
- **[Git Extensions](https://gitextensions.github.io/)** - Windows Git client

### IDE Extensions
- **[GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)** - VS Code Git extension
- **[Git Graph](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph)** - VS Code graph visualizer
- **[Git Integration](https://plugins.jetbrains.com/plugin/7499-git-integration)** - IntelliJ/PyCharm

### CLI Tools
- **[tig](https://jonas.github.io/tig/)** - Text-mode interface for Git
- **[lazygit](https://github.com/jesseduffield/lazygit)** - Simple terminal UI for Git
- **[gh](https://cli.github.com/)** - GitHub CLI

## Advanced Topics

### Git Internals
- **[Git from the Bottom Up](https://jwiegley.github.io/git-from-the-bottom-up/)** - Understanding Git internals
- **[Git Objects](https://git-scm.com/book/en/v2/Git-Internals-Git-Objects)** - How Git stores data

### Advanced Workflows
- **[Gitflow Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)** - Branch management strategy
- **[GitHub Flow](https://guides.github.com/introduction/flow/)** - Simplified workflow for teams
- **[Trunk Based Development](https://trunkbaseddevelopment.com/)** - Alternative workflow

### Specialized Topics
- **[Git Hooks](https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks)** - Automate tasks with Git hooks
- **[Git Submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules)** - Managing nested repositories
- **[Git LFS](https://git-lfs.github.com/)** - Large File Storage
- **[Rewriting History](https://git-scm.com/book/en/v2/Git-Tools-Rewriting-History)** - Interactive rebase and more

## Common Issues & Solutions

### Problem: Merge Conflicts

**Symptoms**: Git can't automatically merge changes

**Solution**:
```bash
# 1. See which files have conflicts
git status

# 2. Open conflicted files - look for markers:
# <<<<<<< HEAD
# your changes
# =======
# their changes
# >>>>>>> branch-name

# 3. Edit files to resolve conflicts (remove markers)

# 4. Mark as resolved
git add <resolved-files>
git commit -m "Resolve merge conflict"
```

### Problem: Pushed to Wrong Branch

**Solution**:
```bash
# If you haven't pushed
git reset --soft HEAD~1    # Undo commit, keep changes
git checkout correct-branch
git add .
git commit -m "Your message"

# If you already pushed (be careful!)
# Contact your team - you may need to revert
```

### Problem: Need to Undo Last Commit

**Solution**:
```bash
# Keep changes, undo commit
git reset --soft HEAD~1

# Discard changes too (CAREFUL!)
git reset --hard HEAD~1

# Already pushed? Use revert instead
git revert HEAD
```

### Problem: Accidentally Deleted Unpushed Commits

**Solution**:
```bash
# Git keeps a reflog of all actions
git reflog

# Find your lost commit hash
git checkout <commit-hash>

# Or create a new branch from it
git branch recovery-branch <commit-hash>
```

### Problem: Large File in Commit

**Solution**:
```bash
# Remove from last commit (before push)
git rm --cached <large-file>
git commit --amend

# Already pushed? Use BFG Repo Cleaner
# https://rtyley.github.io/bfg-repo-cleaner/
```

### Problem: Wrong Commit Message

**Solution**:
```bash
# Last commit, not pushed
git commit --amend -m "New message"

# Already pushed
# Create a new commit explaining the previous one
```

### Problem: Want to Ignore Already Tracked Files

**Solution**:
```bash
# Add to .gitignore first
echo "file-to-ignore" >> .gitignore

# Remove from tracking but keep local file
git rm --cached <file>
git commit -m "Stop tracking file"
```

## Learning Path Suggestions

### Beginner (Week 1-2)
1. Complete [Learn Git Branching](https://learngitbranching.js.org/) levels 1-2
2. Read Pro Git chapters 1-3
3. Complete exercises in [TUTORIAL.md](TUTORIAL.md)
4. Make 3-5 pull requests to this repository

### Intermediate (Week 3-4)
1. Learn about merge strategies and rebasing
2. Practice resolving conflicts
3. Explore Git GUIs
4. Contribute to a real open-source project

### Advanced (Ongoing)
1. Master interactive rebase
2. Learn about Git hooks and automation
3. Understand Git internals
4. Mentor others in Git usage

## Contributing to This List

Found a great Git resource? Add it to this list!

1. Fork this repository
2. Add your resource in the appropriate section
3. Include a brief description
4. Create a pull request

**Quality guidelines:**
- Resources should be beginner-friendly or clearly marked as advanced
- Include a brief description of what the resource offers
- Verify links are working
- Prefer free resources when possible

---

## Quick Reference Card

**Print this for your desk!**

```
Most Used Commands:
┌─────────────────────────────────────────────┐
│ git status          Check what changed     │
│ git add .           Stage all changes      │
│ git commit -m "x"   Commit with message    │
│ git push            Push to remote         │
│ git pull            Get latest changes     │
│ git checkout -b x   Create new branch      │
│ git log --oneline   View history           │
└─────────────────────────────────────────────┘

Emergency Commands:
┌─────────────────────────────────────────────┐
│ git stash           Save changes for later │
│ git reflog          Find lost commits      │
│ git reset --soft    Undo last commit       │
│ git checkout --     Discard changes        │
└─────────────────────────────────────────────┘
```

---

**Happy Learning! 🚀**

Remember: Everyone was a beginner once. Keep practicing, and Git will become second nature!
