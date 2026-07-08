<div align="center">

# 🚗 Distracted Driver Detection Using Custom ResNet50

### Deep Learning | Computer Vision | TensorFlow | Keras

### Driver Behavior Classification using a Custom ResNet50 Architecture Built from Scratch

</div>

---

# 📌 Project Overview

Distracted driving is one of the major causes of road accidents worldwide. Detecting unsafe driver activities in real time can significantly improve road safety and assist intelligent transportation systems.

This project focuses on classifying dashboard camera images into **10 different driver behavior classes** using a **custom implementation of ResNet50** developed from scratch with the **Keras Functional API**. Instead of relying on pretrained models, the residual network architecture is manually constructed using custom residual blocks to better understand the internal working of deep residual learning.

---

# 🎯 Project Objectives

- Build a custom ResNet50 architecture from scratch.
- Classify driver behavior into ten predefined categories.
- Understand residual learning and skip connections.
- Prevent data leakage using driver-wise validation.
- Analyze model performance using bias and variance observations.

---

# 🚘 Driver Activity Classes

| Class | Driver Activity |
|--------|-----------------|
| c0 | Safe Driving |
| c1 | Texting (Right Hand) |
| c2 | Talking on Phone (Right Hand) |
| c3 | Texting (Left Hand) |
| c4 | Talking on Phone (Left Hand) |
| c5 | Operating Radio |
| c6 | Drinking |
| c7 | Reaching Behind |
| c8 | Hair and Makeup |
| c9 | Talking to Passenger |

---

# 📊 Dataset Information

| Property | Details |
|-----------|---------|
| Dataset | State Farm Distracted Driver Detection |
| Source | Kaggle |
| Training Images | 22,424 |
| Number of Classes | 10 |
| Image Size | 64 × 64 × 3 |
| Validation Strategy | Leave-One-Group-Out (LOGO) |

The dataset contains multiple images captured from the same drivers. To avoid information leakage between training and validation sets, **Leave-One-Group-Out (LOGO)** cross-validation is adopted using the driver ID.

---

# 🧠 Model Architecture

The project implements **ResNet50 manually** using the Keras Functional API.

The network consists of:

- Zero Padding
- Initial Convolution Layer
- Batch Normalization
- ReLU Activation
- Max Pooling
- Residual Learning Blocks
  - Identity Blocks
  - Convolutional Blocks
- Average Pooling
- Fully Connected Softmax Output Layer

Unlike transfer learning approaches, this implementation builds every residual block explicitly without using pretrained ResNet models.

---

# 🔄 Model Workflow

```text
Dashboard Image
        │
        ▼
Image Preprocessing
        │
        ▼
Pixel Normalization
        │
        ▼
Custom ResNet50
        │
        ▼
Residual Learning
        │
        ▼
Feature Extraction
        │
        ▼
Softmax Classification
        │
        ▼
Predicted Driver Activity
```

---

# ⚙️ Key Components

### Identity Block

- Preserves input dimensions
- Enables deeper feature learning
- Maintains skip connections

### Convolutional Block

- Changes feature map dimensions
- Performs downsampling
- Learns higher-level image features

---

# 📈 Training Observations

During experimentation, the model demonstrated several practical deep learning challenges.

### Underfitting

- Low training accuracy during initial epochs.
- Indicates the model had not yet learned sufficient feature representations.

### Overfitting

- Difference between training and validation performance increased with additional epochs.
- Suggested improvements include:
  - Data augmentation
  - Dropout
  - L2 Regularization
  - Additional training data
  - Hyperparameter tuning

These observations provide insight into practical model optimization techniques.

---

# 💻 Technologies Used

| Category | Tools |
|----------|------|
| Programming Language | Python |
| Deep Learning | TensorFlow |
| Neural Network API | Keras |
| Data Processing | NumPy, Pandas |
| Visualization | Matplotlib |
| Development Environment | Jupyter Notebook |

---

# 📁 Repository Structure

```text
Distracted Driver Detection
│
├── Distrated Driver detection.ipynb
├── README.md
└── supp
    └── driver.gif
```

---

# 🚀 Skills Demonstrated

- Deep Learning
- Computer Vision
- CNN Architecture Design
- ResNet50
- TensorFlow
- Keras Functional API
- Residual Networks
- Image Classification
- Driver Behavior Analysis
- Model Evaluation
- Bias–Variance Analysis
- Cross Validation

---

# 🌍 Real-World Applications

- Driver Monitoring Systems
- Intelligent Transportation Systems
- Advanced Driver Assistance Systems (ADAS)
- Road Safety Monitoring
- Smart Vehicles
- Autonomous Driving Research

---

# 🔮 Future Enhancements

- Increase training epochs for improved convergence.
- Apply transfer learning for performance comparison.
- Integrate real-time webcam inference.
- Deploy the model as a web application.
- Optimize the model for edge devices.

---

# 👩‍💻 Author

**Noya Falak**

B.Tech – Electronics and Communication Engineering  
Specialization: Generative AI

---

