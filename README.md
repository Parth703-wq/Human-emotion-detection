# Human-emotion-detection
# Facial Expression Recognition using CNN

## Overview

This project implements a **Deep Learning based Facial Expression Recognition system** that classifies human emotions from facial images. The model is trained using **Convolutional Neural Networks (CNN)** with TensorFlow/Keras.

The system can detect **7 different facial emotions** and can be integrated with **OpenCV for real-time webcam emotion detection**.

---

## Emotion Classes

The model classifies faces into the following categories:

* Angry
* Disgust
* Fear
* Happy
* Sad
* Surprise
* Neutral

---

## Model Architecture

The model uses a Convolutional Neural Network consisting of:

* Convolution Layers (Conv2D)
* Batch Normalization
* ReLU Activation
* MaxPooling Layers
* Dropout Regularization
* Fully Connected Dense Layers
* Softmax Output Layer

**Input Image Size:**
48 × 48 grayscale images

---

## Dataset

This project uses a facial emotion dataset similar to **FER2013**.

Dataset structure:

```
dataset/
│
├── train/
│   ├── angry
│   ├── disgust
│   ├── fear
│   ├── happy
│   ├── sad
│   ├── surprise
│   └── neutral
│
└── validation/
    ├── angry
    ├── disgust
    ├── fear
    ├── happy
    ├── sad
    ├── surprise
    └── neutral
```

Note: The dataset is not included in this repository due to size limitations.
DATASET LINK : dropbox.com/scl/fi/qtcrzmsv4jz47cgvr2t0u/train.zip?rlkey=x3sz1h2o797inkqer67q7dg6b&dl=0

---

## Training Configuration

| Parameter     | Value                    |
| ------------- | ------------------------ |
| Image Size    | 48 × 48                  |
| Batch Size    | 64 / 128                 |
| Epochs        | 30 – 48                  |
| Optimizer     | Adam                     |
| Loss Function | Categorical Crossentropy |

Training also uses:

* Data Augmentation
* Early Stopping
* ReduceLROnPlateau
* Model Checkpointing

---

## Installation

Clone the repository:

```
git clone https://github.com/parth703-wq/facial-expression-recognition.git
```

Move into the project folder:

```
cd facial-expression-recognition
```

Install required libraries:

```
pip install -r requirements.txt
```

---

## Run Model Training

```
python src/train.py
```

The trained model will be saved as:

```
facial_expression_best_model.h5
```

---

## Real-Time Emotion Detection (Webcam)

The trained model can be used with OpenCV for live emotion detection.

```
python src/realtime_detection.py
```

This script captures webcam frames, detects faces, and predicts the emotion in real time.

---

## Technologies Used

* Python
* TensorFlow / Keras
* OpenCV
* NumPy
* Matplotlib
* TQDM

---

## Results

The model outputs:

* Training accuracy and loss graphs
* Validation accuracy
* Trained `.h5` model file

---

## Future Improvements

Possible improvements for this project:

* Real-time emotion detection API
* Mobile deployment
* Transformer-based emotion recognition
* Face tracking with emotion history
* Web application interface

---


This project is open source and available under the MIT License.
