# SLAM
Use Turtlebot3 with SLAM approach to create and save a map.
## 1-Install TurtleBot3 Packages
sudo apt-get install ros-melodic-dynamixel-sdk
sudo apt-get install ros-melodic-turtlebot3-msgs
sudo apt-get install ros-melodic-turtlebot3
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




