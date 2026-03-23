# Alzheimer's Disease Detection using Deep Learning 🧠

[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-FF6F00?logo=tensorflow&logoColor=white)](https://tensorflow.org)
[![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)](https://python.org)
[![GPU](https://img.shields.io/badge/Optimized_for-RTX_5060-76B900?logo=nvidia&logoColor=white)](https://nvidia.com)

## 📋 Project Overview
This project implements an automated, data-driven system for the classification of brain MRI scans to support early-stage Alzheimer's Disease (AD) detection. By utilizing a custom Convolutional Neural Network (CNN) and Transfer Learning (Inception v3), the model identifies structural changes and biomarkers in brain images to classify scans into three diagnostic categories: **Mild Impairment**, **Moderate Impairment**, and **Normal**.

## 🔬 Methodology
The system follows a methodical multi-phase approach as detailed in the research presented at the **MLIP-2025** conference:

* **Dataset Management**: Utilizes a dataset of 8,450 MRI images.
* **Stratified Splitting**: Data is divided using a stratified technique into Training (70%), Validation (20%), and Testing (10%) subsets to maintain class distribution.
* **Preprocessing**: Images are normalized, standardized, and resized to a standard 128x128 pixel resolution to ensure consistency.
* **Data Augmentation**: Techniques such as rotation, zooming, and flipping are applied to increase diversity and mitigate overfitting.
* **Architecture**: A Sequential CNN model utilizing Inception v3 for hierarchical feature extraction, followed by MaxPooling, Dropout, and a SoftMax activation layer for final classification.

## 🛠️ Technical Stack & Environment
This repository is optimized for **WSL2 (Windows Subsystem for Linux)** and high-performance NVIDIA hardware.

### Hardware Specifications
* **GPU:** NVIDIA GeForce RTX 5060 (Blackwell Architecture)
* **Memory Management:** TensorFlow Memory Growth enabled to prevent VRAM fragmentation.

### Software Requirements
| Tool | Version |
| :--- | :--- |
| **OS** | Ubuntu 22.04 LTS (WSL2) |
| **Python** | 3.13 |
| **TensorFlow** | 2.16 (Keras 3) |
| **CUDA / cuDNN** | 12.5 / 9.x |

---

### ☁️ Cloud Alternative: Google Colab (Recommended)

If you do not have a local **WSL2 + CUDA** environment configured, it is highly recommended to run this project via **Google Colab**.Plese make use of the Collab ipynb file.

* **Zero Setup:** No local drivers or Python installation required.
* **Free GPU Access:** Provides access to NVIDIA T4/L4 GPUs.
* **Direct Integration:** Seamlessly connects to the Google Drive dataset link.

## 📂 Dataset & Data Handling
The model is trained on the **Alzheimer's Combined Dataset**. 

> **Note on Data Access:** Due to the large file size, the dataset is hosted externally. Please refer to the **Google Drive link** provided below in description to download the required image folders.

## 📊 Performance Results
The model demonstrates high diagnostic reliability on the test set:

| Metric | Score |
| :--- | :--- |
| **Overall Accuracy** | **92%** |
| **Moderate Impairment F1-Score** | **1.00** |
| **No Impairment (Normal) F1-Score** | **0.89** |
| **Mild Impairment F1-Score** | **0.87** |

## 📂 Dataset & Resources
To run the training or inference, please download the following resources:
- **Dataset:** .https://drive.google.com/file/d/1YAAUR4U1yWXoWWnIUeRyRBy4Ctfuaef7/view?usp=drive_link
- **Manuel Inference** .https://drive.google.com/file/d/1i5xg-Cwx8PM92D2i9C4VbhurkkbUANmh/view?usp=drive_link

## 👨‍🔬 About the Author
**Sampara Emmanuel Arther George**
* **B.Tech in CSE (AI & Machine Learning)**, Karunya Institute of Technology and Sciences.
* **Research**: This project was presented at the **MLIP-2025** conference in February 2025.
* **Connect**: [GitHub: Arther-Codes](https://github.com/Arther-Codes)
