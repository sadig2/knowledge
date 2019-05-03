Section "Device"
    	Identifier "Intel Graphics"
    	Driver "intel"
    	Option "AccelMethod" "sna"
    	Option "TearFree" "true"
EndSection

/usr/share/X11/xorg.conf.d
In /xorg.conf.d create a file named 20-intel.conf
