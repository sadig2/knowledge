git config --global user.name “sadig2”  
git config --global user.email “clanzu2@yahoo.com”  

git status  

git init    
git rm -rf .git  

touch .gitignore  / edit file 

git add “file” 
git add -A   /add all

git reset “file” /remove from staging 
git reset  / removes all

git commit -m “ commentary”

git log / commits i made  

git reset --hard f414f3(hascode)  **reset whole project to the state of hashcode commit ** 

git clone  url  .  / current directory  / dont initialize git init 



git remote add origin https://github.com/sadig2/newrep.git
git push -u origin master

git pull origin
