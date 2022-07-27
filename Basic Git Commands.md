# Git-Commands

## Working Tree->Staging Area->History

### ``` git init ```
  > to start git
### ``` git status ``` 
  > to check tracked and untracked files
### ``` git add . ```
  > to add all the files to the Staging Area
### ``` git commit -m "message to be displayed" ```
  > to commit changes to History
### ``` git commit ```
  > take us to file editor for a more brief commit message to be included with the changes to be committed
### ``` git log ```
  > it tells us about the commit graph
### ``` git log -p ```
  > shows the changes that happened in each commit in detail for a specific file
### ``` git log -- <filename> ```
  > shows the commit commands that affect that specific file
### ``` git diff ```
  > allows us to see the edits/differences in content between working tree and staging area
### ``` git diff --staged ```
  > it shows us the difference between Staging Area and History
### ``` git rm <filename> ```
  > removes the file from both working tree and Staging Area but not the History.(it has to be committed to History for deleting S2 wholly->use git commit -m "removed <filename>")
### ``` git checkout -- <filename> ```
  > changes the file in working tree back to its state present in the Staging Area
### ``` git checkout <SHA1 of commit(first 5 characters)> -- <filename> ```
  > brings that particular file back to its original state after the commit mentioned in this command
### ``` git reset HEAD <filename> ```
  > changes the file in Staging Area back to its state present in the History(added with latest commit command...HEAD refers to the latest commit)
### ``` .gitignore ```
  > a directory that contains the files that you dont want git to track
  
  Source/Reference: https://youtu.be/uR6G2v_WsRA
