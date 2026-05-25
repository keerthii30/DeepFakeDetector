````markdown
# DeepFake Detector

A deep learning-based system for detecting manipulated (deepfake) videos. This project provides tools for training models to distinguish between real and fake videos and includes deployable applications for real-time deepfake detection.

---

# Project Overview

This repository contains a complete pipeline for deepfake detection:

- Training and evaluation notebooks
- Flask-based deployment application
- Production-ready web interface for user interaction

The system utilizes:

- ResNext50 for spatial feature extraction
- LSTM for temporal sequence learning
- Face Recognition for detecting and focusing on facial regions

---

# Repository Structure

```bash
DeepFakeDetector/
│
├── Training/
│   ├── Model_train.ipynb
│   └── Preprocess.py
│
├── Deepfake_detector_model_deployment/
│   ├── app.py
│   ├── templates/
│   ├── Dockerfile
│   ├── requirements.txt
│   └── model/
│
├── Final_Deployment/
│   ├── app.py
│   └── templates/
│
└── README.md
````

---

# Features

* Deepfake video detection using deep learning
* Facial region extraction for improved accuracy
* Real-time prediction through web interface
* Confidence score for prediction reliability
* Flask-based deployment

---

# How It Works

The detection pipeline follows these steps:

1. Video upload through the web interface
2. Frame extraction from uploaded video
3. Face detection and extraction
4. Feature extraction using ResNext50
5. Temporal sequence analysis using LSTM
6. Final classification as Real or Fake

---

# Model Architecture

## Feature Extractor

* ResNext50_32x4d pretrained on ImageNet

## Temporal Modeling

* LSTM network for sequential frame analysis

## Classification Layer

* Fully connected neural network layer

---

# Dataset

The model was trained using:

* FaceForensics++ (FF++)

---

# Requirements

Major dependencies:

* Python 3.12.x
* PyTorch
* OpenCV
* Flask
* Face Recognition
* dlib

Install dependencies:

```bash
pip install -r requirements.txt
```

---

# Running the Application

## Clone Repository

```bash
git clone https://github.com/keerthii30/DeepFakeDetector.git
cd DeepFakeDetector
```

## Create Virtual Environment

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### macOS/Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

---

# Install Dependencies

```bash
cd Deepfake_detector_model_deployment
pip install -r requirements.txt
```

---

# Run Application

```bash
python app.py
```

Access the application at:

```bash
http://localhost:3000
```

---

# Training Your Own Model

1. Prepare dataset containing real and fake videos
2. Open `Training/Model_train.ipynb`
3. Train the model using Jupyter Notebook or Google Colab
4. Save the trained model as:

```bash
df_model.pt
```

5. Place the model inside:

```bash
Deepfake_detector_model_deployment/model/
```

---

# Web Interface Usage

1. Open the web application
2. Upload a video file

Supported formats:

* mp4
* avi
* mov
* mkv
* wmv

3. Click **Detect Deepfake**
4. Wait for processing
5. View prediction result with confidence score

---

# Model Performance

The model provides:

* High accuracy in manipulated video detection
* Efficient real-time analysis
* Improved reliability using facial region extraction

---

# Limitations

* Performance may vary with video quality
* Face detection may fail in low-light conditions
* Large videos require longer processing time

---

# Note

The trained model file (`df_model.pt`) is excluded from this repository due to GitHub file size limitations.

---

# Acknowledgments

* PyTorch
* OpenCV
* Face Recognition Library
* Deepfake Detection Research Community
* FaceForensics++ Dataset

---

# Author

Keerthi Thatikonda

GitHub Repository:
[https://github.com/keerthii30/DeepFakeDetector](https://github.com/keerthii30/DeepFakeDetector)

```
```
