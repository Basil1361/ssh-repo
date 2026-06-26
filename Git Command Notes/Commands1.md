## 1. Initialize Repo

```bash
git init
```

## 2. Track Untracked Files:
```bash
git add . is only for that current repo
git add -A is for all the files within the parent repo
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
git diff = before vs after
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