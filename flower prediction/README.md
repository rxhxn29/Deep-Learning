# Flower Classification with ResNet50

A deep learning project for flower image classification using TensorFlow/Keras and the ResNet50 pre-trained model.

## 📋 Project Overview

This project implements a transfer learning approach to classify flower images into 5 categories using a pre-trained ResNet50 model. The model achieves high accuracy in distinguishing between different flower species.

## 🌸 Dataset

The project uses the TensorFlow Flowers dataset containing 5 classes of flowers:
- Daisy
- Dandelion
- Roses
- Sunflowers
- Tulips

**Dataset Details:**
- Total images: 3,670
- Training set: 2,936 images (80%)
- Validation set: 734 images (20%)
- Image size: 180×180 pixels

## 🏗️ Model Architecture

The model is built using transfer learning with the following architecture:

1. **Base Model**: ResNet50 (pre-trained on ImageNet)
   - Includes top: False
   - Input shape: (180, 180, 3)
   - Pooling: Average pooling
   - All layers frozen (non-trainable)

2. **Custom Layers**:
   - Flatten layer
   - Dense layer (512 units, ReLU activation)
   - Output layer (5 units, Softmax activation)

**Model Summary:**
- Total parameters: 24,639,365
- Trainable parameters: 1,051,653
- Non-trainable parameters: 23,587,712

=