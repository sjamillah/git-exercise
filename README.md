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