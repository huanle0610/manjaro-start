＃google-chrome

```shell
$ /usr/bin/yaourt -S aur/google-chrome
```

编辑 eula_text.html 的下载地址 不然下不来

```shell
[root@amtf-pc ~]# ps aux | grep yaourt
amtf     16664  0.0  0.0  17028  5508 pts/7    S+   14:58   0:00 /bin/bash /usr/bin/yaourt -S aur/google-chrome

[root@amtf-pc ~]# lsof -p 16664 
lsof: WARNING: can't stat() fuse.gvfsd-fuse file system /run/user/1000/gvfs 
     Output information may be incomplete. 
COMMAND   PID USER   FD   TYPE DEVICE SIZE/OFF   NODE NAME 
yaourt  16664 amtf  cwd    DIR   0,36      160     56 /tmp/yaourt-tmp-amtf/aur-google-chrome 
yaourt  16664 amtf  255r   REG   8,17    15781 145674 /usr/bin/yaourt

[root@amtf-pc ~]# ls /tmp/yaourt-tmp-amtf/aur-google-chrome
google-chrome.install  google-chrome-stable_59.0.3071.86_amd64.deb  google-chrome-stable.sh  PKGBUILD  src
```
