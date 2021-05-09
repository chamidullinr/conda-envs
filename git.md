# GIT

This section contains list of useful `git` commands.

## Overview
View changes made in the current branch:
```bash
git status
```

View changes made in the file:
```bash
git diff FILE-NAME
```

Undo changes made in the file:
```bash
git checkout -- FILE-NAME
```

View commit history in one line view:
```bash
git log --pretty=oneline
```

## Merge and Rebase

Merge `feature` branch into `master`:
```bash
git checkout master
git merge feature 
```

Rebase `feature` branch into `master`:
```bash
git checkout feature
git rebase master

git checkout master
git merge feature
```

Rebase and pull:
```bash
git pull --rebase
```

## Stash

Stash changes:
```bash
git stash save "optional message"
```

View stashed changes:
```bash
git stash list
```

Unstash changes and keep stash:
```bash
git stash apply STASH-NAME
```

Unstash changes and remove stash:
```bash
git stash pop STASH-NAME
```

Remove stash:
```bash
git stash drop STASH-NAME
```