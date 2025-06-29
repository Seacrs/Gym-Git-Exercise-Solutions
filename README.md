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
freez@FREEZ MINGW64 ~/OneDrive/desktop/project (dev)
$ git branch ft/bundle-2

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (dev)
$ git checkout ft/bundle-2
Switched to branch 'ft/bundle-2'

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/bundle-2)
$ git status
On branch ft/bundle-2
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        services.html

nothing added to commit but untracked files present (use "git add" to track)

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/bundle-2)
$ git add services.html

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/bundle-2)
$ git commit -m "Third Commit"
[ft/bundle-2 6503696] Third Commit
 1 file changed, 11 insertions(+)
 create mode 100644 services.html

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/bundle-2)
$ git push origin ft/bundle-2
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 8 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 685 bytes | 685.00 KiB/s, done.
Total 5 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Seacrs/Project/pull/new/ft/bundle-2
remote:
To https://github.com/Seacrs/Project.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
```
### Exercise 2
```bash
freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/bundle-2)
$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (master)
$ git pull origin master
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (1/1), 892 bytes | 223.00 KiB/s, done.
From https://github.com/Seacrs/Project
 * branch            master     -> FETCH_HEAD
   e19958a..ffff51d  master     -> origin/master
Updating e19958a..ffff51d
Fast-forward
 about.html    | 11 +++++++++++
 home.html     | 11 +++++++++++
 services.html | 11 +++++++++++
 3 files changed, 33 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 services.html

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (master)
$ git branch ft/service-redesign

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (master)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/service-redesign)
$ git add .

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/service-redesign)
$ git commit -m "changes to services"
[ft/service-redesign 3df5767] changes to services
 1 file changed, 6 insertions(+)

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/service-redesign)
$ git push origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 390 bytes | 390.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/Seacrs/Project/pull/new/ft/service-redesign
remote:
To https://github.com/Seacrs/Project.git
 * [new branch]      ft/service-redesign -> ft/service-redesign

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/service-redesign)
$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (master)
$ git add .

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (master)
$ git commit -m "changes to services"
[master ae367e2] changes to services
 1 file changed, 6 insertions(+)

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (master)
$ git push origin master
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 377 bytes | 377.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Seacrs/Project.git
   ffff51d..ae367e2  master -> master

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (master)
$

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (master)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/service-redesign)
$ git diff main..ft/service-redesign
fatal: ambiguous argument 'main..ft/service-redesign': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/service-redesign)
$ git diff master..ft/service-redesign
diff --git a/services.html b/services.html
index c64314e..8067659 100644
--- a/services.html
+++ b/services.html
@@ -7,11 +7,11 @@
   </head>
   <body>
     <h1>Services</h1>
-    <p>We offer a range of activites</p>
-    <ol>
-      <p>Coding</p>
-      <p>Testing</p>
-      <p>Teaching</p>
-    </ol>
+    <p>Our Services</p>
+    <ul>
+      <li>Debugging</li>
+      <li>Penetration testing</li>
+      <li>Security training</li>
+    </ul>
   </body>
 </html>

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/service-redesign)
$ git merge master
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/service-redesign|MERGING)
$ git checkout master
services.html: needs merge
error: you need to resolve your current index first

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/service-redesign|MERGING)
$ git merge master
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/service-redesign|MERGING)
$ git add .

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/service-redesign|MERGING)
$ git merge master
fatal: You have not concluded your merge (MERGE_HEAD exists).
Please, commit your changes before you merge.

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/service-redesign|MERGING)
$ git commit -m "made changes to services"
[ft/service-redesign 76eea5e] made changes to services

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/service-redesign)
$ git merge master
Already up to date.

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/service-redesign)
$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (master)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/service-redesign)
$ git merge master
Already up to date.

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/service-redesign)
$ git push origin ft/service-redesign
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 364 bytes | 364.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Seacrs/Project.git
   3df5767..76eea5e  ft/service-redesign -> ft/service-redesign
```

## Bundle 3

### Exercise 1

```bash
freez@FREEZ MINGW64 ~/OneDrive/desktop/project (master)
$ git branch ft/team-page

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (master)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/team-page)
$ git add team.html

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/team-page)
$ git commit -m "new Team page"
[ft/team-page f8f6d51] new Team page
 1 file changed, 11 insertions(+)
 create mode 100644 team.html

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/team-page)
$ git push -u origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 440 bytes | 440.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/Seacrs/Project/pull/new/ft/team-page
remote:
To https://github.com/Seacrs/Project.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/team-page)
$ git checkou master
git: 'checkou' is not a git command. See 'git --help'.

The most similar command is
        checkout

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/team-page)
$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (master)
$ git branch ft/contact page
fatal: not a valid object name: 'page'

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (master)
$ git branch ft/contact-page

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (master)
$ git checkout ft-team-page
error: pathspec 'ft-team-page' did not match any file(s) known to git

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (master)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/team-page)
$ git log
commit f8f6d512d35c0521b916ef66fb0f63ff8123b7af (HEAD -> ft/team-page, origin/ft/team-page)
Author: Seacrs <shemachris072@gmail.com>
Date:   Sun Jun 29 11:43:04 2025 +0200

    new Team page

commit e518e1fb38f16dd3c298bb03c2a5242e09c29198 (origin/master, origin/HEAD, master, ft/contact-page)
Author: Seacrs <138714004+Seacrs@users.noreply.github.com>
Date:   Sat Jun 28 13:00:10 2025 +0200

    Update services.html

commit 52f08e781d0501f67a3ef130663769c79d7a386f
Merge: ae367e2 76eea5e
Author: Seacrs <138714004+Seacrs@users.noreply.github.com>
Date:   Sat Jun 28 12:51:27 2025 +0200

    Merge pull request #2 from Seacrs/ft/service-redesign

    Added Services

:
commit f8f6d512d35c0521b916ef66fb0f63ff8123b7af (HEAD -> ft/team-page, origin/ft/team-page)
Author: Seacrs <shemachris072@gmail.com>
Date:   Sun Jun 29 11:43:04 2025 +0200

    new Team page

commit e518e1fb38f16dd3c298bb03c2a5242e09c29198 (origin/master, origin/HEAD, master, ft/contact-page)
Author: Seacrs <138714004+Seacrs@users.noreply.github.com>
Date:   Sat Jun 28 13:00:10 2025 +0200

    Update services.html

commit 52f08e781d0501f67a3ef130663769c79d7a386f
Merge: ae367e2 76eea5e
Author: Seacrs <138714004+Seacrs@users.noreply.github.com>
Date:   Sat Jun 28 12:51:27 2025 +0200

    Merge pull request #2 from Seacrs/ft/service-redesign

    Added Services


freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/contact-page)
$ git cherry-pick f9f6d512d35c0521b916ef66fb0f63ff8123b7af
fatal: bad object f9f6d512d35c0521b916ef66fb0f63ff8123b7af

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/contact-page)
$ git cherry-pick f8f6d512d35c0521b916ef66fb0f63ff8123b7af
[ft/contact-page 6400b5b] new Team page
 Date: Sun Jun 29 11:43:04 2025 +0200
 1 file changed, 11 insertions(+)
 create mode 100644 team.html

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/contact-page)
$ git add contact.html

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/contact-page)
$ git commit -m "Added new contacts page"
[ft/contact-page ef1f934] Added new contacts page
 1 file changed, 11 insertions(+)
 create mode 100644 contact.html

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/contact-page)
$ git push -u origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 692 bytes | 692.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/Seacrs/Project/pull/new/ft/contact-page
remote:
To https://github.com/Seacrs/Project.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/contact-page)
$ git branch ft/faq-page

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/contact-page)
$ git checkout ft/faq-page
Switched to branch 'ft/faq-page'

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/faq-page)
$ git add faq.html

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/faq-page)
$ git commit -m "created new faq page"
[ft/faq-page 5cce326] created new faq page
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/faq-page)
$ git push -u origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 435 bytes | 435.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/Seacrs/Project/pull/new/ft/faq-page
remote:
To https://github.com/Seacrs/Project.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/faq-page)
$ git revert f8f6d512d35c0521b916ef66fb0f63ff8123b7af
[ft/faq-page a17656c] Revert "new Team page"
 1 file changed, 11 deletions(-)
 delete mode 100644 team.html

freez@FREEZ MINGW64 ~/OneDrive/desktop/project (ft/faq-page)
$ git push -u origin ft/faq-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 269 bytes | 269.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Seacrs/Project.git
   5cce326..a17656c  ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.
```

### Exercise 2
