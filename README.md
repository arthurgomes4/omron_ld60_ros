[![Image](https://img.shields.io/badge/ROS-Noetic-purple.svg)](https://github.com/arthurgomes4)
[![Image](https://img.shields.io/badge/Gazebo-11.0.0-orange.svg)](https://github.com/arthurgomes4)

ADD IMAGE

# Omron LD-60 ROS  
ROS Package for the Omron LD60 AMR.  

## Introduction  
[Omron LD-60](https://industrial.omron.eu/en/products/ld-60-90) is an autonomous mobile robot designed to increase efficiency and automate various workflows in industries.  
This repository allows you to control and simulate the mobile robot via ROS and Gazebo. The package also integrates [move-base](http://wiki.ros.org/move_base) and [gmapping](http://wiki.ros.org/gmapping) to provide path planning and mapping capabilities.

## Prerequisites  
This package was developed and tested on [Ubuntu 20.04 LTS](https://releases.ubuntu.com/20.04/).  
Software and Tools utilized:  
* ROS Noetic  
* Rviz  
* Gazebo  

Install [ROS Noetic](http://wiki.ros.org/noetic/Installation/Ubuntu) from this official guide.  
To install additional ROS Packages, run this command  
`sudo apt install ros-noetic-xacro ros-noetic-move-base ros-noetic-gmapping ros-noetic-explore-lite ros-noetic-rviz`  

## Usage  

### Install the package  
Clone the ROS package into your ROS workspace and build.  
```
cd ~/catkin_ws/src  
git clone https://github.com/arthurgomes4/Omron_LD60_ROS.git  
cd ..  
catkin_make  
source devel/setup.bash        
```
### Run the launch file  

## Explanation  
### Launch Files
* `display_castors.launch`: launch the robot with castors enabled in rviz with joint publisher gui.
* `display_no_castors.launch`: launch the robot with castors disabled in rviz with joint publisher gui.
* `gazebo_castors.launch`: launch the robot in a gazebo simluation and rviz visualisation with castors enabled and diff drive plugin.
* `gazebo_no_castors.launch`: launch the robot in a gazebo simluation and rviz visualisation with castors disabled and diff drive plugin.  
* `move_base.launch`: Launches the motion planner for the robot. Set 2D Nav goals in rviz to observe this  
* `gmapping.launch`: Launches the SLAM node and maps the environment.  

### Robot Models
* `LD60_castors.xacro`: castors enabled + diff drive.
* `LD60_no_castors.xacro`: castors disabled + diff drive.

### Importing Model into Unity
* use the command `xacro LD60_castors.xacro > LD60_castors.urdf` to generate the urdf.
* In the generated urdf change the line `<mesh filename="package://omron_ld60_ros/models/meshes/LD_Platform.STL" />` to `<mesh filename="meshes/LD_Platform.STL"/>`.


[![Image](https://img.shields.io/badge/Developer-arthurgomes4-blue.svg)](https://github.com/arthurgomes4)
[![Image](https://img.shields.io/badge/Developer-Pranjalmishra30-blue.svg)](https://github.com/Pranjalmishra30)
