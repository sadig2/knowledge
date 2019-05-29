    bar {
            status_command i3blocks -c ~/.config/i3/i3blocks.conf
    }
    # Pulse Audio controls
    bindsym XF86AudioRaiseVolume exec --no-startup-id pactl -- set-sink-volume 0 +5% #increase sound volume
    bindsym XF86AudioLowerVolume exec --no-startup-id pactl -- set-sink-volume 0 -5% #decrease sound volume
    bindsym XF86AudioMute exec --no-startup-id pactl set-sink-mute 0 toggle # mute sound
    
    # Sreen brightness controls
    bindsym XF86MonBrightnessUp exec xbacklight -inc 10 # increase screen brightness
    bindsym XF86MonBrightnessDown exec xbacklight -dec 10 # decrease screen brightness
    
   bindsym $mod+c exec chromium-browser
   bindsym $mod+i exec /opt/apps/idea-IU-191.7141.44/bin/./idea.sh
   bindsym $mod+p exec /opt/apps/pycharm-2019.1.2/bin/./pycharm.sh
   bindsym $mod+shift+x exec i3lock
   exec_always setxkbmap -option grp:alt_shift_toggle us,ru
   bindsym $mod+t exec /opt/apps/Telegram/Telegram

    