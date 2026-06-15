# 🌶️ Chili Plant Disease Detection using Hybrid Deep Learning Model

## Overview

This project presents a **Hybrid Deep Learning Model** for **Chili Plant Disease Detection** using image classification. The model combines the feature extraction capabilities of a **Custom Convolutional Neural Network (CNN)** with the power of the pre-trained **InceptionResNetV2** architecture to improve disease classification accuracy.

The system processes chili plant leaf images and classifies them into different disease categories, helping farmers and agricultural professionals identify plant diseases efficiently.

---

## Features

* Hybrid architecture combining:

  * Custom CNN
  * InceptionResNetV2 (Transfer Learning)
* Automated image preprocessing and resizing
* Multi-class disease classification
* Model training and validation
* Performance visualization using accuracy and loss graphs
* Dataset distribution analysis
* Model export for future deployment

---

## Dataset Structure

```text
Chili_Plant_Disease/
│
├── train/
│   ├── Class_1/
│   ├── Class_2/
│   ├── Class_3/
│   ├── Class_4/
│   └── Class_5/
│
└── test/
    ├── Class_1/
    ├── Class_2/
    ├── Class_3/
    ├── Class_4/
    └── Class_5/
```

The dataset contains chili leaf images categorized into five classes representing different disease conditions.

---

## Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* OpenCV
* PIL
* Matplotlib
* Pandas

---

## Model Architecture

### Custom CNN Branch

* Conv2D (32 filters)
* ReLU Activation
* MaxPooling
* Conv2D (32 filters)
* ReLU Activation
* MaxPooling
* Conv2D (64 filters)
* ReLU Activation
* MaxPooling
* Flatten Layer

### Transfer Learning Branch

* InceptionResNetV2 (Pre-trained on ImageNet)
* Top layers removed
* Frozen weights during training

### Fusion Layer

Features from both branches are concatenated and passed through:

* Dense (512)
* Dense (256)
* Dropout (0.5)
* Dense (128)
* Softmax Output Layer

---

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/chili-plant-disease-detection.git
cd chili-plant-disease-detection
```

Install dependencies:

```bash
pip install tensorflow keras numpy pandas matplotlib opencv-python pillow
```

---

## Training

Run the notebook:

```bash
jupyter notebook trainingHybrid1.ipynb
```

Training Configuration:

```python
Epochs = 50
Optimizer = Adam
Loss Function = Categorical Crossentropy
Activation = Softmax
```

---

## Results

The model evaluates performance using:

* Training Accuracy
* Validation Accuracy
* Training Loss
* Validation Loss

Performance graphs are generated to visualize learning progress throughout training.

---

## Output

The trained model is saved as:

```text
chily.h5
```

This model can be used for future prediction and deployment applications.

---

## Applications

* Smart Agriculture
* Disease Monitoring Systems
* Crop Health Assessment
* Precision Farming
* Agricultural Research

---

## Future Enhancements

* Real-time disease detection using mobile devices
* Web-based prediction interface
* Integration with IoT-enabled smart farming systems
* Disease severity estimation
* Support for additional crop diseases

---

## Author

**RAMKUMAR A**
B.Tech ECE 
Project: Hybrid Deep Learning-Based Chili Plant Disease Detection

---
