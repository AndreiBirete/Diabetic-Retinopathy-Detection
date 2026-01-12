# 🩺 Diabetic Retinopathy Detection using Deep Learning
This repository presents a deep learning–based approach for automatic detection and grading of Diabetic Retinopathy (DR) from retinal fundus images. The project explores transfer learning, model comparison, and cross-dataset generalization using state-of-the-art convolutional neural networks.

📌 Project Overview
Diabetic Retinopathy is a leading cause of vision impairment worldwide. Early detection and accurate grading are essential for preventing severe outcomes.
 This project addresses the problem as a multi-class image classification task (5 severity levels) using pre-trained CNN architectures.
The study includes:
Training and evaluation on APTOS 2019 Blindness Detection


Model comparison between DenseNet121 and ResNet50


Cross-dataset fine-tuning on Messidor-2


Evaluation using clinically relevant metrics such as Quadratic Weighted Kappa (QWK)



📂 Datasets Used
1️⃣ APTOS 2019 – Blindness Detection
5 classes: 0 (No DR) → 4 (Proliferative DR)


High variability in illumination and image quality


Used as the primary training dataset


2️⃣ Messidor-2
Retinal fundus images with DR annotations


Used to evaluate cross-dataset generalization


Fine-tuning performed starting from the APTOS-trained model



🧠 Models Implemented
🔹 DenseNet121
Pre-trained on ImageNet


Used as a baseline architecture


Stable convergence and good generalization


🔹 ResNet50
Pre-trained on ImageNet


Residual connections improve optimization


Achieved the best overall performance



⚙️ Training Strategy
Image resolution: 224 × 224


Data augmentation: horizontal flip, rotation, zoom


Class imbalance handled using class weighting


Optimizer: Adam


Loss function: Sparse Categorical Cross-Entropy


Early stopping to prevent overfitting


Transfer Learning Scenarios
Training from ImageNet weights on APTOS


Fine-tuning APTOS-trained ResNet50 on Messidor-2



📊 Evaluation Metrics
To ensure clinical relevance, multiple metrics were used:
Accuracy


Balanced Accuracy


Quadratic Weighted Kappa (QWK) – primary metric


Confusion Matrix


