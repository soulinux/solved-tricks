# solved-tricks

Vagrant Install - Errors macOS Monterey
--

**Error:** 
*uplibOsInit what: 3 VERR_VM_DRIVER_NOT_INSTALLED (-1908) - The support driver is not installed. On linux, open returned ENOENT.*


**Solved**

Step 1 - run:

>sudo kextload -b org.virtualbox.kext.VBoxDrv

Step 2: 

>Go into System Preferences->Security & Privacy

Step 3: 

>Unlock the security center

Step 4: 

> Approve the software by Oracle

Step 5:

>sudo kextload -b org.virtualbox.kext.VBoxNetFlt
>sudo kextload -b org.virtualbox.kext.VBoxNetAdp
>sudo kextload -b org.virtualbox.kext.VBoxUSB

Step 6: 

>Reboot
