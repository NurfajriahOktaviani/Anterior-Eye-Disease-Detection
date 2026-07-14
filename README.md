# Automatic Anterior Eye Disease Detection Using YOLOV12 with CBAM and ECA Attention Mechanisms


**"Automatic Anterior Eye Disease Detection Using YOLOV12 with CBAM and ECA Attention Mechanisms"**

---

# 📋 Overview

Anterior eye diseases such as cataract, conjunctivitis, uveitis, and eyelid disorders are among the leading causes of visual impairment worldwide. Delayed diagnosis may lead to decreased visual function and reduced quality of life. Therefore, an automatic computer vision-based detection system is required to assist early disease identification.

This research proposes an automatic anterior eye disease detection framework using **YOLOV12** combined with two attention mechanisms: **Convolutional Block Attention Module (CBAM)** and **Efficient Channel Attention (ECA)**. The objective is to improve feature extraction capability while maintaining real-time inference performance.

The research follows the **CRISP-DM** methodology consisting of:

- Business Understanding
- Data Understanding
- Data Preparation
- Modeling
- Evaluation
- Deployment

Image preprocessing consists of quality assurance, image enhancement using CLAHE and Unsharp Masking, smooth balancing, and data augmentation. Model performance is evaluated using Precision, Recall, F1-score, mAP50, and mAP50-95. Explainable Artificial Intelligence (XAI) using Grad-CAM is employed to visualize the model's attention during prediction. The final model is deployed on a Virtual Private Server (VPS) through FastAPI REST API and integrated with a Flutter mobile application.

---

# ✨ Key Features

- Automatic anterior eye disease detection
- YOLOV12 object detection framework
- Comparison between CBAM and ECA attention mechanisms
- CLAHE image enhancement
- Unsharp Masking image sharpening
- Smooth balancing for class distribution
- Data augmentation using Albumentations
- Explainable AI using Grad-CAM
- FastAPI REST API deployment
- Flutter mobile application
- VPS deployment
- Real-time inference

---

# 🎯 Key Contributions

- Developed an automatic anterior eye disease detection framework based on YOLOV12.
- Proposed the integration of CBAM into the YOLOV12 architecture for improved feature attention.
- Compared CBAM and ECA attention mechanisms on the same dataset.
- Designed a complete preprocessing pipeline including image enhancement, augmentation, and smooth balancing.
- Improved model interpretability using Grad-CAM visualization.
- Successfully deployed the detection model on VPS and integrated it with a Flutter mobile application.

---

# 🏗 Project Architecture / Research Workflow

<p align="center">
<img src="project architecture.png" width="900">
</p>

Research workflow:

1. Business Understanding
2. Data Understanding
3. Data Preparation
4. Modeling
5. Evaluation
6. Deployment

---

# 🚀 Installation

## Requirements

- Python 3.11
- CUDA 11.8+
- PyTorch
- Ultralytics YOLO
- OpenCV
- Albumentations
- FastAPI
- Uvicorn
- Flutter SDK

## Clone Repository

```bash
git clone https://github.com/NurfajriahOktaviani/Anterior-Eye-Disease-Detection.git

cd Anterior-Eye-Disease-Detection
```

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 📊 Dataset Preparation

## Dataset

The dataset consists of **2,298 anterior eye images** collected from a public Mendeley dataset.

### Disease Classes

- Cataract
- Conjunctivitis
- Eyelid
- Normal
- Uveitis

### Annotation Format

- JPG / PNG images
- YOLO Annotation (.txt)

### Data Preparation Pipeline

The preprocessing pipeline includes:

- Dataset quality verification
- Blur image inspection
- Duplicate image inspection
- Annotation verification
- CLAHE enhancement
- Unsharp Masking
- Smooth balancing
- Data augmentation
- Dataset splitting (Train, Validation, Test)

Dataset structure:

```
dataset/
│
├── train/
├── valid/
└── test/
```

---

# 🏋 Training

### Training Configuration

| Parameter | Value |
|------------|---------|
| Epoch | 40 |
| Batch Size | 12 |
| Image Size | 512 × 512 |
| Optimizer | AdamW |
| Scheduler | Cosine Learning Rate |
| Warmup Epoch | 3 |
| Early Stopping | Enabled |
| Weight Decay | Enabled |

Training command

```bash
python train.py
```

or

```bash
notebooks/02_training.ipynb
```

---

# 📊 Results

Model evaluation was performed using the **pure test dataset**. Three models were compared: the baseline YOLOV12, YOLOV12 enhanced with CBAM, and YOLOV12 enhanced with ECA.

## Performance Comparison

| Model | mAP50 | mAP50-95 | Precision | Recall | F1-score | Inference Speed | Parameters |
|--------|--------|----------|-----------|--------|----------|-----------------|------------|
| YOLOV12 (Baseline) | 0.6148 | 0.5365 | 0.6108 | 0.6133 | 0.6120 | - | 2,520,639 |
| **YOLOV12 + CBAM (Proposed)** | **0.6401** | **0.5561** | **0.7157** | 0.5925 | **0.6483** | 4.5 ms/image (~222 FPS) | 2,531,075 |
| YOLOV12 + ECA | 0.6235 | 0.5439 | 0.6400 | **0.6180** | 0.6288 | **4.4 ms/image (~238 FPS)** | 2,520,649 |

### Performance Summary

The proposed **YOLOV12+CBAM** achieved the highest overall detection performance with the best mAP50, mAP50-95, Precision, and F1-score. Although the ECA model achieved slightly higher Recall and faster inference speed, CBAM produced more reliable predictions by focusing on the most relevant spatial and channel features.

### Evaluation Outputs

- Precision-Confidence Curve
- Recall-Confidence Curve
- F1-Confidence Curve
- Precision-Recall Curve
- Confusion Matrix
- Grad-CAM Visualization
- Performance Comparison
- Flutter Application Testing
- VPS REST API Deployment

---

# 📁 Project Structure

```
Anterior-Eye-Disease-Detection/
│
├── dataset/
│   ├── train/
│   ├── valid/
│   └── test/
│
├── preprocessing/
│   ├── clahe/
│   ├── unsharp_mask/
│   ├── augmentation/
│   └── smooth_balancing/
│
├── notebooks/
│
├── models/
│   ├── yolov12_base/
│   ├── yolov12_cbam/
│   └── yolov12_eca/
│
├── deployment/
│   ├── fastapi/
│   └── flutter/
│
├── results/
│   ├── confusion_matrix/
│   ├── curves/
│   ├── gradcam/
│   └── comparison/
│
├── requirements.txt
└── README.md
```

---

# 📝 Citation

If you use this work, please cite:

```bibtex
@thesis{oktaviani2026,
  title={Automatic Anterior Eye Disease Detection Using YOLOV12 with CBAM and ECA Attention Mechanisms},
  author={Nurfajriah Oktaviani},
  school={Universitas Multimedia Nusantara},
  year={2026}
}
```

---

# 🙏 Acknowledgments

This research was conducted under:

- Big Data Laboratory
- Information Systems Study Program
- Faculty of Engineering and Informatics
- Universitas Multimedia Nusantara

Special thanks to:

- Ultralytics
- Mendeley Dataset Provider
- OpenCV Community
- Albumentations
- PyTorch Community

---

# 📧 Contact

**Nurfajriah Oktaviani**

Information Systems

Universitas Multimedia Nusantara

GitHub:
https://github.com/NurfajriahOktaviani

---

# 📜 License

This project is released under the MIT License.
