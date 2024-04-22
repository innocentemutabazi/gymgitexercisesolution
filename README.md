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
