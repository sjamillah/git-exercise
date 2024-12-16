This is a file created locally and it will be used for a series of exercises. The following is what is done:
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
- From dev create another branch test
- Go back to the dev branch and delete the test branch