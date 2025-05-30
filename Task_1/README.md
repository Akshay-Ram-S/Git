## Initialize, Commit, and Branch Basics

## Objective
To demonstrate basic Git operations by initializing a repository, creating and committing files, branching, making changes, merging branches, and viewing commit history.

## Commands

```bash
mkdir task_1
cd task_1 
git init
```

The “mkdir task_1” command creates a directory named task_1. <br>
The “cd task_1” command changes the directory to task_1. <br>
The “git init” is used to initialize a git repository. <br>

![SS1](Screenshots_1/git_1_1.png)
<br><br>


```bash
echo "Text for file1" > file1.txt 
git add file1.txt
git commit -m "Added file1.txt" 
echo "Text for file2" > file2.txt 
git add file2.txt 
git commit -m "Added file2.txt"
```
The “echo” command is used to create files file1.txt and file2.txt with some text.<br>
The "git add" command is used to add the file to the staging area. <br>
The "git commit" command is used to commit the file to the repository.<br>

![SS2](Screenshots_1/git_1_2.png)
<br><br>

```bash
git checkout -b branch1
git add file1.txt 
git commit -m "Updated file1 in branch1"
```
The "git checkout" command allows us to create and switch to a new branch - branch1. <br>
The “echo” command is used to change the contents of file1.txt. <br><br>
The “git add” and “git commit” commands are used to add and commit the changes in the new branch - branch1. <br>

![SS3](Screenshots_1/git_1_3.png)
<br><br>

```bash
git checkout master
git merge branch1
```
The "git checkout" is used to switch back to the master branch. <br>
The “git merge” command is used to merge branch1 into master.<br>

![SS4](Screenshots_1/git_1_4.png)
<br><br>


```bash
git log --oneline --all
```
The “git log” command is used to see the commit history in the current branch.<br>
-- oneline : shows each commit on a single line. <br>
--all : displays commit history on all branches. <br>

![SS5](Screenshots_1/git_1_5.png)
