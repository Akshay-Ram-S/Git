## Using Git Hooks for Automated Checks

## Objective

To set up a Git hook to run scripts (like linters) before commits are finalized.

## Commands

***git init task_8 <br>
cd task_8/.git/hooks <br>
touch pre-commit <br>
chmod +x pre-commit <br>
nano pre-commit*** <br>

Go to the hooks directory inside .git directory and create a pre-commit file. <br>
The command "chmod +x pre-commit" command is used to change the file permissions to allow execution. <br>
The pre-commit file is opened in nano editor. <br>

![SS](Screenshots_8/git_8_1.png)
<br><br>

The pre-commit file is written as shown below in nano editor. <br>

![SS](Screenshots_8/git_8_6.png)
<br><br>

***touch eslint.config.js <br>
nano eslint.config*** <br>

![SS](Screenshots_8/git_8_2.png)
<br><br>

We configure the eslint.config.js file to define rules and language options. <br>

![SS](Screenshots_8/git_8_3.png)
<br><br>

***echo "var num = 5" > test.js <br>
git add test.js <br>
git commit -m "Commit with error (Semi-colon missing)"*** <br>

We save test.js with "var num = 5" with a semi-colon missing and we are adding the file to the stage area and committing it. <br>
Since there is error in code, commit will fail as we gave in pre-commit. <br>

![SS](Screenshots_8/git_8_4.png)
<br><br>

***echo "var num = 5;" > test.js <br>
git add test.js <br>
git commit -m "Commit correct code"*** <br>

We are giving the semi-colon and try again to add and commit. <br>
Since there are no errors, the commit is successful. <br>

![SS](Screenshots_8/git_8_5.png)
<br><br>
