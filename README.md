# Linux Oreo
(1)
==================================================================================
The Project 1 for Allwinner H3 pure Linux + busybox fs

1,bootloader/uboot-2017
make ARCH=arm CROSS_COMPILE=arm-linux-gnueabihf- orangepi_one_defconfig
make ARCH=arm CROSS_COMPILE=arm-linux-gnueabihf-

sudo dd if=./spl/sunxi-spl.bin of=/dev/sdb bs=1k seek=8
sudo dd if=./u-boot.bin of=/dev/sdb bs=1k seek=40

2,kernel/linux-4.11
make ARCH=arm CROSS_COMPILE=arm-linux-gnueabihf- sunxi_defconfig
make ARCH=arm CROSS_COMPILE=arm-linux-gnueabihf- zImage -j4
make ARCH=arm CROSS_COMPILE=arm-linux-gnueabihf- dtbs
make ARCH=arm CROSS_COMPILE=arm-linux-gnueabihf- modules

this project reference https://blog.csdn.net/qq_23922117/article/details/86625288
==================================================================================

