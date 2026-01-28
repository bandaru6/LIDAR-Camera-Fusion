# LiDAR–Camera Fusion for 3D Object Detection (KITTI)

## Overview

This project implements a **LiDAR–camera fusion pipeline for 3D object detection and perception** using the **KITTI autonomous driving dataset**. The goal is to explore how multi-modal sensor data (LiDAR point clouds and RGB images) can be processed, aligned, and fused to support reliable perception systems in autonomous driving.

The project emphasizes **data processing, geometry, and systems-level ML integration**, reflecting real-world autonomy pipelines where correctness, numerical stability, and performance are just as important as raw model accuracy.

This work was developed as a standalone **Colab / Jupyter notebook**, focusing on clarity, experimentation, and end-to-end reasoning rather than production infrastructure.

---

## Key Features

### Sensor Fusion
- Projects LiDAR point clouds into camera image space using KITTI calibration matrices
- Aligns 3D LiDAR data with 2D image detections
- Handles coordinate frame transformations and depth filtering

### Data Processing & Mathematical Foundations
- Extensive geometric transformations (homogeneous coordinates, projection matrices)
- Point cloud filtering and spatial reasoning
- Bounding box construction and depth association
- Careful handling of numerical precision and large sensor inputs

### Object Detection Approaches
- Classical computer vision and ML techniques
- Deep learning-based object detection models (e.g., YOLO-style detectors)
- Exploration of newer multimodal and vision-language model ideas for perception reasoning

### Evaluation & Analysis
- Quantitative evaluation of detection performance
- Visualization of fused LiDAR–camera outputs
- Comparison of tradeoffs between classical and modern ML approaches

---

## Technologies Used

- **Language:** Python  
- **Libraries:** NumPy, OpenCV, Matplotlib, PyTorch  
- **Dataset:** KITTI Vision Benchmark Suite  
- **Core Concepts:**  
  - 3D geometry and projections  
  - Sensor calibration and coordinate transformations  
  - Classical computer vision and deep learning  
  - Multi-modal data fusion  

---

## Pipeline Overview

1. **Load KITTI Data**
   - Camera images
   - LiDAR point clouds
   - Sensor calibration files

2. **Preprocess Sensors**
   - Clean and filter point clouds
   - Prepare image inputs for detection

3. **Project LiDAR into Image Space**
   - Apply calibration and projection matrices
   - Map 3D points to 2D pixel coordinates

4. **Object Detection**
   - Run object detection on camera images
   - Associate detections with LiDAR depth information

5. **Fusion & Evaluation**
   - Construct fused detections and bounding boxes
   - Evaluate accuracy and spatial consistency
   - Visualize perception outputs

---

## Why This Project Matters

Autonomous systems rely on **robust perception pipelines** that combine multiple sensors to handle noise, occlusion, and uncertainty. This project demonstrates:

- Strong understanding of **sensor fusion mathematics**
- Hands-on experience with **real autonomous driving datasets**
- Ability to integrate **ML models into end-to-end perception systems**
- Engineering intuition around **performance, correctness, and evaluation**

These skills translate directly to autonomy, robotics, and telemetry-style systems where perception outputs must be reliable, debuggable, and scalable.

---

## Future Work

- Add real-time inference support
- Compare early vs. late fusion strategies
- Integrate temporal consistency across frames
- Benchmark performance under simulated sensor noise
- Extend toward a full perception stack

---

## Author

**Aashrith Bandaru**  
Computer Science + Economics, University of Illinois Urbana-Champaign  
GitHub: https://github.com/bandaru6
