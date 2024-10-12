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



## Cloning

we can clone in three ways : HTTPS, SSH, Github CLI

Since we are using Github CodeSpaces we'll create a temporary directory in our workspaces.

```sh
mkdir /workspaces/tmp
cd /workspaces/tmp
```

### 1. HTTPS : 

```sh
git clone https://github.com/srjbisht01/Ghost-learning-git.git
cd Ghost-learning-git
```

> You'll need to generate a Personal Access Token (PAT). 
https://github.com/settings/token 

You will use the PAT as your password when you login. 

- Give it access to Contents for Commits. 


### 2. SSH

```ssh
git clone git@github.com:srjbisht01/Ghost-learning-git.git
cd Ghost-learning-git
```

we will need to create our own SSH rsa key pair. 
```sh
ssh-keygen -t rsa
```

For WSL users and if you create a non default key you might need to add it.
```sh
eval `ssh-agent`
ssh-add /home/srjbisht01/.ssh/alt-github_id_rsa
``` 

we can test our connection here:
```
ssh -T git@github.com
```


### 3. Github CLI

Install the CLI

eg. Linux(Ubuntu)
```sh
sudo apt update
sudo apt install gh
```

```
gh auth login
gh repo clone srjbisht01/Ghost-learning-git
```



## Commit

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



## Branches

List of Branches
```
git branch 
```

Create a new branch
```
git branch <branch-name>
```

checkout the branch
```
git checkout <branch-name>
```
<<<<<<< HEAD

Switch branch 
```
git switch <branch-name>
```

> both git checkout and git switch can be used to change the branch.  

=======
>>>>>>> dev



## Remotes





## Stashing






## Merging






## Add

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

> "git reset" will revert a "git add ."


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


## Push

when we want to push a repo to our remote origin

```
git push
```