## Working with Remote Repositories and Collaboration

## Objective
To simulate a collaborative workflow with remote repositories.

## Commands

```bash
git init task_9 
cd task_9 
echo "Initial Content" > file.txt 
git add file.txt 
git commit -m "Initial Commit"
```
Initial commit is made after initializing repository. <br>

![SS](Screenshots_9/git_9_1.png)
<br><br>

```bash
git remote add origin https://github.com/Akshay-Ram-S/Git 
git push -u origin master 
git checkout -b new-branch 
echo "Content changed" >> file.txt 
git add file.txt 
git commit -m "Update file.txt"
```
We add the url of the repository to link it remotely and we push the initial commit to it. <br>
We create new branch and modify the file content and commit it. <br>

![SS](Screenshots_9/git_9_2.png)
<br><br>

```bash
git push -u origin new-branch
```
We push the new-branch to git. <br>

![SS](Screenshots_9/git_9_3.png)
<br><br>

We open github and see the pull requests and click on comapre and pull request. <br>

![SS](Screenshots_9/git_9_4.png)
<br><br>

Then we create a pull request in github. <br>

![SS](Screenshots_9/git_9_5.png)
<br><br>

The code review process is carried out. Reviewers can comment on code changes and approve the PR. <br>

![SS](Screenshots_9/git_9_6.png)
<br><br>

```bash
git checkout master
git pull origin master
```
The above commands are used to pull the merged changes locally. <br>

![SS](Screenshots_9/git_9_7.png)

