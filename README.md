# solved-tricks

Vagrant Install - Errors macOS Monterey
--

**Error:** 
*uplibOsInit what: 3 VERR_VM_DRIVER_NOT_INSTALLED (-1908) - The support driver is not installed. On linux, open returned ENOENT.*


**Solved**

- Step 1

```console
$sudo kextload -b org.virtualbox.kext.VBoxDrv
```

- Step 2
```console
$sudo mkdir /etc/vbox | touch /etc/vbox/networks.conf | echo "* 0.0.0.0/0 ::/0" >> /etc/vbox/networks.conf
```

- Step 3 

  > Go into System Preferences->Security & Privacy

- Step 4

  > Unlock the security center

- Step 5 

  > Approve the software by Oracle

- Step 6
```console
$sudo kextload -b org.virtualbox.kext.VBoxNetFlt
$sudo kextload -b org.virtualbox.kext.VBoxNetAdp
$sudo kextload -b org.virtualbox.kext.VBoxUSB
```

- Step 7

  > Reboot
