# Git


***

 # Basic Git Commands:
 
 ---------------------------------------------------------------------------------------------------
 | touch | nano | git status | git log | git init | git add | git commit | git restore | git died |
 ----------------------------------------------------------------------------------------------------
 
 
 ### How to make a new file:-
 
 > touch file.txt

 
 
 
 ### How to write and modify in the file:-
 
 > nano file.txt 
 
 
 
 
 ### How to show the status:-
 
 > git status
 


 
 ### How to show commit logs:-
 
 > git log
 
 
 

 ### How to shortcut the process of creating a message while creating the file in one line:-
 
 > echo 'mssg' > file.txt
 
 create the file with a massage.
 
 
 ### How to preparing the repository:-
 
 > git init

 to create an empty git repository or reinitiolize an exciting one.
 
 
 ### How to preparing the new changes to be commit:-
 
 > git add file.txt
 
 to add the file content to the index preparing the content staged for the next commit.
 
 
 ### How to commit the changes:-
 
 > git commit -m "mssg"
 
 to record the changes to the repository.
 
 
 ### How to change the last commit:-
 
 > git commit --amend -m "mssg"
 
 to replace the message of the current branch by creating a new commit.
 
 
 ### HOw to restore:-
 
 > git restore file.txt
 
 to restore the previous commit.
 
 
 ### How to see the differences betwtween the versions:- 
 
 > git diff
 
 show the differences between the last modified and the last commits.
 
 
 ***
 # Tags
 
  ---------------------------------------------------------------------------------------------------
 | touch | nano | git status | git log | git init | git add | git commit | git restore | git died |
 ----------------------------------------------------------------------------------------------------
 
 ### How to creating a new tag:-
 
 > git tag tagName
 
 
 ### How to show the content of the tag:-
 
 > git show tagName
 
 
 ### How to delete the tag:-
 
 > git tag -d tagName
 
 
 ### How to show a list of all tags:-
 
 > git tag
 
 
 ***
 # Branches
 
  --------------------------------------------
 | git branch | git checkout |
 --------------------------------------------
 
 
 ### How to create a new  branch:-
 
 > git branch branchName 
 
 
 
 ### How to move from a branch to another branch:-
 
 > git checkout branchName
 
 
 
 ### How to create a new branch and move to that branch:-
 
 > git checkout -b brandName

 to shortcut the process of create the command of creating a new branch and then use the command that moving to the new branch.
 
 
 ### How to show all the branches:-
 
 > git branch
 
 to show the list of all the branches in the project.
 
 
 ### How to delete a branch:-
 
 > git branch -d branchName
 
 to delete a branch from the project.
 
***
# Merge:-

**there is two types of merging:**

- Fast Forward Mergw.
- Three Way Merge.

## Fast Forward Merge:

is a direct linear path from the source branch to the target branch pointer without creating an extra merge commit.


## Three Way Merge:

is based on three different commits:
1. On the master branch, the last commit before we diverge the file into different branches.
2. the last commit performed on the master branch.
3. the last commit performed on the feature branch.










 
 

 
 
 
 

