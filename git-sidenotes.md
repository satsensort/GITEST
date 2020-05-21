# To View the Remote Git Repository URL 
1. git config --get remote.origin.url

         #OR#

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
