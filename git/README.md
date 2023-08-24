# GIT

### Config
`git config -l`

`git config --global user.name "<username>"`

`git config --global user.email "<useremail>"`

`git config --global --remove-section user.name`

`git config --global --remove-section user.email`
___
`git init`

`git status`
___

### Add
`git add .`

`git add <file>`

`git add <filename>*`
___
`git rm filename` delete file from git & local disk

`git rm --cached filename` To delete the file from git without removing it from disk


### Logs
`git log`

`git log -p`

`git log --oneline`

`git log --stat`

`git log --graph --oneline`

`git log --graph --oneline --all`

`git show [commit-id]`

### Commits

`git commit -m "<message>"`

`git commit -am "<message>"`

`git commit -m "<message>" --allow-empty`

`git commit -m "<message>" --author "<authorname>"`

`git commit -m "<message>" --date 2024-07-01`

### Branches
`git branch` list the branches

`git branch <branch_name>` create branch

`git branch -d <branch_name>` delete branch

`git branch -m <oldname> <newname>` or `(oldbranch)>git branch -m <newname>` Rename the branch

`git checkout <branch_name>` move to branch

`git checkout -b <branch_name>` create and move to branch

`git checkout main` move to main branch

`git branch --contains <commit_hash>`

### Remote URLs
`git remote add <shortcut> <url>`

`git remote show <remote>`

`git remote -v`   // show all the remote urls linked to repo

### Clone
`git clone <github_url>`

`git clone --branch <branch_name> --single-branch <url> [directory]`

### Push
`git push <url> <branchName>`

`git push <url> <branchName> -f ` forced push

`git push <origin> --delete <branchName>`

