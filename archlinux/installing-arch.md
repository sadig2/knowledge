	 	 	 	
Ping  
pacman -Syy  

pacman -S reflector  
refletctor -c “Sweden” -f 12  -l 10 -n 12 –save /etc/pacman.d/mirrorlist  

fdisk -l  
cfdisk /dev/sda  


uefi 512  

mkfs.fat -F32 /dev/sda5   

bootable write  

mkfs.ext4 /dev/sda1  

mount /dev/sda1 /mnt  
lsblk   

pacstrap -i /mnt base base-devel  

genfstab -U -p /mnt >> /mnt/etc/fstab  

cat /mnt/etc/fstab  

arch-chroot /mnt /bin/bash  
nano /etc/locale.gen  

uncomment en us  

locale-gen  
ln -sf /usr/share/zoneinfo/Europe/Baku /etc/localtime  
hwclock --systohc --utc  

echo clanzu2 > /etc/hostname  

nano /etc/hosts   
127.0.1.1 localhost.localdomain  clanzu2  
 
pacman -S  networkmanager  
systemctl enable NetworkManager  

systemctl enable dhcpcd  

passwd   


pacman -S grub efibootmgr 
mkdir /boot/efi 

mount /dev/sda(efi) /boot/efi  

grub-install --target=x86_64-efi  --bootloader-id=GRUB --efi-directory=/boot/efi  


pacman -S grub  
grub-install /dev/sda 



grub-mkconfig -o /boot/grub/grub.cfg    

mkdir /boot/efi/EFI/BOOT  
cp /boot/efi/EFI/GRUB/grubx64.efi /boot/efi/EFI/BOOT/BOOTX64.EFI  
nano /boot/efi/startup.nsh  
bcf boot add 1 sf0:\EFI\GRUB\grubx64.efi “MyGrub”  
exit  

 


    
exit  

umount -R /mnt  

reboot  



root   

useradd -m -g users -G wheel -s /bin/bash clanzu2  

passwd clanzu2  

EDITOR=nano visudo   

find  wheel all all  


exit  

new user name  

sudo pacman -S pulseaudio pulseaudio-alsa  

sudo pacman -S xorg xorg-xinit  


echo “exec startkde” >  ~/.xinitrc  

sudo pacmant -S plasmadesktop  
sudo pacman -S konsole firefox  

sddm  




wifi  

pacman - S networkmanager  
sudo systemctl enable NetworkManager  

pacman -s iw wpa_supplicant dialog  




network-manager-applet  












 	
	

