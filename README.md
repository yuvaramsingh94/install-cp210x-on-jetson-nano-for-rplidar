# install cp210x driver on jetson nano for rplidar
MIT License

Copyright (c) 2017-2018 Jetsonhacks

The default linux kernel coming with the jetson nano sdk or sdcard installation is missing driver for cp210x. this will not be a problem untill USB to UART chips are connected to jetosn nano . Rplidar A1 is one of the low-cost lidar available in the market best suited for Hobbies looking to build robots. unfortunatly, the missing driver cp210x makes it hard to install and work with Rplidar and other instruments using cp210x chip . the repository from jetsonhacks covers installation of the driver for tx1. in the case of jetson nano the kernel version pose a barrier for using the same compiled version . 

Here i have added a new compiled version of cp210x driver which can be directly installed onto jetson nano

To install:

$ sudo ./installCP210X.sh

<h3>FEB, 2020</h3>
Initial Release


 
