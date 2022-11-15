# turtlebot3_burger

## Installing ROS 2 on a remote PC

```
akbarjon@ubuntu:~$ sudo apt upgrade -y
Reading package lists... Done
Building dependency tree       
Reading state information... Done
Calculating upgrade... Done

akbarjon@ubuntu:~$ wget https://raw.githubusercontent.com/ROBOTIS-GIT/robotis_tools/master/install_ros2_foxy.sh
--2022-11-15 10:44:06--  https://raw.githubusercontent.com/ROBOTIS-GIT/robotis_tools/master/install_ros2_foxy.sh
Resolving raw.githubusercontent.com (raw.githubusercontent.com)... 185.199.109.133, 185.199.108.133, 185.199.111.133, ...
Connecting to raw.githubusercontent.com (raw.githubusercontent.com)|185.199.109.133|:443... connected.
akbarjon@ubuntu:~$ sudo chmod 755 ./install_ros2_foxy.sh
[sudo] password for akbarjon: 
akbarjon@ubuntu:~$ bash ./install_ros2_foxy.sh

[Note] OS version  >>> Ubuntu 20.04 (Focal Fossa)
akbarjon@ubuntu:~$ bash ./install_ros2_foxy.sh

[Note] OS version  >>> Ubuntu 20.04 (Focal Fossa)
[Note] Target ROS version >>> ROS 2 Foxy Fitzroy
[Note] Colcon workspace   >>> /home/akbarjon/colcon_ws
```

Installing Gazebo 11
```
akbarjon@ubuntu:~$ sudo apt-get install ros-foxy-gazebo-*
Reading package lists... Done
Building dependency tree       
Reading state information... Done
akbarjon@ubuntu:~$ sudo apt install ros-foxy-cartographer
Reading package lists... Done
Building dependency tree       
Reading state information... Done
akbarjon@ubuntu:~$ sudo apt install ros-foxy-cartographer-ros
Reading package lists... Done
akbarjon@ubuntu:~$ sudo apt install ros-foxy-navigation2
Reading package lists... Done
akbarjon@ubuntu:~$ sudo apt install ros-foxy-nav2-bringup
Reading package lists... Done
Building dependency tree       
```

## Installing the turtlebot3 packages
```
akbarjon@ubuntu:~$ source ~/.bashrc
akbarjon@ubuntu:~$ sudo apt install ros-foxy-dynamixel-sdk
Reading package lists... Done
Building dependency tree       
Reading state information... Done
akbarjon@ubuntu:~$ sudo apt install ros-foxy-turtlebot3-msgs
Reading package lists... Done
Building dependency tree       
Reading state information... Done
akbarjon@ubuntu:~$ sudo apt install ros-foxy-turtlebot3
Reading package lists... Done
Building dependency tree       
Reading state information... Done
```

## Environemnt configuration
Setting up ROS environment for PV
```
akbarjon@ubuntu:~$ echo 'export ROS_DOMAIN_ID=30 #TURTLEBOT3' >> ~/.bashrc
akbarjon@ubuntu:~$ source ~/.bashrc
```
