The following guide shows you how to successfully install [ChrUbuntu by Jay Lee](http://chromeos-cr48.blogspot.com/) onto your Chromebook

If you have any questions, please visit [/r/Chrubuntu](http://www.reddit.com/r/chrubuntu)

**PREREQUISITES:** [Developer Mode Enabled](http://www.chromium.org/chromium-os/developer-information-for-chrome-os-devices), connected to a power source, USB mouse

**RECOMMENDATIONS:** Make a [Chromebook Recovery USB](https://support.google.com/chromebook/answer/6002417?hl=en) before starting. If you have access to another machine this is not too much of an issue, but if you only have the Chromebook, you'll want this just in case anything goes wrong and you want to start over or go back to ChromeOS only.

**SET LINUX AS DEFAULT** It can be very annoying having to press Ctrl+L every time you wish to boot into linux
at the Dev Screen. By setting Legacy as the default you can bypass this and has the added benefit of protecting
your installation from corruption due to unexpected power loss. Read more on the Arch Linux [wiki](https://wiki.archlinux.org/index.php/Chromebook#Boot_to_SeaBIOS_by_default)

**NOTE**: Installing ChrUbuntu will wipe everything from your machine

1. Ensure that your machine is in Developer Mode. Model-specific instructions can be found [here](http://www.chromium.org/chromium-os/developer-information-for-chrome-os-devices)
2. If you haven't already, fully shut down your device and restart the machine. Do NOT go past the login screen.
3. Ensure that the Chromebook is connected to the internet.
4. Press **CTRL+ALT+=>** (=> is the forward arrow on the keyboard aka F2 on a normal keyboard).
5. Login as user 'chronos', with no password.
6. Run the command to allow booting to Linux and USB devices: 

  `sudo crossystem dev_boot_usb=1 dev_boot_legacy=1`
  
7. Run one of the following commands:
  * If using the ARM-based HP Chromebook 11, Acer C7, Samsung 550 or other older generation machines run the following: 
  
  `wget http://goo.gl/tnyga; sudo bash tnyga`

  * If using a newer model Chromebook (Intel Haswell or Core i5/i7 processors) run the following: 
  
  `curl -L -O http://goo.gl/9sgchs; sudo bash 9sgchs`

8. Answer any prompts and specify the size you wish to allocate to your ChrUbuntu partition. 5GB is the minimum required space and your total drive size minus 7GB for the ChromeOS partition as the maximum in 1GB increments. (i.e. If you have a 16GB SSD, allocate 9GB to ChrUbuntu at the most; similarly 25GB if you have a 32GB SSD).

9. Wait as the script reparitions the drive and reboots.

10. Wait as the Chromebook re-initializes the stateful partition (2-15 minutes).

11. After the Chromebook reboots again, go through the ChromeOS setup until you get to the Google login page.

12. Do steps 3-6 again

13. Run the command:

  **NOTE:** Run `curl -L -O http://goo.gl/<script_name>; sudo bash <script_name> -h` to see all available options

  `curl -L -O http://goo.gl/<script_name>; sudo bash <script_name> -m <ubuntu_flavor> -u <version> -a <architecture>`

  where 

  * `<script_name>` is one of the following:
    1. `tnyga`
    2. `9sgchs` 
  * `<ubuntu_flavor>` can be one of the following:
    1. `ubuntu-desktop`
    2. `kubuntu-desktop`
    3. `lubuntu-desktop`
    4. `xubuntu-desktop`
    5. `edubuntu-desktop`
    6. `ubuntu-standard` - No GUI installed
  * `<version>` can be one of the following:
    1. `lts` - The latest LTS Ubuntu release
    2. 'latest` - The latest official stable Ubuntu release
    3. `dev` - The latest unstable development Ubuntu release (**NOT RECOMMENDED**)
    4. '12.10' - Ubuntu 12.10 release
  * `<architecture>` can be one of the following:
    1. amd64
    2. i386

14. Wait as the required files are downloaded and installed and answer any questions about encoding, locale and language if asked

  **NOTE:** If you are running the `9sgchs` script for the first time, the sript will partition the disk the first time and require you to reboot, re-download and run it once again to actually install the OS. If you already have partitions, this step will not occur
  
  **NOTE:** In the default installation with the `9sgchs` script, username and password for ChrUbuntu will both be `user`. Here is how you can change these to something more secure by editing the script (eg. using `vi`) BEFORE running it to install the OS. If you don't understand shell scripting, do not attempt this since bugs could break your installation. 
  
  Change the following likes:
  ```
  useradd -m user -s /bin/bash
  echo user | echo user:user | chpasswd
  adduser user adm
  adduser user sudo
  if [ -f /usr/lib/lightdm/lightdm-set-defaults ]
  then
    /usr/lib/lightdm/lightdm-set-defaults --autologin user
  fi" > /tmp/urfs/install-ubuntu.sh
  ```
  To look like below where you can specify your own `username` and `password`
  ```
  useradd -m username -s /bin/bash
  echo username | echo username:password | chpasswd
  adduser username adm
  adduser username sudo
  if [ -f /usr/lib/lightdm/lightdm-set-defaults ]
  then
    /usr/lib/lightdm/lightdm-set-defaults --autologin username
  fi" > /tmp/urfs/install-ubuntu.sh
  ```

15. If prompted for where to place the 'GRUB', be sure to check the box next to '/dev/sda'. 

16. Once rebooted, you'll be presented with the Deverloper Mode Boot Screen.
  * To boot ChromeOS, hit **CTRL+D**
  * To boot ChrUbuntu, hit **CTRL+L**
  * **NOTE:** If you ran `tnyga` or are on an ARM machine this will most likely not work. You'll need to additionally run the following command from the ChromeOS shell to make ChrUbuntu the default boot option:
  
    tnyga: `sudo cgpt add -i 6 -P 5 -S 1 /dev/sda`
    
    ARM: `sudo cgpt add -i 6 -P 5 -S 1 /dev/mmcblk0`

  * To make ChromeOS again the default:

    tnyga: `sudo cgpt add -i 6 -P 0 -S 1 /dev/sda`
    
    ARM: `sudo cgpt add -i 6 -P 0 -S 1 /dev/mmcblk0`

17. The username for ChrUbuntu is 'user' and the password is 'user' (unless you have changed them as indicated above)

**Further Reading**
  * [Common ChrUbuntu Fixes](https://github.com/iantrich/ChrUbuntu-Guides#fixes)
  * [ChrUbuntu Tips](https://github.com/iantrich/ChrUbuntu-Guides#tips)
  * [Not an Ubuntu fan? Installing a different flavor of Linux](https://github.com/iantrich/ChrUbuntu-Guides/edit/master/Guides/Installing%20a%20custom%20distro.md)


