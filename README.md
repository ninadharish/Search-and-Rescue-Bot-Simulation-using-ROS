[alt text](/output/output.gif)

# Search and Rescue Bot Simulation using ROS

## Description

The final project is inspired by the the challenge of autonomous robotics for Ur- ban Search and Rescue (US&R). In US&R after a disaster occurs, a robot is used to explore an unknown environment, such as a partially collapsed building, and locates trapped or unconscious human victims of the disaster (see examples of robots in Figure 2). The robot builds a map of the collapsed building as it explores, and places markers in the map of where the victims are located. This map is then given to trained First Responders who use it to go into the building and rescue the victims. Instead of simulated victims, we use ArUco markers (squared fiducial markers) are used. Two turtlebots: the explorer to identify the location of victimes, and the follower to reach these locations and rescue them. The order in which the follower reaches the rescue points depends on the unique ID of the Aruco Marker. This project is a part of the Fall 2021 course ENPM809Y: Introductory Robot Programming taught by Dr. Zeid Kootbally.

## Output

![alt text](/output/output1.png)

Intermediate point in its search.

![alt text](/output/output2.png)

The Mouse reaches its goal position.

![alt text](/output/output3.png)


The Video Output can be found [here]().


## Getting Started

### Dependencies

<p align="left"> 
<a href="https://www.cplusplus.com/" target="_blank" rel="noreferrer"> <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/18/ISO_C%2B%2B_Logo.svg/800px-ISO_C%2B%2B_Logo.svg.png" alt="cpp" width="40" height="40"/> &ensp;</a>
<a href="https://www.ros.org/" target="_blank" rel="noreferrer"> <img align="bottom" src="https://upload.wikimedia.org/wikipedia/commons/b/bb/Ros_logo.svg" alt="ROS" width="70" height="40"/> &ensp;</a>
<a href="https://gazebosim.org/" target="_blank" rel="noreferrer"> <img align="bottom" src="https://upload.wikimedia.org/wikipedia/en/thumb/5/5e/Gazebo_logo_without_text.svg/300px-Gazebo_logo_without_text.svg.png?20150715002113" alt="Gazebo" width="60" height="50"/>&ensp; </a>
<a href="https://www.linux.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" alt="linux" width="40" height="40"/> &ensp;</a>

* [C++](https://www.cplusplus.com/)
* [Robot Operation System (ROS)](http://wiki.ros.org/)

### Installing

* Install ROS using the instructions on the [link](http://wiki.ros.org/Installation/Ubuntu).

* Install other dependencies. Replace '$ROS_DISTRO' with the proper ROS distribution (melodic/noetic).
```
sudo apt install ros-$ROS_DISTRO-turtlebot3
sudo apt install ros-$ROS_DISTRO-turtlebot3-bringup
sudo apt install ros-$ROS_DISTRO-turtlebot3-description
sudo apt install ros-$ROS_DISTRO-turtlebot3-gazebo
sudo apt install ros-$ROS_DISTRO-turtlebot3-msgs
sudo apt install ros-$ROS_DISTRO-turtlebot3-navigation
sudo apt install ros-$ROS_DISTRO-turtlebot3-simulations
sudo apt install ros-$ROS_DISTRO-turtlebot3-slam
sudo apt install ros-$ROS_DISTRO-move-base
sudo apt install ros-$ROS_DISTRO-move-base-msgs
sudo apt install ros-$ROS_DISTRO-aruco-detect
sudo apt install ros-$ROS_DISTRO-tf
sudo apt install ros-$ROS_DISTRO-tf2-ros
sudo apt install ros-$ROS_DISTRO-actionlib
sudo apt install ros-$ROS_DISTRO-actionlib-msgs
sudo apt install ros-$ROS_DISTRO-amcl
sudo apt install ros-$ROS_DISTRO-map-server
sudo apt install ros-$ROS_DISTRO-navigation
sudo apt install ros-$ROS_DISTRO-fiducial-msgs
```

### Executing program

After ROS installation, follow the instructions to execute the program:

* Edit your ./bashrc file and add the following lines.
```
export TURTLEBOT3_MODEL=waffle
export GAZEBO_MODEL_PATH=$GAZEBO_MODEL_PATH:/home/ninadharish/catkin_ws/src/final_project/models
```

* Create and build the Catkin Workspace.
```
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/
catkin build
source ./devel/setup.bash
cd src
```

* Clone the package into this folder and rename it to `final_project`.
```
git clone https://github.com/ninadharish/Search-and-Rescue-Bot-Simulation-using-ROS.git
```

* Build the Catkin workpace again.
```
cd ..
catkin build
source ./devel/setup.bash
```

* Start the ROS Master.
```
roscore
```

* Start the simulation.
```
roslaunch final_project multiple_robots.launch
```

* Start the rescue operation by running the node.

```
rosrun final_project final_project_node
```


## Authors

👤 **Ninad Harishchandrakar**

* [GitHub](https://github.com/ninadharish)
* [Email](ninad.harish@gmail.com)
* [LinkedIn](https://linkedin.com/in/ninadharish)


## Acknowledgments

👤 **Zeid Kootbally**

* [Email](zeidk@umd.edu)
* [GitHub](https://github.com/zeidk)