# ProyectNATRIX
# NATRIX - RoboCup RMRC 2026

**NATRIX** is a semi-autonomous rescue robot developed by **RC SERPENS** for the **RoboCup Rapidly Manufactured Robot Challenge 2026**.

The project focuses on rapid manufacturing, modular mechanical design, reliable electronics integration, teleoperation, sensor-assisted navigation, and real-time visualization for rescue-oriented scenarios.

## Team

**Team Name:** RC SERPENS
**Institution:** FIME - Universidad Autónoma de Nuevo León
**Country:** Mexico
**Category:** RoboCup Rescue Rapidly Manufactured Robot Challenge

## Project Overview

NATRIX was designed as a compact tracked robot capable of operating in complex and irregular environments. The robot uses a crawler-based locomotion system with articulated flippers, a robotic arm for manipulation tasks, multiple cameras for teleoperation, LiDAR for environmental perception, and ROS2-based visualization tools.

The system combines mechanical, electronic, and software subsystems into a single platform designed for rescue robotics applications.

## Main Features

* Tracked locomotion system for uneven terrain.
* Articulated flippers for obstacle traversal.
* Six-degree-of-freedom robotic arm.
* Raspberry Pi 4 for high-level processing.
* ESP32-S2 Mini for low-level actuator and sensor control.
* UART communication between Raspberry Pi and ESP32.
* Multi-camera teleoperation system.
* LiDAR-based environmental scanning.
* BNO055 IMU for orientation tracking.
* MLX90640 thermal camera for heat detection.
* Magnetic sensor for hidden magnet detection.
* ROS2 and RViz integration for 3D visualization.
* PySide6-based graphical user interface.
* Computer vision modules for Hazmat and QR detection.
* Custom PCB for organized wiring and power distribution.

## System Architecture

The robot uses a distributed control architecture divided into three main layers:

### Operator Station

The operator station runs the graphical user interface. It receives video streams, displays robot status, shows RViz visualization, and sends control commands to the robot.

### Raspberry Pi 4

The Raspberry Pi acts as the main onboard computer. It manages video streaming, communication with the operator station, ROS2 visualization, LiDAR processing, and high-level command routing.

### ESP32-S2 Mini

The ESP32 handles low-level control tasks such as motor control, servo control, sensor readings, and execution of commands received from the Raspberry Pi.

## Software Components

This repository is organized to include the following software areas:

```text
firmware/
  ESP32 low-level control code.

robot_server/
  Raspberry Pi server for communication, command parsing, and video streaming.

gui/
  Operator interface developed with PySide6.

ros2_ws/
  ROS2 packages, URDF files, launch files, and RViz configurations.

computer_vision/
  Hazmat detection, QR detection, and camera processing modules.

docs/
  Technical documentation, diagrams, and setup notes.

hardware/
  PCB files, schematics, mechanical references, and bill of materials.
```

## Technologies Used

* Python
* C / C++
* ROS2 Humble
* OpenCV
* PySide6
* PySerial
* NumPy
* Ultralytics YOLO
* Torch
* RViz
* UART
* TCP/IP sockets
* I2C
* USB cameras

## Hardware Summary

Main hardware components include:

* Raspberry Pi 4 8GB
* ESP32-S2 Mini
* REV Core Hex motors
* DS3240 high-torque servomotors
* STS3215 serial servomotors
* BTS7960 motor drivers
* STL-19P / LDROBOT LiDAR
* BNO055 IMU
* MLX90640 thermal camera
* HBV CAM OV9732 cameras
* Magnetic sensor
* Custom PCB
* 3S LiPo batteries
* 3D printed PLA, PETG, and TPU components

## Repository Status

This repository is currently under development. The structure is intended to document and organize the complete NATRIX system, including mechanical design, electronics, firmware, software, ROS2 integration, and testing resources.

## Future Work

Planned improvements include:

* Improved autonomous assistance for navigation.
* Better obstacle detection and alignment.
* Real-time battery and current monitoring.
* Optimization of video latency.
* More robust ROS2 integration.
* Improved modularity for maintenance and competition repairs.

## Acknowledgements

Developed by **RC SERPENS**, representing the RC UANL robotics chapter and FIME - UANL for RoboCup RMRC 2026.
