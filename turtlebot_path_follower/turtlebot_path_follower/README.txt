Simulation with A* Path Planning

Part01 - 2D Simulation

Project Overview
-----------------
This project demonstrates a 2D grid simulation using the A* search algorithm to plan an optimal path for a differential drive robot. The robot navigates an environment filled with obstacles and clearance zones.

Key features include:
• Map Generation: A canvas environment is created with obstacles (represented by custom functions) and safety zones (clearance) around the obstacles.
• Differential Drive Simulation: The robot’s motion is simulated using wheel RPM values, converting them into linear and angular velocities.
• A* Path Planning: The algorithm finds the best path by combining actual motion cost and a heuristic (Euclidean distance) for each node.
• Visualization & Output:
  - Real-time visualization using OpenCV.
  - Exploration animation video saved as "path_planning.mp4".
  - Final path waypoints exported to "final_path.txt".

Prerequisites:
--------------
Ensure you have Python 3.x installed along with the following packages:
• numpy
• opencv-python
• matplotlib

Note: The program is compatible with local machines and Google Colab (for file download functionality).

Installation:
-------------
1. Download the project files from the zip folder.
This python file (.py) is located inside the Part01 folder.

2. Install the required packages. For example, using pip:
   pip install numpy opencv-python matplotlib


How to Run the Simulation:
--------------------------
1. Open a terminal (or command prompt) and navigate to the project directory.

2. Run the Python script. For example:
   python ENPM661_.py

   Replace "your_script_name.py" with the actual filename (e.g., astar_simulation.py).

Input Instructions:
-------------------
When the program runs, you will be prompted to enter the following:

• Start Point: Enter the starting x, y coordinates and orientation (in degrees) as three space-separated integers.
  Example:
  Enter the start point (x y theta): 30 30 0

• Goal Point: Enter the goal x, y coordinates as two space-separated integers.
  Example:
  Enter the goal point (x y): 500 200

• Wheel RPMs: Enter the RPM values for the left and right wheels as two space-separated integers.
  Example:
  Enter the two wheel RPMs (RPM1 RPM2): 15 10

• Clearance: Enter the desired clearance as an integer.
  Example:
  Enter the clearance: 1

After providing the inputs, the simulation will:
• Validate the input points.
• Generate the map with obstacles.
• Execute the A* search to find the path.
• Visualize the path and display the exploration process.
• Save the exploration animation as "path_planning.mp4".
• Export the final path waypoints in "final_path.txt".
