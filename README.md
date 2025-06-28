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
### Exercise 2
```bash
freez@FREEZ MINGW64 ~/OneDrive/desktop/project (dev)
$ git stash list

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (dev)
$ git add home.html

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (dev)
$ git stash
Saved working directory and index state WIP on dev: 8265cea empty

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (dev)
$ git add about.html

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (dev)
$ git stash
Saved working directory and index state WIP on dev: 8265cea empty

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (dev)
$ git add team.html

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (dev)
$ git stash
Saved working directory and index state WIP on dev: 8265cea empty

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (dev)
$ git stash list
stash@{0}: WIP on dev: 8265cea empty
stash@{1}: WIP on dev: 8265cea empty
stash@{2}: WIP on dev: 8265cea empty

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (dev)
$ git stash pop stash@{2}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

Dropped stash@{2} (4598f5c25e723d187fa12cf3c1c0653ad731421a)

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (dev)
$ git stash
Saved working directory and index state WIP on dev: 8265cea empty

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (dev)
$ git stash list
stash@{0}: WIP on dev: 8265cea empty
stash@{1}: WIP on dev: 8265cea empty
stash@{2}: WIP on dev: 8265cea empty

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (dev)
$ git stash pop stash@{2}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{2} (369a7eb874ea9376e8eddc9947a701ace4ab5d43)

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (dev)
$ git stash pop stash@{0}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{0} (9b6e9dc5c752f895b5bd6c0354bb385cd0a32262)

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (dev)
$ git commit -m "Second Commit"
[dev 88521dd] Second Commit
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (dev)
$ git stash list
stash@{0}: WIP on dev: 8265cea empty

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (dev)
$ git stash pop stash@{0}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (1525ba4be08ab7b5cfded9182921294030b8f05c)

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (dev)
$ git reset --hard
HEAD is now at 88521dd Second Commit

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (dev)
$ git push u origin dev
error: src refspec origin does not match any
error: failed to push some refs to 'u'

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (dev)
$ git push -u origin dev
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 789 bytes | 789.00 KiB/s, done.
Total 6 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/Seacrs/Project.git
   de68793..88521dd  dev -> dev
branch 'dev' set up to track 'origin/dev'.
```
## Bundle 2

### Exercise 1
```bash
```
