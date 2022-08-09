## copy foldre from local to remote

    scp -r /local/directory remote_username@10.10.0.2:/remote/directory

## configure ssh client to login with password where /dev/null is no config

    ssh -F /dev/null <username>@<host>


## ssh error known_hosts

    sudo rm /root/.ssh/known_hosts


# to run ssh-agent 
    eval `ssh-agent`

# add private key to agent to connect via ssh

    ssh-add -k path-to-internal-key

# to list active connections

    ssh-add -L
