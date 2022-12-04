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


```
akbarjon@ubuntu:~$ ssh ubuntu@172.20.10.4
ubuntu@172.20.10.4's password: 
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 5.4.0-1074-raspi aarch64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage
```
Install LDS-02 driver and update Turtlebot3 packages
```
ubuntu@ubuntu:~$ sudo apt update
Hit:1 http://packages.ros.org/ros2/ubuntu focal InRelease
Building dependency tree       
Reading state information... Done
```



```
ubuntu@ubuntu:~$ sudo apt install libudev-dev
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)      
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)      
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)      
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)      
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)      
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)      
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)      
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)      
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)      
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)      
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)       
^Citing for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 3876 (apt)... 59s
ubuntu@ubuntu:~$ sudo kill 3876 -9
ubuntu@ubuntu:~$ sudo apt install libudev-dev
E: dpkg was interrupted, you must manually run 'sudo dpkg --configure -a' to correct the problem. 
ubuntu@ubuntu:~$ sudo dpkg --configure -a
Setting up libxcb-dri3-0:arm64 (1.14-2) ...
Setting up libwayland-server0:arm64 (1.18.0-1ubuntu0.1) ...
Setting up libx11-xcb1:arm64 (2:1.6.9-2ubuntu1.2) ...
Setting up libice6:arm64 (2:1.0.10-0ubuntu1) ...
Setting up mysql-common (5.8+1.0.5ubuntu2) ...
update-alternatives: using /etc/mysql/my.cnf.fallback to provide /etc/mysql/my.cnf (my.cnf) in auto mode
Setting up libmysqlclient21:arm64 (8.0.31-0ubuntu0.20.04.2) ...
Setting up libdouble-conversion3:arm64 (3.1.5-4ubuntu1) ...
Setting up libxft2:arm64 (2.3.3-0ubuntu1) ...
Setting up libdrm-nouveau2:arm64 (2.4.107-8ubuntu1~20.04.2) ...
Setting up libxcb-xfixes0:arm64 (1.14-2) ...
Setting up libxcb-xinput0:arm64 (1.14-2) ...
Setting up libwoff1:arm64 (1.0.2-1build2) ...
Setting up libhyphen0:arm64 (2.8.8-7) ...
Setting up libgbm1:arm64 (21.2.6-0ubuntu0.1~20.04.2) ...
Setting up libdrm-radeon1:arm64 (2.4.107-8ubuntu1~20.04.2) ...
Setting up libglvnd0:arm64 (1.3.2-1~ubuntu0.20.04.2) ...
Setting up fonts-lyx (2.3.4.2-2) ...
Setting up libxcb-glx0:arm64 (1.14-2) ...
Setting up libxcb-keysyms1:arm64 (0.4.0-1build1) ...
Setting up libxcb-shape0:arm64 (1.14-2) ...
Setting up libsensors-config (1:3.6.0-2ubuntu1.1) ...
Setting up m4 (1.4.18-4) ...
Setting up libxcb-render-util0:arm64 (0.3.9-1build1) ...
Setting up libxcb-icccm4:arm64 (0.4.1-1.1) ...
Setting up libpthread-stubs0-dev:arm64 (0.4-1) ...
Setting up libpcre2-16-0:arm64 (10.34-7ubuntu0.1) ...
Setting up libopengl0:arm64 (1.3.2-1~ubuntu0.20.04.2) ...
Setting up libxcb-util1:arm64 (0.4.0-0ubuntu3) ...
Setting up libxxf86vm1:arm64 (1:1.1.4-1build1) ...
Setting up poppler-data (0.4.9-2) ...
Setting up libxcb-xkb1:arm64 (1.14-2) ...
Setting up libxcb-image0:arm64 (0.4.0-1build1) ...
Setting up libxcb-present0:arm64 (1.14-2) ...
Setting up xtrans-dev (1.4.0-1) ...
Setting up autotools-dev (20180224.1) ...
Setting up libxcb-xinerama0:arm64 (1.14-2) ...
Setting up libgles2:arm64 (1.3.2-1~ubuntu0.20.04.2) ...
Setting up qt5-qmake-bin (5.12.8+dfsg-0ubuntu2.1) ...
Setting up libxcb-sync1:arm64 (1.14-2) ...
Setting up libllvm12:arm64 (1:12.0.0-3ubuntu1~20.04.5) ...
Setting up libgles1:arm64 (1.3.2-1~ubuntu0.20.04.2) ...
Setting up libxkbcommon-x11-0:arm64 (0.10.0-1) ...
Setting up liborc-0.4-0:arm64 (1:0.4.31-1) ...
Setting up cython3 (0.29.14-0.1ubuntu3) ...
Setting up gcc-8-base:arm64 (8.4.0-3ubuntu2) ...
Setting up libtcl8.6:arm64 (8.6.10+dfsg-1) ...
Setting up libsensors5:arm64 (1:3.6.0-2ubuntu1.1) ...
Setting up libqt5core5a:arm64 (5.12.8+dfsg-0ubuntu2.1) ...
Setting up libglapi-mesa:arm64 (21.2.6-0ubuntu0.1~20.04.2) ...
Setting up libmtdev1:arm64 (1.1.5-1.1) ...
Setting up libvulkan1:arm64 (1.2.131.2-1) ...
Setting up autoconf (2.69-11.1) ...
Setting up libxcb-dri2-0:arm64 (1.14-2) ...
Setting up libxshmfence1:arm64 (1.3-1) ...
Setting up libqt5dbus5:arm64 (5.12.8+dfsg-0ubuntu2.1) ...
Setting up libxcb-randr0:arm64 (1.14-2) ...
Setting up fonts-liberation (1:1.07.4-11) ...
Setting up xorg-sgml-doctools (1:1.11-1) ...
Setting up libxss1:arm64 (1:1.2.3-1) ...
Setting up libopengl-dev:arm64 (1.3.2-1~ubuntu0.20.04.2) ...
Setting up cpp-8 (8.4.0-3ubuntu2) ...
Setting up libqt5sensors5:arm64 (5.12.8-0ubuntu1) ...
Setting up libdaemon0:arm64 (0.14-7) ...
Setting up libqt5test5:arm64 (5.12.8+dfsg-0ubuntu2.1) ...
Setting up libavahi-core7:arm64 (0.7-4ubuntu7.1) ...
Setting up libsm6:arm64 (2:1.2.3-1) ...
Setting up libevdev2:arm64 (1.9.0+dfsg-1ubuntu0.2) ...
Setting up libqt5concurrent5:arm64 (5.12.8+dfsg-0ubuntu2.1) ...
Setting up qtchooser (66-2build1) ...
Setting up libmysqlclient-dev (8.0.31-0ubuntu0.20.04.2) ...
Setting up libdrm-amdgpu1:arm64 (2.4.107-8ubuntu1~20.04.2) ...
Setting up libwacom-common (1.3-2ubuntu3) ...
Setting up libwayland-client0:arm64 (1.18.0-1ubuntu0.1) ...
Setting up automake (1:1.16.1-4ubuntu6) ...
update-alternatives: using /usr/bin/automake-1.16 to provide /usr/bin/automake (automake) in auto mode
Setting up default-libmysqlclient-dev:arm64 (1.0.5ubuntu2) ...
Setting up libvulkan-dev:arm64 (1.2.131.2-1) ...
Setting up qt5-qmake:arm64 (5.12.8+dfsg-0ubuntu2.1) ...
Setting up libtk8.6:arm64 (8.6.10-1) ...
Setting up libqt5positioning5:arm64 (5.12.8+dfsg-0ubuntu1) ...
Setting up libgl1-mesa-dri:arm64 (21.2.6-0ubuntu0.1~20.04.2) ...
Setting up libgstreamer-plugins-base1.0-0:arm64 (1.16.3-0ubuntu1.1) ...
Setting up libqt5network5:arm64 (5.12.8+dfsg-0ubuntu2.1) ...
Setting up libqt5sql5:arm64 (5.12.8+dfsg-0ubuntu2.1) ...
Setting up qtbase5-dev-tools (5.12.8+dfsg-0ubuntu2.1) ...
Setting up libqt5xml5:arm64 (5.12.8+dfsg-0ubuntu2.1) ...
Setting up libegl-mesa0:arm64 (21.2.6-0ubuntu0.1~20.04.2) ...
Setting up libqt5qml5:arm64 (5.12.8-0ubuntu1) ...
Setting up libqt5webchannel5:arm64 (5.12.8-0ubuntu1) ...
Setting up avahi-daemon (0.7-4ubuntu7.1) ...
Created symlink /etc/systemd/system/dbus-org.freedesktop.Avahi.service → /lib/systemd/system/avahi-daemon.service.
Created symlink /etc/systemd/system/multi-user.target.wants/avahi-daemon.service → /lib/systemd/system/avahi-daemon.service.
Created symlink /etc/systemd/system/sockets.target.wants/avahi-daemon.socket → /lib/systemd/system/avahi-daemon.socket.
Setting up libegl1:arm64 (1.3.2-1~ubuntu0.20.04.2) ...
Setting up libwacom2:arm64 (1.3-2ubuntu3) ...
Setting up tk8.6-blt2.5 (2.5.3+dfsg-4) ...
Setting up libglx-mesa0:arm64 (21.2.6-0ubuntu0.1~20.04.2) ...
Setting up libglx0:arm64 (1.3.2-1~ubuntu0.20.04.2) ...
Setting up blt (2.5.3+dfsg-4) ...
Setting up libinput-bin (1.15.5-1ubuntu0.3) ...
Setting up libgl1:arm64 (1.3.2-1~ubuntu0.20.04.2) ...
Setting up libglu1-mesa:arm64 (9.0.1-1build1) ...
Setting up libinput10:arm64 (1.15.5-1ubuntu0.3) ...
Setting up libqt5gui5:arm64 (5.12.8+dfsg-0ubuntu2.1) ...
Setting up libqt5widgets5:arm64 (5.12.8+dfsg-0ubuntu2.1) ...
Setting up libqt5printsupport5:arm64 (5.12.8+dfsg-0ubuntu2.1) ...
Setting up libqt5quick5:arm64 (5.12.8-0ubuntu1) ...
Setting up libqt5quickshapes5:arm64 (5.12.8-0ubuntu1) ...
Setting up libqt5quicktest5:arm64 (5.12.8-0ubuntu1) ...
Setting up qtdeclarative5-dev-tools (5.12.8-0ubuntu1) ...
Setting up libqt5svg5:arm64 (5.12.8-0ubuntu1) ...
Setting up libqt5webkit5:arm64 (5.212.0~alpha4-1ubuntu2.1) ...
Setting up qt5-qmltooling-plugins:arm64 (5.12.8-0ubuntu1) ...
Setting up libqt5quickwidgets5:arm64 (5.12.8-0ubuntu1) ...
Setting up libqt5quickparticles5:arm64 (5.12.8-0ubuntu1) ...
Processing triggers for fontconfig (2.13.1-2ubuntu3) ...
Processing triggers for libc-bin (2.31-0ubuntu9.7) ...
Processing triggers for systemd (245.4-4ubuntu3.15) ...
Processing triggers for man-db (2.9.1-1) ...
Processing triggers for dbus (1.12.16-2ubuntu2.3) ...
Processing triggers for sgml-base (1.29.1) ...
Processing triggers for install-info (6.7.0.dfsg.2-5) ...
Setting up x11proto-dev (2019.2-1ubuntu1) ...
Setting up libxau-dev:arm64 (1:1.0.9-0ubuntu1) ...
Setting up libxdmcp-dev:arm64 (1:1.1.3-0ubuntu1) ...
Setting up x11proto-core-dev (2019.2-1ubuntu1) ...
Setting up x11proto-xext-dev (2019.2-1ubuntu1) ...
Setting up libxcb1-dev:arm64 (1.14-2) ...
Setting up libx11-dev:arm64 (2:1.6.9-2ubuntu1.2) ...
Setting up libxext-dev:arm64 (2:1.3.4-0ubuntu1) ...
Setting up libglx-dev:arm64 (1.3.2-1~ubuntu0.20.04.2) ...
Setting up libgl-dev:arm64 (1.3.2-1~ubuntu0.20.04.2) ...
Setting up libegl-dev:arm64 (1.3.2-1~ubuntu0.20.04.2) ...
Setting up libglu1-mesa-dev:arm64 (9.0.1-1build1) ...
Setting up qtbase5-dev:arm64 (5.12.8+dfsg-0ubuntu2.1) ...
Setting up qtdeclarative5-dev:arm64 (5.12.8-0ubuntu1) ...
Setting up libgles-dev:arm64 (1.3.2-1~ubuntu0.20.04.2) ...
Setting up libglvnd-dev:arm64 (1.3.2-1~ubuntu0.20.04.2) ...
Setting up libqt5webkit5-dev:arm64 (5.212.0~alpha4-1ubuntu2.1) ...
Setting up libgl1-mesa-dev:arm64 (21.2.6-0ubuntu0.1~20.04.2) ...
ubuntu@ubuntu:~$ sudo apt install libudev-dev
Reading package lists... Done
Building dependency tree       
Reading state information... Done
libudev-dev is already the newest version (245.4-4ubuntu3.19).
The following packages were automatically installed and are no longer required:
  avahi-daemon blt cpp-8 cython3 default-libmysqlclient-dev fonts-lyx freeglut3 gcc-8-base libavahi-core7 libdaemon0 libdouble-conversion3
  libdrm-amdgpu1 libdrm-nouveau2 libdrm-radeon1 libegl-dev libegl-mesa0 libegl1 libevdev2 libgbm1 libgl-dev libgl1 libgl1-mesa-dev libgl1-mesa-dri
  libglapi-mesa libgles-dev libgles1 libgles2 libglu1-mesa libglu1-mesa-dev libglvnd-dev libglvnd0 libglx-dev libglx-mesa0 libglx0
  libgstreamer-plugins-base1.0-0 libhyphen0 libice6 libinput-bin libinput10 libllvm12 libmtdev1 libmysqlclient-dev libmysqlclient21 libopengl-dev
  libopengl0 liborc-0.4-0 libpcre2-16-0 libpthread-stubs0-dev libqt5concurrent5 libqt5core5a libqt5dbus5 libqt5gui5 libqt5network5
  libqt5positioning5 libqt5printsupport5 libqt5qml5 libqt5quick5 libqt5quickparticles5 libqt5quickshapes5 libqt5quicktest5 libqt5quickwidgets5
  libqt5sensors5 libqt5sql5 libqt5svg5 libqt5test5 libqt5webchannel5 libqt5webkit5 libqt5webkit5-dev libqt5widgets5 libqt5xml5 libsensors-config
  libsensors5 libsm6 libtcl8.6 libtk8.6 libvulkan-dev libvulkan1 libwacom-common libwacom2 libwayland-server0 libwoff1 libx11-dev libx11-xcb1
  libxau-dev libxcb-dri2-0 libxcb-dri3-0 libxcb-glx0 libxcb-icccm4 libxcb-image0 libxcb-keysyms1 libxcb-present0 libxcb-randr0 libxcb-render-util0
  libxcb-shape0 libxcb-sync1 libxcb-util1 libxcb-xfixes0 libxcb-xinerama0 libxcb-xinput0 libxcb-xkb1 libxcb1-dev libxdmcp-dev libxext-dev libxft2
  libxkbcommon-x11-0 libxshmfence1 libxss1 libxxf86vm1 linux-headers-5.4.0-1028-raspi linux-image-5.4.0-1028-raspi linux-modules-5.4.0-1028-raspi
  linux-raspi-headers-5.4.0-1028 mysql-common poppler-data qt5-qmake qt5-qmake-bin qt5-qmltooling-plugins qtbase5-dev qtbase5-dev-tools qtchooser
  qtdeclarative5-dev qtdeclarative5-dev-tools tk8.6-blt2.5 x11proto-core-dev x11proto-dev x11proto-xext-dev xorg-sgml-doctools xtrans-dev
Use 'sudo apt autoremove' to remove them.
The following packages will be upgraded:
  freeglut3
1 upgraded, 0 newly installed, 0 to remove and 268 not upgraded.
1 not fully installed or removed.
Need to get 0 B/65.0 kB of archives.
After this operation, 293 kB of additional disk space will be used.
(Reading database ... 194365 files and directories currently installed.)
Preparing to unpack .../freeglut3_2.8.1-3_arm64.deb ...
Unpacking freeglut3:arm64 (2.8.1-3) over (2.8.1-3) ...
Setting up freeglut3:arm64 (2.8.1-3) ...
Processing triggers for libc-bin (2.31-0ubuntu9.7) ...
^C
ubuntu@ubuntu:~$ sudo apt install libudev-dev
Reading package lists... Done
Building dependency tree       
Reading state information... Done
libudev-dev is already the newest version (245.4-4ubuntu3.19).
The following packages were automatically installed and are no longer required:
  avahi-daemon blt cpp-8 cython3 default-libmysqlclient-dev fonts-lyx freeglut3 gcc-8-base libavahi-core7 libdaemon0 libdouble-conversion3
  libdrm-amdgpu1 libdrm-nouveau2 libdrm-radeon1 libegl-dev libegl-mesa0 libegl1 libevdev2 libgbm1 libgl-dev libgl1 libgl1-mesa-dev libgl1-mesa-dri
  libglapi-mesa libgles-dev libgles1 libgles2 libglu1-mesa libglu1-mesa-dev libglvnd-dev libglvnd0 libglx-dev libglx-mesa0 libglx0
  libgstreamer-plugins-base1.0-0 libhyphen0 libice6 libinput-bin libinput10 libllvm12 libmtdev1 libmysqlclient-dev libmysqlclient21 libopengl-dev
  libopengl0 liborc-0.4-0 libpcre2-16-0 libpthread-stubs0-dev libqt5concurrent5 libqt5core5a libqt5dbus5 libqt5gui5 libqt5network5
  libqt5positioning5 libqt5printsupport5 libqt5qml5 libqt5quick5 libqt5quickparticles5 libqt5quickshapes5 libqt5quicktest5 libqt5quickwidgets5
  libqt5sensors5 libqt5sql5 libqt5svg5 libqt5test5 libqt5webchannel5 libqt5webkit5 libqt5webkit5-dev libqt5widgets5 libqt5xml5 libsensors-config
  libsensors5 libsm6 libtcl8.6 libtk8.6 libvulkan-dev libvulkan1 libwacom-common libwacom2 libwayland-server0 libwoff1 libx11-dev libx11-xcb1
  libxau-dev libxcb-dri2-0 libxcb-dri3-0 libxcb-glx0 libxcb-icccm4 libxcb-image0 libxcb-keysyms1 libxcb-present0 libxcb-randr0 libxcb-render-util0
  libxcb-shape0 libxcb-sync1 libxcb-util1 libxcb-xfixes0 libxcb-xinerama0 libxcb-xinput0 libxcb-xkb1 libxcb1-dev libxdmcp-dev libxext-dev libxft2
  libxkbcommon-x11-0 libxshmfence1 libxss1 libxxf86vm1 linux-headers-5.4.0-1028-raspi linux-image-5.4.0-1028-raspi linux-modules-5.4.0-1028-raspi
  linux-raspi-headers-5.4.0-1028 mysql-common poppler-data qt5-qmake qt5-qmake-bin qt5-qmltooling-plugins qtbase5-dev qtbase5-dev-tools qtchooser
  qtdeclarative5-dev qtdeclarative5-dev-tools tk8.6-blt2.5 x11proto-core-dev x11proto-dev x11proto-xext-dev xorg-sgml-doctools xtrans-dev
Use 'sudo apt autoremove' to remove them.
0 upgraded, 0 newly installed, 0 to remove and 268 not upgraded.
ubuntu@ubuntu:~$ cd ~/turtlebot3_ws/src
ubuntu@ubuntu:~/turtlebot3_ws/src$ git clone -b ros2-devel https://github.com/ROBOTIS-GIT/ld08_driver.git
fatal: destination path 'ld08_driver' already exists and is not an empty directory.
ubuntu@ubuntu:~/turtlebot3_ws/src$ cd ~/turtlebot3_ws/src/turtlebot3 && git pull
Already up to date.
ubuntu@ubuntu:~/turtlebot3_ws/src/turtlebot3$ rm -r turtlebot3_cartographer turtlebot3_navigation2
rm: cannot remove 'turtlebot3_cartographer': No such file or directory
rm: cannot remove 'turtlebot3_navigation2': No such file or directory
ubuntu@ubuntu:~/turtlebot3_ws/src/turtlebot3$ cd ~/turtlebot3_ws && colcon build --symlink-install
Starting >>> turtlebot3_description
Starting >>> turtlebot3_node                         
Starting >>> turtlebot3_example
Starting >>> turtlebot3_teleop                                                                                        
Finished <<< turtlebot3_description [3.43s]                                                                                                  
Starting >>> ld08_driver
Finished <<< turtlebot3_node [3.50s]                                                                                                                
Starting >>> turtlebot3_bringup
Finished <<< turtlebot3_bringup [0.93s]                                                                                                              
Finished <<< ld08_driver [1.29s]                                                                                     
Finished <<< turtlebot3_teleop [5.28s]                                                  
Finished <<< turtlebot3_example [5.37s]
Starting >>> turtlebot3
Finished <<< turtlebot3 [0.64s]                  

Summary: 7 packages finished [7.69s]
ubuntu@ubuntu:~/turtlebot3_ws$ echo 'export LDS_MODEL=LDS-02' >> ~/.bashrc
ubuntu@ubuntu:~/turtlebot3_ws$ source ~/.bashrc
ubuntu@ubuntu:~/turtlebot3_ws$ sudo dpkg --add-architecture armhf
ubuntu@ubuntu:~/turtlebot3_ws$ sudo apt update
Hit:1 http://packages.ros.org/ros2/ubuntu focal InRelease                                           
Hit:2 http://ports.ubuntu.com/ubuntu-ports focal InRelease                                          
Get:3 http://ports.ubuntu.com/ubuntu-ports focal-updates InRelease [114 kB]
Get:4 http://ports.ubuntu.com/ubuntu-ports focal-backports InRelease [108 kB]
Get:5 http://ports.ubuntu.com/ubuntu-ports focal-security InRelease [114 kB]
Fetched 336 kB in 4s (93.2 kB/s)   
 
Reading package lists... Done
Building dependency tree       
Reading state information... Done
268 packages can be upgraded. Run 'apt list --upgradable' to see them.
ubuntu@ubuntu:~/turtlebot3_ws$  
ubuntu@ubuntu:~/turtlebot3_ws$ sudo apt install libc6:armhf
Reading package lists... Done
Building dependency tree       
Reading state information... Done
libc6:armhf is already the newest version (2.31-0ubuntu9.9).
The following packages were automatically installed and are no longer required:
  avahi-daemon blt cpp-8 cython3 default-libmysqlclient-dev fonts-lyx freeglut3 gcc-8-base libavahi-core7 libdaemon0 libdouble-conversion3
  libdrm-amdgpu1 libdrm-nouveau2 libdrm-radeon1 libegl-dev libegl-mesa0 libegl1 libevdev2 libgbm1 libgl-dev libgl1 libgl1-mesa-dev libgl1-mesa-dri
  libglapi-mesa libgles-dev libgles1 libgles2 libglu1-mesa libglu1-mesa-dev libglvnd-dev libglvnd0 libglx-dev libglx-mesa0 libglx0
  libgstreamer-plugins-base1.0-0 libhyphen0 libice6 libinput-bin libinput10 libllvm12 libmtdev1 libmysqlclient-dev libmysqlclient21 libopengl-dev
  libopengl0 liborc-0.4-0 libpcre2-16-0 libpthread-stubs0-dev libqt5concurrent5 libqt5core5a libqt5dbus5 libqt5gui5 libqt5network5
  libqt5positioning5 libqt5printsupport5 libqt5qml5 libqt5quick5 libqt5quickparticles5 libqt5quickshapes5 libqt5quicktest5 libqt5quickwidgets5
  libqt5sensors5 libqt5sql5 libqt5svg5 libqt5test5 libqt5webchannel5 libqt5webkit5 libqt5webkit5-dev libqt5widgets5 libqt5xml5 libsensors-config
  libsensors5 libsm6 libtcl8.6 libtk8.6 libvulkan-dev libvulkan1 libwacom-common libwacom2 libwayland-server0 libwoff1 libx11-dev libx11-xcb1
  libxau-dev libxcb-dri2-0 libxcb-dri3-0 libxcb-glx0 libxcb-icccm4 libxcb-image0 libxcb-keysyms1 libxcb-present0 libxcb-randr0 libxcb-render-util0
  libxcb-shape0 libxcb-sync1 libxcb-util1 libxcb-xfixes0 libxcb-xinerama0 libxcb-xinput0 libxcb-xkb1 libxcb1-dev libxdmcp-dev libxext-dev libxft2
  libxkbcommon-x11-0 libxshmfence1 libxss1 libxxf86vm1 linux-headers-5.4.0-1028-raspi linux-image-5.4.0-1028-raspi linux-modules-5.4.0-1028-raspi
  linux-raspi-headers-5.4.0-1028 mysql-common poppler-data qt5-qmake qt5-qmake-bin qt5-qmltooling-plugins qtbase5-dev qtbase5-dev-tools qtchooser
  qtdeclarative5-dev qtdeclarative5-dev-tools tk8.6-blt2.5 x11proto-core-dev x11proto-dev x11proto-xext-dev xorg-sgml-doctools xtrans-dev
Use 'sudo apt autoremove' to remove them.
0 upgraded, 0 newly installed, 0 to remove and 268 not upgraded.
ubuntu@ubuntu:~/turtlebot3_ws$ export OPENCR_PORT=/dev/ttyACM0
ubuntu@ubuntu:~/turtlebot3_ws$ export OPENCR_MODEL=burger
ubuntu@ubuntu:~/turtlebot3_ws$ rm -rf ./opencr_update.tar.bz2
ubuntu@ubuntu:~/turtlebot3_ws$ wget https://github.com/ROBOTIS-GIT/OpenCR-Binaries/raw/master/turtlebot3/ROS2/latest/opencr_update.tar.bz2
--2022-11-30 05:58:44--  https://github.com/ROBOTIS-GIT/OpenCR-Binaries/raw/master/turtlebot3/ROS2/latest/opencr_update.tar.bz2
Resolving github.com (github.com)... 20.200.245.247
Connecting to github.com (github.com)|20.200.245.247|:443... connected.
HTTP request sent, awaiting response... 302 Found
Location: https://raw.githubusercontent.com/ROBOTIS-GIT/OpenCR-Binaries/master/turtlebot3/ROS2/latest/opencr_update.tar.bz2 [following]
--2022-11-30 05:58:44--  https://raw.githubusercontent.com/ROBOTIS-GIT/OpenCR-Binaries/master/turtlebot3/ROS2/latest/opencr_update.tar.bz2
Resolving raw.githubusercontent.com (raw.githubusercontent.com)... 185.199.111.133, 185.199.110.133, 185.199.109.133, ...
Connecting to raw.githubusercontent.com (raw.githubusercontent.com)|185.199.111.133|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 686080 (670K) [application/octet-stream]
Saving to: ‘opencr_update.tar.bz2’

opencr_update.tar.bz2                 100%[=======================================================================>] 670.00K  2.45MB/s    in 0.3s    

2022-11-30 05:58:45 (2.45 MB/s) - ‘opencr_update.tar.bz2’ saved [686080/686080]

ubuntu@ubuntu:~/turtlebot3_ws$ tar -xvf ./opencr_update.tar.bz2
opencr_update/
opencr_update/released_0.2.0.txt
opencr_update/waffle.opencr
opencr_update/README.md
opencr_update/turtlebot3_manipulation.opencr
opencr_update/update.bat
opencr_update/opencr_ld_shell_arm
opencr_update/burger.opencr
opencr_update/update.sh
opencr_update/opencr_ld_shell_x86.exe
opencr_update/opencr_ld_shell_x86
ubuntu@ubuntu:~/turtlebot3_ws$ cd ~/opencr_update
ubuntu@ubuntu:~/opencr_update$ ./update.sh $OPENCR_PORT $OPENCR_MODEL.opencr
aarch64
arm
OpenCR Update Start..
opencr_ld_shell ver 1.0.0
opencr_ld_main 
[  ] file name   	: burger.opencr 
[  ] file size   	: 127 KB
[  ] fw_name     	: burger 
[  ] fw_ver      	: V190829R3 
[OK] Open port   	: /dev/ttyACM0
[  ]
[  ] Board Name  	: OpenCR R1.0
[  ] Board Ver   	: 0x17020800
[  ] Board Rev   	: 0x00000000
[OK] flash_erase 	: 0.88s
[OK] flash_write 	: 1.28s 
[OK] CRC Check   	: CBBCC4 CBBCC4 , 0.004000 sec
[OK] Download 
[OK] jump_to_fw 
ubuntu@ubuntu:~/opencr_update$ 

```

<img width="1440" alt="image" src="https://user-images.githubusercontent.com/76453238/205494727-34a9fede-e3f8-4c9e-8221-ac271f01d0f7.png">

```
akbarjon@ubuntu:~$ ssh ubuntu@172.20.10.4
ubuntu@172.20.10.4's password: 
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 5.4.0-1077-raspi aarch64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  System information as of Sun 04 Dec 2022 01:04:58 PM UTC

  System load:  0.42               Temperature:            56.0 C
  Usage of /:   53.4% of 14.32GB   Processes:              153
  Memory usage: 14%                Users logged in:        1
  Swap usage:   0%                 IPv4 address for wlan0: 172.20.10.4

 * Strictly confined Kubernetes makes edge and IoT secure. Learn how MicroK8s
   just raised the bar for easy, resilient and secure K8s cluster deployment.

   https://ubuntu.com/engage/secure-kubernetes-at-the-edge

300 updates can be applied immediately.
2 of these updates are standard security updates.
To see these additional updates run: apt list --upgradable

New release '22.04.1 LTS' available.
Run 'do-release-upgrade' to upgrade to it.


Last login: Sun Dec  4 13:00:45 2022 from 172.20.10.10
ubuntu@ubuntu:~$ ros2 topic list
/battery_state
/cmd_vel
/imu
/joint_states
/magnetic_field
/odom
/parameter_events
/robot_description
/rosout
/scan
/sensor_state
/tf
/tf_static
ubuntu@ubuntu:~$ ros2 service list
/diff_drive_controller/describe_parameters
/diff_drive_controller/get_parameter_types
/diff_drive_controller/get_parameters
/diff_drive_controller/list_parameters
/diff_drive_controller/set_parameters
/diff_drive_controller/set_parameters_atomically
/ld08_driver/describe_parameters
/ld08_driver/get_parameter_types
/ld08_driver/get_parameters
/ld08_driver/list_parameters
/ld08_driver/set_parameters
/ld08_driver/set_parameters_atomically
/motor_power
/reset
/robot_state_publisher/describe_parameters
/robot_state_publisher/get_parameter_types
/robot_state_publisher/get_parameters
/robot_state_publisher/list_parameters
/robot_state_publisher/set_parameters
/robot_state_publisher/set_parameters_atomically
/sound
/turtlebot3_node/describe_parameters
/turtlebot3_node/get_parameter_types
/turtlebot3_node/get_parameters
/turtlebot3_node/list_parameters
/turtlebot3_node/set_parameters
/turtlebot3_node/set_parameters_atomically


ubuntu@ubuntu:~$ export TURTLEBOT3_MODEL=${TB3_MODEL}
ubuntu@ubuntu:~$ ros2 run turtlebot3_teleop teleop_keyboard

Control Your TurtleBot3!
---------------------------
Moving around:
        w
   a    s    d
        x

w/x : increase/decrease linear velocity (Burger : ~ 0.22, Waffle and Waffle Pi : ~ 0.26)
a/d : increase/decrease angular velocity (Burger : ~ 2.84, Waffle and Waffle Pi : ~ 1.82)

space key, s : force stop

CTRL-C to quit

currently:	linear velocity 0.0	 angular velocity 0.0 
currently:	linear velocity 0.0	 angular velocity 0.0 


Control Your TurtleBot3!
---------------------------
Moving around:
        w
   a    s    d
        x

w/x : increase/decrease linear velocity (Burger : ~ 0.22, Waffle and Waffle Pi : ~ 0.26)
a/d : increase/decrease angular velocity (Burger : ~ 2.84, Waffle and Waffle Pi : ~ 1.82)

space key, s : force stop

CTRL-C to quit


```
