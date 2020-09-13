# UDM - Upgrade firmware offline using SCP and SSH



## Factory reset
Wait for UDM to boot (plays a sound), then hold reset button for minimum 10 seconds.



## Upload firmware file
WinSCP (SCP)

192.168.1.1:22
root/ubnt

Copy firmware file over to /tmp/



## Upgrade firmware
PuTTY (SSH)

192.168.1.1:22
root/ubnt

```ubnt-upgrade /tmp/<name_of_file>.bin```



## Confirm upgrade success
PuTTY (SSH)

192.168.1.1:22
root/ubnt

```ubnt-device-info summary```



## Available "ubnt-" commands
```bash
ubnt-ble-http-transport   ubnt-fsck-all.sh          ubnt-rps
ubnt-config-restore       ubnt-geoip-build          ubnt-ssh-keys-install
ubnt-device-info          ubnt-geoip-update         ubnt-systool
ubnt-discover             ubnt-hotplug.sh           ubnt-tools
ubnt-discovery-responder  ubnt-ipcalc               ubnt-upgrade
ubnt-fan-speed            ubnt-make-support-file    ubnt-upgrade-common.sh
ubnt-file-download        ubnt-rf-env               ubnt-upgrade-platform.sh
```



## Resources
* https://dl.ubnt.com/qsg/UDM/UDM_EN.html