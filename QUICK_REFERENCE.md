# Git Quick Reference Guide 📋

A one-page cheat sheet you can print and keep at your desk!

---

## Setup (Do Once)

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

---

## Starting a Project

```bash
# Start fresh
git init

# Copy existing project
git clone https://github.com/username/repo.git
```

---

## Daily Workflow

```bash
# 1. Check status (do this often!)
git status

# 2. See what changed
git diff

# 3. Stage changes
git add filename          # Add specific file
git add .                # Add all changes

# 4. Save snapshot
git commit -m "Brief description of changes"

# 5. Upload to GitHub
git push origin branch-name

# 6. Download from GitHub
git pull
```

---

## Branching

```bash
# Create new branch
git checkout -b my-new-branch

# Switch branches
git checkout branch-name

# List branches
git branch

# Delete branch (after merging)
git branch -d branch-name
```

---

## Fork Workflow (Contributing to Others' Projects)

```bash
# 1. Fork on GitHub (click Fork button)

# 2. Clone your fork
git clone https://github.com/YOUR-USERNAME/project.git

# 3. Create branch
git checkout -b my-feature

# 4. Make changes, commit
git add .
git commit -m "Add my feature"

# 5. Push to your fork
git push origin my-feature

# 6. Create Pull Request on GitHub
```

---

## Viewing History

```bash
# See commits
git log

# Compact view
git log --oneline

# Visual graph
git log --oneline --graph --all

# Who changed what
git blame filename
```

---

## Undo Changes

```bash
# Discard unstaged changes in file
git checkout -- filename

# Unstage a file (keep changes)
git reset HEAD filename

# Undo last commit (keep changes)
git reset --soft HEAD~1

# Undo last commit (discard changes) - CAREFUL!
git reset --hard HEAD~1
```

---

## Stashing (Save Work for Later)

```bash
# Save current work
git stash

# See stashed work
git stash list

# Restore stashed work
git stash pop
```

---

## Getting Help

```bash
# Help for any command
git help <command>
git <command> --help
```

---

## Common Situations

### "I made a typo in my commit message"
```bash
# Before pushing
git commit --amend -m "New message"
```

### "I committed to the wrong branch"
```bash
# Before pushing
git reset --soft HEAD~1
git checkout correct-branch
git add .
git commit -m "Message"
```

### "I need to update my branch with main"
```bash
git checkout main
git pull
git checkout my-branch
git merge main
```

### "I have a merge conflict"
```bash
# 1. Git will tell you which files have conflicts
git status

# 2. Open files, look for:
# <<<<<<< HEAD
# your changes
# =======
# their changes
# >>>>>>> branch-name

# 3. Edit files to resolve, remove markers

# 4. Mark as resolved
git add filename
git commit -m "Resolve merge conflict"
```

---

## Pro Tips 💡

1. **Commit often** - Small commits are easier to manage
2. **Write clear messages** - Future you will thank you
3. **Pull before you push** - Stay up to date
4. **Use branches** - Keep main clean
5. **Check status frequently** - Know what's happening
6. **Don't commit passwords** - Add them to .gitignore

---

## Status Symbols

```
?? - Untracked file (new file)
M  - Modified file
A  - Added file (staged)
D  - Deleted file
R  - Renamed file
```

---

## Essential Git States

```
Working Directory  →  git add  →  Staging Area  →  git commit  →  Repository
     (modified)                     (staged)                    (committed)
```

---

## Need More Help?

- See [RESOURCES.md](RESOURCES.md) for detailed guides
- Check [TUTORIAL.md](TUTORIAL.md) for hands-on practice
- Ask in repository issues
- Read official docs: https://git-scm.com/doc

---

**Print this page and keep it handy!** 📄

_Last updated: October 2025_
