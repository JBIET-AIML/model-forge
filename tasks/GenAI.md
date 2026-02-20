# 🏆 Hackathon Problem Statement

## **GenAI Vision 2026: Image Enhancement & Super-Resolution Challenge**

---

## 📌 Background

In many real-world scenarios — surveillance systems, medical imaging, satellite monitoring, and mobile photography — captured images suffer from:

* Low resolution
* Noise
* Blur
* Unknown degradation processes

Enhancing low-quality images into high-resolution, visually faithful outputs is a core challenge in computer vision and generative AI.

Modern deep learning approaches such as GANs, diffusion models, and transformer-based super-resolution networks have significantly improved performance. However, handling **unknown degradation operators** remains an open research problem.

This challenge focuses on building robust models capable of restoring high-resolution (HR) images from low-resolution (LR) inputs under unknown degradation conditions.

---

# 🎯 Core Objective

Participants must build a model that:

* Takes **Low-Resolution (LR)** images as input
* Outputs **High-Resolution (HR)** enhanced images
* Upscales by a factor of ×2
* Handles unknown degradation operators

---

# 📊 Dataset Description

The dataset consists of paired images:

## High-Resolution Images (HR)

* Training HR images
* Validation HR images

These serve as ground truth targets.

---

## Low-Resolution Images (LR)

* Training LR images (Track 2 – unknown degradation, ×2 downscale)
* Validation LR images (Track 2 – unknown degradation, ×2 downscale)

The LR images were generated using unknown degradation operators, which may include:

* Gaussian blur
* Noise injection
* Compression artifacts
* Mixed distortions

Participants must learn the degradation mapping implicitly.

---

# 🧠 Challenge Tracks

## 🔹 Track 2 – Unknown Degradation (×2)

Upscale LR images by a factor of 2 and reconstruct high-quality HR outputs.

No knowledge of the degradation process will be provided.

---

# 📏 Evaluation Metrics

Models will be evaluated on the validation and test sets using:

### 📌 Objective Metrics

* **PSNR (Peak Signal-to-Noise Ratio)**
* **SSIM (Structural Similarity Index)**

Higher is better.

---

### 📌 Perceptual Quality (Optional Bonus)

* LPIPS (Learned Perceptual Image Patch Similarity)
* Human evaluation score (if applicable)

---

# 🏆 Scoring Breakdown

| Component                             | Weight |
| ------------------------------------- | ------ |
| PSNR                                  | 40%    |
| SSIM                                  | 30%    |
| Generalization to Unknown Degradation | 15%    |
| Model Efficiency (Speed/Memory)       | 10%    |
| Innovation & Documentation            | 5%     |

---

# 🛠 Allowed Approaches

Participants may use:

### 🔹 CNN-based Models

* SRCNN
* EDSR
* RCAN

### 🔹 GAN-based Methods

* SRGAN
* ESRGAN

### 🔹 Transformer-based Models

* SwinIR
* Vision Transformers

### 🔹 Diffusion-based Super-Resolution Models

Pretrained models are allowed but must be disclosed.

---

# ⚙ Rules & Constraints

* Only provided training data may be used (unless external data is explicitly allowed)
* Test ground truth HR images will not be provided
* Inference must be reproducible
* Models must upscale exactly ×2
* No manual editing of outputs

---

# 📦 Submission Requirements

Participants must submit:

1. Enhanced HR images for the validation/test LR inputs
2. Model architecture description
3. Training methodology
4. Hyperparameter configuration
5. Runtime and hardware specifications
6. Short technical report (max 8 pages)

---