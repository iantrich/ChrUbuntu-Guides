These are tips that I've found useful over time and ones that can make life easier/prettier

1. Install Guake

  ```
  $ sudo apt-get install guake
  $ sudo ln -s /usr/share/applications/guake.desktop /etc/xdg/autostart/
  ```
  
  **NOTE:** Open Guake Preferences and bind a new shortcut key as `F12` isn't normally setup on Chromebooks or make a key binding for `F12` using the [Useful Key Mappings Guide](https://github.com/iantrich/ChrUbuntu-Guides/blob/master/Tips/Useful%20Key%20Mappings.md)
2. Install Oracle Java 7 (Recommended over OpenJDK)

  ```
  $ sudo add-apt-repository -y ppa:webupd8team/java
  $ sudo apt-get update
  $ sudo apt-get install -y python-software-properties oracle-java7-installer
  ```
  
3. Install Numix Theme/Icons

  ```
  $ sudo add-apt-repository -y ppa:numix/ppa
  $ sudo apt-get update
  $ sudo apt-get install -y numix-gtk-theme numix-icon-theme-circle
  ```
  
  **NOTE:** Setting these themes is usually distro specific. (e.g. System Settings for Mint, Ubuntu Tweaks for Ubuntu, Elementary Tweaks for elementary OS)

4. Install Build Essentials (If you plan on ever doing an dev work or building any source files for custom drivers, etc; you’ll want these)
 
  `$sudo apt-get install -y build-essential libssl-dev curl git-core`

5. Install TLP (for battery savings)
  
  ```
  $ sudo add-apt-repository -y ppa:linrunner/tlp
  $ sudo apt-get update
  $ sudo apt-get install -y tlp tlp-rdw
  ```
  
6. Configure zram

  `sudo apt-get isntall -y zram-config`
  
7. Give external ext4 SD Card write permissions (Useful if you’re keeping apps and games, etc on one)
  
  ```
  $ sudo chgrp adm /media/<username>/<device name>
  $ sudo chmod g+w /media/<username>/<device name>
  ```
  
8. Create Custom Launchers
  *Create a “<app name>.desktop” file in ~/.local/share/applications*
  
  ```  
  [Desktop Entry]
  Name=<App Name>
  Comment=<App Name>
  Exec=<full-path-to-script>
  Icon=<full-path-to-icon>
  Terminal=false
  StartupNotify=true
  Type=Application
  Categories=<category>;
  ```
  
9. Install Microsoft Fonts

  `$ sudo apt-get install -y msttcorefonts`
  
10. Recommended Additions:

  `$ sudo apt-get install -y gimp vlc qbittorrent glipper shutter`
