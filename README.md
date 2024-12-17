This is a file created locally and it will be used for a series of exercises. The following is what is done:
1. Bundle 1-Exercise 1
- Create a project and initialize git
- Files and contents added to make changes to the project
- Renaming the main branch from master to main(or vice versa if the branch name is main then it should be changed to master)
    `git branch -M main //this is used to change the  branch name from master to main or vice versa based on the branch you've by default`
- Stage the changes and commit them
    `git add . //to stage the changes`
    `git commit -m "<your-message>" //to commit your changes`
- Creation of a GitHub repo and connect it with the project
    `git remote add origin <link-of-the-repo>`
- Push the changes to GitHub
    `git push //to push your changes to the GitHub repo`
- Create a new branch name dev
    `git checkout -b <branch-name>`
- From dev create another branch test
- Go back to the dev branch and delete the test branch
`git checkout <branch-name>`
`git branch -D <branch-name> //to delete the branch`
`git push origin --delete <branch-name> //pushes the changes and deletes the branch on the repo`

Solution:
``` bash
LENOVO@DESKTOP-533N1K0 MINGW64 ~/Desktop (master)
$ mkdir Git-Exercise

LENOVO@DESKTOP-533N1K0 MINGW64 ~/Desktop (master)
$ cd Git-Exercise/

LENOVO@DESKTOP-533N1K0 MINGW64 ~/Desktop/Git-Exercise (master)
$ git init
Initialized empty Git repository in C:/Users/LENOVO/Desktop/Git-Exercise/.git/

LENOVO@DESKTOP-533N1K0 MINGW64 ~/Desktop/Git-Exercise (master)
$ code .

jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git branch -M main
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git remote add origin https://github.com/sjamillah/git-exercise.git
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)       
        README.md

nothing added to commit but untracked files present (use "git add" to track)
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git 
add .
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git 
commit -m "learning the basics of GitHub"
[main (root-commit) e1e6738] learning the basics of GitHub
 1 file changed, 12 insertions(+)
 create mode 100644 README.md
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git 
push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git 
push --set-upstream origin main^C
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main
To https://github.com/sjamillah/git-exercise.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/sjamillah/git-exercise.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git pull
error: cannot pull with rebase: You have unstaged changes.
error: please commit or stash them.
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git pull
There is no tracking information for the current branch.
Please specify which branch you want to rebase against.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> main

jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git pull main
fatal: 'main' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ ls
README.md
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git pull
There is no tracking information for the current branch.
Please specify which branch you want to rebase against.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> main

jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git 
remote add origin https://github.com/sjamillah/git-exercise.git
error: remote origin already exists.
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git remote add origin https://github.com/sjamillah/git-exercises.git       
error: remote origin already exists.
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git 
add .
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git 
commit -m "git basics exercises"
On branch main
nothing to commit, working tree clean
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git 
pull
There is no tracking information for the current branch.
Please specify which branch you want to rebase against.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> main

jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git 
pull origin main
fatal: couldn't find remote ref main
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git 
pull main
fatal: 'main' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git 
push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git 
push --set-upstream origin main
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (6/6), 904 bytes | 53.00 KiB/s, done.
Total 6 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
remote: This repository moved. Please use the new location:
remote:   https://github.com/sjamillah/git-exercises.git
To https://github.com/sjamillah/git-exercise.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git 
checkout -b dev
Switched to a new branch 'dev'
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git 
push origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: This repository moved. Please use the new location:
remote:   https://github.com/sjamillah/git-exercises.git
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/sjamillah/git-exercises/pull/new/dev   
remote:
To https://github.com/sjamillah/git-exercise.git
 * [new branch]      dev -> dev
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git 
checkout -b test
Switched to a new branch 'test'
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git 
push origin test
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: This repository moved. Please use the new location:
remote:   https://github.com/sjamillah/git-exercises.git
remote:
remote: Create a pull request for 'test' on GitHub by visiting:        
remote:      https://github.com/sjamillah/git-exercises/pull/new/test  
remote:
To https://github.com/sjamillah/git-exercise.git
 * [new branch]      test -> test
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git 
checkout dev
M       README.md
Switched to branch 'dev'
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git 
branch -D test
Deleted branch test (was 736641d).
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git 
push --delete test
fatal: --delete doesn't make sense without any refs
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git push origin --delete test
remote: This repository moved. Please use the new location:
remote:   https://github.com/sjamillah/git-exercises.git
To https://github.com/sjamillah/git-exercise.git
 - [deleted]         test
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git 
checkout main
M       README.md
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git 
add .
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git 
commit -m "made some changes"
[main 5b4bb76] made some changes
 1 file changed, 5 insertions(+), 1 deletion(-)
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git 
push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 402 bytes | 21.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.   
remote: This repository moved. Please use the new location:
remote:   https://github.com/sjamillah/git-exercises.git
To https://github.com/sjamillah/git-exercise.git
   736641d..5b4bb76  main -> main
   ```
2. Bundle 1-Exercise 2
- Create a new `home.html` file, add some html changes and save them
- Stash save your current changes
- Repeat the same process for a new `about.html` page and stash save your changes
- Repeat the same process for a new `team.html` page and stash save your changes
- Using stash pop restore the changes of the `about.html` page
- With the help of an index use stash pop bring back the `home.html` page changes
- Commit the current changes and push them
- Using stash pop restore the changes of the `team.html` page index
- Reset the current changes using git reset and go back to the changes without the `team.html` page
``` bash
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git status
On branch main
Your branch is behind 'origin/main' by 2 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

Untracked files:
  (use "git add <file>..." to include in what will be committed)       
        home.html

nothing added to commit but untracked files present (use "git add" to track)
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git stash list
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ git 
 README.md | 209 ++++++++++++++++++++++++++++++++++++++++++++++++++++-
 1 file changed, 208 insertions(+), 1 deletion(-)
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Git-Exercise$ cd ..
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop$ mv Git-Exercise/
mv: missing destination file operand after 'Git-Exercise/'
Try 'mv --help' for more information.
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop$ mv Git-Exercise/ Gym Git Exercise
mv: target 'Exercise' is not a directory
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop$ mv Git-Exercise/ Gym-Git-Exercise
mv: cannot move 'Git-Exercise/' to 'Gym-Git-Exercise': Permission denied
```
Solution of changing the folder name
``` bash
LENOVO@DESKTOP-533N1K0 MINGW64 ~/Desktop (master)
$ mv Git-Exercise/ Gym-Git-Exercise

LENOVO@DESKTOP-533N1K0 MINGW64 ~/Desktop (master)
$ code .

LENOVO@DESKTOP-533N1K0 MINGW64 ~/Desktop (master)
$ code Gym-Git-Exercise/
```
Continuation:
``` bash
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$
se$ git pull
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)  
Unpacking objects: 100% (3/3), 1.06 KiB | 11.00 KiB/s, done.
From https://github.com/sjamillah/git-exercise
   52b6b6f..9f92303  main       -> origin/main
Updating 56c8151..9f92303
Fast-forward
 README.md | 35 +++++++++++++++++++++++++++++++++++
 1 file changed, 35 insertions(+)
git stash list
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git add home.html 
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git stash pop
No stash entries found.
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git stash
Saved working directory and index state WIP on main: 27a004c removed a file
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git add about.html 
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git stash
Saved working directory and index state WIP on main: 27a004c removed a file
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git stash list
stash@{0}: WIP on main: 27a004c removed a file
stash@{1}: WIP on main: 27a004c removed a file
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git add team.html 
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git stash
Saved working directory and index state WIP on main: 27a004c removed a file
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git stash list
stash@{0}: WIP on main: 27a004c removed a file
stash@{1}: WIP on main: 27a004c removed a file
stash@{2}: WIP on main: 27a004c removed a file
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git stash pop stash@{1}
On branch main
Your branch is behind 'origin/main' by 1 commit, and can be fast-forwarded.
  (use "git pull" to update your local branch)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (61de795632eaabc61eaf4753131dcf19765fd0d9)
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git stash list
stash@{0}: WIP on main: 27a004c removed a file
stash@{1}: WIP on main: 27a004c removed a file
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git stash pop stash@{1}
On branch main
Your branch is behind 'origin/main' by 1 commit, and can be fast-forwarded.
  (use "git pull" to update your local branch)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (cec49db83d379040ba8d48a242b4e9b90ee22de7)
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git commit -m "staged and stashed about and home pages"
[main 5cd91f0] staged and stashed about and home pages
 2 files changed, 23 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git stash pop stash@{0}
On branch main
Your branch and 'origin/main' have diverged,
and have 1 and 1 different commits each, respectively.
  (use "git pull" to merge the remote branch into yours)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (8eee61ddee072b4449dfb2a4492bab9434096b19)
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git reset --hard HEAD
```
3. Bundle 2 Exercise 1
- - Create a new branch named `ft/bundle-2`
- Add new changes to your project. create a new page named `services.html` and add some changes
- Commit your changes and create a Pull Request against the `main` branch in your github repository
- Request a review and make sure your Pull request gets merged (Look for someone to merge your PR)

Solution
``` bash
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git add services.html 
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git commit -m "added content in the services page"
[ft/bundle-2 cfe13b1] added content in the services page
 1 file changed, 23 insertions(+)
 create mode 100644 services.html
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git status
On branch ft/bundle-2
nothing to commit, working tree clean
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git push --set-upstream origin ft/bundle-2
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 953 bytes | 63.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 1 local object.   
remote: This repository moved. Please use the new location:
remote:   https://github.com/sjamillah/git-exercises.git
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting: 
remote:      https://github.com/sjamillah/git-exercises/pull/new/ft/bundle-2
remote:
To https://github.com/sjamillah/git-exercise.git
Branch 'ft/bundle-2' set up to track remote branch 'ft/bundle-2' from 'origin'.
```
4. Bundle 2 Exercise 2
- - Checkout your `main` branch and pull the latest changes
- Create a new branch named `ft/service-redesign`
- Add new changes to the `service.html` page
- commit and push them
- create a new PR for your changes
- go back to your `main` branch and add again new changes to your `service.html` page, you can add different changes but make sure to affect the same part(line of code) as you did in the other PR
- Commit and push those changes
- Now go back to the Github PR you had created for the `ft/service-redesign`branch, you will then see that you have conflicts with the `main` branch
- In your project checkout the `ft/service-redesign`branch
- Compare the `ft/service-redesign`with the `main` branch using git diff and observe the changes
- Using git merge, merge the `main` branch with `ft/service-redesign` branch and commit and push you changes again

Solution:
``` bash
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git pull
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git pull
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
error: could not apply de8b279... made updates
hint: Resolve all conflicts manually, mark them as resolved with
hint: "git add/rm <conflicted_files>", then run "git rebase --continue".
hint: You can instead skip this commit: run "git rebase --skip".
hint: To abort and get back to the state before "git rebase", run "git rebase --abort".
Could not apply de8b279... made updates
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git pull
error: Pulling is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git status
interactive rebase in progress; onto e76b7b0
Last command done (1 command done):
   pick de8b279 made updates
No commands remaining.
You are currently rebasing branch 'main' on 'e76b7b0'.
  (fix conflicts and then run "git rebase --continue")
  (use "git rebase --skip" to skip this patch)
  (use "git rebase --abort" to check out the original branch)

Unmerged paths:
        both modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git pull
Updating e76b7b0..903224c
Fast-forward
 services.html | 23 +++++++++++++++++++++++
 1 file changed, 23 insertions(+)
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ jamillah@DESKTOP-533N1K0jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ jamillah@DESKTOP-533N1K0jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git add services.html 
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git commit -m "added new
 changes to the services page"
[ft/service-redesign 48dce7d] added new changes to the services page
 1 file changed, 8 insertions(+)
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 481 bytes | 10.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: This repository moved. Please use the new location:
remote:   https://github.com/sjamillah/git-exercises.git
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/sjamillah/git-exercises/pull/new/ft/service-redesign
remote:
To https://github.com/sjamillah/git-exercise.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
Branch 'ft/service-redesign' set up to track remote branch 'ft/service-redesign' from 'origin'.
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git add services.html 
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git commit -m "added cha
nges to services in the main branch"
[main f77b2fc] added changes to services in the main branch
 1 file changed, 9 insertions(+)
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 511 bytes | 28.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: This repository moved. Please use the new location:
remote:   https://github.com/sjamillah/git-exercises.git
To https://github.com/sjamillah/git-exercise.git
   903224c..f77b2fc  main -> main
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git diff main ft/service-redesign
diff --git a/services.html b/services.html
index 4847df2..4263c73 100644
--- a/services.html
+++ b/services.html
@@ -19,13 +19,12 @@
             <p>Designing intuitive and high-performance mobile applications for iOS and Android.</p>
diff --git a/services.html b/services.html
index 4847df2..4263c73 100644
--- a/services.html
+++ b/services.html
@@ -19,13 +19,12 @@
             <p>Designing intuitive and high-performance mobile applications for iOS and Android.</p>
         </div>
         <div class="service-box">
-        <h2>Digital Marketing</h2>
-                <p>Boosting your business visibility through SEO, PPC campaigns, and social media strategies.</p>
-                <ul>
-                    <li>Search Engine Optimization</li>
-                    <li>Social Media Management</li>
-                    <li>Pay-Per-Click Campaigns</li>
-                </ul>
+            <h2>SEO Optimization</h2>^M
+            <p>Improving your website's visibility on search engines with effective SEO strategies.</p>^M
+        </div>^M
:...skipping...
diff --git a/services.html b/services.html
index 4847df2..4263c73 100644
--- a/services.html
+++ b/services.html
@@ -19,13 +19,12 @@
             <p>Designing intuitive and high-performance mobile applications for iOS and Android.</p>
         </div>
         <div class="service-box">
-        <h2>Digital Marketing</h2>
-                <p>Boosting your business visibility through SEO, PPC campaigns, and social media strategies.</p>
-                <ul>
-                    <li>Search Engine Optimization</li>
-                    <li>Social Media Management</li>
-                    <li>Pay-Per-Click Campaigns</li>
-                </ul>
+            <h2>SEO Optimization</h2>^M
+            <p>Improving your website's visibility on search engines with effective SEO strategies.</p>^M
+        </div>^M
+        <div class="service-box">^M
+            <h2>Technical Support</h2>^M
+            <p>Offering ongoing support and maintenance to keep your systems running smoothly.:...skipping...
diff --git a/services.html b/services.html
index 4847df2..4263c73 100644
--- a/services.html
+++ b/services.html
@@ -19,13 +19,12 @@
             <p>Designing intuitive and high-performance mobile applications for iOS and Android.</p>
         </div>
         <div class="service-box">
-        <h2>Digital Marketing</h2>
-                <p>Boosting your business visibility through SEO, PPC campaigns, and social media strategies.</p>
-                <ul>
-                    <li>Search Engine Optimization</li>
-                    <li>Social Media Management</li>
-                    <li>Pay-Per-Click Campaigns</li>
-                </ul>
+            <h2>SEO Optimization</h2>^M
+            <p>Improving your website's visibility on search engines with effective SEO strategies.</p>^M
+        </div>^M
+        <div class="service-box">^M
+            <h2>Technical Support</h2>^M
+            <p>Offering ongoing support and maintenance to keep your systems running smoothly.</p>^M
:...skipping...
diff --git a/services.html b/services.html
index 4847df2..4263c73 100644
--- a/services.html
+++ b/services.html
@@ -19,13 +19,12 @@
             <p>Designing intuitive and high-performance mobile applications for iOS and Android.</p>
         </div>
         <div class="service-box">
-        <h2>Digital Marketing</h2>
-                <p>Boosting your business visibility through SEO, PPC campaigns, and social media strategies.</p>
-                <ul>
-                    <li>Search Engine Optimization</li>
-                    <li>Social Media Management</li>
-                    <li>Pay-Per-Click Campaigns</li>
-                </ul>
+            <h2>SEO Optimization</h2>^M
+            <p>Improving your website's visibility on search engines with effective SEO strategies.</p>^M
             <p>Designing intuitive and high-performance mobile applications for iOS and Android.</p>
         </div>
         <div class="service-box">
-        <h2>Digital Marketing</h2>
-                <p>Boosting your business visibility through SEO, PPC campaigns, and social media strategies.</p>
-                <ul>
-                    <li>Search Engine Optimization</li>
-                    <li>Social Media Management</li>
-                    <li>Pay-Per-Click Campaigns</li>
-                </ul>
+            <h2>SEO Optimization</h2>^M
+            <p>Improving your website's visibility on search engines with effective SEO strategies.</p>^M
         </div>
         <div class="service-box">
-        <h2>Digital Marketing</h2>
-                <p>Boosting your business visibility through SEO, PPC campaigns, and social media strategies.</p>
-                <ul>
-                    <li>Search Engine Optimization</li>
-                    <li>Social Media Management</li>
-                    <li>Pay-Per-Click Campaigns</li>
-                </ul>
+            <h2>SEO Optimization</h2>^M
+            <p>Improving your website's visibility on search engines with effective SEO strategies.</p>^M
-                <p>Boosting your business visibility through SEO, PPC campaigns, and social media strategies.</p>
-                <ul>
-                    <li>Search Engine Optimization</li>
-                    <li>Social Media Management</li>
-                    <li>Pay-Per-Click Campaigns</li>
-                </ul>
+            <h2>SEO Optimization</h2>^M
+            <p>Improving your website's visibility on search engines with effective SEO strategies.</p>^M
-                    <li>Search Engine Optimization</li>
-                    <li>Social Media Management</li>
-                    <li>Pay-Per-Click Campaigns</li>
-                </ul>
+            <h2>SEO Optimization</h2>^M
+            <p>Improving your website's visibility on search engines with effective SEO strategies.</p>^M
-                    <li>Social Media Management</li>
-                    <li>Pay-Per-Click Campaigns</li>
-                </ul>
+            <h2>SEO Optimization</h2>^M
+            <p>Improving your website's visibility on search engines with effective SEO strategies.</p>^M
+            <h2>SEO Optimization</h2>^M
+            <p>Improving your website's visibility on search engines with effective SEO strategies.</p>^M
+        </div>^M
+        <div class="service-box">^M
+            <h2>Technical Support</h2>^M
+            <p>Offering ongoing support and maintenance to keep your systems running smoothly.+        <div class="service-box">^M
+            <h2>Technical Support</h2>^M
+            <p>Offering ongoing support and maintenance to keep your systems running smoothly.</p>^M
+            <p>Offering ongoing support and maintenance to keep your systems running smoothly.</p>^M
         </div>
</p>^M
         </div>
         </div>
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git merge main
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git merge main
Auto-merging services.html
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.      
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git add services.html
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git commit -m "Merge branch 'main' into ft/service-redesign"
[ft/service-redesign 2d4b503] Merge branch 'main' into ft/service-redesign
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ g
it push
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 242 bytes | 14.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
remote: This repository moved. Please use the new location:
remote:   https://github.com/sjamillah/git-exercises.git
To https://github.com/sjamillah/git-exercise.git
```
5. Bundle 3 Exercise 1
- - Create a new branch named `ft/team-page`
- Create a new html page named `team.html` and add some changes
- commit and push those changes
- Create a new PR for the changes
- Go back to `main` branch (checkout the `main` branch)
- Create new branch named `ft/contact-page`
- Go back to the `ft/team-page`
- With the help of git log look for the last commit and copy its hash
- Checkout again `ft/contact-page` using git cherry-pick get the changes from the last commit on the `ft/team-page` branch.
- Add new changes for the contact page and commit, push them
- Create a new PR for the contact page
- From the `ft/contact-page` branch create a new branch called `ft/faq-page`
- Create a new `faq.html` page and add some changes there
- Commit and push those changes
- Using git revert, revert the changes of the last commit of the `ft/team-page` branch. (use the commit hash you copied earlier)
- Push the changes and create a new PR

Solution:
``` bash
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
g
it status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git status
On branch ft/team-page
nothing to commit, working tree clean
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git add team.html 
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git commit -m "created the teams' page"
[ft/team-page 0c6eb94] created the teams' page
 1 file changed, 22 insertions(+)
 create mode 100644 team.html
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git push
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git push --set-upstream origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 536 bytes | 23.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.   
remote: This repository moved. Please use the new location:
remote:   https://github.com/sjamillah/git-exercises.git
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting 
remote:      https://github.com/sjamillah/git-exercises/pull/new/ft/team-page
remote:
To https://github.com/sjamillah/git-exercise.git
 * [new branch]      ft/team-page -> ft/team-page
Branch 'ft/team-page' set up to track remote branch 'ft/team-page' from 'origin'.
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git log
commit 0c6eb94b4d437684dd1a0eb5b64819a8aa876b3d (HEAD -> ft/team-page, origin/ft/team-page)
Author: sjamillah <j.ssozi@alustudent.com>
Date:   Tue Dec 17 15:45:29 2024 +0200

    created the teams' page

commit bf0faa914b6434771bf180c9855daeda5cac9300 (origin/main, main, ft/contact-page)
Merge: ce17988 2d4b503
Author: Ssozi Jamillah <127307233+sjamillah@users.noreply.github.com>  
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git log -1
commit 0c6eb94b4d437684dd1a0eb5b64819a8aa876b3d (HEAD -> ft/team-page, origin/ft/team-page)
Author: sjamillah <j.ssozi@alustudent.com>
Date:   Tue Dec 17 15:45:29 2024 +0200

    created the teams' page
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git checkout ft/contact-page 
Switched to branch 'ft/contact-page'
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git cherry-pick 0c6eb94b4d437684dd1a0eb5b64819a8aa876b3d
[ft/contact-page 9279a79] created the teams' page
 Date: Tue Dec 17 15:45:29 2024 +0200
 1 file changed, 22 insertions(+)
 create mode 100644 team.html
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git add services.html 
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git reset services.html
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git cherry-pick 0c6eb94b4d437684dd1a0eb5b64819a8aa876b3d
On branch ft/contact-page
You are currently cherry-picking commit 0c6eb94.
  (all conflicts fixed: run "git cherry-pick --continue")
  (use "git cherry-pick --skip" to skip this patch)
  (use "git cherry-pick --abort" to cancel the cherry-pick operation)  

Untracked files:
  (use "git add <file>..." to include in what will be committed)       
        contact.html

nothing added to commit but untracked files present (use "git add" to track)
The previous cherry-pick is now empty, possibly due to conflict resolution.
If you wish to commit it anyway, use:

    git commit --allow-empty

Otherwise, please use 'git cherry-pick --skip'
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git cherry-pick 0c6eb94b4d437684dd1a0eb5b64819a8aa876b3d
On branch ft/contact-page
You are currently cherry-picking commit 0c6eb94.
  (all conflicts fixed: run "git cherry-pick --continue")
  (use "git cherry-pick --skip" to skip this patch)
  (use "git cherry-pick --abort" to cancel the cherry-pick operation)  

nothing to commit, working tree clean
The previous cherry-pick is now empty, possibly due to conflict resolution.
If you wish to commit it anyway, use:

    git commit --allow-empty

Otherwise, please use 'git cherry-pick --skip'
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git diff 0c6eb94b4d437684dd1a0eb5b64819a8aa876b3d
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git log
commit 9279a79f19dc2851da80be868e5bddbd08194e1f (HEAD -> ft/contact-page)
Author: sjamillah <j.ssozi@alustudent.com>
Date:   Tue Dec 17 15:45:29 2024 +0200

    created the teams' page

commit bf0faa914b6434771bf180c9855daeda5cac9300 (origin/main, main)    
Merge: ce17988 2d4b503
Author: Ssozi Jamillah <127307233+sjamillah@users.noreply.github.com>  
Date:   Tue Dec 17 15:10:48 2024 +0200

    Merge pull request #2 from sjamillah/ft/service-redesign

    added new changes to the services page

commit ce17988aa80001a2137a28292e9a9094f9ec0c11
Author: sjamillah <j.ssozi@alustudent.com>
Date:   Tue Dec 17 15:09:16 2024 +0200

    updated the readme file

jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git add --all
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git commit -m "added the contacts page"
[ft/contact-page 936527a] added the contacts page
 Date: Tue Dec 17 15:45:29 2024 +0200
 1 file changed, 14 insertions(+)
 create mode 100644 contact.html
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git push
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/contact-page

jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git push --set-upstream origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 1.01 KiB | 54.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 1 local object.   
remote: This repository moved. Please use the new location:
remote:   https://github.com/sjamillah/git-exercises.git
remote: 
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/sjamillah/git-exercises/pull/new/ft/contact-page
remote:
To https://github.com/sjamillah/git-exercise.git
 * [new branch]      ft/contact-page -> ft/contact-page
Branch 'ft/contact-page' set up to track remote branch 'ft/contact-page' from 'origin'.
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git add faq.html 
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git add -all
error: did you mean `--all` (with two dashes)?
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git add --all
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git commit -m "created the frequently asked questions page"
[ft/faq-page efe57a1] created the frequently asked questions page
 1 file changed, 20 insertions(+)
 create mode 100644 faq.html
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ 
git push
fatal: The current branch ft/faq-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/faq-page

jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git push --set-upstream origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 623 bytes | 56.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.   
remote: This repository moved. Please use the new location:
remote:   https://github.com/sjamillah/git-exercises.git
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting: 
remote:      https://github.com/sjamillah/git-exercises/pull/new/ft/faq-page
 * [new branch]      ft/faq-page -> ft/faq-page
Branch 'ft/faq-page' set up to track remote branch 'ft/faq-page' from 'origin'.
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git revert 0c6eb94b4d437684dd1a0eb5b64819a8aa876b3d
[ft/faq-page e3d27d2] Revert "created the teams' page"
 1 file changed, 22 deletions(-)
 delete mode 100644 team.html
jamillah@DESKTOP-533N1K0:/mnt/c/Users/LENOVO/Desktop/Gym-Git-Exercise$ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 280 bytes | 56.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: This repository moved. Please use the new location:
remote:   https://github.com/sjamillah/git-exercises.git
To https://github.com/sjamillah/git-exercise.git
```