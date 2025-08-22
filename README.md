# GitHub Flow: Complete Step-by-Step Guide

This comprehensive guide will help you set up your project in GitHub using Git and Git Bash, perfect for beginners and as a teaching resource.

---

## 📋 Prerequisites

Before we start, make sure you have:

- ✅ GitHub account (free at [github.com](https://github.com))
- ✅ Git installed on your computer
- ✅ Git Bash (comes with Git installation)
- ✅ Basic understanding of folders and command line

**Check if Git is installed:**

```bash
git --version
```

If you see a version number, you're ready to go!

---

## 🌟 GitHub Flow Workflow Diagram

```
Local Computer                    GitHub (Remote)
     │                                 │
     ├── 1. Clone Repository ←─────────┤
     │                                 │
     ├── 2. Make Changes               │
     │                                 │
     ├── 3. Stage Files (git add)      │
     │                                 │
     ├── 4. Commit (git commit)        │
     │                                 │
     ├── 5. Push Changes ──────────────→
     │                                 │
     └── 6. Pull Updates ←─────────────┤
```

---

## 🚀 Step-by-Step Process

### Step 1: Create Repository (on GitHub)

1. **Log in** to your GitHub account
2. Click the **"+"** button in top-right corner
3. Select **"New repository"**
4. **Repository setup:**
   - Enter a **repository name** (e.g., "my-awesome-project")
   - Add a **description** (optional but recommended)
   - Choose **Public** (anyone can see) or **Private** (only you)
   - ✅ Check **"Add a README file"** (recommended for new projects)
   - Select a **license** if needed (MIT is popular for open source)
5. Click **"Create repository"**

---

### Step 2: Clone Repository (to your computer)

**Open Git Bash** and navigate to where you want your project:

```bash
# Navigate to your desired folder (e.g., Desktop)
cd ~/Desktop

# Clone the repository
git clone <repository-link>

# Enter the project folder
cd <repository-folder-name>
```

**Real Example:**

```bash
cd ~/Desktop
git clone https://github.com/johnsmith/my-awesome-project.git
cd my-awesome-project
```

**💡 Tip:** Get the repository link by clicking the green **"Code"** button on GitHub and copying the HTTPS URL.

---

### Step 3: Add Your Project Files

1. **Add your files** to the cloned folder using File Explorer/Finder
2. **Check the status** of your repository:

```bash
git status
```

This shows:

- 🟢 **Untracked files** (new files Git doesn't know about)
- 🟡 **Modified files** (files that have been changed)
- 🟢 **Staged files** (files ready to be committed)

---

### Step 4: Stage, Commit, and Push Your Changes

Follow this **essential 3-step process:**

#### 4a. Stage Files (Prepare for commit)

```bash
# Stage all files
git add .

# Or stage specific files
git add filename.txt
git add folder/
```

#### 4b. Commit Changes (Save a snapshot)

```bash
git commit -m "Your descriptive commit message here"
```

**✅ Good commit message examples:**

- `"Add homepage layout with navigation"`
- `"Fix login form validation bug"`
- `"Update README with installation instructions"`

**❌ Poor commit message examples:**

- `"update"`
- `"changes"`
- `"fix"`

#### 4c. Push to GitHub (Upload changes)

```bash
git push origin main
```

**Complete workflow example:**

```bash
git add .
git commit -m "Add initial project files and setup"
git push origin main
```

---

### Step 5: Verify Your Upload

1. **Go to your GitHub repository page**
2. **Refresh the page** (F5)
3. **Confirm your files** are visible
4. **Check commit history:**

```bash
git log --oneline
```

---

## 🔧 Essential Additional Commands

### Before Making Changes - Always Pull First

```bash
# Get the latest changes from GitHub
git pull origin main
```

### Working with Branches

```bash
# Create and switch to a new branch
git checkout -b feature-login

# List all branches
git branch

# Switch back to main branch
git checkout main

# Delete a branch (after merging)
git branch -d feature-login
```

### Ignore Unwanted Files

Create a `.gitignore` file in your project root:

```gitignore
# Dependencies
node_modules/
vendor/

# Environment files
.env
.env.local

# Build outputs
dist/
build/
*.log

# OS generated files
.DS_Store
Thumbs.db
```

### Check Repository Information

```bash
# View remote repository URL
git remote -v

# View commit history with details
git log

# View current branch and status
git status

# View differences in files
git diff
```

---

## 🔄 Daily Workflow Summary

Here's your **daily development routine:**

1. **Start your work session:**

   ```bash
   git pull origin main    # Get latest changes
   ```

2. **Make your changes** (edit files, add features, etc.)

3. **Save your work:**

   ```bash
   git add .                           # Stage changes
   git commit -m "Descriptive message" # Commit changes
   git push origin main                # Push to GitHub
   ```

4. **Repeat** as needed throughout your development

---

## 🆘 Common Issues & Solutions

### Issue: "Permission denied"

**Solution:** Make sure you're logged in to GitHub and have access to the repository.

### Issue: "Repository not found"

**Solution:** Double-check the repository URL and ensure it exists.

### Issue: "Your branch is behind"

**Solution:** Run `git pull origin main` before pushing.

### Issue: "Merge conflict"

**Solution:** This happens when the same file is edited differently. Git will mark the conflicts in your files - edit them manually and commit.

---

## 🎯 Best Practices

1. **Commit frequently** - Small, focused commits are better than large ones
2. **Write clear commit messages** - Future you will thank you
3. **Pull before pushing** - Avoid conflicts
4. **Use branches for features** - Keep main branch stable
5. **Review changes before committing** - Use `git status` and `git diff`

---

## 📚 What's Next?

Once comfortable with basics, explore:

- **GitHub Issues** for project management
- **Pull Requests** for code review
- **GitHub Actions** for automation
- **Collaborating** with other developers
- **Advanced Git** commands and workflows

---

_Happy coding! 🚀_
