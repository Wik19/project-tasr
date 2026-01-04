# project-tasr# UR5 Robot Control Interface (ROS2)

This project provides a ROS2-based interface to control a **UR5 robot** manipulator. The system is fully containerized using **Docker** for a plug-and-play experience and uses a custom node to manage robot movement through a graphical interface.

## Features
* **Robot Platform**: Universal Robots UR5.
* **ROS2 Integration**: Uses custom nodes to publish to the `/scaled_joint_trajectory_controller/joint_trajectory` topic.
* **Automated Launch**: Includes a ROS2 launch file that initializes all nodes and drivers simultaneously.
* **Dockerized**: High portability via a Docker setup.

## Prerequisites
* Linux environment with Docker installed.
* The script `run_project.sh` must have execution permissions (`chmod +x run_project.sh`).

## Quick Start Instructions

1.  **Launch the System**:
    Run the following command in your Linux terminal to start the Docker containers and ROS2 environment:
    ```bash
    ./run_project.sh
    ```

2.  **Access the Interface**:
    Once the containers are active, open your web browser and navigate to:
    [http://192.168.56.101:6080/vnc.html?host=192.168.56.101&port=6080](http://192.168.56.101:6080/vnc.html?host=192.168.56.101&port=6080)

3.  **Operation**:
    * If the robot driver has not started automatically within the VNC desktop, initiate it.
    * Run the control program.
    * **Control Logic**: Click on a point in the interface window. If the clicked point is **above** the center of the screen, the UR5 base rotates in one direction; if it is **below** the center, it rotates in the opposite direction.

## Project Structure
* **Launch Files**: Automate the startup of robot drivers and custom nodes.
* **Custom Node**: Processes user clicks to generate joint trajectory commands.
* **Docker Configuration**: Defines the environment for seamless deployment.

---
*Developed by Marco Wiktor Santoro and Olaf Bukowski*