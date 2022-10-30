#   Git Remote Commands
#### ``` git clone <https link> ```
> clone repo you want to
### GIT USERNAMES
     git config --local user.name "<username>"
###### 
     git config --local user.emai1 "<mail>"
#### ``` git remote ```
> displays our remotes
#### ``` git remote -v ``` 
> displays our remotes with full addresses
##### (On displaying the git log using graph we can see origin/master branch existing now.This is the remote-tracking branch which tells us what the master branch looks like at origin.(origin is the remote here...))
#### ``` git fetch origin ```
> to fetch the current status of remote
#### ``` git merge origin/master ```
> merge the commit referenced by origin/master into our local master branch(fast forwarding occurs)
#### ``` git pull ```
> combined working of git fetch and git merge
#### ``` git push ```
> the edits on the local master branch is pushed to the remote
### FORK
> Fork is used to copy a repo from another user to contribute or work with it own your own. This option is available on Github.
#### ``` git remote add <name of remote> <location of the repo to be forked> ```
> adding a remote to a foreign repo
#### ``` git remote remove <remote name> ```
> remove the remote with the specified name
#### ``` git fetch <name of remote> ``` 
> adds a new tracking branch for the specifies remote
