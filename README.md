# Git-GitHub

Official website Git
https://git-scm.com/
https://git-scm.com/downloads

Official website GitHub
https://github.com/

Git Commands
https://git-scm.com/docs

Official website VS Code
https://code.visualstudio.com/

Merges Strategies
https://git-scm.com/docs/merge-strategies

Advanced Merging
https://git-scm.com/book/en/v2/Git-Tools-Advanced-Merging#_advanced_merging

---

### **Git**

- Version Control System
- Manage Code History
- Track Changes

---

### **GitHub**

- Largest Development Platform
- Cloud Hosting & Collaboration Provider
- Git Repository Hosting

---

Absolute path: cd C:\Users\Desktop\GitHub
Relative path: cd \GitHub
Go to the root directory: cd /
Make new folder: mkdir GitHub
Make new file: echo our first file > test.txt
Check directory: dir / ls
Delete file: del test.txt
Delete directory: rmdir GitHub
Copy file: copy test.txt GitHub2
Move file: move test.txt GitHub2
Move folder: move GitHub2 main

cd - print current path
dir - list items
cls - clear command prompt
cd (..) - change directory
echo text > name (.type) - create file
mkdir foldername - create directory
del file - delete file
rmdir folder - delete folder
copy file - copy file
move file folder - move file or folder

https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/windows-commands
https://learn.microsoft.com/en-us/powershell/scripting/overview?view=powershell-7.3&viewFallbackFrom=powershell-7

---

commit = snapshot

---

.git (hidden)
GIT = Tracking changes - NOT storing files again and again!

---

Check installed Git vesion
git --version


> **Create empty Git repository**
-git init

> **Check working directory & staging area status**
git status

> **Add single file or all WD files to staging area**
git add .
git add fileName

> **Create new commit**
git commit -m "Message"

git config --global user.email "Name Name"

> **Display all commits of current branch**
git log

> **Checkout commit (detached head!)**
git checkout idCommit

> **Check the current branch**
git branch

> **Go to main branch**
```
git checkout main
```

> **Create new branch**
```
git branch new-branch
git switch new-branch
```

> **Create and access new branch**
```
git checkout -b new-branch
git switch -c new-branch
```

Bring other branch's changes to current branch
```
git merge new-branch
```

HEAD
git checkout idCommit
git branch





List data in staging area
git ls-files

git rm fileName.txt

git checkout fileName.txt
git checkout .

git restore fileName.txt
git clean -dn
git clean -df

git reset fileName.txt
git restore --staged fileName.txt


> ** Delete branch:**
git branch -D new-branch

git branch detached-head idBranch
git switch detached-branch


WD File*
git rm fileName
git add fileName

---

### Unstaged Changes

Revert changes in tracked files
git checkout (--) .
git restore fileName or .

Delete untracked files
git clean -df

---

### Staged Changes

Remove file(s) from staging area
git reset fileName &
git checkout -- fileName
git restore --staged fileName or .

---

Latest commits

Undo latest (~1) commit

git reset HEAD~1
git reset --soft HEAD~1
git reset --hard HEAD~1

---



Temporary storage for unstaged and uncommited changes
git stash

git stash apply 0, 1, 2
git stash push -m "message"
git stash pop 0
git drop 0
git stash list
git stash clear

---
A log of all project changes made including deleted commits
git reflog

---

Go to main branch
git merge --squash new-branch
git merge --no-ff new-branch   - recursive strategy

---

Change the base (i.e. the parent commit) of commits in another branch
git rebase

Go to new-branch
git rebase main

---
Combining commits from different branches by creating a new merge commit (recursive) or by moving the HEAD (fast-forward)
git merge

git merge --abort
git log --merge
git diff

---

Copy commit including the changes made only in this commit as HEAD to other branch
git cherry-pick

git cherry-pick idCommit

---

Check tags
git tag

git tag 1.0 idCommit
git show 1.0
git checkout 1.0

> **Delete tag**
git tag -d 1.0

git tag -a 2.0 -m "Message"
git show 2.0

---

git remote add origin URL

> **Rename branch to main**
```
git branch -M main
```

git push -u origin main

---

Create personal access token

Credential manager

---

git branch -a
git fetch origin
git pull origin main
git ls-remote

---

git branch --track new-branch

> **Show remote tracking branches**
git branch -r

> **Show detailed configuration**
git remote show origin

> **List local tracking branches and their remotes**
git branch -vv

> **Create local tracking branch**
git branch --track new-branch origin/new-branch


> **Delete remote branch**
git branch --delete --remotes origin/new-branch
git push origin --delete new-branch

git push --force origin main

