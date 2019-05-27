---
title: "git and github"
author: "Milca Tarshish"
date: "5/27/2019"
output: 
  html_document:
    keep_md: true
---

### git hub  
[git hub site](https://github.com/Milcat) is the location to see all git checked in repositories and files.  

### git bash 
git bash is a windows sw that can connect between local computer files and git hub.  

### git fork  
git fork <url path> will fork someone else git repo to our git hub - as a new repository.  
This is done form the github.  

### git init  
from git bash: to open a new repository in the current directory:  
*git init*  

### git remote add
from git bash: after opening a new git repo in our local computer with git init - we can connect it to a github url by:  
*git remote add origin http://github.com/Milcat/new_repo_name*  

### git clone  
In order to clone a repo from github to local computer:  
*git clone http://github.com/Milcat/repo_name*  

### git add  
adding a new file (that is not in repo yet) to repo:  
*git add filename*  

### git commit
doing check-in to repo of new added files, or of edited files:  
*git commit -m "add a comment here" file1 file2 file3* 

### git push  
to push all commited files from local computer - to github:  
*git push*  

### git status   
to get a status in git bash - of all files under current directory:  
*git status*  

### git branch  
to checkout a specific version of the repo (will be checked out to a local branch):  
*git branch -b branchname*   

To see in which branch we are:  
*git branch*  

to get back to master branch:  
*git branch master*  



