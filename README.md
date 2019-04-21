# project_template

__steps for using github for version control (in rstudio)__

a: Create a git repository on github

b: Create a new project in rstudio, choose the option *version control*. Use the URL of your recently created repository when creating this project.

c: Open the R project. Now, you should create a new branch to work on. You __never__ want to work directly on the master branch because changes there effect anyone who is contributing to the repository. You can create a branch by going to the rstudio bash terminal and typing the command `git checkout -b <branchname>`, branchname being the name of the branch you wish to checkout (and create). In the future you can use `git checkout <branchname>` to switch between branches.

d: Make changes to your files!

e: If you created any new files, add them to git. Use `git add <filename>`. This will tell git to track this file.

f: Commit your changes! Use `git commit -m <"commit message">` to commit your changes (to be pushed soon). Remember to add the `-m` tag because if you don't you will be dropped into VI, a common commandline text editor. If you are dropped into VI, do press `:` and then write `wq` and press `return`. This will exit VI.

g: Push your changes to the git repository! Now it is time to send your changes you have made locally to the git repository on the web (anyone who has access to the repository can see them). Use `git push --set-upstream origin <branchname>` to create a branch of the same name as your local branch on the repository and push your changes to it. In the future you can use `git push` to push your changes (once the upstream branch is set).

h: Go on the github website and create a pull request to give an opportunity for your collegues to review your changes. Once they have made their comments and you have (hopefully) been receptive to their feedback you can merge this branch with the master branch. This will update the master branch and apply the changes you have made, sending those changes to anyone else using the repository.

i: Now, after your collegues made changes to your code in the pull request (you misspelt something) you need to pull those changes back to your local version of the repository. Use `git pull` to bring changes from the remote (the github repo) to your local copy of the repo.
