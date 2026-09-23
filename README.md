# Deepfake Detection System (ResNeXt & LSTM with Custom UI)

![Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)
![Framework](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=flat&logo=django&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=flat&logo=docker&logoColor=white)

> **Acknowledgment & Contribution Declaration:** 
> The core deep learning architecture (ResNeXt + LSTM) and model training methodologies referenced in this repository are based on the open-source work by Abhijit Jadhav et al. 
> **My primary contribution to this project is the independent design, development, and integration of the entire Django-based frontend web application**, providing a seamless, user-friendly interface for the backend detection model.

## 📖 Overview
This repository contains a comprehensive Deepfake Detection System. The project aims to identify manipulated facial videos utilizing a Spatio-Temporal deep learning architecture. My work focuses on bridging the gap between complex AI models and end-users by building a robust, fully Dockerized Django web interface for real-time inference.

## 💻 Web Interface Showcase (My Contribution)
*(注：建议你在这里放 1-2 张你自己设计的网页前端截图，展示你的工作成果。截图上传到项目里后，替换下面的链接即可)*
> **[TODO: Add screenshot of your Django Web Interface here]**
> `![Web UI](github_assets/my_custom_ui_screenshot.png)`

## 🔬 Backend Methodology (Referenced Architecture)
The backend detection system utilizes a Spatio-Temporal architecture to capture both frame-level artifacts and temporal inconsistencies:
1. **Spatial Feature Extraction:** A pre-trained **ResNeXt50** Convolutional Neural Network (CNN) is utilized via transfer learning to extract high-level spatial feature vectors from individual facial frames.
2. **Temporal Sequence Analysis:** An **LSTM (Long Short-Term Memory)** network processes the sequential features extracted by the CNN to analyze the temporal dynamics, detecting unnatural flickers or temporal anomalies.

## 📊 Experimental Results
Extensive experiments demonstrate the impact of the number of frames processed per video on detection accuracy (evaluated on a dataset of 6,000 videos).

| Model Checkpoint | Videos | Frames per Video | Accuracy |
| :--- | :---: | :---: | :---: |
| `model_84_acc_10_frames.pt` | 6000 | 10 | 84.21% |
| `model_87_acc_20_frames.pt` | 6000 | 20 | 87.79% |
| `model_89_acc_40_frames.pt` | 6000 | 40 | 89.34% |
| `model_90_acc_60_frames.pt` | 6000 | 60 | 90.59% |
| `model_91_acc_80_frames.pt` | 6000 | 80 | 91.49% |
| **`model_93_acc_100_frames.pt`**| **6000** | **100** | **93.58%**|

## 📁 Directory Structure
```text
.
├── Django Application/    # Custom-designed Dockerized web application (My Contribution)
├── Model Creation/        # Data preprocessing and PyTorch model scripts (Referenced)
├── Documentation/         # Project documentation and reports
├── github_assets/         # Images used in this README
└── README.md
