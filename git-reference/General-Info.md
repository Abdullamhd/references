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