## To install i3 windows manager

    zypper install i3 dmenu i3status

## configure screen resolution

    xrandr -s 1920x1080

### copy and paste

    to copy just highlight the text  and to paste shit+ctrl+insert

## generate configuration file for i3

    i3-config-wizard

## configure config file

    in directory ~/.config/i3 find file config

    bindsym $mod+shift+x exec i3lock
    bindsym F2 exec amixer set Master 5%-
    bindsym F3 exec amixer set Master 5%+
    bindsym F1 exec amixer set Master toggle

========================
amixer is utility of alsa

---

add these lines to the bottom of the document
and run shift+super(windows button)+r to refresh i3

## set layout switch in i3

    bindsym F11 exec setxkbmap ru
    bindsym F12 exec setxkbmap gb

## edit i3status.conf

    vim /etc/i3status.conf

###

[i3status.conf](https://i3wm.org/i3status/manpage.html) -to set up further

## change layout i3 xkb

    setxkbmap -option grp:alt_shift_toggle us,ru

## add screenshooter shortcut first install xfce4-clipman

        sudo apt install xfce4-clipman

## then optionally create .sh file in /opt/apss and add lines >

        xfce4-screenshooter -r -c
