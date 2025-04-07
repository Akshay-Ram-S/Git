## Undoing Changes and Reverting Commits

## Objective

To experiment with undoing changes in our working directory and commits.

## Commands

***git log --oneline*** <br>
***git restore file1.txt*** <br>
***git revert head --no-edit*** <br>
***git log --oneline*** <br><br>
The “git restore” command will discard the new changes, reverting file1.txt to the last committed state. <br>
The “git revert” command is used to create a new commit that undoes the changes from the "Second Commit" and --no-edit means no message is included. <br>
The “git log” command is used to see the past commits for comparison. <br>

![SS](Screenshots_3/git_3_1.png)
<br><br>


***git log --oneline <br>
git reset --soft 96b8c53 <br>
git log --oneline <br>
git reset --hard 96b8c53 <br>
git log --oneline <br>
git reset --mixed 96b8c53*** <br><br>
The “git reset” command is used to reset when we want to move the repository back to a previous commit, discarding any changes made after that commit.<br>
soft reset - moves HEAD back, but the changes remain staged. <br>
hard reset - completely removes the commit and its changes from the working directory and history. <br>
mixed reset - moves HEAD back, unstages the changes, but keeps them in your working directory. <br>

![SS](Screenshots_3/git_3_2.png)
<br><br>


<br> ***git checkout*** vs ***git restore*** <br>
**git checkout** - Originally used for switching branches and checking out commits. Over time, it’s also been used to discard changes in files. <br>
**git restore** - Designed specifically to restore files to their last committed state, making it more intuitive for undoing changes. <br><br>

***git revert vs git reset*** <br>
**git revert** - Creates a new commit that undoes the changes introduced by a previous commit. The commit history remains, which is crucial for shared/public branches. <br>
**git reset** - Moves the HEAD pointer to a different commit, effectively removing commits from the history (hard or mixed resets). It can affect both the commit history and your working directory depending on the mode used. <br>


