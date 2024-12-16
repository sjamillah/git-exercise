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
