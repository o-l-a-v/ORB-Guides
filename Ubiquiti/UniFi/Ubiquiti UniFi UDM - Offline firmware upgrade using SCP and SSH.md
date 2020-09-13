# UDM - Upgrade firmware offline using SCP and SSH



## Prerequirements
**I'm not responsible if your equipments ends up broken. Do this at your own risk.**

This procedure was done 13.09.2020, upgrading from 1.5.6 to 1.8.1RC3.
* Your milage may wary.



## Procedure
### 1. Download firmware from ui.com
Find the firmware you want flashed from ui.com.


### 2. Factory reset
Wait for UDM to boot (plays a sound), then hold reset button for minimum 10 seconds.


### 3. Upload firmware file
WinSCP (SCP)

* **Address:** 192.168.1.1:22
* **UN/PW:** root/ubnt

Copy firmware file over to /tmp/


### 4. Upgrade firmware
PuTTY (SSH)

* **Address:** 192.168.1.1:22
* **UN/PW:** root/ubnt

```ubnt-upgrade /tmp/<name_of_file>.bin```


### 5. Confirm upgrade success
PuTTY (SSH)

* **Address:** 192.168.1.1:22
* **UN/PW:** root/ubnt

```ubnt-device-info summary```



## Resources
### Available "ubnt-" commands
```bash
ubnt-ble-http-transport   ubnt-fsck-all.sh          ubnt-rps
ubnt-config-restore       ubnt-geoip-build          ubnt-ssh-keys-install
ubnt-device-info          ubnt-geoip-update         ubnt-systool
ubnt-discover             ubnt-hotplug.sh           ubnt-tools
ubnt-discovery-responder  ubnt-ipcalc               ubnt-upgrade
ubnt-fan-speed            ubnt-make-support-file    ubnt-upgrade-common.sh
ubnt-file-download        ubnt-rf-env               ubnt-upgrade-platform.sh
```

### Sources
* https://dl.ubnt.com/qsg/UDM/UDM_EN.html
* https://www.putty.org/
* https://winscp.net/