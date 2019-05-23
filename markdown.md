[article](https://devpew.com/knowledgebase/)
```html
sudo dpkg-reconfigure tzdata  
sudo apt update && sudo apt upgrade -y
sudo apt install -y curl wget vim git unzip socat bash-completion apt-transport-https build-essential


curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -

sudo apt install -y nodejs 



sudo npm install -g npm@latest

sudo mkdir /var/www/gitbook  
cd /var/www/gitbook  
npm install gitbook-cli -g  
gitbook init   - ## generates readme.md and summary files inside docs 

vim book.json  - # outside of docs in gitbook directory  



{
        "root": "./docs",  
        "title": "dpkb",  
        "author": "devpew",  
        "description": "just my knowledge",  
        "plugins": [  
                "folding-chapters-2",  
                "theme-code",  
                "-sharing"  
        ],  
        "pluginsConfig": {  
                "theme-default": {  
                        "showLevel": false  
                }  
        }  
}  

gitbook install  -generate two md files


npm install -g gitbook-summary    - plugin to generate summary file 

book sm g    - inside docs file  
gitbook serve

 
  