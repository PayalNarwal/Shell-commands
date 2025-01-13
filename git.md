# Git Commands Cheat Sheet

This document provides a quick reference for basic Git commands to help you manage version control effectively.

---

## 1. **Setup and Configuration**
- **Set your username:**
  ```bash
  git config --global user.name "Your Name"
  ```
- **Set your email:**
  ```bash
  git config --global user.email "your.email@example.com"
  ```
- **Check current configuration:**
  ```bash
  git config --list
  ```

---

## 2. **Basic Git Workflow**
### Initialize a Repository:
- **Create a new Git repository:**
  ```bash
  git init
  ```
- **Clone an existing repository:**
  ```bash
  git clone <repository_url>
  ```

### Stage and Commit Changes:
- **Check the status of the repository:**
  ```bash
  git status
  ```
- **Add specific files to the staging area:**
  ```bash
  git add <file_name>
  ```
- **Add all changes to the staging area:**
  ```bash
  git add .
  ```
- **Commit staged changes:**
  ```bash
  git commit -m "Your commit message"
  ```

---

## 3. **Branching and Merging**
- **Create a new branch:**
  ```bash
  git branch <branch_name>
  ```
- **Switch to a branch:**
  ```bash
  git checkout <branch_name>
  ```
- **Create and switch to a new branch:**
  ```bash
  git checkout -b <branch_name>
  ```
- **Merge a branch into the current branch:**
  ```bash
  git merge <branch_name>
  ```
- **Delete a branch:**
  ```bash
  git branch -d <branch_name>
  ```

---

## 4. **Remote Repositories**
- **Add a remote repository:**
  ```bash
  git remote add origin <repository_url>
  ```
- **View remote repositories:**
  ```bash
  git remote -v
  ```
- **Push changes to a remote repository:**
  ```bash
  git push origin <branch_name>
  ```
- **Pull changes from a remote repository:**
  ```bash
  git pull origin <branch_name>
  ```
- **Fetch changes without merging:**
  ```bash
  git fetch origin
  ```

---

## 5. **Undoing Changes**
- **Unstage a file:**
  ```bash
  git restore --staged <file_name>
  ```
- **Discard changes in a file:**
  ```bash
  git restore <file_name>
  ```
- **Revert to a previous commit:**
  ```bash
  git revert <commit_hash>
  ```
- **Reset to a previous commit:**
  ```bash
  git reset --hard <commit_hash>
  ```

---

## 6. **Viewing History**
- **Show commit history:**
  ```bash
  git log
  ```
- **Show a summary of commits:**
  ```bash
  git log --oneline
  ```
- **View changes in the working directory:**
  ```bash
  git diff
  ```

---

## 7. **Stashing Changes**
- **Save changes temporarily:**
  ```bash
  git stash
  ```
- **List stashes:**
  ```bash
  git stash list
  ```
- **Apply the most recent stash:**
  ```bash
  git stash apply
  ```
- **Drop a stash:**
  ```bash
  git stash drop
  ```

---

## 8. **Collaboration Commands**
- **View all branches (local and remote):**
  ```bash
  git branch -a
  ```
- **Pull changes and rebase:**
  ```bash
  git pull --rebase origin <branch_name>
  ```
- **Resolve merge conflicts:**
  Resolve conflicts in your editor, then stage the resolved files and commit:
  ```bash
  git add <file_name>
  git commit -m "Resolved merge conflicts"
  ```

---

Keep this cheat sheet handy for quick reference while working with Git. Happy coding!
