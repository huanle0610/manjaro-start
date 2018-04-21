```shell
[root@amtf-pc tmp]# pacman -Qe | grep nginx 
nginx 1.10.2-2 
[root@amtf-pc tmp]# pacman -Qe | grep virtual 
virtualbox 5.1.12-2 
[root@amtf-pc tmp]# pacman -Qe | grep  dkms 
[root@amtf-pc tmp]# pacman -Qe | grep  ibus 
ibus 1.5.14-1 
ibus-pinyin 1.5.0-5 
ibus-qt 1.3.3-7 
ibus-table 1.9.14-1
ibus-table-chinese 1.8.2-1

[root@amtf-pc tmp]# pacman -Qi ibus 
Name            : ibus 
Version         : 1.5.14-1 
Description     : Next Generation Input Bus for Linux 
Architecture    : x86_64 
URL             : http://ibus.googlecode.com
Licenses        : LGPL
Depends On      : dconf  gtk2  gtk3  hicolor-icon-theme  libnotify  python-dbus  python-gobject 
                 iso-codes  python2-gobject2  python2-dbus  python2-gobject  librsvg 
                 libibus=1.5.14 
Optional Deps   : None
Required By     : ibus-pinyin  ibus-qt  ibus-table
Build Date      : 2016年08月06日 星期六 11时21分41秒 
Install Date    : 2017年01月17日 星期二 22时51分00秒 
Install Reason  : Explicitly installed 
Install Script  : Yes
Validated By    : Signature


[root@amtf-pc tmp]# pacman -Si linux310-headers 
Repository      : core 
Name            : linux310-headers 
Version         : 3.10.104-1 
Description     : Header files and scripts for building modules for Linux310 kernel 
Architecture    : x86_64 
URL             : http://www.kernel.org/ 
Licenses        : GPL2 
Groups          : None 
Provides        : linux-headers=3.10.104 
Depends On      : None 
Optional Deps   : None 
Conflicts With  : None 
Replaces        : None 
Download Size   : 5.71 MiB 
Installed Size  : 39.99 MiB 
Packager        : Philip Mueller <philm@manjaro.org> 
Build Date      : 2016年10月22日 星期六 03时05分07秒
Validated By    : MD5 Sum  SHA-256 Sum  Signature
```

#依赖关系
##依赖
```shell
[amtf@amtf-s3 git]$ pactree mariadb | head -n 10
mariadb
├─mariadb-clients
│ ├─libmariadbclient
│ │ ├─bzip2
│ │ │ ├─glibc
│ │ │ │ ├─linux-api-headers
│ │ │ │ ├─tzdata
│ │ │ │ └─filesystem
│ │ │ │   └─iana-etc
│ │ │ └─bash provides sh
...
```

##被依赖
```shell
[root@amtf-pc amtf]# pactree -r mariadb 
mariadb 
└─akonadi 
 └─akonadi-contacts 
   └─digikam
```