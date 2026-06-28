## Prereq:


## 1. Initialize Repo

```bash
git init
```

## 2. Track Untracked Files:
```bash
git add . = add files whose names begin with a dot in that current repo
git add -A = for all the files within the parent repo
git add * = means add all files in the current directory, except for files whose name begin with a dot.
```

## 3. Commiting Files:
```bash
git commit = commiting the files
git commit --amend --no-edit = Fast edit without committing
-m = message
-am = all of the files, with a message 
```

## 4. File Status:
```bash
git status = checking status of each files
git log --oneline = check audits, simplified in one line
git log --graph - Show a visual diagram, useful for diverging paths.
git diff = Differences between the working directory and the staging area.
# Changing the colour of the changes
git config --global color.diff.old yellow
git config --global color.diff.new blue

# 
git diff --staged = Differences between staging area and previous commit.
git diff HEAD~1 = Differences between current commit and previous commit.
```

## 5. Changing File Stuff:
```bash
mv = rename
rm = remove Local File
git rm = Deletes Local File and remove git tracking
git rm --cached  = delete local file but removes from Git Tracking
touch = create new file
touch "File Name"/.git-keep = Keep Track of Empty File
code = open/create new file without save
```

## 6. Recovering File (if deleted a file):
1. If Git still has the file 
```bash
git checkout -- "file-name"
```

2. If Git doesnt have the file (git rm)
```bash
git reset HEAD "file-name"
git checkout -- "file-name"
```

3. If removed, then already committed
```bash
git reset --hard HEAD^
git checkout -- "file-name"
```

## 7. Reverting back to the previous commits:
```bash
git revert --no-edit HEAD = undo changes
git checkout "specific hash" . = specific hashes
# hash is obtained from git log
```

## 8. Checking Versions and help
```bash
git --version
git --help
```

## 9. Setting identity:
```bash
git config --global user.name "First Last"
git config --global user.email "me@example.com"
git config --global --list
```
## 10. Branch:
```bash
git branch — Lists all local branches in your repository.git branch 
-r — Displays only remote tracking branches.git branch 
-a — Shows both local and remote branches combined.git branch 
-v — Lists branches along with their latest commit 

git branch <branch-name> — Creates a new branch without switching to it.git checkout
-b <branch-name> — Creates a new branch and immediately switches to it.git switch 
-c <branch-name> — The modern Git syntax to create and switch to a branch.

git merge <branch-name> — Combines history from the specified branch into your current branch.git merge 
--abort — Cancels an in-progress merge if conflict resolution gets too messy.
git rebase <branch-name> — Applies your current branch commits on top of the specified branch's latest commit for a cleaner linear history.
```

``` bash
git push origin <branch-name> = Pushes a newly created local branch to your remote repository.
git push -u origin <branch-name> — Pushes the branch and links it as an upstream tracking branch.
git push origin --delete <branch-name> — Deletes the branch from your remote repository.
```

## 11. Instantly without commit message
``` bash
git commit --amend --no-edit
```

## 12. Check stage phase
``` bash
git ls -files --stage
```

## 13. Add things in a file
``` bash
echo "node_modules/" >> .gitignore = append a thing to a file
```

## Additional Notes:
```bash
HEAD is the pointer that indicates your current position in the project history
```
__________________________________________________________________________
# Github:
## Create new Repo on Command line:
```bash
git init
git add .
git commit -m "Message"
git remote add origin "..."
git push -u origin master
```
## Push existing Repository
```bash
git remote add origin "..."
git push -u origin master

```