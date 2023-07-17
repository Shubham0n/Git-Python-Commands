# **Git Command**

#### Check Git Version and Set the config of Git

| Command                                              | Description                                                                        |
| :--------------------------------------------------- | :--------------------------------------------------------------------------------- |
| `git --version`                                    | Check Git version                                                                  |
| `git config --global user.name` [name]   | Sor set Global configuration of User Name and also check config without adding name |
| `git config --global user.email` [email] | Set Global configuration of User Email and also check config without adding email  |
| `git config user.name`                   | Set Username config in particular folder                                           |
| `git config user.email`                  | Set Email config in particular folder                                              |

#### Git Status

| Command                          | Type of Result | Description                                                    |
| -------------------------------- | -------------- | -------------------------------------------------------------- |
| `git status`         | T (Tracked)    | Those files add to the repository (Git knows that file)        |
|                                  | U (Untracked)  | Working Directory files/ Those files are not added to the repository |
| `git status --short` |                | Check Status                                                   |
|                                  | ??             | Untracked files                                                |
|                                  | A              | File add to stage                                              |
|                                  | M              | MOdified files                                                 |
|                                  | D              | Deleted files                                                  |

#### Getting & Creating Projects

| Command                                                             | Description                                |
| ------------------------------------------------------------------- | ------------------------------------------ |
| `git init`                                                        | Initialize a local Git repository          |
| `git clone` ssh://git@github.com/[username]/[repository-name].git | Create a local copy of a remote repository |

#### Sharing & Updating Projects

| Command                                                                                | Description                                              |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| `git remote add` [orgin] ssh://git@github.com/[username]/[repository-name].git       | Add a remote repository                                  |
| `git remote -v`                                                                      | Check configured remotes                                |
| `git remote rename` [origin] [new name]                                              | Change name of origin                                    |
| `git remote set-url` [origin] ssh://git@github.com/[username]/[repository-name].git | Set a repository's origin branch to SSH                  |
| `git push --set-upstream [origin] [branch name]                                     | Set branch to remote repository                          |
| `git push -u` [origin] [branch name]                                                 | Push changes to the remote repository OR remember the branch |
| `git push`                                                                           | Push changes to remote repository OR remembered branch   |
| `git push` [origin] [branch name]                                                    | Push a branch to your remote repository                  |
| `git push -f`                                                                        | Force push a branch to your remote repository            |
| `git fetch`                                                                          | Fetch changes from remote repository branch              |
| `git fetch --all`                                                                    | Fetch all changes from remote repository                 |
| `git pull`                                                                           | Update local repository with new fetched changes         |
| `git pull` [origin] [branch name]                                                    | Pull changes from remote repository                      |

#### Local Branch Commands

| Command                                                          | Description                                             |
| ---------------------------------------------------------------- | ------------------------------------------------------- |
| **`git branch`** [branch-name]                           | Create a new branch                                     |
| **`git branch`**                                         | List branches (the asterisk denotes the current branch) |
| `git branch -a`                                                | List all branches (local and remote)                    |
| **`git checkout`** [branch-name]                         | Move to Other branch                                    |
| **`git branch -D`** [branch-name]                        | Delete the branch                                       |
| **`git checkout -b`** [branch-name]                      | Create and Move to the Branch                           |
| `git checkout -`                                               | Switch to the branch last checked out                   |
| `git checkout --` [file name]                                  | Discard changes to a file                               |
| **`git branch -m`** [old-branch-name] [new-branch-name] | Rename the Branch                                       |
| `git rm -r` [file-name.txt]                                    | Remove a file (or folder)                               |
| `git marge` [branch name]                                      | Merge a branch into the active branch                   |
| `git marge` [source branch] [target branch]                    | Merge a branch into a target branch                     |
| `git stash`                                                    | Stash changes in a dirty working directory              |
| `git stash clear`                                              | Remove all stashed entries                              |

#### Remote Branch Commands

| Command                                                | Description                            |
| ------------------------------------------------------ | -------------------------------------- |
| `git push origin --delete` [branch name]             | Delete a remote branch                 |
| `git checkout -b` [branch name] origin/[branch name] | Clone a remote branch and switch to it |

#### Add Files Commands

| Command                                       | Description                                       |
| --------------------------------------------- | ------------------------------------------------- |
| **`git add`** [file-name/folder-name] | Add single file or folder                         |
| **`git add -all`**                    | Add all new and changed files to the staging area |
| **`git add -a`**                      | Add all new and changed files to the staging area |
| `git add -A`                                | Add all new and changed files to the staging area  |
| **`git add .`**                       | Add all new and changed files to the staging area |

#### Commit Commands

| Command                                          | Description                                                                                          |
| ------------------------------------------------ | ---------------------------------------------------------------------------------------------------- |
| `git commit -m` "[Add commit message]"         | Add commit                                                                                           |
| `git commit --amend --no-edit`                 | Add files without change previous commit<br />(after this command you need to push code force push) |
| `git log`                                      | Show all commit / View changes                                                                       |
| `git log --summary`                            | View changes (detailed)                                                                              |
| `git log --oneline`                            | View changes (briefly)                                                                               |
| `git diff` [source branch] [target branch]     | Preview changes before merging                                                                       |
| `git log --pretty=format:"%h - %an, %ar : %s"` | Show all commit with format                                                                          |

#### Sub-module Commands

| Command                                          | Description                                                                                          |
| ------------------------------------------------ | ---------------------------------------------------------------------------------------------------- |
| `git submodule add https://github.com//[username]/[repository-name].git `         |  Add repository as a submodule                                   |
| `git submodule add /path/to/local/repo`        | Add the local repository as a submodule |
| `git submodule add`  | Git will clone the local repository and add it as a submodule to your project |

#### Generate SSH Key

| Command                                     | Description                                                           |
| ------------------------------------------- | --------------------------------------------------------------------- |
| ssh-keygen                                  | Generate ssh key                                                      |
| /Users/[username]/.ssh/id_rsa_[name]        | Enter the file in which to save the key (mac os)                         |
| cat/.ssh/id_rsa_[name].pub                  | show ssh key (mac os)                                                |
| type c:\users\\[user-name]\\.ssh\id_rsa.pub | show ssh key (window)                                                |
| cat ~/.ssh/config                           | List of all host and identity files (mac os)                           |
| vi ~/.ssh/config                            | Open the SSH client configuration file in the Vi text editor (mac os) |
| git clone git@[Host]:Shubham0-n/Git-Python-Commands.git | To use a specific SSH key when cloning a project from a different host, you need to update the SSH configuration file (~/.ssh/config) to define a custom host and associate it with the desired SSH key. |


#### Generate SSH Key of (cat ~/.ssh/config)
Host github.com-Ram
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_rsa_Ram
  IdentitiesOnly yes

Host github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_rsa
  IdentitiesOnly yes
 
Host github.com-Shubham2
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_shubham
  IdentitiesOnly yes

