# linuxdxduwu
hjfjhkjh is notes yes uwuwuwuuwu
xD
cryptsetup luksOpen /dev/sda3 uwu
lvm pvcreate /dev/mapper/uwu
vgcreate uwuxd /dev/mapper/uwu
lvcreate -L 120G -n root uwuxd
lvcreate -l 100%FREE -n home uwuxd
mkdir /mnt/linuxd
cd /mnt/linuxd/


mount /dev/mapper/uwuxd-root /mnt/linuxd/
tar -xvpf ./stage3-amd64-20201115T214503Z.tar.xz --xattrs --numeric-owner


mount -t proc /proc /mnt/linuxd/proc
mount --rbind /sys /mnt/linuxd/sys
mount --make-rslave /mnt/linuxd/sys
mount --rbind /dev /mnt/linuxd/dev
mount --make-rslave /mnt/linuxd/dev

chroot /mnt/linuxd /bin/bash 
export PS1="(chroot) $PS1"
mount /dev/sda2 /boot 
mount /dev/sda1 /boot/efi

