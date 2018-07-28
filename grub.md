```bash
[amtf@amtf-s3 ~]$ grep GRUB_CMDLINE_LINUX_DEFAULT /etc/default/grub
GRUB_CMDLINE_LINUX_DEFAULT="quiet resume=UUID=a2ec2f85-9b43-46e6-a356-e6df9acf102d"
[amtf@amtf-s3 ~]$ lsblk -o NAME,UUID
NAME   UUID
sda    
|-sda1 c3b63e0b-6bd6-4bc9-9fd4-1605ab444f2c
`-sda2 a2ec2f85-9b43-46e6-a356-e6df9acf102d
sdb    
`-sdb1 eb488dd2-804e-48f4-97f7-5da0ebfe11cd
```
