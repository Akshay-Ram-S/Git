## Working with Remote Repositories and Collaboration

## Objective
To simulate a collaborative workflow with remote repositories.

## Commands

***git init task_9 <br>
cd task_9 <br>
echo "Initial Content" > file.txt <br>
git add file.txt <br>
git commit -m "Initial Commit"*** <br>

Initial commit is made after initializing repository. <br>


<br><br>

***git remote add origin https://github.com/Akshay-Ram-S/Git <br>
git push -u origin*** <br>

We add the url of the repository to link it remotely and we push the initial commit to it. <br>


<br><br>

***git checkout -b new-branch <br>
echo "Content changed" >> file.txt <br>
git add file.txt <br>
git commit -m "Update file.txt"*** <br>

We create new branch and modify the file content and commit it. <br>


<br><br>

***git push -u origin new-branch*** <br>

We push the new-branch to git. <br>


***git checkout master <br>
git pull origin master*** <br>

The above commands are used to pull the merged changes locally. <br>





