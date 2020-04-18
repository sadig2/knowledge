## copy foldre from local to remote

    scp -r /local/directory remote_username@10.10.0.2:/remote/directory

## configure ssh client to login with password where /dev/null is no config

    ssh -F /dev/null <username>@<host>
