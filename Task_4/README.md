## Simulating and Resolving Merge Conflicts

## Objective

To create a scenario that produces a merge conflict and resolve it.

## Commands

***git init <br>
echo "Content in file" > file.txt <br>
git add file.txt <br>
git commit -m "Initial Commit"*** <br><br>
The initial commits are made in the master branch.<br><br>

***git checkout -b branch1 <br>
echo "branch1 content" > file.txt <br>
git add file.txt <br>
git commit -m "Edit file in branch1"*** <br><br>
We create branch1 and commit the above changes in file.txt. <br><br>

***git checkout master <br>
git checkout -b branch2 <br>
echo "branch2 content" > file.txt <br>
git add file.txt <br>
git commit -m "Edit file in branch2"*** <br><br>
We create branch2 and commit the same changes we did in branch1. <br><br>

***git merge branch1 <br>
git status*** <br><br>
When we merge branch1 into branch2, we get the above CONFLICT : Merge conflict in file.txt. <br> 
We use the “git status” command to display the state of the staging area.<br>
We manually go to the file.txt and change it manually however we would like it to be. <br><br>

***git add file.txt <br>
git commit -m "Resolved Conflict" <br>
git checkout master <br>
git merge branch2*** <br><br> 
After changing the file manually, we commit the file on branch2. Then, we move to the master branch and merge branch2. <br>

