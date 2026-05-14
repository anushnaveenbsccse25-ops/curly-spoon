
# =========================================================
# GIT COMPLETE WORKFLOW USING VS CODE (WINDOWS)
# =========================================================

# ---------------------------------------------------------
# INITIAL CONFIGURATION (Once on Local Machine)
# ---------------------------------------------------------

# Open VS Code
# Open Terminal:
# Terminal -> New Terminal

# Set Git username
git config --global user.name "Your Name"

# Set Git email
git config --global user.email "your@email.com"

# Enable colored output
git config --global color.ui auto

# Why --global?
# Applies configuration to all repositories on your computer.

# Other options:

# --local
# Applies only to current repository.

# Example:
git config --local user.name "Anush"

# --system
# Applies to entire system (admin permission required).

# Priority:
# Local > Global > System

# Example color output:
# modified: app.js      (yellow)
# deleted: style.css    (red)
# new file: index.html  (green)

# =========================================================
# PUSHING CODE TO GITHUB
# =========================================================

# Step 1:
# Create repository on GitHub

# Step 2:
# Open project folder in VS Code

# OR use terminal:
cd path/to/your/project

# Example:
# cd /c/Users/Anush/Desktop/project

# Open current folder in VS Code
code .

# Step 3:
# Initialize Git
git init

# Converts folder into Git repository.

# Step 4:
# Add all files
git add .

# Files move:
# Working Directory -> Staging Area

# Step 5:
# Commit files
git commit -m "Initial commit"

# Step 6:
# Connect GitHub repository
git remote add origin https://github.com/username/repository.git

# Check remotes
git remote -v

# Step 7:
# Rename branch
git branch -M main

# Push to GitHub
git push -u origin main

# =========================================================
# CLONING REPOSITORY
# =========================================================

# Step 1:
# Open repository on GitHub

# Step 2:
# Click "Code" and copy URL

# Step 3:
# Open terminal in VS Code

# Move to desired folder
cd path/to/folder

# Step 4:
# Clone repository
git clone https://github.com/username/repository.git

# Step 5:
# Enter repository
cd repository-name

# Open in VS Code
code .

# =========================================================
# FORKING
# =========================================================

# Step 1:
# Open repository on GitHub

# Step 2:
# Click "Fork"

# Step 3:
# Select your account

# Step 4:
# Forked repository created

# Step 5:
# Clone fork locally

git clone https://github.com/your-username/repo-name.git

cd repo-name

code .

# =========================================================
# PULL REQUEST WORKFLOW
# =========================================================

# Step 1:
# Fork repository

# ---------------------------------------------------------

# Step 2:
# Clone forked repository
git clone https://github.com/your-username/repo-name.git

cd repo-name

code .

# ---------------------------------------------------------

# Step 3:
# Add upstream repository
git remote add upstream https://github.com/original-owner/repo.git

# Check remotes
git remote -v

# Change origin URL
git remote set-url origin https://github.com/yourname/newrepo.git

# ---------------------------------------------------------

# Step 4:
# Create new branch
git checkout -b feature-update

# ---------------------------------------------------------

# Step 5:
# Edit code in VS Code

# Check changes
git status

# ---------------------------------------------------------

# Step 6:
# Stage and commit changes
git add .

git commit -m "Added new feature"

# ---------------------------------------------------------

# Step 7:
# Push branch to fork
git push origin feature-update

# Remove origin
git remote remove origin

# Add new origin
git remote add origin https://github.com/yourname/forkedrepo.git

# ---------------------------------------------------------

# Step 8:
# Create Pull Request

# Open forked repository on GitHub

# Click:
# "Compare & pull request"

# Base repo:
# Original repository

# Compare:
# feature-update branch

# Add title and description

# Click:
# "Create Pull Request"

# ---------------------------------------------------------

# Step 9:
# Review & Merge

# Repository owner reviews code
# and merges PR.

# =========================================================
# MERGE CONFLICT IN VS CODE
# =========================================================

# Create folder
mkdir merge-demo

cd merge-demo

# Initialize Git
git init

# Open in VS Code
code .

# Create file manually:
# story.txt

# Add content:
# Once upon a time, there was a coder.

# Stage and commit
git add story.txt

git commit -m "Initial commit"

# Create branch A
git checkout -b feature-A

# Edit story.txt:
# Once upon a time, there was a coder. They loved working with Git.

git add story.txt

git commit -m "Feature A change"

# Return to main/master
git checkout master

# If branch is main:
# git checkout main

# Create branch B
git checkout -b feature-B

# Edit story.txt:
# Once upon a time, there was a coder. They enjoyed solving puzzles.

git add story.txt

git commit -m "Feature B change"

# Return to master/main
git checkout master

# Merge branch A
git merge feature-A

# Merge branch B
git merge feature-B

# Merge conflict occurs.

# Open story.txt in VS Code

# VS Code shows:
# Accept Current Change
# Accept Incoming Change
# Accept Both Changes
# Compare Changes

# Resolve conflict manually.

# Example final text:
# Once upon a time, there was a coder.
# They loved Git and solving puzzles.

# Save file.

# Final commit
git add story.txt

git commit -m "Resolved merge conflict"

# =========================================================
# IMPORTANT COMMANDS
# =========================================================

# Check status
git status

# View branches
git branch

# View commit history
git log --oneline

# Switch branch
git checkout branch-name

# Pull latest changes
git pull

# Push changes
git push

# Fetch latest changes
git fetch

# =========================================================
# IMPORTANT VIVA QUESTIONS
# =========================================================

# What is Git?
# Distributed version control system.

# What is GitHub?
# Cloud platform for hosting Git repositories.

# What is repository?
# Project folder tracked by Git.

# What is commit?
# Snapshot/version of project.

# What is staging area?
# Temporary area before commit.

# Difference between clone and fork?
# Clone = local copy
# Fork = GitHub copy under your account

# What is origin?
# Default name of remote repository.

# What is upstream?
# Original repository from which fork was created.

# What is Pull Request?
# Request to merge changes into another repository.

# What is merge conflict?
# Conflict when Git cannot merge changes automatically.

# Why branches are used?
# To develop features independently without affecting main code.
