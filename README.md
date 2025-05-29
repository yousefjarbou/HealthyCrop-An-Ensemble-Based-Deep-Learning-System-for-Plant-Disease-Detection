# HealthyCrop: An Ensemble-Based Deep Learning System for Plant Disease Detection

This repository contains the full implementation of **HealthyCrop**, an ensemble-based image classification system for detecting plant diseases from RGB leaf images. The system leverages the strengths of 7 state-of-the-art CNN architectures to maximize accuracy through majority voting.

---

## Dataset

- **Source**: [Kaggle - Plant Leaves for Image Classification](https://www.kaggle.com/datasets/csafrit2/plant-leaves-for-image-classification)
- **Classes**: Healthy vs. Diseased across 12 crop species
- **Total Images**: 4,503
- **Preprocessing**:
  - Resized to 224×224
  - Normalization
  - Augmentation: rotation, flipping, Gaussian blur, scaling, noise

---

## Models Used

The following pre-trained CNN architectures were fine-tuned on the dataset using PyTorch:

| Model File              | Model Name     | Test Accuracy (%) |
|-------------------------|----------------|--------------------|
| `alexnet90.pth`         | AlexNet        | 90.00              |
| `efficientnet_95.77.pth`| EfficientNet-B0| 95.77              |
| `resnet50_91.pth`       | ResNet50       | 91.00              |
| `Resnet_94_5.pth`       | ResNet18       | 94.50              |
| `mobilenet_90.pth`      | MobileNet V3   | 90.00              |
| `densenet_91_82.pth`    | DenseNet121    | 82.00              |
| `ConvNeXt_90.pth`       | ConvNeXt-Tiny  | 90.00              |

➡**Ensemble (Hard Voting)**: ~**99.2%** Accuracy

---

## Features

- ✅ Transfer learning with stratified sampling
- ✅ Extensive augmentation for generalization
- ✅ Regularization: Dropout + Weight Decay
- ✅ Training & testing visualizations included
- ✅ Final ensemble prediction script for inference
- ✅ Plots of per-model performance included

---

## 📂 Repository Structure

