Step 1

# VCS Task – Git & GitHub Hands-on

This repository contains the solution for the VCS Task. All scripts, branches, and Git operations have been completed using **Git Bash / Shell**. Screenshots of each step are included.

---

## **Step 1 – Create Folder & Scripts**
```bash
mkdir vcs-task
cd vcs-task
echo "echo Hello from script1" > script1.sh
echo "echo Hello from script2" > script2.sh
ls

Step 2 – Initialize Git & Commit

git init
git add .
git commit -m "Initial commit with script files"
git status

Step 3 – Create GitHub Repo & Push

git remote add origin https://github.com/YOUR_USERNAME/vcs-task.git
git branch -M main
git push -u origin main

Step 4 – Create & Merge Branch

git checkout -b feature-branch
echo "echo Feature branch code" >> script1.sh
git add script1.sh
git commit -m "Added feature branch changes"

Step 5 – Rebase

git checkout -b rebase-branch
echo "echo Rebase branch changes" >> script2.sh
git add script2.sh
git commit -m "Updated script2 in rebase branch"

git checkout main
echo "echo Change from main branch" >> script2.sh
git add script2.sh
git commit -m "Main branch update"

git checkout rebase-branch
git rebase main


Step 6 – Stash

echo "Temporary change" >> script1.sh
git stash
git stash list
git stash apply

Step 7 – Push All Branches

git checkout main
git push origin main
git push origin feature-branch
git push origin rebase-branch



git checkout main
git merge feature-branch
