# Human Disease Classification using Deep Learning

## Overview

This project implements a deep learning-based image classification system for identifying human diseases from medical images. The model is built using TensorFlow and Keras, leveraging transfer learning with EfficientNetB0 to classify images into multiple disease categories.

The notebook covers the complete machine learning pipeline, including:

- Dataset preparation
- Data augmentation
- Train/Validation/Test split
- Transfer learning using EfficientNetB0
- Model training and evaluation
- Disease prediction on unseen images

---

## Dataset

The dataset consists of medical images belonging to **30 disease classes**.

### Dataset Distribution

| Split | Images |
|---------|---------:|
| Training | 43,291 |
| Validation | 12,364 |
| Testing | 6,204 |

Class imbalance was handled using computed class weights during training.

---

## Model Architecture

### Base Model
- EfficientNetB0 (Pretrained on ImageNet)

### Additional Layers
- Global Average Pooling Layer
- Dense Classification Layer
- Softmax Output Layer

### Frameworks Used
- TensorFlow
- Keras
- NumPy
- OpenCV
- Matplotlib
- Scikit-learn

---

## Training Configuration

| Parameter | Value |
|------------|---------|
| Model | EfficientNetB0 |
| Epochs | 25 |
| Learning Rate | 1e-4 |
| Optimizer | Adam |
| Loss Function | Categorical Crossentropy |
| Batch Size | TensorFlow Dataset Pipeline |

---

## Training Results

During training, the model steadily improved its validation performance.

### Best Validation Performance

| Metric | Value |
|----------|---------|
| Validation Accuracy | ~80.9% |
| Validation Loss | ~0.88 |

---

## Test Performance

The trained model was evaluated on a separate test set.

| Metric | Value |
|----------|---------|
| Test Accuracy | **79.45%** |
| Test Loss | **0.98** |

---

## Features

- Multi-class disease classification
- Transfer learning with EfficientNetB0
- Class imbalance handling through class weights
- Automated dataset splitting
- Data augmentation support
- Test-set evaluation
- Single-image disease prediction

---

