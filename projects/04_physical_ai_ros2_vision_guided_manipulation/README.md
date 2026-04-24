# ROS2 Vision-Guided Manipulation

## Status

`Planned`

## Why This Project Exists

This is the differentiating project for the repository.

It should prove that perception can be connected to spatial reasoning and robot action in simulation, with a path toward real hardware later.

Target system story:

`camera -> detection -> coordinate transform -> planning -> action`

## Target Stack

- ROS2
- Python and C++
- TF2
- OpenCV
- depth or pose estimation
- MoveIt2 or a simple action/planning layer
- Gazebo or equivalent simulator

## Minimum Deliverables

- ROS2 workspace
- at least one perception node
- transform from image or camera frame into robot/world frame
- action triggered by perception
- simulation demo
- architecture diagram

## Strong Portfolio Evidence

- latency or FPS notes
- TF tree explanation
- motion planning tradeoffs
- failure cases such as occlusion or calibration drift
- demo video

## Recommended Repository Shape

```text
projects/04_physical_ai_ros2_vision_guided_manipulation/
  README.md
  ros2_ws/
  docs/
  videos/
```

## Hiring Signal

This project supports:

- Robotics Software Engineer
- Robotics ML Engineer
- Physical AI / intelligent robotics roles
