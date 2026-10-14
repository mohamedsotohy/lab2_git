####################################################
repo link

---

https://github.com/mohamedsotohy/lab2_git/tree/main

#####################################################

git init
git remote add origin git@github.com:mohamedsotohy/lab2_git.git
git add .
git commit -m "first commit ever"
git push -u origin main

git switch -c dev
Switched to a new branch 'dev'
git status
On branch dev
Untracked files:
(use "git add <file>..." to include in what will be committed)
fileOne.txt

nothing added to commit but untracked files present (use "git add" to track)
git add .
git commit -m "fileOne commited"
[dev d3d3c26] fileOne commited
1 file changed, 0 insertions(+), 0 deletions(-)
create mode 100644 fileOne.txt
git switch main  
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
git switch -c test  
Switched to a new branch 'test'
git branch
dev
main

- test
  git add .
  git commit -m "fileTwo commited"

git push origin test

git push origin dev

git merge dev

git merge test

git branch -d dev
git branch -d test
git switch main
git push origin --delete test
git push origin --delete dev

git stash
git stash  
Saved working directory and index state WIP on main: 9d7815a Merge branch 'test'

git switch -c test
git switch main

git stash pop

git tag -a v1.4 -m "my version 1.4"  
 git tag  
v1.4
git log
commit 9d7815a0143a871bfe1cee6abd251fe6b3f12714 (HEAD -> main, tag: v1.4, origin/main) // i see the tag as a commit

git push origin v1.4
