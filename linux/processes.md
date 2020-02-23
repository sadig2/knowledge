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

        