# ROS_SLAM Getting Start (RP Lidar) - RVIZ

open terminal (ctrl + alt + t)

1. USB Port (setting authority)
$ ls /dev/ttyUSB0
$ ls -l /dev | grep ttyUSB0
$ sudo chmod 666 /dev/ttyUSB0
Default is ros-kinetic-ros-base if no packages are specified.

 2. 
Usage:
$ cd catkin_ws/
$ catkin_make
$ source devel/setup.bash
$ roslaunch rplidar_ros rplidar.launch

3
How to Start SLAM
$ source devel/setup.bash
$ roslaunch hector_slam_launch tutorial_tif.launch


Copyright (c) 2020 joosun_lee

