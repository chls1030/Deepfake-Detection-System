# Deepfake Detection System

![Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)
![Framework](https://img.shields.io/badge/framework-PyTorch%20%7C%20Django-green.svg)
![License](https://img.shields.io/badge/license-GPL--3.0-blue.svg)

## 📖 Overview
This repository contains the source code and documentation for a comprehensive Deepfake Detection System. The project aims to identify manipulated facial videos utilizing deep learning techniques, providing a robust backend model alongside a user-friendly Django web interface for real-time inference.

## 🔬 Methodology & Architecture
Our detection system utilizes a Spatio-Temporal deep learning architecture to capture both frame-level artifacts and temporal inconsistencies in videos.

* **Data Preprocessing:** Videos are split into sequence frames, followed by automatic face cropping to isolate the region of interest.
* **Spatial Feature Extraction:** A pre-trained **ResNeXt50** model is utilized via transfer learning to extract high-level spatial features from individual facial frames.
* **Temporal Sequence Analysis:** An **LSTM (Long Short-Term Memory)** network is placed on top of the CNN backbone to analyze the temporal sequence of frames, detecting unnatural flickers or temporal anomalies common in deepfake videos.
* **Web Interface:** A Django-based application allows users to upload media and receive authenticity probability scores.

## 📊 Datasets 
The model was trained and evaluated on large-scale standard benchmarks:
- **FaceForensics++**
- **Celeb-DF**
- **Deepfake Detection Challenge (DFDC)**

*(Note: Preprocessed cropped face datasets and trained `.pt` weights are available via Google Drive links in the `model_creation` directory).*

## 📁 Repository Structure
```text
├── Django Application/    # Django web application for user interface
├── Model Creation/        # Source code for data preprocessing and PyTorch model training
├── Documentation/         # Project documentation and slides (PDF)
├── README.md
