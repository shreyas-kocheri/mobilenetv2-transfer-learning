# MobileNetV2 Transfer Learning

A hands-on deep learning project to understand and implement **Transfer Learning** using **MobileNetV2** and the Intel Image Classification dataset.

## 📌 Project Overview

This project demonstrates how a pretrained CNN model can be reused for a new image classification task.

Instead of training a CNN from scratch, we use **MobileNetV2 pretrained on ImageNet** and compare two transfer learning approaches:

1. **Feature Extraction**
2. **Fine-Tuning**

The goal of this project was to understand how pretrained models work and how their performance changes when they are adapted to a new dataset.

## 📂 Dataset

**Intel Image Classification Dataset**

The dataset contains six classes:

- Buildings
- Forest
- Glacier
- Mountain
- Sea
- Street

The dataset is organized into training and testing directories, with each class represented by a separate folder.

## 🧠 Transfer Learning Approaches

### 1. Feature Extraction

The pretrained MobileNetV2 layers are frozen and used as a feature extractor.

Only the newly added classification layers are trained.

```text
Input Image
     ↓
MobileNetV2 (Frozen)
     ↓
Global Average Pooling
     ↓
Dense Layer
     ↓
6-Class Output
