# installing-ROS-on-ubuntu20

To install ROS Noetic in ubuntu you need to execute these commands in the terminal:   
1- setup our computer to accept software from packages.ros.org.  
$ sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'  

2- Set up your keys  
$ sudo apt install curl  
$ curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -  

3- make sure your Debian package index is up-to-date  
$ sudo apt update  

4- install the desktop-full to install the whole ROS  
$ sudo apt install ros-noetic-desktop-full  

5- environment setup (bash)  
$ echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc  
$ source ~/.bashrc  

6- install dependencies for building ROS packages  
$ sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential  

7- initialize rosdep  
$ sudo apt install python3-rosdep  
$ sudo rosdep init  
$ rosdep update  

now ROS is installed and you can find out which version of ROS you installed you can run the following command  
$ roscore  

in my case i installed version Noetic 1.15.14
