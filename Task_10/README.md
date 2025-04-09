## Comprehensive Workflow with Forced Pushes and Recovery

## Objective

To simulate an advanced Git scenario that includes forced pushes, recovering lost commits, and a multi-branch workflow.

## Commands

***git init task_10 <br>
cd task_10 <br>
echo "Initial commit" > file.txt <br>
git add file.txt <br>
git commit -m "Initial commit on master branch"*** <br>

Initialized a repository, added file.txt and made on commit on it. <br>

![SS](Screenshots_10/git_10_1.png)
<br><br>

***git remote add origin https://github.com/Akshay-Ram-S/Test.git <br>
git checkout -b feature <br>
echo "Feature implementation" > feature.txt <br>
git add feature.txt <br>
git commit -m "Add feature"*** <br>

Add the origin and give the github link to store repository. <br>
Created "feature" branch, added feature.txt and made commit. <br>

![SS](Screenshots_10/git_10_2.png)
<br><br>

***git checkout master <br>
git checkout -b bug-fix <br>
echo "Bug fix implementation" > bug-fix.txt <br>
git add bug-fix.txt <br>
git commit -m "Fix bug"*** <br>

Created "bug-fix" branch, added bug-fix.txt and made commit. <br>

![SS](Screenshots_10/git_10_3.png)
<br><br>

***git checkout master <br>
git checkout -b release <br>
echo "Release notes" > release.txt <br>
git add release.txt <br>
git commit -m "Release notes commit"*** <br>

Created "release" branch, added release.txt and made commit. <br>

![SS](Screenshots_10/git_10_4.png)
<br><br>

***git push -u origin feature <br>
git checkout feature <br>
echo "Feature complete" >> feature.txt <br>
git add feature.txt <br>
git commit -m "Feature complete" <br>
git rebase -i HEAD~2*** <br>

Switched to feature branch, made changes in feature.txt and made commit. <br>

![SS](Screenshots_10/git_10_5.png)
<br><br>

The rebase opens and we change the second commit as "squash" to combine both commits. <br>

![SS](Screenshots_10/git_10_6.png)
<br><br>

**Forced Push :** <br>

***git push -u origin feature <br>
git push --force origin feature*** <br>

Since we’ve rewritten history, Git will not allow a regular push and will instead require a forced push as we can see below. <br>
The --force option for git push allows you to override this rule: the commit history on the remote will be forcefully overwritten with your own local history. <br>

![SS](Screenshots_10/git_10_7.png)
<br><br>

**Simulate a mistake and recover lost commit :** <br>

***git checkout master <br>
echo "Second commit" >> file.txt <br>
git add file.txt <br>
git commit -m "Second commit" <br>
git reset --hard HEAD~1 <br>
git push --force origin master*** <br>

We make a commit again so that now we have two commits. The "git reset --hard HEAD~1" command is used to revert back one commit. The last commit is gone, and the history has been rewritten and pushed. <br>
The force push is a dangerous operation, as any changes that others may have made are now lost and rewritten

![SS](Screenshots_10/git_10_8.png)
<br><br>

***git reflog*** <br>

The reflog is a powerful tool for maintaining a safety net in your Git repository and recovering from various accidental or unexpected changes, such as those times when you need to recover lost commits or branches and have lost track of your Git history. <br>

![SS](Screenshots_10/git_10_9.png)
<br><br>

***git checkout HEAD@{1} <br>
git checkout -b recover-branch <br>
git push origin recover-branch <br>
git log --oneline*** <br>

The "git checkout HEAD@{1}" is used to recover the commit we want. <br>
Create a new branch with the recover commit and push it to the repository. <br>
The "git log" command is used to verify the commits. <br>

![SS](Screenshots_10/git_10_10.png)
<br><br>

***Best practices for collaborating with teams when rewriting history and using force pushes***

1. Force pushes should only be used when absolutely necessary. <br>
2. Always inform your team when performing a force push. <br>
3. The --force-with-lease option is a safer alternative to --force, as it ensures that you can only force push if your local branch is up-to-date with the remote branch. <br>
4. If you absolutely need to perform a force push, it’s a good idea to create a backup branch first, just in case something goes wrong. 


