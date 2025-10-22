# Git Collaboration Tutorial - Hands-On Exercises 🎓

This tutorial provides step-by-step exercises to help you master Git collaboration. Work through each exercise in order for the best learning experience.

## Table of Contents

1. [Exercise 1: Add Yourself as a Contributor](#exercise-1-add-yourself-as-a-contributor)
2. [Exercise 2: Fix a Typo](#exercise-2-fix-a-typo)
3. [Exercise 3: Add a New Resource](#exercise-3-add-a-new-resource)
4. [Exercise 4: Create Documentation](#exercise-4-create-documentation)
5. [Exercise 5: Review Someone Else's Pull Request](#exercise-5-review-someone-elses-pull-request)
6. [Exercise 6: Resolve a Merge Conflict](#exercise-6-resolve-a-merge-conflict)
7. [Exercise 7: Collaborate on a Document](#exercise-7-collaborate-on-a-document)

---

## Exercise 1: Add Yourself as a Contributor

**Goal**: Make your first pull request by adding your name to the contributors list.

**Skills Practiced**: Forking, cloning, branching, committing, pushing, creating PRs

### Steps

1. **Fork this repository**
   - Click the "Fork" button on GitHub
   - This creates a copy in your account

2. **Clone your fork**
   ```bash
   git clone https://github.com/YOUR-USERNAME/LBMC_tutorial_collaborative_git.git
   cd LBMC_tutorial_collaborative_git
   ```

3. **Create a new branch**
   ```bash
   git checkout -b add-my-name
   ```

4. **Edit CONTRIBUTORS.md**
   - Open `CONTRIBUTORS.md`
   - Add your information in this format:
     ```markdown
     - Your Name - @your-github-username - Brief bio or interest
     ```

5. **Commit your changes**
   ```bash
   git add CONTRIBUTORS.md
   git commit -m "Add [Your Name] to contributors"
   ```

6. **Push to your fork**
   ```bash
   git push origin add-my-name
   ```

7. **Create a Pull Request**
   - Go to your fork on GitHub
   - Click "Compare & pull request"
   - Fill in the PR description
   - Submit!

**Success Criteria**: Your PR is created and shows your name addition in the Files Changed tab.

---

## Exercise 2: Fix a Typo

**Goal**: Practice making small improvements to documentation.

**Skills Practiced**: Finding issues, making targeted changes, descriptive commits

### Steps

1. **Create a new branch**
   ```bash
   git checkout main
   git pull origin main
   git checkout -b fix-typo-in-readme
   ```

2. **Find and fix a typo**
   - Look through the markdown files
   - Fix any typos, grammatical errors, or formatting issues you find
   - If you can't find any, improve the wording of a sentence

3. **Commit with a descriptive message**
   ```bash
   git add .
   git commit -m "Fix typo in README: [describe what you fixed]"
   ```

4. **Push and create PR**
   ```bash
   git push origin fix-typo-in-readme
   ```

**Success Criteria**: Your commit message clearly describes what you fixed.

---

## Exercise 3: Add a New Resource

**Goal**: Contribute helpful content to the community.

**Skills Practiced**: Adding value through contributions, proper formatting

### Steps

1. **Create a branch**
   ```bash
   git checkout main
   git pull origin main
   git checkout -b add-git-resource
   ```

2. **Add a resource to RESOURCES.md**
   - Open `RESOURCES.md`
   - Add a helpful Git tutorial, tool, or article
   - Follow the existing format
   - Add it in the appropriate section

3. **Commit and push**
   ```bash
   git add RESOURCES.md
   git commit -m "Add [resource name] to Git resources"
   git push origin add-git-resource
   ```

4. **Create a PR with context**
   - In the PR description, explain why this resource is helpful
   - What will people learn from it?

**Success Criteria**: Your PR includes context about why the resource is valuable.

---

## Exercise 4: Create Documentation

**Goal**: Practice creating new content in a collaborative repository.

**Skills Practiced**: Content creation, organizing information, using markdown

### Steps

1. **Choose a topic**
   - Think of something you've learned about Git
   - Examples: "How to write good commit messages", "Understanding .gitignore", "Git aliases"

2. **Create a branch**
   ```bash
   git checkout main
   git pull origin main
   git checkout -b docs-your-topic-name
   ```

3. **Create a new file in the docs/ folder**
   ```bash
   # Create the file
   touch docs/your-topic.md
   ```

4. **Write documentation**
   - Use proper markdown formatting
   - Include:
     - Title (# heading)
     - Introduction
     - Main content with examples
     - Summary or tips
   - Use code blocks for commands

5. **Commit and push**
   ```bash
   git add docs/your-topic.md
   git commit -m "Add documentation for [your topic]"
   git push origin docs-your-topic-name
   ```

**Success Criteria**: Your documentation is well-formatted and includes code examples.

---

## Exercise 5: Review Someone Else's Pull Request

**Goal**: Learn the review process from the reviewer's perspective.

**Skills Practiced**: Code review, constructive feedback, collaboration

### Steps

1. **Find an open PR**
   - Go to the "Pull Requests" tab on GitHub
   - Find an open PR from another contributor

2. **Review the changes**
   - Click on "Files changed"
   - Read through the changes carefully
   - Look for:
     - Typos or errors
     - Formatting consistency
     - Clarity of writing

3. **Leave a review**
   - Add comments on specific lines if you have suggestions
   - Or leave a general review:
     - "Approve" if it looks good
     - "Comment" for feedback without approval
     - "Request changes" if something needs fixing
   - Be kind and constructive!

4. **Example good review comments**
   - ✅ "Great addition! Could you add an example here to make it clearer?"
   - ✅ "Nice work! Just a small typo on line 23: 'teh' → 'the'"
   - ✅ "This looks good to me! 👍"
   
   **Bad review comments:**
   - ❌ "This is wrong"
   - ❌ "Bad"
   - ❌ "lol"

**Success Criteria**: You leave at least one constructive comment or review on a PR.

---

## Exercise 6: Resolve a Merge Conflict

**Goal**: Learn to handle merge conflicts confidently.

**Skills Practiced**: Conflict resolution, merging, communication

### Steps

This exercise simulates a common real-world scenario.

1. **Create a branch and make a change**
   ```bash
   git checkout main
   git pull origin main
   git checkout -b my-conflict-branch
   ```

2. **Edit a file that others might also edit**
   - Edit a line in `CONTRIBUTORS.md` or `RESOURCES.md`
   - Commit and push:
   ```bash
   git add .
   git commit -m "Update contributors list"
   git push origin my-conflict-branch
   ```

3. **Meanwhile, simulate the main branch changing**
   - Before you create your PR, someone else's PR gets merged
   - This changes the same file you edited

4. **Update your branch from main**
   ```bash
   git checkout main
   git pull origin main
   git checkout my-conflict-branch
   git merge main
   ```

5. **If there's a conflict:**
   - Git will tell you which files have conflicts
   - Open the file(s) - you'll see conflict markers:
   ```
   <<<<<<< HEAD
   Your changes
   =======
   Changes from main
   >>>>>>> main
   ```

6. **Resolve the conflict**
   - Edit the file to keep what you want
   - Remove the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`)
   - Save the file

7. **Complete the merge**
   ```bash
   git add .
   git commit -m "Resolve merge conflict in [filename]"
   git push origin my-conflict-branch
   ```

**Success Criteria**: You successfully resolve a conflict and the PR can be merged.

**Note**: If you don't encounter a real conflict, that's okay! Understanding the process is the key learning.

---

## Exercise 7: Collaborate on a Document

**Goal**: Work with others on a shared document.

**Skills Practiced**: Team collaboration, communication, coordinated changes

### Steps

1. **Choose a collaborative document**
   - Use `exercises/collaborative-story.md` or `exercises/team-tips.md`

2. **Coordinate with others**
   - In the Issues or Discussions, say what you plan to add
   - Example: "I'll add a paragraph about code reviews"

3. **Create your branch**
   ```bash
   git checkout main
   git pull origin main
   git checkout -b contribute-to-story
   ```

4. **Make your addition**
   - Add your contribution to the document
   - Make sure it flows with existing content

5. **Create a PR with coordination info**
   - Title: "Add [your contribution] to collaborative document"
   - Description: Explain what you added and how it fits

6. **Communicate**
   - If you see someone else working on the same document, communicate!
   - You might need to coordinate timing or sections

**Success Criteria**: Your contribution is merged and works well with others' contributions.

---

## Advanced Challenges

Once you've completed the basic exercises, try these:

### Challenge 1: Squash Commits
- Make multiple small commits on a branch
- Use `git rebase -i` to squash them into one clean commit
- Force push and update your PR

### Challenge 2: Cherry-pick a Commit
- Create a commit on one branch
- Use `git cherry-pick` to apply it to another branch

### Challenge 3: Use Git Stash
- Make changes without committing
- Use `git stash` to save them temporarily
- Switch branches, then apply the stash later

### Challenge 4: Set Up Git Aliases
- Create shortcuts for common commands
- Example: `git config --global alias.co checkout`

### Challenge 5: Write a Git Hook
- Create a pre-commit hook to check for common issues
- Example: Check for debug statements or large files

---

## Tips for Success

1. **Read other people's PRs** - You'll learn a lot from seeing how others contribute
2. **Don't be afraid to make mistakes** - That's what this repository is for!
3. **Ask questions** - Open an issue if you're stuck
4. **Start small** - Begin with simple changes and build confidence
5. **Be patient** - Learning Git takes practice
6. **Help others** - Review PRs, answer questions, share what you learn

---

## Completion Checklist

Track your progress:

- [ ] Exercise 1: Added myself to contributors
- [ ] Exercise 2: Fixed a typo or improved wording
- [ ] Exercise 3: Added a helpful resource
- [ ] Exercise 4: Created new documentation
- [ ] Exercise 5: Reviewed someone else's PR
- [ ] Exercise 6: Handled a merge conflict
- [ ] Exercise 7: Collaborated on a shared document

---

## What's Next?

After completing these exercises, you'll have hands-on experience with:
- The complete Git workflow
- Collaborative development practices
- Pull request creation and review
- Conflict resolution
- Team communication

**You're ready to contribute to real projects!** 🚀

Keep practicing, keep learning, and most importantly - keep collaborating!

---

**Questions or suggestions?** Open an issue or check [RESOURCES.md](RESOURCES.md) for more help.
