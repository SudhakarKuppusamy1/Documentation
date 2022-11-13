# Read Hat

All Linux distributions are based on a predefined kernel. But, if you want to disable several options and drivers or try experimental patches, you need to build a Linux kernel.

# Building Kernel:

1. Install Required packages

        sudo dnf install -y ncurses-devel make gcc bc bison flex elfutils-libelf-devel openssl-devel grub2

2. To make changes to the configuration file, run the make command:

        make menuconfig

3. building the kernel by running the following command:

        make -j2

4. Install the required modules with this command:

        sudo make modules_install

5. install the kernel by typing:

        sudo make install 

6. run reboot command

        sudo reboot

7. Verify Kernel Version

        uname -mrs
