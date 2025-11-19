# ROS2 Robot Controller - Introduction Project

This is an introductory ROS2 project developed as part of my Operating Systems coursework. The project demonstrates fundamental ROS2 concepts including nodes, publishers, subscribers, and turtle simulation control.

## Project Overview

This package contains several ROS2 nodes that interact with the TurtleSim simulator to demonstrate:
- Basic node creation
- Publisher/Subscriber pattern
- Turtle pose monitoring
- Velocity control
- Circular motion patterns

## Prerequisites

- ROS2 (Humble/Jazzy/Foxy/Galactic)
- Python 3.8+
- TurtleSim package

## Installation

1. Clone this repository into your ROS2 workspace:
```bash
cd ~/ros2_ws/src
git clone <your-repo-url>
```

2. Build the package:
```bash
cd ~/ros2_ws
colcon build --packages-select my_robot_controller
source install/setup.bash
```

## Package Contents

### Nodes

- **my_first_node.py**: Basic ROS2 node demonstrating node creation and logging
- **draw_circle.py**: Makes the turtle draw circles by publishing velocity commands
- **pose_subscriber.py**: Subscribes to turtle pose topic and logs position information
- **turtle_controller.py**: Advanced turtle control with custom logic

## Usage

1. Start TurtleSim:
```bash
ros2 run turtlesim turtlesim_node
```

2. Run individual nodes:

**Draw Circle:**
```bash
ros2 run my_robot_controller draw_circle
```

**Pose Subscriber:**
```bash
ros2 run my_robot_controller pose_subscriber
```

**Turtle Controller:**
```bash
ros2 run my_robot_controller turtle_controller
```

## Topics Used

- `/turtle1/cmd_vel` - Publishes velocity commands (geometry_msgs/Twist)
- `/turtle1/pose` - Subscribes to turtle position (turtlesim/Pose)

## Learning Objectives

This project demonstrates:
- ✅ ROS2 node initialization and lifecycle
- ✅ Publisher-Subscriber communication pattern
- ✅ Working with standard ROS2 message types
- ✅ Timer callbacks for periodic operations
- ✅ Python package structure in ROS2

## Course Work Information

**Course**: Operating Systems  
**Year**: 3, Semester 5  
**University**: Technical University of Sofia  
**Author**: Asen Popov

## License

This project is created for educational purposes as part of university coursework.

## Acknowledgments

- ROS2 Documentation
- TurtleSim Tutorial
- Operating Systems Course Materials
