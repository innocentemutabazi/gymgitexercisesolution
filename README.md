# BUNDLE 1
## Exercise 1

```
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git init
Initialized empty Git repository in /home/thegym/Desktop/GIT-EXERCISES/.git/
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git config --global init.defaultBranch main
thegym@thegym-Precision-5530:~/D
thegym@thegym-Precision-5530:~/Desktop
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        browserfile.html
        main.js
        styles.css

nothing added to commit but untracked files present (use "git add" to track)
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git add .
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git commit -m 'made minor changes like adding files and rename'
[main (root-commit) 1ce3e8d] made minor changes like adding files and rename
 3 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 browserfile.html
 create mode 100644 main.js
 create mode 100644 styles.css
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git remote add origin https://github.com/innocentemutabazi/git-exercises.git
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git remote -v
origin  https://github.com/innocentemutabazi/git-exercises.git (fetch)
origin  https://github.com/innocentemutabazi/git-exercises.git (push)
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git push --set-upstream origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 265 bytes | 265.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/innocentemutabazi/git-exercises.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git branch dev
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git switch -c dev
fatal: A branch named 'dev' already exists.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git branch
  dev
* main
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git switch dev
Switched to branch 'dev'
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git switch -c test
Switched to a new branch 'test'
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git switch dev
Switched to branch 'dev'
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git branch
* dev
  main
  test
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git branch -d test
Deleted branch test (was 1ce3e8d).
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git branch
* dev
  main
```
## Exercise 2
```
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git DD 
git: 'DD' is not a git command. See 'git --help'.

The most similar commands are
        am
        gc
        mv
        mw
        rm
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git add .
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git stash
Saved working directory and index state WIP on dev: 1ce3e8d made minor changes like adding files and rename
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git stash list
stash@{0}: WIP on dev: 1ce3e8d made minor changes like adding files and rename
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git status
On branch dev
nothing to commit, working tree clean
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git add about.html
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git stash
Saved working directory and index state WIP on dev: 1ce3e8d made minor changes like adding files and rename
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git stash
No local changes to save
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git stash list
stash@{0}: WIP on dev: 1ce3e8d made minor changes like adding files and rename
stash@{1}: WIP on dev: 1ce3e8d made minor changes like adding files and rename
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git add team.html
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git stash
Saved working directory and index state WIP on dev: 1ce3e8d made minor changes like adding files and rename
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git stash list
stash@{0}: WIP on dev: 1ce3e8d made minor changes like adding files and rename
stash@{1}: WIP on dev: 1ce3e8d made minor changes like adding files and rename
stash@{2}: WIP on dev: 1ce3e8d made minor changes like adding files and rename
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git stash pop stash@{1} 
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (cc2eb898091135a5c803a2777591404534c3de02)
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git stash list
stash@{0}: WIP on dev: 1ce3e8d made minor changes like adding files and rename
stash@{1}: WIP on dev: 1ce3e8d made minor changes like adding files and rename
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (19651f5c5ccccd00f35017c5edd13f7d524e72ed)
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git commit -m 'Completed the second exercise BUNDLE 1'
[dev 7e9ec1d] Completed the second exercise BUNDLE 1
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git stash list
stash@{0}: WIP on dev: 1ce3e8d made minor changes like adding files and rename
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git stash pop stash@{0}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (154f9f01a81819c178ddd1133890c1664cbd63c6)
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git reset --hard
HEAD is now at 7e9ec1d Completed the second exercise BUNDLE 1
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git status
On branch dev
nothing to commit, working tree clean
```
# BUNDLE 2
## Exercise 1

```
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git switch -c ft/bundle-2 
Switched to a new branch 'ft/bundle-2'
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git add .
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git commit -commit 'Exercise 1 of Bundle 2'
fatal: could not lookup commit ommit
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git -commit 'Exercise 1 of Bundle 
> 
> '
unknown option: -commit
usage: git [--version] [--help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           [--super-prefix=<path>] [--config-env=<name>=<envvar>]
           <command> [<args>]
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git -commit 'Exercise 1 of Bundle'
unknown option: -commit
usage: git [--version] [--help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           [--super-prefix=<path>] [--config-env=<name>=<envvar>]
           <command> [<args>]
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git -commit "Exercise 1 of Bundle"
unknown option: -commit
usage: git [--version] [--help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           [--super-prefix=<path>] [--config-env=<name>=<envvar>]
           <command> [<args>]
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git commit -m "Exercise 1 of Bundle"
[ft/bundle-2 c66d080] Exercise 1 of Bundle
 1 file changed, 11 insertions(+)
 create mode 100644 services.html
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$     git push --set-upstream origin ft/bundle-2
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 12 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (7/7), 832 bytes | 416.00 KiB/s, done.
Total 7 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), done.
remote: 
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/innocentemutabazi/git-exercises/pull/new/ft/bundle-2
remote: 
To https://github.com/innocentemutabazi/git-exercises.git



 * [new branch]      ft/bundle-2 -> ft/bundle-2
Branch 'ft/bundle-2' set up to track remote branch 'ft/bundle-2' from 'origin'.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$
```
![Screenshot from 2024-04-22 14-29-02](https://github.com/innocentemutabazi/gymgitexercisesolution/assets/159420918/06e9c217-45e1-4b25-9974-d07c531f8e07)

## Exercise 2
```
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git checkout
Your branch is up to date with 'origin/ft/bundle-2'.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git pull
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 907 bytes | 907.00 KiB/s, done.
From https://github.com/innocentemutabazi/git-exercises
   1ce3e8d..cc07f40  main       -> origin/main
Updating 1ce3e8d..cc07f40
Fast-forward
 about.html    | 11 +++++++++++
 home.html     | 11 +++++++++++
 services.html | 11 +++++++++++
 3 files changed, 33 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 services.html
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git switch -c ft/service-redesign
Switched to a new branch 'ft/service-redesign'
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git add .
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git commit -m 'New changes on the service.html page'
[ft/service-redesign 6286f4b] New changes on the service.html page
 1 file changed, 2 insertions(+)
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$     git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 353 bytes | 353.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: 
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/innocentemutabazi/git-exercises/pull/new/ft/service-redesign
remote: 
To https://github.com/innocentemutabazi/git-exercises.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
Branch 'ft/service-redesign' set up to track remote branch 'ft/service-redesign' from 'origin'.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git add .
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git commit -m 'updated the service file'
[main 508baeb] updated the service file
 1 file changed, 3 insertions(+), 1 deletion(-)
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 403 bytes | 403.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/innocentemutabazi/git-exercises.git
   cc07f40..508baeb  main -> main
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git add .
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git push
Everything up-to-date
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git commit -m 'updated the service file'
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git pull origin ft/service-redesign 
From https://github.com/innocentemutabazi/git-exercises
 * branch            ft/service-redesign -> FETCH_HEAD
hint: You have divergent branches and need to specify how to reconcile them.
hint: You can do so by running one of the following commands sometime before
hint: your next pull:
hint: 
hint:   git config pull.rebase false  # merge (the default strategy)
hint:   git config pull.rebase true   # rebase
hint:   git config pull.ff only       # fast-forward only
hint: 
hint: You can replace "git config" with "git config --global" to set a default
hint: preference for all repositories. You can also pass --rebase, --no-rebase,
hint: or --ff-only on the command line to override the configured default per
hint: invocation.
fatal: Need to specify how to reconcile divergent branches.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git pull
Already up to date.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git git status
git: 'git' is not a git command. See 'git --help'.

The most similar command is
        init
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git merge ft/service-redesign 
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git diff
diff --cc services.html
index a85adbf,7a716b4..0000000
--- a/services.html
+++ b/services.html
@@@ -6,8 -6,8 +6,14 @@@
      <title>Document</title>
  </head>
  <body>
++<<<<<<< HEAD
 +    <h1>SERVICE PAGE of the website</h1>
 +    <p>This is the service page of our website</p>
 +    <h2>Find Below a List of the services we provide</h2>
++=======
+     <h1>SERVICE PAGE</h1>
+     <p>This is the service page</p>
+     <p>This is the service page</p>
++>>>>>>> ft/service-redesign
  </body>
  </html>
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git add .
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git commit -m 'Resolved conflicts'
[main 335d6f1] Resolved conflicts
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git push
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 220 bytes | 220.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/innocentemutabazi/git-exercises.git
   508baeb..335d6f1  main -> main
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$
```
# BUNDLE 3
## Exercise 1
```
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git switch -c ft/team-page
Switched to a new branch 'ft/team-page'
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git add .
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git commit -m 'Created a team page'
[ft/team-page 970b806] Created a team page
 1 file changed, 11 insertions(+)
 create mode 100644 team.html
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git push
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$     git push --set-upstream origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 424 bytes | 424.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/innocentemutabazi/git-exercises/pull/new/ft/team-page
remote: 
To https://github.com/innocentemutabazi/git-exercises.git
 * [new branch]      ft/team-page -> ft/team-page
Branch 'ft/team-page' set up to track remote branch 'ft/team-page' from 'origin'.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git checkout
Your branch is up to date with 'origin/main'.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git switch main
Already on 'main'
Your branch is up to date with 'origin/main'.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git switch -c ft/contact-page
Switched to a new branch 'ft/contact-page'
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git switch ft/team-page 
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git log 
commit 970b806589aace00072832af4667a4b720c2cc37 (HEAD -> ft/team-page, origin/ft/team-page)
Author: innocentemutabazi <innocentemutabazi@gmail.com>
Date:   Mon Apr 22 15:38:54 2024 +0200

    Created a team page

commit 335d6f13fe9a388c42860f6da4528576832f563a (origin/main, main, ft/contact-page)
Merge: 508baeb 6286f4b
Author: innocentemutabazi <innocentemutabazi@gmail.com>
Date:   Mon Apr 22 15:21:42 2024 +0200

    Resolved conflicts

commit 508baeb2b906a70aded2b6b06c8eb048e3fe0340
Author: innocentemutabazi <innocentemutabazi@gmail.com>
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git switch ft/contact-page 
Switched to branch 'ft/contact-page'
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git cherry-pick 970b806589aace00072832af4667a4b720c2cc37
[ft/contact-page 8f23fc5] Created a team page
 Date: Mon Apr 22 15:38:54 2024 +0200
 1 file changed, 11 insertions(+)
 create mode 100644 team.html
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git add .
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git commit -m 'Added changes to contact page'
[ft/contact-page 9b833e3] Added changes to contact page
 1 file changed, 11 insertions(+)
 create mode 100644 contact.html
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git push
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/contact-page

thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$     git push --set-upstream origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 694 bytes | 347.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/innocentemutabazi/git-exercises/pull/new/ft/contact-page
remote: 
To https://github.com/innocentemutabazi/git-exercises.git
 * [new branch]      ft/contact-page -> ft/contact-page
Branch 'ft/contact-page' set up to track remote branch 'ft/contact-page' from 'origin'.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git switch ft/contact-page
Already on 'ft/contact-page'
Your branch is up to date with 'origin/ft/contact-page'.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git switch -c ft/faq-page
Switched to a new branch 'ft/faq-page'
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git add .
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git commit -m 'added a faq page'
[ft/faq-page 4e8bdb9] added a faq page
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git push
fatal: The current branch ft/faq-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/faq-page

thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$     git push --set-upstream origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 438 bytes | 438.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/innocentemutabazi/git-exercises/pull/new/ft/faq-page
remote: 
To https://github.com/innocentemutabazi/git-exercises.git
 * [new branch]      ft/faq-page -> ft/faq-page
Branch 'ft/faq-page' set up to track remote branch 'ft/faq-page' from 'origin'.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git push
Everything up-to-date
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git log
commit 4e8bdb921d4305dfaa21fc830bd85dc768a565fb (HEAD -> ft/faq-page, origin/ft/faq-page)
Author: innocentemutabazi <innocentemutabazi@gmail.com>
Date:   Mon Apr 22 16:03:09 2024 +0200

    added a faq page

commit 9b833e3c8ef36cc71311f883e060f85bce8bea9c (origin/ft/contact-page, ft/contact-page)
Author: innocentemutabazi <innocentemutabazi@gmail.com>
Date:   Mon Apr 22 15:58:25 2024 +0200

    Added changes to contact page

commit 8f23fc504eee2d1d75d307a5acdab450ba889273
Author: innocentemutabazi <innocentemutabazi@gmail.com>
Date:   Mon Apr 22 15:38:54 2024 +0200

    Created a team page

commit 335d6f13fe9a388c42860f6da4528576832f563a (origin/main, main)
Merge: 508baeb 6286f4b
Author: innocentemutabazi <innocentemutabazi@gmail.com>
Date:   Mon Apr 22 15:21:42 2024 +0200

    Resolved conflicts

commit 508baeb2b906a70aded2b6b06c8eb048e3fe0340
Author: innocentemutabazi <innocentemutabazi@gmail.com>
Date:   Mon Apr 22 15:03:33 2024 +0200

    updated the service file

commit 6286f4bfd56472e498c2a1b7cfc760e8dfa43b2f (origin/ft/service-redesign, ft/service-redes
ign)
Author: innocentemutabazi <innocentemutabazi@gmail.com>
Date:   Mon Apr 22 14:40:25 2024 +0200

    New changes on the service.html page

commit cc07f40d571769c84f0f5a9458d6d2f1212a8552
Merge: 1ce3e8d c66d080
Author: Ivy-Murage <108492757+IvyMurage@users.noreply.github.com>
Date:   Mon Apr 22 14:25:48 2024 +0200

    Merge pull request #1 from innocentemutabazi/ft/bundle-2
    
    Ft/bundle 2

commit c66d080da9328e9120db339f0639960e09dd2b26 (origin/ft/bundle-2, ft/bundle-2)
Author: innocentemutabazi <innocentemutabazi@gmail.com>
:...skipping...
:...skipping...
:...skipping...
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git switch ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git log
commit 970b806589aace00072832af4667a4b720c2cc37 (HEAD -> ft/team-page, origin/ft/team-page)
Author: innocentemutabazi <innocentemutabazi@gmail.com>
Date:   Mon Apr 22 15:38:54 2024 +0200

    Created a team page

commit 335d6f13fe9a388c42860f6da4528576832f563a (origin/main, main)
Merge: 508baeb 6286f4b
Author: innocentemutabazi <innocentemutabazi@gmail.com>
Date:   Mon Apr 22 15:21:42 2024 +0200

    Resolved conflicts

commit 508baeb2b906a70aded2b6b06c8eb048e3fe0340
Author: innocentemutabazi <innocentemutabazi@gmail.com>
Date:   Mon Apr 22 15:03:33 2024 +0200

    updated the service file

commit 6286f4bfd56472e498c2a1b7cfc760e8dfa43b2f (origin/ft/service-redesign, ft/service-redesign)
Author: innocentemutabazi <innocentemutabazi@gmail.com>
Date:   Mon Apr 22 14:40:25 2024 +0200

    New changes on the service.html page

commit cc07f40d571769c84f0f5a9458d6d2f1212a8552
Merge: 1ce3e8d c66d080
Author: Ivy-Murage <108492757+IvyMurage@users.noreply.github.com>
Date:   Mon Apr 22 14:25:48 2024 +0200

    Merge pull request #1 from innocentemutabazi/ft/bundle-2
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git switch ft/faq-page
Switched to branch 'ft/faq-page'
Your branch is up to date with 'origin/ft/faq-page'.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git revert 970b806589aace00072832af4667a4b720c2cc37
[ft/faq-page 66985af] Revert "Created a team page"
 1 file changed, 11 deletions(-)
 delete mode 100644 team.html
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git status
On branch ft/faq-page
Your branch is ahead of 'origin/ft/faq-page' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 277 bytes | 277.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/innocentemutabazi/git-exercises.git
   4e8bdb9..66985af  ft/faq-page -> ft/faq-page
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$
```
## Exercise 2
```
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git switch ft/faq-page
Already on 'ft/faq-page'
Your branch is up to date with 'origin/ft/faq-page'.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git switch -c ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git add .
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git commit -m 'Made some changes on the home page'
[main 6e16e43] Made some changes on the home page
 1 file changed, 1 insertion(+)
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 345 bytes | 345.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/innocentemutabazi/git-exercises.git
   335d6f1..6e16e43  main -> main
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git switch ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git add .
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git add .
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git commit -m 'made changes'
[ft/home-page-redesign 2409e3e] made changes
 1 file changed, 1 insertion(+)
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git push
fatal: The current branch ft/home-page-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/home-page-redesign

thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$     git push --set-upstream origin ft/home-page-redesign
Enumerating objects: 16, done.
Counting objects: 100% (16/16), done.
Delta compression using up to 12 threads
Compressing objects: 100% (14/14), done.
Writing objects: 100% (14/14), 1.44 KiB | 295.00 KiB/s, done.
Total 14 (delta 8), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (8/8), completed with 2 local objects.
remote: 
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/innocentemutabazi/git-exercises/pull/new/ft/home-page-redesign
remote: 
To https://github.com/innocentemutabazi/git-exercises.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
Branch 'ft/home-page-redesign' set up to track remote branch 'ft/home-page-redesign' from 'origin'.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$
```
# BUNDLE 4
## Exercise
```
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git main checkout
git: 'main' is not a git command. See 'git --help'.

The most similar command is
        mailinfo
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git remote add git-copy https://github.com/innocentemutabazi/gitexercise2.git
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git add .
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git commit -m 'made few changes on the homepage'
[main fd58a6d] made few changes on the homepage
 1 file changed, 2 insertions(+)
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 343 bytes | 343.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/innocentemutabazi/git-exercises.git
   6e16e43..fd58a6d  main -> main
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git add .
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git commit -m 'made few changes on the homepage'
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$ git push -u git-copy main
Enumerating objects: 24, done.
Counting objects: 100% (24/24), done.
Delta compression using up to 12 threads
Compressing objects: 100% (23/23), done.
Writing objects: 100% (24/24), 3.17 KiB | 360.00 KiB/s, done.
Total 24 (delta 13), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (13/13), done.
To https://github.com/innocentemutabazi/gitexercise2.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'git-copy'.
thegym@thegym-Precision-5530:~/Desktop/GIT-EXERCISES$`
```
