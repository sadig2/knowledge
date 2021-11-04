git config --global user.name “sadig2”  
git config --global user.email “clanzu2@yahoo.com”

git status

git init  
git rm -rf .git

touch .gitignore / edit file

git add “file”
git add -A /add all

git “file” /remove from staging
git reset / removes all

git commit -m “ commentary”

git log / commits i made

git reset --hard f414f3(hascode) **reset whole project to the state of hashcode commit **

git clone url . / current directory / dont initialize git init

git remote add origin https://github.com/sadig2/newrep.git
git push -u origin master

git pull origin

## to save local data temporarily before pull - so it ll be invisible to later return it

    git stash save "name of the file or directory"

## to make saved data visible type in

    git stash apply

## git clone specific branch 
    git clone --single-branch --branch <branchname> <remote-repo>


// delete branch locally
git branch -d localBranchName

// delete branch remotely
git push origin --delete remoteBranchName

## to remove remote origin

    git remote remove origin

## untrack all files -r recursive all files in directory . means untrack all

    git rm -r --cached .

## to show old hidden detached commits

    git reflog

## to add detached commit into new branch

    git branch new-branch ba5a739

## then i can merge it checking out in master branch beforehands

    git checkout master
    git merge new-branch

## to force git to push

    git push -f

## to delete commit locally and remotely 
    git reset --hard {commit id}
    git push --force

# git change url 

    git remote set-url origin

#  squash all commits in branch into 1
    git merge --squash feature/login

# delete all branches except master
    git branch | grep -v "master"| xargs git branch -D {}