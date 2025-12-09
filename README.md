# Autonomous Delivery Drone

A collective codebase for the simulation of an autonomous delivery drone as a part of my submissions for the WingSpann Hackathon.
## Requisites
  1. ROS Melodic
  2. Gazebo
  3. OpenCV
  4. pyzbar library
  
  
  
## Description of Tasks

  - Task 1: This task includes 2 basic cascading PID scripts to control the attitude (roll, pitch, yaw) and the position (latitude, longitude) of the drone.
  

  - Task 2: In this task, the drone detects the coordinates of the delivery address through the QR Code on the parcel. The drone then goes to that address and drops the package while avoiding obstacles in the way.

  - Task 3: In this task, the drone goes to multiple specified locations and executes a search pattern to look for a specific landing marker. After finding the landing marker, the drone hovers over it and then goes to the next location.
    
    
## How to use

  1. Clone repository in the root directory
  2. On the terminal execute:
     ``` cd ~/delivery_drone
         catkin build
         sudo echo 'source ~/delivery_drone/devel/setup.bash' >> ~/.bashrc
     ```
  3. Execute launch file for whichever task for example:
     ```roslaunch vitarana_drone task_1.launch```
     
     
     
## Issues
  
  1. The drone crashes at random moments on some runs and works perfectly fine on most other runs. This is due to inherent issues with the drone model and Gazebo.
  2. Drone could be tuned to move faster by tuning the PID of the attitude and position controller scripts better.
