disk space   

    df -h  (h stand for human)  


lsblk 
sudo fdisk /dev/sda
n  create new partition
p  view new partition
w  write 

sudo mkfs.vfat -F 32 /dev/sda1




