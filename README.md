# Autonomous Delivery Drone

A unified codebase for the **simulation of an autonomous delivery drone**, developed as part of my submission for the **WingSpann Hackathon**.

## Overview

This project demonstrates a fully autonomous drone capable of:

* Stabilized flight control using PID loops
* Parcel delivery using QR code localization
* Intelligent search and hover operations

The system is built and tested in **ROS2 Jazzy** with **Gazebo simulation**, integrating **computer vision** for visual-based navigation.

## Prerequisites

Ensure the following dependencies are installed before running the simulation:

1. **ROS2 Jazzy**
2. **Gazebo**
3. **OpenCV**
4. **pyzbar** (for QR code detection)

## Task Descriptions

### **Task 1: Attitude and Position Control**

Implements two cascading **PID controllers**:

* **Attitude control:** manages roll, pitch, and yaw stability.
* **Position control:** governs latitude and longitude movements.

This ensures stable and responsive drone flight dynamics.

### **Task 2: Autonomous Parcel Delivery**

* The drone reads a **QR code** from the parcel to extract the delivery coordinates.
* It autonomously flies to the detected location, navigating around obstacles.
* Upon arrival, the drone safely **drops the package** at the destination.


### **Task 3: Multi-Location Search and Hover**

* The drone travels to **multiple predefined coordinates**.
* At each site, it executes a **search pattern** to locate a specific **landing marker**.
* Once the marker is detected, the drone hovers above it before proceeding to the next location.
  

## How to Use

1. **Clone the Repository**

   ```bash
   git clone https://github.com/<your-username>/delivery_drone.git
   cd delivery_drone
   ```

2. **Build the Workspace**

   ```bash
   catkin build
   echo 'source ~/delivery_drone/devel/setup.bash' >> ~/.bashrc
   source ~/.bashrc
   ```

3. **Launch a Task**
   Example for Task 1:

   ```bash
   roslaunch vitarana_drone task_1.launch
   ```


## Known Issues

1. **Random Simulation Crashes**
   Occasionally, the drone crashes during flight due to known instability issues in the **Gazebo model**. Most runs, however, perform correctly.

2. **PID Tuning**
   The drone’s responsiveness and speed can be further improved through refined **PID parameter tuning** for both attitude and position controllers.


## Future Improvements

* Implement real-time obstacle avoidance using LiDAR or depth sensing.
* Integrate computer vision-based landing detection.
* Add delivery confirmation via camera or sensor feedback.

## License

This project is developed for **WingSpann Hackathon** and is open for educational and research use.

Would you like me to make this version **Markdown-styled with emojis and formatting for GitHub (bold, tables, etc.)**, or keep it **plain and minimalist for technical submission format** (as typically required in hackathons)?
