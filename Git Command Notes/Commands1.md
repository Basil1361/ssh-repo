## Prereq:
```bash
HEAD is the pointer that indicates your current position in the project history
Working Directory: Your project files where you are making changes.
Staging Area (Index): A preparation area for grouping changes you want to save to history.
Repository: The permanent records of your project's development history.
```

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
rm = remove
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

## 10. Branches:
### We use branches to
"Prevent a messy history"
"Avoid non-working versions in the history from incomplete work"
"Work on multiple features/fixes at the same time"

1. Main Branch: Usually the trusted working version, and the first branch. (historically called master)
2. Feature Branch: A safe isolated space to develop without affecting the trusted version.
3. Merging: Combining changes from different branches.


- Fast-forward merge: Move the new commits from the child branch onto the parent branch.
- Merge commit: Apply the changes as a single new commit on the parent branch. Leave the child branch in the network for traceability.
- Squash merge: Collapse the commits from one branch into a single new commit on the other branch.

```bash
git branch "my-new-feature" = Start a branch from the current branch.
git checkout "my-new-feature" - Change your working directory to a different version from the repository history.
git merge - Apply the commits from one branch onto another branch. (Default: Fast forward merge)
git switch 
```


