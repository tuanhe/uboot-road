# uboot-road
uboot学习之路


遇到了一个Your GCC is older than 6.0 and is not supported的问题，可以参考这个链接更改下mk文件https://blog.csdn.net/smile_5me/article/details/81981415
（这个是在编译树莓派3的时候遇到的）

如果是编译树莓派A或者B则没有这个报错了，应该是gcc版本太老导致的

关于树莓派的uboot具体编译流程，可以参考这个链接
http://www.embeddedforu.com/embedded-linux/raspberry-pi/how-to-compile-mainline-u-boot-for-raspberry-pi/

用到的指令是：
1，$ git clone git://git.denx.de/u-boot.git
2，sudo apt-get install gcc-arm-linux-gnueabi
3，$ ls configs/rpi_*
4，make rpi_defconfig
5，$ make -j4
过一小会就编译好了


反正编译uboot用到的几个指令就是：
git clone git://git.denx.de/u-boot.git && cd u-boot
make am335x_boneblack_defconfig
ARCH=arm CROSS_COMPILE=arm-linux-gnueabi- make
make j4






