
# ROS2 Publisher and Subscriber Project

## Introduction

This project demonstrates the use of ROS2 (Robot Operating System) to create publishers and subscribers for various tasks, including controlling a turtlesim, publishing "Hello World" messages, and handling multiple publishers for the same subscriber. This project is intended to showcase basic ROS2 functionalities and provide a foundational understanding of working with ROS2 nodes, topics, and messages.

## Prerequisites

### Software Requirements
- Docker
- ROS2 (Humble)

### Hardware Requirements
- None (all simulations can be run on a standard computer)

## File Structure
```
ROS2_PubSub_Project/
│
├── Dockerfile               # Dockerfile to build the environment
├── ros2_ws/                 # ROS2 workspace
│   ├── src/
│   │   ├── hw1/
│   │   │   └── hw1/
│   │   │       ├── draw_circle.py
│   │   │       ├── publisher_member_function.py
│   │   │       ├── subscriber_member_function.py
│   │   │       ├── publisher_name.py
│   │   │       ├── publisher_count.py
│   │   │       ├── subscriber_all.py
│
└── hw1_report.pdf           # Report with screenshots of running code
```

## Setup and Usage

1. **Build Docker Environment:**
   ```bash
   docker build -t ros2_pubsub_project .
   ```

2. **Run Docker Container:**
   ```bash
   docker run --net=ros -it ros2_pubsub_project bash
   ```

3. **Navigate to Workspace:**
   ```bash
   cd /root/ros2_ws/
   ```

4. **Build ROS2 Workspace:**
   ```bash
   colcon build
   source /opt/ros/humble/setup.bash
   source /root/ros2_ws/install/setup.bash
   ```

5. **Run Turtlesim Node:**
   ```bash
   ros2 run turtlesim turtlesim_node
   ```

### Part A: The Turtle Sim
- Edit and run `draw_circle.py` to control the turtlesim and make it draw a circle.

### Part B: Hello World!
- Edit and run `publisher_member_function.py` and `subscriber_member_function.py` to publish and subscribe to "Hello, [Your Name]" messages.

### Part C: Multiple Publishers to the Same Subscriber
- Edit and run `publisher_name.py`, `publisher_count.py`, and `subscriber_all.py` to handle multiple publishers and ensure the subscriber correctly processes messages from both.

## Contributing
Feel free to fork this repository, submit issues, and send pull requests. Contributions are welcome!

## License
This project is licensed under the MIT License.
