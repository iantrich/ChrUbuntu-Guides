The following guide shows you how to successfully install [ChrUbuntu by Jay Lee](http://chromeos-cr48.blogspot.com/) onto your Chromebook

If you have any questions, please visit [/r/Chrubuntu](http://www.reddit.com/r/chrubuntu)

**Prerequisites**: [Developer Mode Enabled](http://www.chromium.org/chromium-os/developer-information-for-chrome-os-devices), connected to a power source, USB mouse

**NOTE**: Installing ChrUbuntu will wipe everything from your machine

1. Ensure that your machine is Deverloper Mode. Model-specific instructions can be found [here](http://www.chromium.org/chromium-os/developer-information-for-chrome-os-devices)

2. If you haven't already, fully shut down your device and restart the machine. Do NOT go past the login screen.

3. Ensure that the Chromebook is connect to the internet.

4. Press CTRL+ALT+=> (=> is the forward arrow on the keyboard aka F2 on a normal keyboard).

5. Login as user 'chronos', with no password.

6. Run the command to allow booting to Linux and USB devices:

```
sudo crossystem dev_boot_usb=1 dev_boot_legacy=1
```

7.

--*a. If using the ARM-based HP Chromebook 11, Acer C7, Samsung 550 or other older generation machines run the following:

```
wget http://goo.gl/tnyga; sudo bash tnyga
```

--*b. If using a newer model Chromebook run the following:

```
curl -L -O http://goo.gl/9sgchs; sudo bash 9sgchs
```

8. Answer any prompts and specify the size you wish to allocate to your ChrUbuntu partition. 5GB is the minimum required space and your total drive size minus 7GB for the ChromeOS partition as the maximum in 1GB increments. (i.e. If you have a 16GB SSD, allocate 9GB to ChrUbuntu at the most; similarly 25GB if you have a 32GB SSD).

9. Wait as the script reparitions the drive and reboots.

10. Wait as the Chromebook re-initializes the stateful partition (2-15 minutes).

11. After the Chromebook reboots again, go through the ChromeOS setup until you get to the Google login page.

12. Do steps 3-6 again

13. Run the command:

**NOTE:** Run `curl -L -O http://goo.gl/<script_name>; sudo bash <script_name> -h` to see all available options

```
curl -L -O http://goo.gl/<script_name>; sudo bash <script_name> -m <ubuntu_flavor> -u <version> -a <architecture>
```

where 

--* `<script_name>` is one of the following:
--1. `tnyga`
--2. `9sgchs` 
--* `<ubuntu_flavor>` can be one of the following:
--1. `ubuntu-desktop`
--2. `kubuntu-desktop`
--3. `lubuntu-desktop`
--4. `xubuntu-desktop`
--5. `edubuntu-desktop`
--6. `ubuntu-standard` - No GUI installed
--* `<version>` can be one of the following:
--1. `lts` - The latest LTS Ubuntu release
--2. 'latest` - The latest official stable Ubuntu release
--3. `dev` - The latest unstable development Ubuntu release (**NOT RECOMMENDED**)
--4. '12.10' - Ubuntu 12.10 release
--* `<architecture>` can be one of the following:
--1. amd64
--2. i386

14. Wait as the required files are downloaded and installed and answer any questions about encoding, locale and language if asked

15. If prompted for where to place the 'GRUB', be sure to check the box next to '/dev/sda'. 

16. Once rebooted, you'll be presented with the Deverloper Mode Boot Screen.
--* To boot ChromeOS, hit CTRL+D
--* To boot ChrUbuntu, hit CTRL+L

17. The username for ChrUbuntu is 'user' and the password is 'user'

**Further Reading**
--* [Common ChrUbuntu Fixes]() //Coming Soon
--* [ChrUbuntu Tips]() //Coming Soon
--* [Not an Ubuntu fan? Installing a different flavor of Linux]() //Coming Soon


