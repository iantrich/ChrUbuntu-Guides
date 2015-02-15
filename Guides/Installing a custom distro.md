**CAUTION:** This may possibly corrupt your dual boot. If you follow our guides fully, you should have a fully 
functional linux machine and should be okay with Linux only, but be forewarned.

**NOTE:** If you wish to eliminate your ChromeOS partition fully and make your Chromebook a more traditional Linux 
laptop, checkout installing [John Lewis](https://wiki.archlinux.org/index.php/Chromebook#Custom_Firmware) coreboot firmware.

**NOTE:** This installation is to be done instead of ChrUbuntu but it is possible to wipe out your ChrUbuntu partition once installed to install a different distro starting at steps 7

**PREREQUISITES** This guide assumes you have already created a Live USB to install from with your choosen distro.
Look [here](https://github.com/iantrich/ChrUbuntu-Guides/blob/master/Guides/Creating%20a%20Live%20USB.md) on how to do this.

1. Ensure that your machine is in Developer Mode. Model-specific instructions can be found [here](http://www.chromium.org/chromium-os/developer-information-for-chrome-os-devices)
  **Developer Mode will wipe your machine once turned on**
2. Login to your machine
3. Press **CTRL+ALT+T** to open crosh
4. Type `shell` into the command line
5. Login as user 'chronos', with no password.
6. Run the command to allow booting to Linux and USB devices:

  `sudo crossystem dev_boot_usb=1 dev_boot_legacy=1`
  
7. Shut down the Chromebook
8. Insert Live Linux USB
9. Start the machine and press **CTRL+L** to boot into Legacy Mode
10. Press **Esc** when prompted to enter the Boot Menu
11. Select the option for *USB Device*
  **NOTE:** Some Live Linux USBs will complain about 'not enough memory' If you see this try the following:
  From the GRUB menu hit **Esc** to edit the GRUB command line. At the end of the line add
    
    `MEM=2G`
    
  Exit and try to boot the USB again
12. Once booted, connect to a network and go through the installation process. You can choose to take the full drive
thereby surely wiping out ChromeOS but gaining space, or have the installer install next to the ChromeOS partition.
Most installers make this a simple selection in their GUI. If not, you'll have to refer to that distro's procedures.
13. Once rebooted, you'll be presented with the Deverloper Mode Boot Screen.
  * To boot ChromeOS, hit **CTRL+D**
  * To boot ChrUbuntu, hit **CTRL+L**
  
**Further Reading**
  * [Common ChrUbuntu Fixes](https://github.com/iantrich/ChrUbuntu-Guides#fixes)
  * [ChrUbuntu Tips](https://github.com/iantrich/ChrUbuntu-Guides#tips)
