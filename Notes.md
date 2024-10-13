## Git Hidden Folder
There is a hidden folder called `.git` which tells that our project is a git repo.

If we wanted to create a git repo in a new project we will create the folder and then we will initialize that repo using `git init` .

```
mkdir /workspaces/tmp/new-project
cd /workspaces/tmp/new-project
git init
touch Readme.md
code Readme.md
git status
git add Readme.md
# makes changes to Readme.md
git commit -m "add readme file"
```

## Cloning
There are three ways for cloing : HTTPS, SSH, GITHUB CLI

since we are using github codespaces we will create a temproray directory in our workspace.

``` sh
mkdir workspace/tmp
cd workspace/tmp/
```

### HTTPS: 

``` sh
git clone https://github.com/srjbisht01/Ghost-learning-git.git
cd Ghost-learning-git
```

## Commit

when we want to commit code we can write git commit which will open up the commit edit message in the editor of choice. 

```sh
git commit
```

Set the global editor
```
git config --global core.editor emacs
```

Make a commit and commit message without opening an editor
```
git commit -m "add another exclamation"
```

## Branches


## Remotes


## Stashing


## Merging


## Add

when we want to stage changes that will be included in the commit we can use the . to add all possible files. 

```
git add Readme.md
git add .
```

## Git Reset

Reset allows you to move staged changes to be unstaged.
This is useful when you want to revert all files not to be committed. 

```
git add .
git reset
```
> git resest will revert a git add .


## Git Status

Git Status shows you what files will or will not be commited. 
```
git status
```

## Gitconfig file

The Gitconfig file is what stores your global configurations for git such as email, name, editor or more. 

showing the contents of our .gitconfig file 
```
git config --list --show-origin
```

when you first install Git on a machine you are suppose to set up your name and email. 

```sh
git config --global user.name "John Doe"
git config --global user.email "JohnDoe@gmail.com"
```

# Log 

git log will show recent git commits to the git tree 


## Push

When we want to push a repo to our remote origin

```
git push
```
