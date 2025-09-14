# 🧠 Brain Tumor Detection using Deep Learning

## 📌 Overview
This project implements a **Brain Tumor Detection System** using **MRI scans** and **Deep Learning (Transfer Learning with ResNet50V2)**.  
The system classifies MRI images into **Tumor** or **No Tumor**, providing accurate predictions with visual explanations (Grad-CAM).  

---

## 📊 Dataset
- Source: [Kaggle – Brain Tumor MRI Dataset by Masoud Nickparvar](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset)  
- Subsets:  
  - [Training set (~131 MB)](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset?select=Training)  
  - [Testing set (~24 MB)](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset?select=Testing)  
- Classes: **Tumor**, **No Tumor**  
- Format: MRI brain scan images (JPEG/PNG)  
- Task: Binary classification (detecting presence of brain tumor)  


## 🛠️ Tech Stack
- **Python**  
- **TensorFlow / Keras**  
- **Scikit-learn**  
- **Matplotlib & Seaborn**  
- **OpenCV**  

---

## 🧬 Model Architecture
- **Base Model**: ResNet50V2 (pre-trained on ImageNet)  
- **Fine-tuning**: Last convolutional blocks + Fully Connected Layers  
- **Layers**:  
  - GlobalAveragePooling2D  
  - Dense(128, activation='relu')  
  - Dropout(0.3)  
  - Dense(1, activation='sigmoid')  

---

## 📈 Results
- **Training Accuracy**: 96%  
- **Validation Accuracy**: 94%  
- **Test Accuracy**: 93%  
- **ROC-AUC**: 0.97  
- **Sensitivity**: 92%  
- **Specificity**: 95%  

Confusion Matrix:  

|             | Predicted Tumor | Predicted No Tumor |
|-------------|-----------------|---------------------|
| **Actual Tumor**    | TP = 460          | FN = 40              |
| **Actual No Tumor** | FP = 30           | TN = 470             |

---

