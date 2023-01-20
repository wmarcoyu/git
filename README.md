<h1>Daily workflow with git</h1>

<h3>1. Before writing any new code, do a git pull.</h3>

`git pull <remote_repo> <branch_name>` <br>
<br>
If it works without errors. Go to step 2. <br>

If there is a conflict(merge method not specified), do <br>

`git pull --rebase <remote_repo> <branch_name>` <br>

Then conflicts will show. Fix the conflicts manually in a text editor, and **commit** the changes! <br>

`git add .` <br>

`git commit -m "<commit_message>"` <br>

Now conflicts have been resolved. Continue rebase by doing <br>

`git rebase --continue` <br>

Now commits on the remote branch have been rebased to the front of the  local branch. It is safe to make changes.

<h3>2. Make changes locally.</h3>

<h3>3. Commit changes made and push to the remote repo.</h3>

Commit changes:

`git add .` <br>

`git commit -m "<commit_message>"` <br>

Push changes to the remote repo. <br>

`git push -u <remote_repo> <branch_name>` <br>

Caveat: `<branch_name>` has to match the name of current local branch. <br>

<h2>Useful git commands</h2>

Check current branch name: `git branch` <br>

Change current branch name: `git branch -M <new_name>` <br>

Create a new branch: `git branch <new_branch>` <br>

Switch to a different branch: `git checkout <target_branch>` <br>

Delete a branch: `git branch --delete <branch_name>` <br>
