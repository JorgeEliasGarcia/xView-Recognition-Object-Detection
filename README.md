# Object Detection on xView-Recognition dataset with YOLOv11

This project builds an **object detection** system using the **YOLOv11** architecture on the **xView-recognition dataset**, a large-scale benchmark for overhead/aerial imagery understanding.  
The notebook covers the end-to-end workflow required to train a YOLO detector for aerial scenes, from dataset setup to inference and qualitative evaluation.

---

## Objectives
- Fine-tunning a **YOLOv11** model for object detection on **xView-recognition**.
- Learn a complete detection workflow: data configuration, training, and inference.
- Analyze model behavior and common error patterns in overhead imagery.
- Produce and visualize detections on unseen images.

---

## Dataset: xView-Recognition
The **xView-recognition dataset** contains aerial/overhead images with object categories relevant to remote sensing scenarios.

In this project, it is used for **object detection**, which requires:
- Images
- Bounding box annotations
- Class labels for each object instance

### Data Preparation
Typical steps included in the notebook:
- Organizing images and labels in the format expected by YOLO training.
- Defining a dataset configuration file (classes, paths, splits).
- Splitting data into training/validation (and optionally test) sets.
- Applying standard image preprocessing/augmentation used in YOLO pipelines.

---

## Model: YOLOv11
- Single-stage detector designed for fast and accurate predictions.
- Produces bounding boxes and class probabilities in a single forward pass.
- Well suited for detection tasks where efficiency matters.

### Training Setup
- Initialize from pretrained weights (transfer learning) or train from scratch depending on the notebook configuration.
- Optimize detection losses and monitor convergence during training.
- Save the best-performing weights for inference.

---

## Training Pipeline
The notebook follows a standard YOLO training workflow:
1. Dataset configuration and sanity checks
2. Model initialization
3. Training with monitored losses/metrics
4. Checkpointing and model export (if applicable)

---

## Evaluation and Inference
Evaluation includes:
- Visual inspection of predicted bounding boxes on validation/test images
- Qualitative analysis of false positives/negatives
- Observing detection performance under scale variation and clutter (common in aerial imagery)

---

## Technologies Used
- Python
- Ultralytics
- NumPy
- Matplotlib

---


