## To install i3 windows manager
zypper install i3 dmenu i3status
### copy and paste
to copy just highlight the text  and to paste shit+ctrl+insert   
## generate  configuration file for i3
i3-config-wizard
## configure config file
in directory ~/.config/i3 find file config

bindsym $mod+shift+x exec i3lock  
bindsym F2 exec amixer set Master 5%-  
bindsym F3 exec amixer set Master 5%+  
bindsym F1 exec amixer set Master toggle  
========================
amixer is utility of alsa 
----------------------------
add these lines to the bottom of the document 
and run  shift+super(windows button)+r  to refresh i3

 
