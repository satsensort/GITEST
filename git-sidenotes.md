# To View the Remote Git Repository URL 
1. git config --get remote.origin.url
         OR
2.  git remote -v

    output:
    origin  https://github.com/satsensort/learning-k8s.git

# To add new Remote Repository as Origin 

git remote add <repo-name> <repo-url>

git remote add origin /s/remote-repo

# To See the difference between two branches (Master and Test Branch)

git diff master test
