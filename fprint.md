
[Fprint](https://wiki.archlinux.org/index.php/Fprint)

For most people, don't install thinkfinger https://bugs.launchpad.net/ubuntu/+source/thinkfinger/+bug/278703/comments/1

```shell
[amtf@amtf-pc dict]$ cat /etc/pam.d/kde 
#%PAM-1.0 

auth            include         system-login 

account         include         system-login 

password        include         system-login 

session         include         system-login

[amtf@amtf-pc dict]$ cat /etc/pam.d/system-login 
#%PAM-1.0 

auth      sufficient pam_fprintd.so 
auth       required   pam_tally.so         onerr=succeed file=/var/log/faillog 
auth       required   pam_shells.so 
auth       requisite  pam_nologin.so 
auth       include    system-auth 

account    required   pam_access.so 
account    required   pam_nologin.so 
account    include    system-auth 

password   include    system-auth 

session    optional   pam_loginuid.so 
session    include    system-auth 
session    optional   pam_motd.so          motd=/etc/motd 
session    optional   pam_mail.so          dir=/var/spool/mail standard quiet 
-session   optional   pam_systemd.so 
session    required   pam_env.so
```
