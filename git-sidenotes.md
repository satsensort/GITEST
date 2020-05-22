# To View the Remote Git Repository URL 
1. git config --get remote.origin.url

         # OR #

2.  git remote -v

    output:
    origin  https://github.com/satsensort/learning-k8s.git

# To list all branches

git branch -a 

# To add new Remote Repository as Origin 

 git remote add #repo-name# #repo-url#

 git remote add origin /s/remote-repo

# To See the difference between two branches (Master and Test Branch)

 git diff master test

# To Merge a Git Branch with Master

1. git checkout -b bug-fix
2. vi sample.md #Edit the file 
3. git status #on branch bug-fix
4. git add sample.md 
5. git commit #on branch bug-fix
6. git checkout master #switch to master branch from bug-fix
7. git merge bug-fix #It would replace the contents of sample.md file from bug-fix branch to Master branch


# Git log - To view log details of all branches on a Single Line.

git log --decorate --oneline --graph --all

# Fixing Git Conflicts between local and remote repositories

The simplest way to fix a conflict is to pick either the local or remote version by using 
 
 git checkout --theirs Quotes.txt 
 
 OR
 
 git checkout --ours Quotes.txt
  
 OR 

 git mergetool

If you need more control, manually edit the file(s) like normal.
Once the files are in the desired state, checkout either manually or by using Git. Stage and commit the changes. When committing, a default commit message is created with details of the merge and the conflicted files.

# To revert to previous state in middle of merge
To revert to the previous state during the middle of a merge, and try again, use the command: 

git reset --HARD head;.

git commit --no-edit to use the default commit message.

# To view difference between local master and remote master

git diff master origin/master

# To Compare the head with upstream branch

git diff @{upstream} 

# To Rebase the local master to remote master branch 

git pull --rebase origin master

# To abort rebase operation

git rebase --abort

# To Restore Deleted Files

# How to restore a deleted file ?

First, find the commit ID where the file was deleted: 

git rev-list -n 1 HEAD -- filename

Then checkout to that commit ID to get back the file using:

git checkout deletingcommitid^ -- filename

# Git Cheat Sheet 

git revert <commit>: Creates a new commit that undoes all changes made in the commit and applies it to the current branch

git reset <file>: Moves file changes from staging area to working directory.

git reset <commit>: Moves current branch's HEAD tip to the old <commit>. All the changes in the commits (that you skipped to move to the old commit) are moved to the working area.

git commit --amend: Adds staged changes to the last commit and allows for editing the old commit message

git rm --cached(file_name): Untracks the current file

git checkout <commit>: Switches the HEAD to the provided commit

## To Add a new file or edit the file to the previous commit 

# If editing an existing file, perform the changes to that file using VIM and then perform git add

 git add new-file OR old-file
 git commit --amend -m "new commit message" 

  OR 
 
 git commit --amend --no-edit

# To view changes between working tree and last commit 

git diff HEAD

# To clear the changes made in the working directory

$ git checkout filename

