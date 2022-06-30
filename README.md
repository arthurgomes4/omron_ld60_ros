[![Image](https://img.shields.io/badge/ROS-Noetic-purple.svg)](https://github.com/arthurgomes4)
[![Image](https://img.shields.io/badge/Gazebo-11.0.0-orange.svg)](https://github.com/arthurgomes4)

# TO DO  
Goal: To get frontier explore working in gazebo  

Checklist  
- [x] Get omron-model in gazebo world (takshak)  
- [x] Get navigation working  
    - gmapping
    - move_base
- [ ] Get Exploration working

# Omron_LD60_ROS
miscellaneous ROS packages for the Omron LD60 UGV

## Usage
Clone this package into your local workspace's `src` directory. Build and source.

## Launch Files
* `display_castors.launch`: launch the robot with castors enabled in rviz with joint publisher gui.
* `display_no_castors.launch`: launch the robot with castors disabled in rviz with joint publisher gui.
* `gazebo_castors.launch`: launch the robot in a gazebo simluation and rviz visualisation with castors enabled and diff drive plugin.
* `gazebo_no_castors.launch`: launch the robot in a gazebo simluation and rviz visualisation with castors disabled and diff drive plugin.

## Robot Models
* `LD60_castors.xacro`: castors enabled + diff drive.
* `LD60_no_castors.xacro`: castors disabled + diff drive.

## Importing Model into Unity
* use the command `xacro LD60_castors.xacro > LD60_castors.urdf` to generate the urdf.
* In the generated urdf change the line `<mesh filename="package://omron_ld60_description/models/meshes/LD_Platform.STL" />` to `<mesh filename="meshes/LD_Platform.STL"/>`.


[![Image](https://img.shields.io/badge/developed%20using-VSCode-green.svg)](https://code.visualstudio.com/)
[![Image](https://img.shields.io/badge/Developer-arthurgomes4-blue.svg)](https://github.com/arthurgomes4)
