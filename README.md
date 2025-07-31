# 🌿 Sugarcane Disease Detection Using CNN

This project implements a **Convolutional Neural Network (CNN)** to automatically detect **Red Rot disease** in sugarcane leaves from image data. It classifies sugarcane leaf images into two categories:

- ✅ Healthy  
- ❌ Red Rot Infected  

Early detection of Red Rot is crucial for managing crop health and improving yield. This deep learning-based solution provides an efficient, automated way to assist farmers and agricultural experts in disease diagnosis.

---

## 📂 Dataset

To run this project, you **must download the dataset** from the link below:

📎 **[Download Dataset](https://drive.google.com/file/d/1Svp70KvoKT1u2b3E00BdUNU1NC8pg0W_/view?usp=drive_link)**

The dataset contains two folders of labeled sugarcane leaf images:

- `Healthy` (images of healthy leaves)  
- `Red Rot` (images of diseased leaves)

> ⚠️ After downloading:
> - Extract the contents.
> - Place the folders in the same directory as the notebook or update the path in the code accordingly.

---

## 🧠 How It Works

### 1. Data Preprocessing
- All images are resized to **128x128 pixels**
- Augmentation using Keras' `ImageDataGenerator`:
  - Rotation
  - Zoom
  - Horizontal flipping
- Data is split into **training** and **validation** sets automatically.

### 2. CNN Model
The model is built using the Keras Sequential API and consists of:

- Convolutional layers with ReLU activation
- MaxPooling for downsampling
- Flatten layer
- Dense layers
- Output layer with **2 neurons** (Softmax for binary classification)

### 3. Model Training
- Optimizer: `adam`  
- Loss Function: `categorical_crossentropy`  
- Metric: `accuracy`  
- Trained for **10 epochs**

### 4. Evaluation
- Visualizes accuracy and loss curves for training/validation
- Predicts new images using the trained model

---

## 📊 Results

The trained CNN demonstrates high accuracy in distinguishing between healthy and Red Rot-infected leaves. It generalizes well across validation data and can be easily adapted for mobile or web deployment.

---

## 📦 Requirements

Install the required libraries:

```bash
pip install tensorflow numpy matplotlib opencv-python
