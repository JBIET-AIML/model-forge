# 🏆 Hackathon Problem Statement

## **EduVision 2026: Classroom Crowd Detection & Student Counting**

---

## 📌 Background

Accurately detecting and counting people in real-world classroom environments is a key problem in:

* Smart campus automation
* Attendance monitoring
* Classroom utilization analytics
* Safety and crowd management

Unlike ideal datasets with single-person images, classroom scenes feature:

* Varying lighting conditions
* Occlusions (students overlapping)
* Different viewing angles
* Diverse class sizes
* Furniture shadows and background noise

This competition simulates a **real-world computer vision deployment**, where models must not only identify where people are, but also provide accurate crowd counts under challenging conditions.

---

# 🎯 Core Objective

Participants must build a fully automated system that:

### 📍 Classroom Crowd Detection

Detect the location (bounding boxes) of all human subjects in classroom images.

### 📍 Student Count Estimation

Accurately estimate the number of students present in each image.

---

# 📊 Dataset Description

The dataset is provided via Kaggle:

The dataset includes:

* Classroom images from different angles
* Both small and large class sizes
* Varying lighting and background conditions
* Manual annotations for people (bounding boxes and class labels)

Typical classroom scenes show anywhere from a handful to dozens of students, and may include:

* Chairs & desks
* Partial occlusions
* Non-student persons (e.g., instructors)

---

# 🧠 Challenge Tasks

## 1️⃣ Person Detection

Teams must develop models that:

* Detect all persons in each image
* Output bounding boxes
* Distinguish between students and non-students (optional bonus)

Model outputs must follow standard object detection formats (e.g., COCO-style).

---

## 2️⃣ Student Counting

From detection outputs, compute a **count** of students present in the frame.

This can be derived from:

* Detection model class predictions
* Post-processing filters (size thresholds, context clustering)
* Custom regression/counting algorithms

Participants may use:

* Deep learning object detectors (e.g., YOLOv8, Faster R-CNN)
* Crowd counting regressors (CSRNet, MCNN)
* Hybrid approaches

---

# 📏 Evaluation Metrics

## 🧠 Detection Score (50%)

Evaluated using:

* **Mean Average Precision (mAP)**

> Based on IoU thresholds (0.5:0.95)

---

## 🔢 Counting Score (50%)

Evaluated using:

* **Mean Absolute Error (MAE)**

> MAE = average(abs(predicted_count - true_count))

Lower is better.

---

# 🗂 Rules & Constraints

* No external datasets unless explicitly allowed
* All models must run within the provided test time and memory limits
* Pretrained weights are allowed if disclosed
* Use of public pre-trained backbones (ImageNet, COCO) is permitted
* Test set labels will be withheld for fair evaluation
* Participants must provide reproducible code

---

# 📜 Deliverables

Participants must submit:

1. Model weights and architecture details
2. Inference code + instructions
3. Predictions on the test dataset:

   * Detection bounding boxes
   * Student count per image
4. Technical report describing:

   * Model design
   * Data augmentation
   * Post-processing logic
   * Evaluation analysis

---
