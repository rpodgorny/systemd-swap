# systemd-swap
Script for auto-creation and mounting of: zram swaps, swap files (through loop) devices, swap partitions.
It is configurable in /etc/systemd-swap.conf.
Source:
```
/etc/modprobe.d/90-systemd-swap.conf
/etc/systemd/system/systemd-swap.service
/etc/systemd-swap.conf
/usr/lib/systemd/scripts/systemd-swap.sh
```
Using:
```
# systemctl enable systemd-swap
```
* ![logo](http://www.monitorix.org/imgs/archlinux.png "arch logo")Arch: in the [AUR](https://aur.archlinux.org/packages/systemd-swap/).

Note:

In package install /etc/modprobe.d/90-systemd-swap.conf - this file create zram devices, 32 - this is maximum for this module.

You can use empty devices.

32 - because zram can't create new devices if others already in using, like loop module.
