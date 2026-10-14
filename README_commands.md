# Git Lab 2

## 📎 Repo Link

https://github.com/mohamedsotohy/lab2_git/tree/main

---

## 📑 Table of Contents

1. [Initialize & First Push](#1-initialize--first-push)
2. [Create the `dev` Branch](#2-create-the-dev-branch)
3. [Create the `test` Branch](#3-create-the-test-branch)
4. [Push Branches](#4-push-branches)
5. [Merge Branches](#5-merge-branches)
6. [Delete Branches](#6-delete-branches)
7. [Stash](#7-stash)
8. [Tags](#8-tags)

---

## 1. Initialize & First Push

```bash
git init

git remote add origin git@github.com:mohamedsotohy/lab2_git.git

git add .
git commit -m "first commit ever"

git push -u origin main
```

---

## 2. Create the `dev` Branch

```bash
git switch -c dev
```

```text
Switched to a new branch 'dev'
```

```bash
git status
```

```text
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        fileOne.txt

nothing added to commit but untracked files present (use "git add" to track)
```

```bash
git add .
git commit -m "fileOne commited"
```

```text
[dev d3d3c26] fileOne commited
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 fileOne.txt
```

```bash
git switch main
```

```text
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
```

---

## 3. Create the `test` Branch

```bash
git switch -c test
```

```text
Switched to a new branch 'test'
```

```bash
git branch
```

```text
  dev
  main
* test
```

```bash
git add .
git commit -m "fileTwo commited"
```

---

## 4. Push Branches

```bash
git push origin test

git push origin dev
```

---

## 5. Merge Branches

```bash
git merge dev

git merge test
```

---

## 6. Delete Branches

```bash
git branch -d dev
git branch -d test
git switch main
git push origin --delete test
git push origin --delete dev
```

---

## 7. Stash

```bash
git stash
```

```text
Saved working directory and index state WIP on main: 9d7815a Merge branch 'test'
```

```bash
git switch -c test
git switch main


git stash pop
```

---

## 8. Tags

```bash
git tag -a v1.4 -m "my version 1.4"
git tag
```

```text
v1.4
```

```bash
git log
```

```text
commit 9d7815a0143a871bfe1cee6abd251fe6b3f12714 (HEAD -> main, tag: v1.4, origin/main)  // i see the tag as a commit
```

```bash
git push origin v1.4
```
