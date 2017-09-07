# Github Basics

### Pushing a new project to github (from the command line)
The first thing you want to do is go to github and create a new project. 

Inside your terminal navigate to the root directory of your project.

```cd /path/to/project```

On windows, this will be: 
```dir /path/to/project```

Then enter the following:

```touch README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/c0ldlimit/vimcolors.git
git push -u origin master```

