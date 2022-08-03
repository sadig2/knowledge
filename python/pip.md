## to check which python2 or python3 has pip module
    python -m pip --version  
    python3 -m pip --version  


# manage multiple python versions 


    Add python 3.5 & python 3.7 to update-alternatives:

    $ sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.6 1
    $ sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.7 2
    Type this command to configure:

    sudo update-alternatives --config python3


## install python from source

[python_source](https://github.com/julianobarbosa/OpenSUSE-Python3)

## install pip
    apt install python-pip

