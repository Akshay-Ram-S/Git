## Stashing Changes for Context Switching

## Objective
To learn how to use Git stash to save uncommitted work temporarily.

## Commands

***git init task_6 <br>
cd task_6 <br>
echo "Initial content" > file.txt <br>
git add file.txt <br>
git commit -m "Initial commit"*** <br><br>

Initial commit is made after initializing and adding file.txt. <br>

<br><br>

***echo "Uncommitted changes" > file.txt <br>
git stash*** <br><br>

The above command will stash the changes in your working directory and revert the file to last committed state. <br>


<br><br>

***git checkout -b new-branch <br>
echo "New branch opened" >> file.txt <br>
git add file.txt <br>
git commit -m "Changes made in new branch"*** <br><br>
A new branch is created and some changes are made in file.txt and committed. <br><br>


<br><br>

***git checkout master <br>
git stash pop <br>
git log --oneline*** <br><br>

The branch is switched back to the master branch. <br>
The "git stash pop" command applies the stashed changes back to the working directory and removes the stash from the stash list. <br>


<br><br>

***echo "Content for stash 1" >> file.txt <br>
git stash <br>
echo "Content for stash 1" >> file.txt <br>
git stash <br>
echo "Content for stash 1" >> file.txt <br>
git stash*** <br><br>

Creating a list of stash. <br>


<br><br>

***git stash list <br>
git stash drop stash@{2} <br>
git stash list <br>
git stash clear <br>
git stash list*** <br><br>

The "git stash list" is used list all the saved stashes. <br>
The "git stash drop" is used to delete a specific stash from the stash list. <br>
The "git stash clear" is used to reomve all stashes in the list. <br>




