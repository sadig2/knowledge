sudo zypper ar -cfp 90 -n Packman http://ftp.gwdg.de/pub/linux/misc/packman/suse/openSUSE_Leap_15.0/ packman
sudo zypper ref
sudo zypper in vlc vlc-codecs
sudo zypper dup --from packman --allow-vendor-change
