## Pushing to an existing repository 

The basic github work cycle is fork > edit > commit > pull request > merge. 

### Clone the repository

First, you want to get a copy of the repository
Copy the ssh url from the repository homepage then enter:

```
git clone git@github.com:<project>.git
```

Change into the newly-created project directory, where you’ll find all the source code of your project.

Now you’re in the working directory, the set of files that you currently have in front of you, available to edit. We want to know its status:

```
$ git status
# On branch master
nothing to commit (working directory clean)
```

### Create a new branch

Now you want to create a branch specifically for your changes

```
$ git checkout -b mycoolbranch
Switched to a new branch 'mycoolbranch'
```

```git checkout``` is a command you’ll use a lot, to switch between branches. The ```-b``` flag tells it to create a new branch at the same time. By default, the new branch is based upon whatever branch you were on.

### Make some changes

Edit some files within your project then type:
```git status```. This should now return with the list of the pages you made edits to. 

### Stage your changes

Git has a staging area, for files that you want to commit. On GitHub when you edit a file, you commit it as soon as you save it. On your machine, you can edit a number of files and commit them altogether.

Staging a file in Git’s terminology means adding it to the staging area, in preparation for a commit.

Add your amended files to the staging area:

```
git add .
```

The ```.``` refers to everything in the current directory. You  may also choose to add a only a specific file. Ex: 
```
git add myfile.txt
```

It's not your file that are stages rather the changes to your files, that are staged. 

### Commit your changes

When you’re happy with your files, and have added the changes you want to commit to the staging area:

```
git commit -m "made some coolio changes"
```

The -m flag is for the message on the commit - every commit needs a commit message.

### Push your changes to GitHub

You have multiple branches here, so you need to tell git where to push (i.e. back to the remote repository you cloned from, on GitHub) and what exactly to push (your new branch).

The repository you cloned from - yours - can be referred to as origin. The new branch is called mycoolbranch. So:

```
git push origin mycoolbranch
```

### Finally

Go on github and create a pull request to merge your next branch in the master branch.

Source: [Read the docs](http://dont-be-afraid-to-commit.readthedocs.io/en/latest/git/commandlinegit.html)
