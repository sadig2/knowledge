## to check which python2 or python3 has pip module
    python -m pip --version  
    python3 -m pip --version  


# manage multiple python versions for ubuntu


    Add python 3.5 & python 3.7 to update-alternatives:

    sudo apt-get install python3.7-venv

    $ sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.6 1
    $ sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.7 2
    Type this command to configure:

    sudo update-alternatives --config python3

# manage multiple python versions for mac

    brew install pyenv
    brew install openssl readline sqlite3 xz zlib

    pyenv install --list
    pyenv install version

    pytest global version



## install python from source

[python_source](https://github.com/julianobarbosa/OpenSUSE-Python3)

## install pip
    apt install python-pip

