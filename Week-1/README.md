# Garbage Classification - Week 1 Report

## 🔍 Project Overview
This project is part of a 4-week internship focused on building and improving an image classification model for garbage type detection. The model aims to classify images into multiple waste categories using deep learning.

## ✅ Week 1 Goals
- Set up the dataset pipeline
- Build a baseline model using EfficientNetV2B2
- Establish performance benchmarks for future improvements

## 📁 Work Done in Week 1

### 📦 Dataset Preparation
- Mounted dataset from Google Drive
- Resized all images to **260×260** (EfficientNetV2B2 standard)
- Normalized pixel values with `Rescaling`
- Split data into:
  - **80% Training**
  - **10% Validation**
  - **10% Test** (by further splitting validation using `.take()` and `.skip()`)

### 🎨 Data Augmentation
Applied basic augmentation using `keras.Sequential`:
- `RandomFlip`
- `RandomRotation`
- `RandomZoom`
- `RandomContrast`

### ⚖️ Class Weights
Calculated class weights using `compute_class_weight` from `sklearn` to address class imbalance.

### 🧠 Model Setup
- Used `EfficientNetV2B2` (with preprocessing layer included)
- Added:
  - Global Average Pooling
  - Dropout
  - Dense softmax output layer

### 🛠️ Callbacks
- `EarlyStopping`: to prevent overfitting
- `ReduceLROnPlateau`: for dynamic learning rate adjustment
- `ModelCheckpoint`: to save the best model during training

### 📊 Visualizations
- Displayed class-wise sample images
- Printed training and validation accuracy/loss

## 📌 Next Steps
In Week 2:
- Add confusion matrix & classification report
- Visualize Grad-CAM for interpretability
- Improve underperforming class recall

---

_This notebook establishes a strong and clean baseline for the garbage classification task using transfer learning._
