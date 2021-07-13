## GIT GUIDE 
A list of commonly used git commands

### Set Up 🛠
| Command | Description 
|:--- |:--- 
|`git clone https://github.com/[username]/[repository-name].git`| Retrieve an entire repository from a hosted location via URL 
|`git clone ssh://git@github.com/[username]/[repository-name].git`|Retrieve an entire repository from a hosted location via SSH
|`git init`| Initialise an existing directory as a Git repository 
|`git config --global user.name “[firstname lastname]”`| Set a name that is identifiable for credit when review version history 
|`git config --global user.email “[valid-email]”`| Set an email address that will be associated with each history marker 
|`git remote set-url origin [repository-URL]`| Set repository URL
|`get remote -v`| Verify remote URL

### Update 📲
| Command | Description 
|:--- |:--- 
|`git pull`| Fetch and merge any commits from the tracking remote branch
|`git pull origin [branch-name]`|  Pull changes from locally stored branch and merge into local checked-out branch

### Branch 🌳
| Command | Description 
|:--- |:--- 
|`git branch`| A list of current branches
|`git branch -r`| View all local and remote branches
|`git branch -v`| View the last commit on each branch
|`git branch [branch-name]`| Create a new branch at the current commit
|`git branch --merged`| View which branches are already merged into the current branch
|`git checkout [branch-name]`| Navigate to the specified branch
|`git checkout -b [branch-name]`| Create a new branch and switch to that branch

### Stage 🚥
| Command | Description 
|:--- |:--- 
|`git status`| Show modified files in working directory, staged for next commit
|`git add [file]`| Add changes from specified file to the staging area
|`git add .`| Add changes from all files to the staging area
|`git reset [file]`| Unstage a file while retaining the changes in working directory
|`git diff`| View the difference of what is changed but not yet staged
|`git diff --staged`| View the difference of what is staged but not yet committed

### Commit 💬
| Command | Description 
|:--- |:--- 
|`git commit -m “[descriptive message]”`| Commit the staged content as a new commit snapshot
|`git commit --amend -m “[updated commit message]”`| Combine staged changes with previous commit instead of creating a new commit
|`git commit --amend --no-edit`| Make amendment to the commit without changing commit message|
|`git push -u origin [branch-name]`| Push local content to git

### Merge 🧬
| Command | Description 
|:--- |:--- 
|`git merge [branch]`| Merge the specified branch’s history into the current branch

### Compare 📖
| Command | Description 
|:--- |:--- 
|`git log`| View a repo's history
|`git log --oneline`| View repo's history with each commit condensed to one line
|`git log branchB..branchA`| View all the commits that are in branchA but not in branchB
|`git diff branchB...branchA`| View the difference of what is in branchA that is not in branchB

### Move 📦
| Command | Description 
|:--- |:--- 
|`git mv [existing-path] [new-path]`| Change an existing file path and stage the move

### Delete 🗑
| Command | Description 
|:--- |:--- 
|`git branch -D [branch-name]`| Force delete the specified local branch 
|`git push origin --delete [branch-name]`| Delete the specified remote branch
|`git branch --merged | grep -v \* | xargs git branch -D` | Delete all remote branches that have already been merged
|`git ls-files | tr '\n' '\0' | xargs -0 git update-index --assume-unchanged`| Remove files from local without removing from remote
|`rm -rf .git`| Clear git history
|`git remote rm origin`| Remove git origin


### Temporary 🍃
| Command | Description 
|:--- |:--- 
|`git stash`| Saves uncommitted changes (both staged and unstaged) for later use
|`git stash pop`| Reapplies previously stashed changes

