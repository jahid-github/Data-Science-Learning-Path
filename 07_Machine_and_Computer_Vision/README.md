# Phase 7 — Machine and Computer Vision

Computer vision gives machines the ability to interpret and understand the visual world. It is one of the most impactful application areas of modern AI and the **primary perception layer for Physical AI and Robotics** (Phase 8).

**Application domains:**
- Image classification, object recognition
- Medical imaging and diagnostics
- Manufacturing inspection and quality control
- Surveillance, tracking, and smart cameras
- Autonomous vehicles and mobile robots
- Retail analytics and smart devices
- Edge AI systems

---

## Tools & Libraries

| Tool | Description |
|------|-------------|
| **OpenCV** | Industry-standard CV library — preprocessing, segmentation, HSV masking, contours, morphology, pipelines |
| **YOLO (Ultralytics)** | Real-time object detection system — identifies and locates multiple objects in a single neural network pass, optimized for speed |
| **MediaPipe** | Google's cross-platform ML framework for multimodal pipelines (video, audio, sensors) — real-time perception on mobile, web, and edge devices |
| **Detectron2** | Meta AI (FAIR) high-performance library — object detection, instance segmentation, panoptic segmentation (PyTorch-based) |
| **PyTorch + torchvision** | Deep learning backbone for custom vision models and transfer learning |
| **Albumentations** | Fast image augmentation library for training robust vision models |
| **Open3D** | 3D point cloud processing — used for depth cameras and LiDAR in robotics |
| **SAM (Segment Anything)** | Foundation model for zero-shot image segmentation (Meta AI) |
| **CLIP** | Vision-language model — connect images and text (OpenAI) |

---

## Learning Steps

### Classical Computer Vision (OpenCV)
- Image preprocessing: resize, crop, normalize, color space conversion
- Edge detection: Canny, Sobel, Laplacian
- Thresholding and contours
- Morphological operations: erosion, dilation, opening, closing
- Motion detection and optical flow
- Feature extraction: SIFT, ORB, HOG

### Deep Learning for Vision (PyTorch)
- CNN architectures: LeNet → ResNet → EfficientNet → ViT
- Image classification with transfer learning
- Object detection: YOLO family, Faster R-CNN, SSD
- Segmentation: Semantic (FCN, DeepLab), Instance (Mask R-CNN), Panoptic
- Video analysis: tracking, temporal models

### Edge AI & Robotics Vision
- Real-time inference pipelines — optimize for FPS on edge hardware
- Depth estimation: monocular and stereo
- Multi-camera systems and calibration
- 3D point cloud processing (Open3D, PCL)
- Foundation vision models: SAM, CLIP, DINO

### Vision Evaluation
- Classification: Accuracy, Top-5 Accuracy
- Detection: mAP (mean Average Precision), IoU
- Segmentation: Dice coefficient, pixel accuracy
- Profiling: inference time (ms), FPS, model size (MB), FLOPS

---

## Real-World Task Categories

### Computer Vision Engineering
- Image preprocessing and annotation quality
- Model selection by task (classification vs detection vs segmentation)
- Evaluation metrics appropriate to the task
- Inference speed and memory constraints
- Deployment environment awareness

### Robotics, Autonomous Systems, and Edge AI
- Perception pipelines with real-time inference
- Camera and sensor integration (RGB, depth, stereo, thermal)
- Efficient vision models for latency-constrained environments
- Safety-critical thinking for autonomous systems

### Applied AI Products
- Retail analytics (product recognition, shelf monitoring)
- Manufacturing QA (defect detection, surface inspection)
- Healthcare imaging (anomaly detection, segmentation)
- Document vision (OCR, layout parsing)
- Smart devices (gesture recognition, face detection)
- Multimodal systems (vision + language)

---

## Future-Ready Skills

Strong vision practitioners develop:
- Intuition about data quality and labeling quality
- Comfort with transfer learning over training from scratch
- Understanding of multimodal AI (image + language)
- Awareness of model size, latency, and hardware constraints
- Ability to compare fast practical models vs high-accuracy heavier models
- Evaluation habits on real failure cases, not only benchmark scores

---

## How to Study This Section Well

- Inspect raw images — understand how preprocessing changes the input
- Compare classical OpenCV methods with CNN-based approaches
- Train at least one image classifier and analyze failure cases
- Study object detection and segmentation separately — their goals and metrics are different
- Use transfer learning early — it reflects practical industry workflows
- Pay attention to inference speed, especially for edge and robotics use cases

---

## Resources

* [Stanford CS231n: CNNs for Visual Recognition](https://cs231n.stanford.edu/)
* [OpenCV Documentation and Tutorials](https://docs.opencv.org/4.x/)
* [PyTorch Computer Vision Tutorial](https://pytorch.org/tutorials/beginner/blitz/cifar10_tutorial.html)
* [Ultralytics YOLO Documentation](https://docs.ultralytics.com/)
* [fast.ai Practical Deep Learning for Coders](https://course.fast.ai/)
* [Kaggle Learn: Computer Vision](https://www.kaggle.com/learn/computer-vision)
* [DataCamp Computer Vision Courses](https://www.datacamp.com/courses-all?technology=Computer+Vision)
