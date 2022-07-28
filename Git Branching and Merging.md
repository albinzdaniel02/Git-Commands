# Git Branching and Merging

#### MASTER
  > the original branch created by git automatically
#### HEAD
  > shows the branch we are viewing

### ``` git log ```
  > show our commit history
### ``` git log --all --decorate --oneline --graph ```
  > better labelled commit graph
### ``` alias <alt. name> = "original git command you want to replace" ```
  > for frequent usage of long commands, we can use short aliases for our convenience

##### Example:
##### alias graph="git log --all --decorate --oneline --graph"
##### Calling "graph" next time actually does the command on the RHS.

### ``` git branch <branch_name> ```
  > creates a branch with the name specified
### ``` git branch ```
  > shows us all the branches that exist along with the one we are checking out with an asterisk in the front and green color
### ``` git checkout <branch_name> ```
  > moves HEAD to branch specified
### ``` nano <filename> ```
  > to open command line text editor
### ``` git commit -a -m "message" ```
  > stage and commit modified files in one step
### ``` git diff master..<branchname> ```
  > shows the difference in data that can happen if that branch is merged with the master
### ``` git branch --merged ```
  > allows us to see which all branches merged
### ``` git branch -d <branchname> ```
  > allows us to delete that branch that has been completely merged(a warning is provided if its not fully merged)
### ``` git branch -D <branchname> ```
  > allows us to delete that branch that has been completely merged(**_NO_** warning is provided if its not fully merged)

#### FAST FORWARD MERGE
  > when there exists a direct path between the 2 versions(the latest version will be committed and pointer moves there)

#### THREE WAY MERGE
  > when there doesn't exists a direct path(done automatically using the same command:git merge <branchname>),a new merge commit is made to join the 2 versions

### ``` git checkout -b <branchname> ```
  > does the combined function of "git branch <branchname>" and "git checkout <branchname>"
### ``` git merge --abort ```
  > used in cases of conflicts between versions(helps us in resolving the conflicts ourselves)

#### change vs no change in a line:change wins

#### same change:change is committed

#### deleting a line in one version also brings conflict)
  
### RESOLVING:
  > open the file and edit it (use nano command mentioned earlier if you want to)accordingly you want it in the latest version
then "git  add < filename >" to add the edited file but merging is still happening...so do "git commit" command too

### DETACHED HEAD STATE
#### use git checkout <version hash>->HEAD is not attached to this version...(HEAD,stage) is seen generally
#### use git checkout stage(it is that version you checked out first but HEAD is now attached to it)
### ``` git stash ```
  > to clear the working tree(by saving uncommitted changes to be worked on later when switching to a different version without committing)
### ``` git stash list ```
  > list out the stashed edits
### ``` git stash list -p ```
  >list and shows the changes not saved in each stash...(shows the difference in files)
### ``` git stash apply ```
  > apply all the stashed edits to the working directory and commit them to save them(does NOT  remove the stash from the stash list)
### ``` git stash apply <label of the stash-Ex: stash@{0}> ```
  > apply that particular stash to your working directory(does NOT remove the stash from the stash list)
### ``` git stash pop ```
  > apply the latest stash to your working directory(removes the stash from the stash list)
### ``` git stash save <message or name> ```
  > create a stash at that point with a description or name as given
  
  Source/Reference: https://youtu.be/FyAAIHHClqI
