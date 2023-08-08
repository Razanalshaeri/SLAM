# SLAM
Use Turtlebot3 with SLAM approach to create and save a map.
## 1-Install TurtleBot3 Packages
``` 
sudo apt-get install ros-melodic-dynamixel-sdk
sudo apt-get install ros-melodic-turtlebot3-msgs
sudo apt-get install ros-melodic-turtlebot3
``` 
### Set TurtleBot3 Model Name:
echo "export TURTLEBOT3_MODEL=burger" >> ~/.bashrc
## 2-Gazebo-Simulation
### Install Simulation Package:
cd ~/catkin_ws/src/
git clone -b noetic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
cd ~/catkin_ws && catkin_make
### Launch Simulation World:
export TURTLEBOT3_MODEL=waffle
roslaunch turtlebot3_gazebo turtlebot3_world.launch
<img width="911" alt="Gazebo" src="https://github.com/Razanalshaeri/SLAM/assets/135154136/a7d782a1-c474-401c-aa51-78f71b44bed1">
## 3-SLAM-Simulation:
export TURTLEBOT3_MODEL=burger
roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
<img width="926" alt="Turtelbot3" src="https://github.com/Razanalshaeri/SLAM/assets/135154136/1d255837-b8d4-4c05-a6b1-c60766ca5918">
## 4-Run Teleoperation Node:
export TURTLEBOT3_MODEL=burger
roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
<img width="328" alt="Terminal" src="https://github.com/Razanalshaeri/SLAM/assets/135154136/8f60338f-0b99-45fd-9f39-6aede9c10daf">
## 5-Save Map:
rosrun map_server map_saver -f ~/map
<img width="287" alt="Save map" src="https://github.com/Razanalshaeri/SLAM/assets/135154136/5115ee27-15f4-4b8e-8309-51f653251770">





