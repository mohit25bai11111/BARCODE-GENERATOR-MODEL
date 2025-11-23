# Deep Learning Barcode Verification System

![Python](https://img.shields.io/badge/Python-3.8%2B-blue) ![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange) ![Status](https://img.shields.io/badge/Status-Active-green)

A robust Deep Learning-based system designed to classify and verify barcodes. This project uses a Convolutional Neural Network (CNN)—specifically **MobileNetV2** via Transfer Learning—to achieve high accuracy (>90%) in distinguishing between valid/readable barcodes and damaged/invalid ones.

---

## 📋 Table of Contents
- [Project Overview](#-project-overview)
- [Features](#-features)
- [Folder Structure](#-folder-structure)
- [Prerequisites & Installation](#-prerequisites--installation)
- [Dataset Preparation](#-dataset-preparation)
- [Usage](#-usage)
  - [Training the Model](#1-training-the-model)
  - [Evaluation & Confusion Matrix](#2-evaluation--confusion-matrix)
  - [Inference (Testing)](#3-inference-testing)
- [Results](#-results)
- [Troubleshooting](#-troubleshooting)

---

## 🔭 Project Overview
This system automates the quality control or recognition process for barcodes. Instead of traditional computer vision techniques (like simple thresholding), it leverages Deep Learning to handle noise, blur, and variable lighting conditions.

**Key Capabilities:**
- **Binary Classification:** Determines if a barcode is "Valid/Readable" or "Defective/Unreadable".
- **High Accuracy:** Optimized to reach over 90% accuracy on validation sets using Transfer Learning.
- **Visual Metrics:** Generates accuracy plots and Confusion Matrices for detailed performance analysis.

---

## 🚀 Features
- **Transfer Learning:** Utilizes pre-trained weights (ImageNet) for faster convergence and better feature extraction.
- **Data Augmentation:** Automated rotation, zooming, and shifting to prevent overfitting on small datasets.
- **Confusion Matrix:** Visual heatmap to identify False Positives and False Negatives.
- **Model Checkpointing:** Automatically saves the best version of the model (lowest validation loss) during training.

---

## 📂 Folder Structure
Ensure your project directory matches this structure for the scripts to run correctly:

```text
Barcode_Project/
│
├── dataset/
│   ├── train/
│   │   ├── valid/            # Images of good barcodes
│   │   └── defective/        # Images of bad/no barcodes
│   │
│   └── validation/
│       ├── valid/
│       └── defective/
│
├── output/                   # Generated plots and saved models
│   ├── barcode_model.h5
│   ├── accuracy_plot.png
│   └── confusion_matrix.png
│
├── train_model.py            # Main script for training
├── predict.py                # Script for testing single images
├── requirements.txt          # Dependencies
└── README.md
