# Ubuntu

All Linux distributions are based on a predefined kernel. But, if you want to disable several options and drivers or try experimental patches, you need to build a Linux kernel.

# Building Kernel:

1. Install Required packages

        sudo apt-get install git fakeroot build-essential ncurses-dev xz-utils libssl-dev bc flex libelf-dev bison

2. To make changes to the configuration file, run the make command:

        make menuconfig

3. building the kernel by running the following command:

        make -j2

4. Install the required modules with this command:

        sudo make modules_install

5. install the kernel by typing:

        sudo make install 

6. Update the initramfs to the installed kernel version:

        sudo update-initramfs -c -k <version>

   Example:
   
        sudo update-initramfs -c -k 5.9.6

7. Update the GRUB bootloader with this command:

        sudo update-grub

8. run reboot command

        sudo reboot

9. Verify Kernel Version

        uname -mrs
