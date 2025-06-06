# 🧠 Alzheimer's Disease Segmentation with Deep Learning

This project aims to classify and segment Alzheimer’s disease from brain MRI scans using multiple deep learning models:
- ✅ Custom CNN with 4 convolutional blocks and 3 fully connected layers
- ✅ Pre-trained EfficientNet
- ✅ Pre-trained VGG16

We apply data balancing and safe data augmentation to improve performance.

---

## 🚀 Dataset

The dataset is organized into four classes:
- **MildDemented**
- **ModerateDemented**
- **NonDemented**
- **VeryMildDemented**

To address class imbalance, we:
- Downsampled or upsampled images to have **1000 samples per class**.
- Applied **non-geometric data augmentation** using Albumentations for upsampling (noise, blur, brightness).

---


---

## 🛠️ Models

### 🔷 Custom CNN
- 4 convolutional blocks:
  - Conv2D → BatchNorm → ReLU → MaxPool
- 3 fully connected layers:
  - Dense → Dropout → Dense → Dropout → Output
- Implemented from scratch in PyTorch.

### 🔷 EfficientNet
- Pre-trained EfficientNet-B0 from `efficientnet_pytorch`.
- Fine-tuned last few layers.

### 🔷 VGG16
- Pre-trained VGG16.
- Fully connected layers adapted for 4-class classification.

---

## 🎨 Data Augmentation

We used **Albumentations** for **safe (non-geometric)** data augmentation:
- Random brightness/contrast
- Gaussian blur
- Gauss noise
- Random gamma
- Multiplicative noise

---

## 🏃‍♂️ Training

- Optimizer: **Adam**
- Learning rate: `1e-4`
- Loss: **CrossEntropyLoss**
- Metrics: **Accuracy**, **F1-score**





