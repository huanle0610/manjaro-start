#nmcli connect wifi

First, run

```shell
nmcli c
```

This will list your connections, with the first column being the SSID, and the second column being the UUID of the connection.

Copy the UUID of the SSID you want to connect to so you can paste it into the next command.

Next, run

```shell
nmcli c up WIFI-NAME
or
nmcli c up uuid <paste uuid here>
```

```shell
[amtf@amtf-s3 ~]$ nmcli c
NAME                UUID                                  TYPE             DEVICE
1319                8b39db1e-a19d-4e0a-9ac0-bc6690130aae  802-11-wireless  wlp3s0
he-ipv6             4c20ec03-bfd3-46c5-adb4-65f3bf15d646  ip-tunnel        he-ipv6
Wired connection 1  ea245d54-3aa4-3617-8cbf-75fdb1f45ef7  802-3-ethernet   --

nmcli --ask c up 1319
or
nmcli --ask c up uuid 8b39db1e-a19d-4e0a-9ac0-bc6690130aae
```
