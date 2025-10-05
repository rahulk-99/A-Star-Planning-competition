# A* Path Planning for TurtleBot4 in a Competitive Environment

This project implements A* path planning algorithm for TurtleBot4 navigation in both simulation (Gazebo) and hardware environments. The implementation includes path smoothing and differential drive constraints for realistic robot motion.

## Project Overview

The project consists of two main components:
1. A* Path Planning with Differential Drive Constraints
2. Path Following Implementation for TurtleBot4

### Demo: TurtleBot4 Competition Run
![TurtleBot4 A* Path Planning](docs/A_star.gif)

*Real-world implementation of A* path planning and following on TurtleBot4 in the competition environment*

### Features

- A* path planning with differential drive kinematics
- Path smoothing for optimal trajectories
- Obstacle avoidance with customizable clearance
- Support for both simulation and hardware testing
- Real-time visualization of path planning
- Configurable wheel RPMs for motion control

## Environment Setup

The environment consists of vertical obstacles in a competitive arena. The dimensions are:
- Canvas: 540mm × 300mm
- Robot: TurtleBot4 (radius: 33.5mm/2)
- Wheel specifications:
  - Radius: 3.6mm
  - Distance between wheels: 235mm

## Dependencies

- ROS2 Humble
- Python 3.x
- OpenCV
- NumPy
- Matplotlib
- Gazebo

## Installation

1. Create a ROS2 workspace:
```sh
mkdir -p project_ws/src
cd ~/project_ws/src
```

2. Clone the repository:
```sh
git clone https://github.com/rahulk-99/A-Star-Planning-competition.git
```

3. Install dependencies:
```sh
pip install numpy opencv-python matplotlib
```

4. Build the workspace:
```sh
cd ~/project_ws
colcon build
source install/setup.bash
```

## Usage

### 1. Path Planning

Run the Jupyter notebook `Planning_a_star.ipynb` to (follow README.txt):
- Generate optimal paths using A* algorithm
- Visualize the planning process
- Save waypoints to `final_path.txt`

Input parameters:
- Start position (x, y, θ)
- Goal position (x, y)
- Wheel RPMs (RPM1, RPM2)
- Clearance from obstacles

### 2. Simulation Testing

Launch the Gazebo simulation:
```sh
ros2 launch turtlebot3_project3 competition_world.launch.py
```

Run the path follower node:
```sh
ros2 run turtlebot_path_follower turtlebot3_path_follower.py
```

### 3. Hardware Implementation

For hardware testing:
1. Connect to TurtleBot4
2. Upload the generated `final_path.txt`
3. Run the hardware path follower node



## Algorithm Details

### A* Path Planning
- Uses differential drive constraints
- Generates smooth trajectories
- Includes obstacle clearance
- Optimizes for shortest path


## Results

The implementation successfully:
1. Generates optimal paths avoiding obstacles
2. Smooths trajectories for better robot motion
3. Follows generated paths in both simulation and hardware
4. Maintains safe clearance from obstacles

