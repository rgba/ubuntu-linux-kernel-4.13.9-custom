# ubuntu-linux-kernel-4.13.9-custom

This custom ubuntu kernel contains a patch provided by ursm (https://github.com/ursm) for properly supporting the Elan touchpad of the Lenovo X1 Carbon 5th gen model. 

https://gist.github.com/ursm/6d1007f44a1d6beeb670b3c3a6a78ea4

# Installation instructions 

1. Download all the *.deb files into a directory
2. Within the directory execut following command to install the new kernel 
   
       dpkg -i *.deb

   You should now see following output

       ~# dpkg -i *.deb
        Selecting previously unselected package linux-firmware-image-4.13.9-custom.
        (Reading database ... 39889 files and directories currently installed.)
        Preparing to unpack linux-firmware-image-4.13.9-custom_4.13.9-custom-2_amd64.deb ...
        Unpacking linux-firmware-image-4.13.9-custom (4.13.9-custom-2) ...
        Selecting previously unselected package linux-headers-4.13.9-custom.
        Preparing to unpack linux-headers-4.13.9-custom_4.13.9-custom-2_amd64.deb ...
        Unpacking linux-headers-4.13.9-custom (4.13.9-custom-2) ...
        Selecting previously unselected package linux-image-4.13.9-custom.
        Preparing to unpack linux-image-4.13.9-custom_4.13.9-custom-2_amd64.deb ...
        Unpacking linux-image-4.13.9-custom (4.13.9-custom-2) ...
        Selecting previously unselected package linux-image-4.13.9-custom-dbg.
        Preparing to unpack linux-image-4.13.9-custom-dbg_4.13.9-custom-2_amd64.deb ...
        Unpacking linux-image-4.13.9-custom-dbg (4.13.9-custom-2) ...
        Preparing to unpack linux-libc-dev_4.13.9-custom-2_amd64.deb ...
        Unpacking linux-libc-dev (4.13.9-custom-2) over (4.4.0-91.114) ...
        Setting up linux-firmware-image-4.13.9-custom (4.13.9-custom-2) ...
        Setting up linux-headers-4.13.9-custom (4.13.9-custom-2) ...
        Setting up linux-image-4.13.9-custom (4.13.9-custom-2) ...
        update-initramfs: Generating /boot/initrd.img-4.13.9-custom
        W: mdadm: /etc/mdadm/mdadm.conf defines no arrays.
        Generating grub configuration file ...
        Warning: Setting GRUB_TIMEOUT to a non-zero value when GRUB_HIDDEN_TIMEOUT is set is no longer supported.
        Found linux image: /boot/vmlinuz-4.13.9-custom
        Found initrd image: /boot/initrd.img-4.13.9-custom
        Found linux image: /boot/vmlinuz-4.4.0-83-generic
        Found initrd image: /boot/initrd.img-4.4.0-83-generic
        done
        Setting up linux-image-4.13.9-custom-dbg (4.13.9-custom-2) ...
        Setting up linux-libc-dev (4.13.9-custom-2) ...

3. Reboot your PC
4. Run following command to verify that you are running the custom kernel
 
        ~# uname -r
        4.13.9-custom
