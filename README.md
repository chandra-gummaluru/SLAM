# SLAM on ROS #

This project runs on ROS Kinetic for Ubuntu 16.04

## Setting up the ROS Environment ##
1. Perform ROS Kinetic full install. See: [ROS Kinetic Installation](http://wiki.ros.org/kinetic/Installation/Ubuntu)
2. Install husky desktop and simulator. See: [Clearpath ROS Tutorial](https://www.clearpathrobotics.com/assets/guides/ros/Drive%20a%20Husky.html) or [Husky Simulation Wiki](http://wiki.ros.org/husky_gazebo/Tutorials/Simulating%20Husky).
Run:
```
$ sudo apt-get update
$ sudo apt-get install ros-kinetic-husky-desktop
$ sudo apt-get install ros-kinetic-husky-simulator
```
3. Install the Navigation stack: `sudo apt-get install ros-kinetic-navigation`

## Creating the ROS Workspace ##
Before cloning the git repository, create a workspace. Then run:
```
# Creates CMake file in src
$ mkdir -p ~/slam-ws/src
$ cd ~/slam-ws/src
$ catkin_init_workspace

# Creates setup files - build/ and devel/ folders
$ cd ~/slam-ws
$ catkin_make
```

## Creating a Package for using the Navigation Stack ##
**NOTE:** Do not execute this section, it's just documentation to how the nav_husky_gazebo package was set up.
Create the nav_husky_gazebo package with its dependencies:
```
$ catkin_create_pkg nav_husky_gazebo rospy move_base nav_msgs sensor_msgs std_msgs tf
```

### Useful ROS Resources ###
- [ROS Wiki](http://wiki.ros.org)
- [A Gentle Introduction to ROS](https://cse.sc.edu/~jokane/agitr/agitr-letter.pdf)
- [Programming with ROS](http://marte.aslab.upm.es/redmine/files/dmsf/p_drone-testbed/170324115730_268_Quigley_-_Programming_Robots_with_ROS.pdf?fbclid=IwAR2iVBeZ9WQu1uG614YMamUZlxvd8nJoHbxW5BntgaEjgVI4MBOzqOCdYi8)
