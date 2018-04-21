#  自动设置源

```shell
  [root@amtf-pc summer]# pacman-mirrors -c China -R
  :: Querying servers, this may take some time...
  China
  -> 0.118 http://mirrors.ustc.edu.cn/manjaro/stable/$repo/$arch
  -> 0.189 http://ftp.cuhk.edu.hk/pub/Linux/manjaro/stable/$repo/$arch
  -> 0.149 http://mirrors.tuna.tsinghua.edu.cn/manjaro/stable/$repo/$arch
  :: Generated and saved '/etc/pacman.d/mirrorlist' mirrorlist.
```

# 更新包信息

```shell
# pacman -Syy:
-S: Sync packages
-yy: refresh package database, force refresh even if local database appears up-to-date
```

# 更新系统

```shell
# pacman -Syu

# pacman -Syuu:
-S: Sync packages
-y: refresh package database Passing two --refresh or -y flags will force a refresh of all package databases, 
    even if they appear to be up-to-date.
-uu: sys upgrade all packages, repeated 'u' flag enables downgrades (from man page):

           Pass this option twice to enable package downgrades; in this case, pacman
           will select sync packages whose versions do not match with the local
           versions. This can be useful when the user switches from a testing repository
           to a stable one.
```

# pacman

```shell
pacman -S package_name #安装软件包
pacman -R package_name #删除软件包
pacman -Rs package_name #顺便删除软件包相关依赖
pacman -Syu #升级系统中的所有包

pacman -Syy #同步包信息
pacman -Ss package #查询软件包
pacman -Qs package #查询已安装的包
pacman -Qi package #显示查找的包的信息
pacman -Ql package #显示你要找的包的文件都安装的位置
pacman -Sw package #下载但不安装包
pacman -U /path/package.pkg.tar.gz #安装本地包
pacman -Scc #清理包缓存，下载的包会在/var/cache 这个目录
pacman -Sf pacman #重新安装包
```