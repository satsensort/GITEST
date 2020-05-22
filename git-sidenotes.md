# To View the Remote Git Repository URL 
1. git config --get remote.origin.url

         # OR #

2.  git remote -v

    output:
    origin  https://github.com/satsensort/learning-k8s.git

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

git log --all --decorate --oneline

# Fixing Git Conflicts between local and remote repositories

The simplest way to fix a conflict is to pick either the local or remote version by using 

 git checkout --theirs Quotes.txt 
 OR 
 git checkout --ours Quotes.txt

If you need more control, manually edit the file(s) like normal.
Once the files are in the desired state, checkout either manually or by using Git. Stage and commit the changes. When committing, a default commit message is created with details of the merge and the conflicted files.

# To revert to previous state in middle of merge
To revert to the previous state during the middle of a merge, and try again, use the command: 

git reset --HARD head;.

git commit --no-edit to use the default commit message.


