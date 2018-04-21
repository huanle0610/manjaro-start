```shell
$ sudo pacman -S create_ap
$ sudo create_ap wlp3s0 wlp3s0 oneness xxxxxxxx 
Config dir: /tmp/create_ap.wlp3s0.conf.bg99MQBv 
PID: 21991 
Network Manager found, set ap0 as unmanaged device... DONE 
wlp3s0 is already associated with channel 7 (2442 MHz), fallback to channel 7 
Creating a virtual WiFi interface... ap0 created. 
Sharing Internet using method: nat 
hostapd command-line interface: hostapd_cli -p /tmp/create_ap.wlp3s0.conf.bg99MQBv/hostapd_ctrl 
Configuration file: /tmp/create_ap.wlp3s0.conf.bg99MQBv/hostapd.conf 
Using interface ap0 with hwaddr 60:6c:66:4f:86:f8 and ssid "oneness" 
ap0: interface state UNINITIALIZED->ENABLED 
ap0: AP-ENABLED  
ap0: STA e4:e4:ab:64:0f:22 IEEE 802.11: authenticated 
ap0: STA e4:e4:ab:64:0f:22 IEEE 802.11: associated (aid 1) 
ap0: AP-STA-CONNECTED e4:e4:ab:64:0f:22
```
