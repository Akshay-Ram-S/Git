## Using .gitignore and Tracking Files

## Objective

To set up a .gitignore file to exclude certain files or directories and verify that ignored files are not tracked by Git.

## Commands

The .gitignore file is designed to ignore all the log and temporary files with .log and .tmp extensions. <br>

We have added app.log file, temp.tmp file, main.txt file and .gitignore file to the git repository. <br><br>
***git status*** <br>
The “git status” command is used to display the state of the working directory and the staging area. <br>
The main.txt and .gitignore files are only added whereas app.log and temp.tmp files are ignored.
