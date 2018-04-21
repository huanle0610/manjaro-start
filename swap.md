#添加swap

```shell
[root@amtf-pc git]# fallocate -l 8G /data/swap  
[root@amtf-pc git]# chmod 600 /data/swap  
[root@amtf-pc git]# mkswap /data/swap  
Setting up swapspace version 1, size = 8 GiB (8589930496 bytes) 
no label, UUID=126b1d20-9123-46ab-ba89-72b679cee93e 
[root@amtf-pc git]# swapon /data/swap



# /etc/fstab: static file system information.
#
# Use 'blkid' to print the universally unique identifier for a device; this may
# be used with UUID= as a more robust way to name devices that works even if
# disks are added and removed. See fstab(5).
#
# <file system> <mount point> <type> <options> <dump> <pass>
UUID=A02C-471A /boot/efi vfat defaults,noatime 0 2
UUID=eb488dd2-804e-48f4-97f7-5da0ebfe11cd / ext4 defaults,noatime,discard 0 1
UUID=586503d4-f66c-4030-93e9-7a9f875a6418 /data ext4 defaults,noatime,discard 0 1
UUID=126b1d20-9123-46ab-ba89-72b679cee93e none swap defaults 0 0
tmpfs /tmp tmpfs defaults,noatime,mode=1777 0 0
```