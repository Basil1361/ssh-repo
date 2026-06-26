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


## Additional Notes:
```bash
HEAD is the pointer that indicates your current position in the project history

```