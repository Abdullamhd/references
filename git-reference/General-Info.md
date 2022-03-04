General Git Information 
---

## List git configuration files 
```git config --list```

## Getting help from Git manual 
Examples : 
- git add -h 
- git commit - 
- git help config 


## Generic git from Base chapter 
- ``` git status -s ``` # this short list of status of the file 
- ``` git diff ``` ## compare between working dir and staged 
- ``` git diff --staged ``` ## for what you staged so far 

## Git Commiting the change 
- ``` git commit -v ``` ## used for pass the changes to commit editor so every changes displays clearly 
- ``` git commit -v -a ``` ## Skipping the Staging Area in GIT 

---

## Removing files 

1- First Remove the file from working directory 
2- then run the ``` git rm FileName ``` and it's stage the file removal 
3- commit the removal of the file 

## This is particularly useful if you forgot to add something to your .gitignore file and accidentally staged it, like a large log file 


```
git rm --cached README
```

---
## Git log 

### For showing the difference between each commit (Very helpful)
- ```git log -p```

### For showing log for specific branch 
- git log branchname --decorate --oneline

### for showing log in all branches 
- git log --all 
### this option display how many lines added , how many files modified , how many lines removed etc
- git log --stat

## This option will display the summary of commit log
- git log --pretty --oneline

## takes a string and shows only those commits that changed the number of occurrences of that string
- git log -S functionName | SearchString 

## If you specify a directory or file name, you can limit the log output to commits that introduced a change to those files. 
- git log -- path/to/file


## display graph of logs 
- git log --oneline --decorate --graph --all

## Show the log by author name 
- ```git log --author "Abdullah" ```

---
## Undoing Things 

### redo that commit, make the additional changes you forgot, stage them, and commit again using the ```--amend``` option  

```bash
git commit --amend 
```

## Unstaging the staged file (this suggestion available when we type git status)

- git restore --staged CONTRIBUTING.md

---

## Unmodifying a Modified File 

- git checkout filename 

## Unmodifying a Modified File with git restore

- git restore CONTRIBUTING.md
- git restore fileame --staged


 ---

 ## working with remote
 ### to display the remote urls :
 - git remote -v 
 ### This will display more information
 - git remote show origin 


 ---
 ## Tagging 
 ### Listing the tags 
 - git tag 
 - git tag -l 
 - git tag -l "seach term"
 ### It's recommended to create Annotated tag 

#### Creating Annotated TAG 
 -  git tag -a v1.4 -m "my version 1.4"
 -  git show v1.4 
 - 
#### Create tag for specifc commit ID 
 -   git tag -a v1.2 9fceb02
#### push tags 
- git push origin --tags
- git push origin v1.5

#### Deleting tag
- git tag -d tagname
####  Delete remote tag
- git push origin --delete v1.0 
---
### Branching & Merging

#### Creating new branch and switching to 
- git checkout -b branchName
- git switch -c newBranch 
##### Return to previously created branch
- git switch - 

##### Delete branch
- ```git branch -d branchName ```

##### to see the last commit in branch 
- ``` git branch -v ``` 




