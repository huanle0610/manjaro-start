
#creating ext4
https://wiki.archlinux.org/index.php/persistent_block_device_naming

##格式化磁盘
```shell

# umount /dev/sda8
# mke2fs -t ext4 /dev/sda8
mke2fs 1.43.3 (04-Sep-2016)
/dev/sda8 contains a ntfs file system labelled 'mdata'
Proceed anyway? (y,n) y 
Creating filesystem with 10751744 4k blocks and 2689904 inodes 
Filesystem UUID: 586503d4-f66c-4030-93e9-7a9f875a6418 
Superblock backups stored on blocks:  
       32768, 98304, 163840, 229376, 294912, 819200, 884736, 1605632, 2654208,  
       4096000, 7962624 

Allocating group tables: done                             
Writing inode tables: done                             
Creating journal (65536 blocks): done
Writing superblocks and filesystem accounting information: done
[root@amtf-pc dict]# lsblk -fs 
NAME  FSTYPE LABEL           UUID                                 MOUNTPOINT
                                                            
sda8  ext4   data            586503d4-f66c-4030-93e9-7a9f875a6418 /data 
└─sda                                                              
sda9  ntfs   Lenovo_Recovery 5A582698582672C5                      
└─sda                                                              
sdb1  ext4                   eb488dd2-804e-48f4-97f7-5da0ebfe11cd / 
└─sdb                                                              
sdb2                                                               
└─sdb   
```

## 自动挂载
```
[root@amtf-pc dict]# cat /etc/fstab
UUID=586503d4-f66c-4030-93e9-7a9f875a6418 /data          ext4    defaults,noatime,discard 0  

[root@amtf-s3 git]# blkid /dev/sdb 
/dev/sdb: PTUUID="30f156ac-092e-4a91-8190-f8c803717752" PTTYPE="gpt" 
[root@amtf-s3 git]# blkid /dev/sda9 
/dev/sda9: LABEL="ee" UUID="e75f7d43-2565-4ab1-b2e3-4e5c16377a6f" TYPE="ext4" PARTUUID="b760d44d-d9fa-4c8a-a69e-a21d
```