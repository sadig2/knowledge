# delete files except this one grep

    ls | grep -v 'xx.txt' | xargs rm
    ls | grep -v 'xx.txt' | xargs rm -rf
## copy files grep with .json extension

    cp -r  $(ls * |grep .json) xren/

#  stop the process  
    ctrl + z    
bg  move last process to the background

## list all running processes     ====  ps -ef -A 
#  list regex processes  ====  ps -ef | grep "id"
  
    kill all node js processes   ps -ef | grep node
    kill  "pid of node" or pkill -f node
 
**pwd** -- show full path

**sudo  journalctl -xe** shows log  

wget "url"   - to download a file

## change hostname

        sudo hostnamectl set-hostname newhostname

        sudo nano /etc/hosts


## to increase number of files monitored by the system 

                sudo gedit /etc/sysctl.conf

        Add a line at the bottom

        fs.inotify.max_user_watches=524288

        Then save and exit!

        sudo sysctl -p

        to check it


## list all pid of processes

    pgrep "app_name"

    kill $(pgred "app_name")

        