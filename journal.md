### clear cache
pacman -Sc


### clear journal
```bash
rm -rf /var/log/journal/*/*
killall -9 systemd-journald
```
