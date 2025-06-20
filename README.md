
# 🧰 Git Setup & Commit Guide

This guide helps you set up Git for any new project and push it to GitHub with clean commit practices.

---

## 🔹 Step 1: Initialize Git and First Push to GitHub

```bash
# Create README file (optional but recommended)
echo "# Git-Config-setup" >> README.md

# Initialize Git
git init

# Add README or all files
git add README.md
# OR
git add .

# Make first commit
git commit -m "first commit"

# Rename default branch to main
git branch -M main

# Connect to GitHub repository
git remote add origin https://github.com/isantoshg/Git-Config-setup.git

# Push the first commit to GitHub
git push -u origin main
```

---

## 🔹 Step 2: Making Changes and Committing

```bash
# Add all modified/new files
git add .

# OR add a specific file
git add filename.php

# Commit changes with message
git commit -m "meaningful commit message"
```

---

## 🔹 Step 3: Push Changes to GitHub

```bash
git push origin main
```

---

## 🔥 If You Get This Error While Pushing:

> `! [rejected] main -> main (fetch first)`  
> `error: failed to push some refs to ...`

### ✅ Fix It Like This:

```bash
# First pull and rebase remote changes
git pull origin main --rebase

# Resolve any merge conflicts if shown (in your code editor or terminal)

# Then push again
git push origin main
```

💡 **Why use `--rebase`?**  
To keep your Git history clean and linear without unnecessary merge commits.

---

## 🛠️ Optional but Useful Git Config Setup (Run Once Globally)

```bash
# Set your name and email (required for commits)
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"

# Set default editor (optional)
git config --global core.editor "code"  # for VS Code
```

---

## 🧾 Helpful Git Commands

```bash
git status             # Show changes
git log --oneline      # Show commit history
git diff               # View unstaged changes
git restore filename   # Discard changes in file
```

---

## 📦 .gitignore (Optional Setup)

To avoid committing unnecessary files, create a `.gitignore` file:

```bash
# Sample contents
node_modules/
.env
*.log
vendor/
.DS_Store
```

You can also use https://www.toptal.com/developers/gitignore to generate `.gitignore` for specific stacks.

---

✅ Now you’re ready to work with Git and GitHub like a pro.
