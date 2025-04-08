## Interactive Rebasing for Clean Commit History

## Objective

To demonstrate how to clean up a commit history using Git's interactive rebase feature, which helps in maintaining a readable and organized project history.

## Commands

***git init task_5 <br>
cd task_5 <br>
echo "Initial content" > file.txt <br>
git add file.txt <br>
git commit -m "Initial commit"*** <br>

We initialize a repository, add a text file and commit it. <br>


<br><br>

***echo "First change" >> file.txt <br>
git add file.txt <br>
git commit -m "First change commit" <br>
echo "Second change" >> file.txt <br>
git add file.txt <br>
git commit -m "Second change commit" <br>
echo "Third change" >> file.txt <br>
git add file.txt <br>
git commit -m "Third change commit"*** <br>

A series of commits are made.


<br><br>

***git rebase -i HEAD~3*** <br>
The above command opens up previous 3 commits in the editor. <br>


<br><br>

We are using “squash” to combine the lastt commit with the immediate previous commit. <br>
The following are the commands available: <br>
p, pick = use commit <br>
r, reword = use commit, but edit the commit message <br>
e, edit = use commit, but stop for amending <br>
s, squash = use commit, but meld into previous commit <br>
f, fixup = like "squash", but discard this commit's log message <br>
x, exec = run command (the rest of the line) using shell <br>
d, drop = remove commit <br>

After changing the desired commands, we will save and exit the editor and another editor will be opened as shown below. <br>
Here we can edit the commit messages if required. After editing/confirming, save the editor and close it. It will redirect you to the git bash terminal. <br>


<br><br>

***git log --oneline***
Since we used the squash command, the "Third change commit" and "Second change commit" are converted into one single commit as "Combined commit". <br>


<br><br>

**Squashing** <br>

Squashing helps by combining multiple commits into a single, coherent commit before merging into the main branch. <br>
When working on a feature branch, you often make multiple commits to implement a feature and fix bugs. <br>
These changes might be sometimes very minor and need not be listed as separate commits. We can combine all these minor commits into one major commit. <br>

*Advantages* <br>
1. Cleaner and readable commit history <br>
2. Easier code reviews

