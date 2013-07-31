Using GitHub for xAPI-Design
============================

GitHub is a web-based hosting service for software development projects that use the Git revision control system. 

## Quick Steps Code Change Workflow Summary:
1. Update your local master: `git pull upstream master`
2. Create a new branch to work in: `git checkout -b <new branch>`
3. Make changes in that branch
4. Commit regularly: `git commit -a -m "message about the commit / changes"`
5. Push changes to your remote repository: `git push origin <new branch>`
6. Repeat steps 3-5
7. When finished, send a pull request to the main/master remote repository: on your github repository page, select the correct branch, choose pull request, review code changes, press pull request button


## Setting up your project

Your xAPI project will be created in the master repository and will be located at a location similar to this: 

`https://github.com/adlnet/project_name`

Once every person on your team is signed up to GitHub, each member can fork the master project into their own 
'origin' directory that can be located here: 

`https://github.com/username/project_name`  

Origin is simply an alias for your own forked repository of the master repo.

After you download git onto your machine, you can clone your origin repo onto your machine. Open a terminal and 
navigate to the desired repository you want the code to reside. Then simply perform the git clone command

`git clone https://github.com/username/project_name`

Download link: http://git-scm.com/downloads

The first thing we’ll do is add a remote repository that links the master repository to your working directory. 
Run the remote add command

`git remote add upstream https://github.com/adlnet/project_name`

Upstream now acts as an alias for the master repository located on GitHub (https://github.com/adlnet/project_name). 
We’ll come back to importance of this later.

## Setting up a working branch

Before you get to adding or editing anything, you want to create a branch to work in. If you run '''git branch''' 
you’ll see you’re in the master branch. To make sure you’re working with the most recent code, run 

`git pull upstream master` 

This pulls and merges any new code anyone else on your team has merged into the master repository into your local 
master branch. That step is essential so you don’t run into any merge conflicts.   Perform 

`git checkout –b branch_name` 

to create a new branch and check it out. If you run the “git branch” command again you’ll see you are in the newly 
created branch. Now that you’re up to date, you’re ready to add/edit code.

After you’ve done your work, if you perform 

`git status`

you’ll see if you edited anything it’s ready to be committed or if you’ve added anything, it’s ready to be added. 
If there are files that need added, do that first by running 

`git add file1 file2 file3 etc etc`

Each file name is separated by a space. Now after another `git status` you’ll see that the files you just added 
are ready to be committed. 

## Committing changes

To commit all of your files run

`git commit –a –m “message goes here`

The “-a” flag signifies you want to commit everything but if you don’t want to commit everything, 
you can just list which files you want to instead of using “-a”. The “-m” flag allows you to write a message with 
the commit saying what you changed.

After everything is committed, you can now push everything to a branch in your origin repository. Run 

`git push origin branch_name` 

This will push everything you just committed in your local branch to a branch on your origin repository with the 
same branch name as your local branch.

## Pull Requests

Now it’s time to create a pull request. Go to your origin repo in your browser and click on your branch drop down list. 
Click the name of the branch you just created and it will take you to that branch. Since you have changes from the 
master repository, you’ll see a button that says something along the lines of ‘Send Pull Request’.  Add any additional 
messages and continue through the steps. 

If you visit your master repository in your browser now, click Pull Requests on the right hand side. Your pull request 
will be listed so click it. It should be automatically allowed to be merged now so you can click Merge pull request to 
merge your code into the master repo.

Back on your local branch, checkout your master branch 

`git checkout master`

and run `git pull upstream master` 

Your local master branch will now have the changes you merged into the master repository. 

NOTE:  Whenever you create a new local branch, always make sure you branch from your master branch and remember to 
pull the new changes into it.

## Other helpful links

http://git-scm.com/docs/gittutorial
http://try.github.io/levels/1/challenges/1
http://rogerdudler.github.io/git-guide/
