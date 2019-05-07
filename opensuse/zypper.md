
zypper lr -d    (lists repos)
zypper modifyrepo -d  “number of repo”

zypper addrepo  “url”
zypper removerepo “url”
zypper dup --from “repo”

zypper ar -cfp 90 http://ftp.gwdg.de/pub/linux/misc/packman/suse/openSUSE_Tumbleweed/ packman
zypper dup --from packman


zypper -is | grep packagename    - to search for package

rpm -qa | grep packagename

zypper rm pacakge



[cheatlist](https://www.2daygeek.com/zypper-command-examples-manage-packages-opensuse-system/#)