**NOTE:** ChromeOS is not able to create a Live Linux USB

* On Linux from terminal:
**IMPORTANT:** The drive you are writing to must be unmounted. Use `umount`.

`sudo dd if=file.iso of=/dev/usb_device bs=1M`

  *(where usb_device is the usb drive)*
  **NOTE:** If you don't know the drive name, run `lsblk`.
* [On Mac OS X](https://wiki.archlinux.org/index.php/USB_flash_installation_media#In_Mac_OS_X)
* On Windows: Use [Win32 Disk Imager](http://sourceforge.net/projects/win32diskimager/)
