## Initialize, Commit, and Branch Basics

## Objective
To demonstrate basic Git operations by initializing a repository, creating and committing files, branching, making changes, merging branches, and viewing commit history.

## Commands with Screenshots

***mkdir task_1*** <br>
The above command creates a directory named task_1. <br><br>
***cd task_1*** <br>
The above command changes the directory to task_1. <br><br>
***git init*** <br>
The above command is used to initialize a git repository. <br><br>

The “echo” command is used to create files file1.txt and file2.txt with some text.<br><br>
***git add file1.txt*** <br>
The above command is used to add the file to the staging area. <br><br>
***git commit -m "Added file1.txt"*** <br>
The above command is used to commit the file to the repository.<br><br>

***git checkout -b branch1*** <br>
The above command allows us to create and switch to a new branch - branch1. <br>
The “echo” command is used to change the contents of file1.txt. <br><br>
***git add file1.txt*** <br>
***git commit -m "Updated file1 in branch1"*** <br>
The “git add” and “git commit” commands are used to add and commit the changes in the new branch - branch1. <br><br>

***git checkout master*** <br>
The above command is used to switch back to the master branch. <br><br>
***git merge branch1*** <br>
The “git merge” command is used to merge branch1 into master.<br><br>

***git log --oneline --all*** <br>
The “git log” command is used to see the commit history in the current branch.
-- oneline : shows each commit on a single line.
--all : displays commit history on all branches.
