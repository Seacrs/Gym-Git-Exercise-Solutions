# Gym-Git-Exercise-Solutions

## Bundle 1

### Exercise 1

```bash
freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (main)
$ git init
Initialized empty Git repository in C:/Users/freez/OneDrive/Desktop/Project/.git/

freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (main)
$ git branch -m main master

freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (master)
$ git add .

freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (master)
$ git commit -m "First Commit"
[master (root-commit) de68793] First Commit
 3 files changed, 42 insertions(+)
 create mode 100644 Git.txt
 create mode 100644 index.html
 create mode 100644 style.css

freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (master)
$ git status
On branch master
nothing to commit, working tree clean

freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (master)
$ git remote add origin https://github.com/Seacrs/Project.git
bash: $'\026git': command not found

freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (master)
$ git remote add origin https://github.com/Seacrs/Project.git

freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (master)
$ git branch -M master

freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (master)
$ git push -u origin master
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (5/5), 719 bytes | 719.00 KiB/s, done.
Total 5 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Seacrs/Project.git
 * [new branch]      master -> master
branch 'master' set up to track 'origin/master'.

freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (master)
$ git branch dev

freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (master)
$ git checkout dev
Switched to branch 'dev'

freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (dev)
$ git branch test

freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (dev)
$ git branch
* dev
  master
  test

freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (dev)
$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (master)
$ git branch
  dev
* master
  test

freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (master)
$ git checkout branch
error: pathspec 'branch' did not match any file(s) known to git

freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (master)
$ git checkout dev
Switched to branch 'dev'

freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (dev)
$ git branch -d test
Deleted branch test (was de68793).

freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (dev)
$ git push origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Seacrs/Project/pull/new/dev
remote:
To https://github.com/Seacrs/Project.git
 * [new branch]      dev -> dev

freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (dev)
$ git status
On branch dev
nothing to commit, working tree clean

freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (dev)
$ git checkout main
error: pathspec 'main' did not match any file(s) known to git

freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (dev)
$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (master)
$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean

freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (master)
$ git add .

freez@FREEZ MINGW64 ~/OneDrive/desktop/Project (master)
$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
```
