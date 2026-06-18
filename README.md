# LungVision: Lung Cancer Classification Using Deep Learning

## 📌 Overview

LungVision is a deep learning-based medical imaging project designed to classify lung CT scan images into three categories: **Normal**, **Benign**, and **Malignant**. The project leverages Convolutional Neural Networks (CNNs) to automatically learn discriminative features from CT scans, assisting in the early detection and diagnosis of lung cancer.

This system aims to reduce manual analysis effort and provide an AI-assisted approach for identifying potentially cancerous lung abnormalities.

---

## 🎯 Objectives

* Develop an automated lung cancer classification system.
* Classify CT scan images into:

  * Normal
  * Benign
  * Malignant
* Perform image preprocessing and normalization.
* Train a CNN model for multi-class classification.
* Evaluate model performance using validation accuracy and loss metrics.

---

## 🏥 Problem Statement

Lung cancer is one of the leading causes of cancer-related deaths worldwide. Early diagnosis significantly improves treatment outcomes. However, manual analysis of CT scans can be time-consuming and prone to human error.

LungVision addresses this challenge by utilizing deep learning techniques to automatically identify patterns associated with different lung conditions.

---

## 📂 Dataset

The dataset consists of lung CT scan images categorized into three classes:

                                                                LungCancerDataset/
                                                                │
                                                                ├── Normal cases/
                                                                ├── Benign cases/
                                                                └── Malignant cases/


### Dataset Classes

| Class     | Description                      |
| --------- | -------------------------------- |
| Normal    | Healthy lung tissue              |
| Benign    | Non-cancerous lung abnormalities |
| Malignant | Cancerous lung tumors            |

---

## ⚙️ Data Preprocessing

The following preprocessing steps were performed:

* Image loading using OpenCV
* Conversion to grayscale
* Resizing images to **128 × 128**
* Pixel value normalization (0–255 → 0–1)
* Label encoding
* Train-test splitting

### Input Shape

128 × 128 × 1


## 🧠 Model Architecture

The classification model is built using TensorFlow/Keras and follows a Convolutional Neural Network (CNN) architecture.

### Architecture Flow


                                                      Input Image (128×128×1)
                                                                  │
                                                                  ▼
                                                      Conv2D (32 Filters, 3×3)
                                                                  │
                                                                  ▼
                                                      MaxPooling2D
                                                                  │
                                                                  ▼
                                                      Conv2D (64 Filters, 3×3)
                                                                  │
                                                                  ▼
                                                      MaxPooling2D
                                                                  │
                                                                  ▼
                                                      Conv2D (64 Filters, 3×3)
                                                                  │
                                                                  ▼
                                                      Flatten
                                                                  │
                                                                  ▼
                                                      Dense (64 Neurons)
                                                                  │
                                                                  ▼
                                                      Softmax Output Layer
                                                                  │
                                                                  ▼
                                                      Normal / Benign / Malignant


---

## 🔍 Key Components

### Convolutional Layers

Extract image features such as:

* Edges
* Textures
* Tumor patterns

### ReLU Activation

Introduces non-linearity to enable learning complex visual patterns.

### Max Pooling

* Reduces feature map dimensions
* Lowers computational cost
* Helps prevent overfitting

### Softmax Layer

Generates probabilities for the three output classes.

---

## 🚀 Training Configuration

| Parameter         | Value                    |
| ----------------- | ------------------------ |
| Framework         | TensorFlow / Keras       |
| Optimizer         | Adam                     |
| Loss Function     | Categorical Crossentropy |
| Batch Size        | 32                       |
| Epochs            | 10                       |
| Evaluation Metric | Accuracy                 |

---

## 📈 Evaluation

The model was evaluated using:

* Training Accuracy
* Validation Accuracy
* Loss Curves

Training performance was visualized using Matplotlib to monitor convergence and identify potential overfitting.

---

## 🛠️ Technologies Used

### Languages

* Python

### Libraries

* TensorFlow
* Keras
* OpenCV
* NumPy
* Matplotlib
* Scikit-learn

---

## 📚 Key Concepts Implemented

* Deep Learning
* Convolutional Neural Networks (CNN)
* Medical Image Classification
* Image Preprocessing
* Multi-Class Classification
* Feature Extraction
* Softmax Classification
* Model Evaluation
