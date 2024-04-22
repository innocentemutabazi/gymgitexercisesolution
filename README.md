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
nothing to commit, working tree clean```
