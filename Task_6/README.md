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

![SS](Screenshot_6/git_6_1.png)
<br><br>

***echo "Uncommitted changes" > file.txt <br>
git stash*** <br>

The above command will stash the changes in your working directory and revert the file to last committed state. <br>

![SS](Screenshot_6/git_6_2.png)
<br><br>

***git checkout -b new-branch <br>
echo "New branch opened" >> file.txt <br>
git add file.txt <br>
git commit -m "Changes made in new branch"*** <br><br>
A new branch is created and some changes are made in file.txt and committed. <br>

![SS](Screenshot_6/git_6_3.png)
<br><br>

***git checkout master <br>
git stash pop <br>
git log --oneline*** <br>

The branch is switched back to the master branch. <br>
The "git stash pop" command applies the stashed changes back to the working directory and removes the stash from the stash list. <br>

![SS](Screenshot_6/git_6_4.png)
<br><br>

***echo "Content for stash 1" >> file.txt <br>
git stash <br>
echo "Content for stash 1" >> file.txt <br>
git stash <br>
echo "Content for stash 1" >> file.txt <br>
git stash*** <br>

Creating a list of stash. <br>

![SS](Screenshot_6/git_6_5.png)
<br><br>

***git stash list <br>
git stash drop stash@{2} <br>
git stash list <br>
git stash clear <br>
git stash list*** <br>

The "git stash list" is used list all the saved stashes. <br>
The "git stash drop" is used to delete a specific stash from the stash list. <br>
The "git stash clear" is used to reomve all stashes in the list. <br>

![SS](Screenshot_6/git_6_6.png)


