## set up volume and brigtness control for i3 in ubuntu 
    sudo apt-get update; sudo apt-get install xbacklight alsa-utils pulseaudio

## install and move i3blocks.conf to .config/i3/  
	apt install i3blocks 
	sudo mv  /etc/i3blocks.conf ~/.config/i3

## then add lines to config 

# Pulse Audio controls
 bar { 
        status_command i3blocks -c ~/.config/i3/i3blocks.conf 
} 
 
bindsym XF86AudioRaiseVolume exec --no-startup-id pactl -- set-sink-volume 0 +5% #increase sound volume 
bindsym XF86AudioLowerVolume exec --no-startup-id pactl -- set-sink-volume 0 -5% #decrease sound volume 
bindsym XF86AudioMute exec --no-startup-id pactl set-sink-mute 0 toggle # mute sound 
 
# Sreen brightness controls 
bindsym XF86MonBrightnessUp exec xbacklight -inc 20 # increase screen brightness 
bindsym XF86MonBrightnessDown exec xbacklight -dec 20 # decrease screen brightness 
 
 
 
bindsym $mod+c exec chromium-browser 
bindsym $mod+i exec /opt/apps/idea-IU-191.7141.44/bin/./idea.sh 
bindsym $mod+p exec /opt/apps/pycharm-2019.2.1/bin/./pycharm.sh 
bindsym $mod+shift+x exec i3lock 
exec_always setxkbmap -option grp:alt_shift_toggle us,ru 
bindsym $mod+t exec /opt/apps/Telegram/Telegram


(san fransisco font)[https://github.com/supermarin/YosemiteSanFranciscoFont]

## osx render 
    sudo add-apt-repository ppa:no1wantdthisname/ppa
    sudo apt-get update
    sudo apt-get upgrade
    sudo apt-get install fontconfig-infinality


## set up i3blocks  bar

    [volume]
    label=VOL
    #label=♪
    instance=Master
    #instance=PCM
    interval=1
    signal=10
    command=/usr/share/i3blocks/volume 5 pulse


add this code in i3blocks.conf  after you moved it to .config/i3

