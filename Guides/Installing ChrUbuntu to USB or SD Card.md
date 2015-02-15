While it is possible to install ChrUbuntu to an SD card or USB drive, the easiest method is actual much more direct.

**PREREQUISTES** 2 cards/drives to install onto and use and the installer. This guide assumes you have already created a Live 
USB to install from with your choosen distro. Look [here](https://github.com/iantrich/ChrUbuntu-Guides/blob/master/Guides/Creating%20a%20Live%20USB.md) 
on how to do this.

**NOTE:** If you already have Linux installed, you can start at step 7.

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
12. Once booted, insert the card/drive that you wish to install to and start the installation process. Select the
card/drive as the installation target and go through the installation process.
13. Once rebooted, you'll be presented with the Deverloper Mode Boot Screen.
  * To boot ChromeOS, hit **CTRL+D**
  * To boot ChrUbuntu, hit **CTRL+L**
  
**Further Reading**
  * [Common ChrUbuntu Fixes](https://github.com/iantrich/ChrUbuntu-Guides#fixes)
  * [ChrUbuntu Tips](https://github.com/iantrich/ChrUbuntu-Guides#tips)
