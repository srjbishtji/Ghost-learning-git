## Git Hidden Folder

There is a hidden folder called `.git` which tells you that our project is a git repo.

If we wanted to create a git repo in a new project we create the folder and then we initialize that repo using `git init` .

```
mkdir /workspaces/tmp/new-folder
cd /workspaces/tmp/new-folder
git init
touch README.md
code README.md
git status
git add README.md
# make changes to `README.md`
git commit -m "add README file"
```



## cloning

we can clone in three ways : HTTPS, SSH, Github CLI

Since we are using Github CodeSpaces we'll create a temporary directory in our workspaces.

```sh
mkdir /workspaces/tmp
cd /workspaces/tmp
```

### HTTPS : 

```sh
git clone https://github.com/srjbisht01/Ghost-learning-git.git
cd Ghost-learning-git
```

## commit

when we want to commit code we can write `git commit` which will open up the commit edit message in the editor of choice.

```sh
git commit
```

set the global editor

```
git config --global core.editor emacs  
```

Make a commit and a commit message without opening an editor
```sh
git commit -m "added another exclamation mark"
```

# branches

# remotes

# stashing

## Merging

## add

when we want to stage changes that will be included in the commit we can use the `.` to add all possible files.
```
git add readme.md
git add .
```

## Reset

Reset allows you to move staged changes to be unstaged. 
This is useful when you want to revert all files not to be not committed.

```
git add . 
To unstage all changes: `git reset` 
If you want to unstage specific files, you can use: `git reset HEAD <file>
`
```

> git reset will revert a git add .


## Git status

Git status shows you what files will or will not be committed.

```
git status
```


## GitConfig file

The gitconfig file is what stores your global configuration for git such as email, name, editor and more. 

Showing the contents of our `.gitconfig` file
```
git config --list
```

```
git config --list --show-origin
```

when you first install git on a machine you are suppose to set up your name and email.

```sh
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```


## Log 

git log will show recent git commits to the git tree. 

```
git log
```