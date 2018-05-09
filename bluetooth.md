# bluetooth

```shell
[root@amtf-s3 ~]# pacman -S bluez-utils
[root@amtf-s3 ~]# bluetoothctl  
Agent registered 
[bluetooth]# devices 
Device E0:A6:70:0C:E9:B6 Nokia 5320di XpressMusic 
Device 00:1D:43:F0:62:36 NE-618 
[bluetooth]# remove E0:A6:70:0C:E9:B6 
[DEL] Device E0:A6:70:0C:E9:B6 Nokia 5320di XpressMusic 
Device has been removed 
[bluetooth]# power on 
Changing power on succeeded 
[bluetooth]# scan on 
Discovery started 
[CHG] Controller 60:6C:66:4F:86:FB Discovering: yes 
[CHG] Device 00:1D:43:F0:62:36 RSSI: -59 
[CHG] Device 00:1D:43:F0:62:36 TxPower: 2 
[bluetooth]# pair 00:1D:43:F0:62:36 
Attempting to pair with 00:1D:43:F0:62:36 
Failed to pair: org.bluez.Error.AlreadyExists 
[bluetooth]# devices 
Device 00:1D:43:F0:62:36 NE-618 
[bluetooth]# remove 00:1D:43:F0:62:36 
[DEL] Device 00:1D:43:F0:62:36 NE-618 
Device has been removed 
[NEW] Device 00:1D:43:F0:62:36 NE-618 
[bluetooth]# pair 00:1D:43:F0:62:36 
Attempting to pair with 00:1D:43:F0:62:36 
[CHG] Device 00:1D:43:F0:62:36 Connected: yes 
[CHG] Device 00:1D:43:F0:62:36 UUIDs: 00001108-0000-1000-8000-00805f9b34fb 
[CHG] Device 00:1D:43:F0:62:36 ServicesResolved: yes 
[CHG] Device 00:1D:43:F0:62:36 Paired: yes 
Pairing successful 
[CHG] Device 00:1D:43:F0:62:36 ServicesResolved: no 
[CHG] Device 00:1D:43:F0:62:36 Connected: no 

[CHG] Device 00:1D:43:F0:62:36 Connected: yes 
[CHG] Device 00:1D:43:F0:62:36 ServicesResolved: yes 
[CHG] Device 00:1D:43:F0:62:36 Alias: NE-618 
[CHG] Device 00:1D:43:F0:62:36 Trusted: yes
```