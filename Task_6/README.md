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

***git checkout -b new-feature <br>
echo "Work on new feature" >> file.txt <br>
git add file.txt <br>
git commit -m "Add new feature"***


