## move to $home directory cd $home

open .bashrc file and add export PATH=\$PATH:/opt/apps/jdk-11.0.3/bin  
then run **source .bashrc**

## executing commands linux shell start looking for variable \$PATH first

Example (Unix Bash shell):

    export _SETTINGS_MODULE=mysite.settings

-admin runserver
Example (Windows shell):

    set _SETTINGS_MODULE=mysite.settings

-admin runserver
