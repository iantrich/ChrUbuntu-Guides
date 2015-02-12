A big thanks to [/u/hugegreenbug](http://www.reddit.com/u/hugegreenbug) for his hard work in porting this to Linux. Check out his [github repo](https://github.com/hugegreenbug/xf86-input-cmt) for more details.

**NOTE** You must be running Ubuntu 13.10 or newer to install this.

1. Add hugegreenbug's cmt repo.
 
  `$ sudo add-apt-repository ppa:hugegreenbug/cmt`
2. Update your sources.
 
  `$ sudo apt-get update`
3. Install cmt and dependencies.
 
  `$ sudo apt-get install -y libevdevc libgestures  xf86-input-cmt`
4. Move your current touchpad configuration.
 
  `$ sudo mv /usr/share/X11/xorg.conf.d/50-synaptics.conf /usr/share/X11/xorg.conf.d/50-synaptics.conf.old`
5. Replace the moved configuration with the ported ChromeOS configuration.

  `$ sudo cp /usr/share/xf86-input-cmt/50-touchpad-cmt-<model>.conf /usr/share/X11/xorg.conf.d/` 
  **The current options for `<model>` are:**
  * `aebl` - ?
  * `alex` - Series 5
  * `butterfly` - HP Pavilion
  * `daisy` - Series 3
  * `elan` - ?
  * `falco` - HP 14
  * `kaen` - ?
  * `leon` - CB30
  * `link` - Pixel
  * `lumpy` - Series 5 550
  * `mario` - Cr-48
  * `parrot` - C710
  * `peppy` - C720
  * `pi` - Samsung 2 13
  * `pit` - Samsung 2 11
  * `puppy` - ?
  * `spring` - HP 11
  * `stout` - X131e
  * `wolf` - Dell 11
  * `zgb` - AC700
6. Reboot

  `$ sudo reboot`
