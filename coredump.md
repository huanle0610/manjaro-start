#格式
```shell
cat /proc/sys/kernel/core_pattern
```

[Disabling_automatic_core_dumps](https://wiki.archlinux.org/index.php/Core_dump#Disabling_automatic_core_dumps)


```shell
[root@amtf-pc jupyter]# ls /var/lib/systemd/coredump 
'core.http\x2eso.1000.3dc9074b9c024341ba5a97cea7264e4d.2347.1489805272000000000000.lz4' 
core.kdenlive.1000.0dc8b207a13740998dbe748ce9fbcde8.15187.1489812453000000000000.lz4 
core.kdenlive.1000.0dc8b207a13740998dbe748ce9fbcde8.15264.1489812574000000000000.lz4 
core.kdenlive.1000.0dc8b207a13740998dbe748ce9fbcde8.15519.1489812668000000000000.lz4 
core.kdenlive.1000.0dc8b207a13740998dbe748ce9fbcde8.15625.1489812756000000000000.lz4 
core.kdenlive.1000.0dc8b207a13740998dbe748ce9fbcde8.15703.1489812759000000000000.lz4 
core.kdenlive.1000.0dc8b207a13740998dbe748ce9fbcde8.1761.1489807753000000000000.lz4 
core.plasmashell.1000.0dc8b207a13740998dbe748ce9fbcde8.1054.1489812129000000000000.lz4 
[root@amtf-pc jupyter]# du -h /var/lib/systemd/coredump 
701M    /var/lib/systemd/coredump 
[root@amtf-pc jupyter]# rm -rf /var/lib/systemd/coredump/*
```