# Update to newest the stable kernel: 

**NOTE** I recommend not upgrading to release candidate kernels. At the time of writing, 3.19 is the newest stable kernel available

1. Open the folder to the kernel you wish to upgrade to. The most recently released kernels are at the bottom of the [page](http://kernel.ubuntu.com/~kernel-ppa/mainline/).
2. Download the following packages:
  * linux-image-3.xx.x-generic_3.xx.x_<architecture>.deb
  * linux-headers-3.xx.x-generic_3.xx.x_<architecture>.deb
  * linux-headers-3.xx,x_3.xx.x_all.deb
  **NOTE:** `<architecture>` will be either *i386* for 32-bit processors or *amd64* for 64-bit processors.
3. Run the commands: 
  * `$ sudo dpkg -i ~/Downloads/linux-image*.deb`
  * `$ sudo dpkg -i ~/Downloads/linux-headers*.deb`
4. Reboot `$ sudo reboot`
