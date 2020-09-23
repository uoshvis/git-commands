## First time git configuration

Terminal configuration is in .bash_profile file.

```
# sets up Git with your name
git config --global user.name "<Your-Full-Name>"

# sets up Git with your email
git config --global user.email "<your-email-address>"

# makes sure that Git output is colored
git config --global color.ui auto

# displays the original state in a conflict
git config --global merge.conflictstyle diff3

git config --list
```

Git & code editor
```
$ git config --global core.editor "subl -n -w"

```

## Find The Version Of Git

`git --version`

## Create A New Git Repository

1. Go to the fold of the project.

2. Run `git init`

## Clone An Existing Git Repository

Cloning is the process of pulling down a copy of a repository stored on a server.

1. Go to the parent folder of where you want to repository's folder to be in.

2. `git clone [url to repository's git file] [name of folder / repository you want]`

## Clone into existing directory

```
git init
git remote add origin [my-repo]
git fetch
git checkout origin/master -ft
```

## Check The Status Of A Git Repository

`git status`

## Tell Git To Track A File

`git add readme.md`

`git add <file1> <file2> … <fileN>`

## Make A Commit

`git commit --m "First commit"`

## Tell Git To Track A Whole Folder

`git add chapter2/`

## Tell Git To Track (And Stage) All Files And Subfolders In A Directory

`git add -A`

`git add .`

## Add marker on a specific commit

`git tag -a <name> <SHA>`

## View All Branches

`git branch`

## Create A New Branch

`git branch new_model`

## Create A New Branch on specific commit

`git branch new_model <SHA>`

## Create Branch and Checkout

`git checkout -b footer master`

## Switch To A Branch

`git checkout new_model`

## Create A New Branch And Switch To It

`git checkout -b new_ux`

## Delete branch

`git branch -d <branchname>`

## Merge One Branch Into Another

1. Switch to the branch you want to pull changes into: `git checkout master`

2. Pull changes from another branch into your branch: `git merge new_ux`

## Merge Conflict Indicators
```
# everything below this line (until the next indicator) shows you what's on the current branch
<<<<<<< HEAD
# everything below this line (until the next indicator) shows you what the original lines were
||||||| merged common ancestors
# is the end of the original lines, everything that follows (until the next indicator) is what's on the branch that's being merged in
======
#  is the ending indicator of what's on the branch that's being merged in (in this case, the heading-update branch)
>>>>>>> heading-update
```

## Set A Remote Github Repository

1. Go to GitHub.com and create a new repository.

2. Set that repository's url as the origin repo: `git remote add origin https://github.com/chrisalbon/git_tutorial.git`

## Push Master Branch To A Github Repository

The `-u` sets the origin as the default for this branch

`git push -u origin master`

## Pull Down From A Branch From A GitHub Repository To Local Repository

`git pull origin master`

## Pull Down All Branches From GitHub

`git fetch origin`

## View All Remote Branches

`git branch --remote`

## View Log

```
git log

# one commit per line + message
git log --oneline

# modified files, lines, summary
git log --stat

# start at specific commit
git log -p {SHA}

# show branching

git log --oneline --graph --all

```

*uses less(Unix) program*

## View Unstagged Changes To Files

`git diff`

## Unstage A File (default --mixed)

`git reset filename`

## Undo Last Commit, Move Commits Changes To Staging

`git reset --soft HEAD^`

`^ idicates the parent commit` 

`~ indicates the first parent commit`

## Undo Last Commit, Remove All Changes In Your Working Directory

`git reset --hard HEAD^`


## Clone A Remote Repository Locally 

`git clone url`

## Show Changes From A Particular Commit

`git show --pretty="format:" <commitID>`

## Revert A Commit By Creating A New Commit With Opposite Changes

`git revert <commitID>`

## Alter most recent commit

`git commit --amend`

## To access erased commits

`git reflog`

