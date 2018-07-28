#used for uninstalled or installed
```shell
$ sudo pacman -S pkgfile
$ sudo pkgfile --update

#list package info
pkgfile -l flatpak
```

##search file

```bash
[amtf@amtf-s3 manjaro-start]$ pkgfile -g */bin/ls
core/coreutils
community/9base
community/plan9port
[amtf@amtf-s3 manjaro-start]$ pkgfile -r .*/bin/ls$
core/coreutils
community/9base
community/plan9port
[amtf@amtf-s3 manjaro-start]$ pkgfile -r .*/bin/netstat$
core/net-tools
[amtf@amtf-s3 manjaro-start]$ pkgfile -s netstat        
core/net-tools
extra/munin-node
[amtf@amtf-s3 manjaro-start]$ pkgfile -s ls     
core/coreutils
community/9base
community/epic4
community/mc
community/plan9port


[amtf@amtf-s3 ucd]$ pkgfile -s Blocks.txt
core/perl
extra/unicode-character-database
[amtf@amtf-s3 ucd]$ pkgfile -l extra/unicode-character-database | grep Blocks.txt
extra/unicode-character-database        /usr/share/unicode/Blocks.txt
```

#used for installed only

```shell
sudo pacman -Ql gvim
```
