# joosun.lee-wegokorea.kr
ROS_SLAM_getting start (RP Lidar)
installROSTX2
Install Robot Operating System (ROS) on NVIDIA Jetson TX2

These scripts will install Robot Operating System (ROS) on the NVIDIA Jetson TX2 development kit.

For L4T 28.2 (JetPack 3.2)

See releases or tags for earlier versions.

The script is based on the Ubuntu ARM install of ROS Kinetic: http://wiki.ros.org/kinetic/Installation/Ubuntu

Maintainer of ARM builds for ROS is http://answers.ros.org/users/1034/ahendrix/

There are two scripts:

installROS.sh

Usage: ./installROS.sh  [[-p package] | [-h]]
 -p | --package <packagename>  ROS package to install
                               Multiple Usage allowed
                               The first package should be a base package. One of the following:
                                 ros-kinetic-ros-base
                                 ros-kinetic-desktop
                                 ros-kinetic-desktop-full
 
Default is ros-kinetic-ros-base if no packages are specified.

Example Usage:

$ ./installROS.sh -p ros-kinetic-desktop -p ros-kinetic-rgbd-launch

This script installs a baseline ROS environment. There are several tasks:

Enable repositories universe, multiverse, and restricted
Adds the ROS sources list
Sets the needed keys
Loads specified ROS packages, defaults to ros-kinetic-base-ros if none specified
Initializes rosdep
You can edit this file to add the ROS packages for your application.

setupCatkinWorkspace.sh Usage:

$ ./setupCatkinWorkspace.sh [optionalWorkspaceName]

where optionalWorkspaceName is the name of the workspace to be used. The default workspace name is catkin_ws. This script also sets up some ROS environment variables. Refer to the script for details.

Note: On June 7, 2019 the GPG key for ROS was changed due to security issues. If you have ROS installed on your system before this, you should delete the GPG key:

$ sudo apt-key del 421C365BD9FF1F717815A3895523BAEEB01FA116
Release Notes
June 2019

L4T 28.2
Update GPG Key for ROS server
April 2018

L4T 28.2
November 2017

L4T 28.1
March 2017

Initial Release
L4T 27.1
License
MIT License

Copyright (c) 2017-2018 Jetsonhacks

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
