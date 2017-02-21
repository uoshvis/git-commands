

## Find The Version Of Git

`git --version`

## Create A New Git Repository

1. Go to the fold of the project.

2. Run `git init`

## Clone An Existing Git Repository

Cloning is the process of pulling down a copy of a repository stored on a server.

1. Go to the parent folder of where you want to repository's folder to be in.

2. `git clone [url to repository's git file] [name of folder / repository you want]`

## Check The Status Of A Git Repository

`git status`

## Tell Git To Track A File

`git add readme.md`

## Make A Commit

`git commit --m "First commit"`

## Tell Git To Track A Whole Folder

`git add chapter2/`

## Tell Git To Track (And Stage) All Files And Subfolders In A Directory

`git add --a`

## View All Branches

`git branch`

## Create A New Branch

`git branch new_model`

## Switch To A Branch

`git checkout new_model`

## Create A New Branch And Switch To It

`git checkout -b new_ux`

## Merge One Branch Into Another

1. Switch to the branch you want to pull changes into: `git checkout master`

2. Pull changes from another branch into your branch: `git merge new_ux`

## Set A Remote Github Repository

1. Go to GitHub.com and create a new repository.

2. Set that repository's url as the origin repo: `git remote add origin https://github.com/chrisalbon/git_tutorial.git`

## Push Master Branch To A Github Repository

`git push -u origin master`
