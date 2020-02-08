# install cp210x driver on jetson nano for rplidar
MIT License

Copyright (c) 2017-2018 Jetsonhacks

The default linux kernel coming with the jetson nano sdk or sdcard installation is missing driver for cp210x. this will not be a problem untill USB to UART chips are connected to jetosn nano . Rplidar A1 is one of the low-cost lidar available in the market best suited for Hobbies looking to build robots. unfortunatly, the missing driver cp210x makes it hard to install and work with Rplidar and other instruments using cp210x chip . the repository from jetsonhacks covers installation of the driver for tx1. in the case of jetson nano the kernel version pose a barrier for using the same compiled version . 

Here i have added a new compiled version of cp210x driver which can be directly installed onto jetson nano

To install:

$ sudo ./installCDCACM.sh

<h2>cp210x USB to serial converter</h2>
This script install the CP210x USB to serial converter module. There are several different types of USB to serial converters (FTDI is built into the L4T 28.1 kernel), the CP210x is used by devices such as the RP-LIDAR products

<h2>ch341</h2>
This script install the CH-341 USB to serial converter module. There are several different types of USB to serial converters (FTDI is built into the L4T 28.1 kernel), this is the CH-341 which is used by many Arduino clones.


<h2>Notes</h2>
These scripts expect a stock kernel, kernel version 4.4.38-tegra

More than likely, you will need to replug the USB device for it to be detected properly after installing the kernel module.

These scripts check the version magic of the module and compares it to the kernel version running on the machine. If the two do not match, the user is asked if they still want to continue the installation. If the two match, the module is installed.

Note that on a version mismatch, the user can still install the module. However, some extra steps may be needed after the installation to get the module installed fully. The steps are not covered here, but should be readily available elsewhere.

These scripts are for L4T 28.1. L4T version 28.2 includes cp210x and cdc-acm modules.

<h2>Release Notes</h2>
<h3>February, 2018</h3>
Add cp210x and ch341 modules and install scripts

<h3>November, 2017</h3>
Initial Release


 
