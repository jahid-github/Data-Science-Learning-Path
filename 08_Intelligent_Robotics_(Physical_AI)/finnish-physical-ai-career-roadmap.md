# Finnish Physical AI Career Roadmap

This guide turns Phase 8 into a career-focused plan for a HAMK ICT robotics student who wants to build real systems in Finland, not study robotics only in theory.

## Purpose

- Build toward a `Physical AI / Robotics ML Engineer` role
- Focus on robots and intelligent machines that sense, decide, and act in the physical world
- Use HAMK labs, thesis work, and internship opportunities to build credible industrial projects
- Target Finnish sectors where physical AI is practical: forestry, mining, cranes, factory automation, and warehouse logistics

## What This Path Should Lead To

The strongest story for this phase is not "I know robotics tools." It is:

`I can build a full perception -> planning -> action loop for a robot, explain the failure modes, and ship it as a working demo.`

That story fits:

- industrial autonomy
- intelligent machines
- vision-guided manipulation
- edge AI for physical systems
- language-conditioned robot workflows later in the path

## Physical AI Automation Stack

| Layer | What it does | Typical tools | Finland-oriented examples |
|------|--------------|---------------|---------------------------|
| Sense | Capture the physical world as measurements | RGB/depth cameras, LiDAR, IMU, force sensors, ROS2 drivers | forest machine sensors, crane cameras, warehouse robot telemetry |
| Perceive | Turn sensor data into a usable world model | OpenCV, YOLO, segmentation, RTAB-Map, Open3D | obstacle detection, defect detection, localization, terrain understanding |
| Decide | Select the next safe and useful action | Nav2, MoveIt2, BehaviorTree.CPP, MPC, RL | route planning, pick sequence, stop zones, manipulation planning |
| Act | Convert decisions into motion and industrial commands | ros2_control, robot APIs, TwinCAT, CAN, EtherCAT | arm motion, vehicle control, conveyor or cell automation |
| Learn | Improve the system using logs and experiments | ROS bags, DVC, MLflow, LeRobot, Isaac Lab | sim-to-real tuning, policy improvement, performance tracking |

### Example Reference Systems

- Autonomous forest machine: detect trees, estimate terrain, plan safe motion, control the boom or vehicle, log data for retraining
- Warehouse AMR: map the building, localize, detect pallets or people, navigate, stop safely, report telemetry to a dashboard
- Vision-guided industrial cell: inspect objects, estimate pose, plan a pick or reject action, trigger the robot or PLC, track failures

## Finland-Oriented Portfolio Project Ideas

Build fewer projects, but make them deeper. Each project should have a diagram, a short demo video, reproducible setup steps, and a short section on failure cases.

| Project | What you build | Core stack | Why it matters |
|--------|----------------|------------|----------------|
| Autonomous forest inspection robot | A simulated mobile robot that detects "trees," builds a map, and navigates between targets | ROS2, Gazebo or Isaac Sim, Nav2, YOLO, RTAB-Map | Strong fit for forestry, field robotics, and autonomous machinery |
| Vision-based defect detection cell | A camera pipeline that inspects parts and runs edge inference with alerts or telemetry | PyTorch, YOLO, OpenCV, TensorRT or ONNX Runtime, Grafana | Fits manufacturing, machine vision, and industrial QA |
| Smart crane or yard safety monitor | Multi-camera or single-camera safety zone monitoring with human or obstacle detection | OpenCV, object tracking, ROS2 or FastAPI, dashboarding | Relevant to ports, cranes, and heavy equipment safety |
| Warehouse AMR with telemetry | An autonomous mobile robot in sim with mapping, navigation, and live robot health metrics | TurtleBot3, ROS2, Nav2, InfluxDB, Grafana, Docker | Shows full-stack robotics engineering, not only ML |
| Vision-guided pick-and-place | Detect an object, transform to robot frame, and execute a grasp in simulation | ROS2, TF2, MoveIt2, depth sensing, OpenCV | Strong demonstration of perception-to-action integration |
| Language-conditioned manipulation | A sim demo where a command such as "pick the red block" becomes a robot action | LeRobot or OpenVLA concepts, ROS2, MoveIt2 | Good advanced capstone for frontier Physical AI |

## Recommended Learning Path

### Stage 1: Core Robotics Foundations (0-3 months)

Goal: become comfortable building and debugging ROS2 systems.

- C++ for robotics: memory basics, classes, CMake, colcon
- ROS2 fundamentals: nodes, topics, services, actions, launch files, parameters, TF2
- URDF, RViz, Gazebo, robot descriptions
- Linux, Docker, Git, debugging tools
- Nav2 basics with a mobile robot in simulation

Deliverable:

- a clean ROS2 workspace with one Python node and one C++ node
- a TurtleBot3 or similar robot navigating in simulation

### Stage 2: Perception + Control Integration (4-8 months)

Goal: connect AI models to robot behavior.

- OpenCV and PyTorch for detection or segmentation
- camera calibration, depth, and pose estimation
- SLAM and localization
- MoveIt2 or manipulation basics
- ros2_control and low-level control concepts
- edge inference basics on Jetson or desktop GPU

Deliverable:

- one navigation project and one manipulation project
- one project with clear latency or FPS measurements

### Stage 3: Modern Physical AI (9-18 months)

Goal: move from classical robotics into learned policies and sim-to-real.

- imitation learning and behavior cloning
- reinforcement learning in simulation
- Isaac Lab, LeRobot, or similar embodied AI tooling
- data collection, evaluation, and experiment tracking
- deployment optimization with TensorRT, ONNX Runtime, or OpenVINO
- thesis or internship project tied to a real use case

Deliverable:

- one advanced project showing sim-to-real, policy learning, or language-conditioned control
- one thesis or internship artifact that solves a real industrial problem

## 8-Week Kickoff Plan

| Week | Focus | Deliverable |
|------|-------|-------------|
| 1 | C++ refresh, CMake, ROS2 dev environment in Docker | ROS2 workspace with basic publisher/subscriber in Python and C++ |
| 2 | ROS2 core: nodes, topics, services, parameters, launch | Small two-node system with launch files and config |
| 3 | TF2, URDF, RViz, robot description | Simulated robot visualized correctly with transforms |
| 4 | Gazebo + Nav2 | Mobile robot that navigates to goals autonomously |
| 5 | OpenCV + YOLO refresher | Real-time perception node publishing detections |
| 6 | Spatial intelligence | Convert image detections into robot-frame coordinates |
| 7 | Planning or manipulation integration | Robot uses perception output to choose and execute an action |
| 8 | Demo packaging | GitHub README, architecture diagram, metrics, and short video |

## How To Use HAMK Well

- Use work placement for robotics, automation, or industrial AI, not generic IT support
- Turn the thesis into a portfolio asset with a real industrial question
- Use campus lab access to capture real demos, even if the final project is mostly in simulation
- Ask for projects that let you touch ROS2, vision, PLC integration, or robot control

## Project Quality Checklist

Every serious Physical AI project in this folder should show:

- the system architecture
- the sensor inputs and outputs
- the control or planning loop
- evaluation metrics such as FPS, latency, success rate, or navigation accuracy
- failure cases and what you changed after testing
- how to run the project from a fresh clone

## Narrative To Build Across The Repo

Phase 7 gives you perception.

Phase 8 should prove you can connect perception to motion, planning, control, and safety.

Phase 9 can then extend the robot with language interfaces, dashboards, agents, and automation around the physical system.
