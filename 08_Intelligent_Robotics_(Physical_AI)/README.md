# Intelligent Robotics (Physical AI)
## 1. Foundations (Non-negotiable)

### Math

- Linear Algebra (vectors, matrices, transformations)
- Probability & Statistics (for ML)
- Basic Calculus (optimization)

### Programming

- Python (main)
- C++ (important for robotics & ROS)

### Core topics

- Data structures
- Algorithms
- Linux basics (you already use VM → good)

## 2. Core AI & Machine Learning

- Supervised learning (Regression, Classification)
- Model evaluation (Precision, Recall, F1, RMSE)
- Feature engineering
- Scikit-learn

👉 Then move to:

- Deep Learning (PyTorch preferred)
- CNNs (for vision)
- Transfer learning

## 3. Computer Vision

This is the eyes of physical AI.

- OpenCV
- Image processing (thresholding, contours, morphology)
- Object detection (YOLO, Faster R-CNN)
- Image classification
- Segmentation

👉 Advanced:

- Depth estimation
- Multi-camera systems
- Real-time pipelines

4. Spatial Intelligence

- Coordinate systems (pixel → world)
- Camera calibration
- Homography
- Pose estimation

Example:

Detect object → convert (u, v) → (X, Y) → robot moves

## 5. Robotics & Control Systems

Now connect AI → real world.

- Robot kinematics (forward & inverse)
- Motion planning basics
- PID control

**Tools:**

- ROS2 (VERY IMPORTANT)
- Gazebo / simulation
- Robot APIs (like Dobot MG400)

## 6. Sensors & Hardware

Physical AI ≠ only software.

**Learn:**

- Cameras (RGB, depth)
- LiDAR basics
- IMU sensors
- Microcontrollers (Arduino / Raspberry Pi)

## 7. Real-Time Systems

- Multithreading
- Latency optimization
- Edge AI (run models locally)
- Streaming pipelines

## 8. AI + Cloud Integration

- Google Cloud (BigQuery, Vertex AI)
- APIs (Gemini)

**Now extend:**

- Deploy models on edge + cloud hybrid
- Real-time inference APIs (FastAPI)
- Data logging + monitoring

## 9. System Design

Think like an engineer.

**Design pipelines like:**

**Camera → AI Model → Decision → Robot Action → Feedback Loop**

Should be able to explain:

- Data flow
- Failure cases
- Latency
- Scalability

## Resources

* [NVIDIA Physical AI Learning](https://docs.nvidia.com/learning/physical-ai/index.html)
