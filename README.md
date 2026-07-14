# Automatic Anterior Eye Disease Detection Using YOLOV12 with CBAM and ECA Attention Mechanisms

Official implementation of the undergraduate thesis:

**"Automatic Anterior Eye Disease Detection Using YOLOV12 with CBAM and ECA Attention Mechanisms"**

---

## 📋 Overview

Anterior eye diseases such as cataract, conjunctivitis, uveitis, and eyelid disorders are among the leading causes of visual impairment worldwide. Early diagnosis is important to prevent disease progression and improve treatment outcomes. However, manual examination requires experienced ophthalmologists and is often time-consuming.

This research proposes an automatic anterior eye disease detection system using **YOLOV12** enhanced with two attention mechanisms: **Convolutional Block Attention Module (CBAM)** and **Efficient Channel Attention (ECA)**. The research follows the **CRISP-DM** methodology, consisting of Business Understanding, Data Understanding, Data Preparation, Modeling, Evaluation, and Deployment.

The preprocessing pipeline includes image quality assurance, CLAHE enhancement, Unsharp Masking, data augmentation, and smooth balancing. The models are evaluated using Precision, Recall, F1-score, and Mean Average Precision (mAP). Explainable Artificial Intelligence (XAI) using Grad-CAM is also employed to visualize the model's attention. The final model is deployed on a VPS through FastAPI REST API and integrated into a Flutter mobile application.

---

## ✨ Key Features

- Automatic detection of anterior eye diseases
- YOLOV12 object detection framework
- Comparison of CBAM and ECA attention mechanisms
- Image preprocessing using CLAHE and Unsharp Masking
- Data augmentation with Albumentations
- Smooth balancing for class distribution
- Explainable AI using Grad-CAM
- FastAPI REST API deployment
- Flutter mobile application integration
- Real-time inference

---

## 🎯 Key Contributions

- Developed an automatic anterior eye disease detection framework based on YOLOV12.
- Compared the performance of CBAM and ECA attention mechanisms.
- Designed a complete preprocessing pipeline consisting of image quality verification, enhancement, augmentation, and balancing.
- Improved model interpretability using Grad-CAM visualization.
- Successfully deployed the model on VPS and integrated it with a Flutter mobile application.

---

# 🏗 Project Architecture / Research Workflow

<p align="center">
<img src="docs/architecture.png" width="900">
</p>

The overall workflow consists of:

1. Business Understanding
2. Data Understanding
3. Data Preparation
4. Modeling (YOLOV12 + CBAM / YOLOV12 + ECA)
5. Evaluation
6. Deployment

---

# 🚀 Installation

## Requirements

- Python 3.11
- CUDA 11.8
- PyTorch
- Ultralytics YOLO
- OpenCV
- Albumentations
- FastAPI
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

The dataset consists of **2,298 anterior eye images** with five disease categories.

| Class |
|-------|
| Cataract |
| Conjunctivitis |
| Eyelid |
| Normal |
| Uveitis |

Image preprocessing includes:

- Blur Quality Verification
- Duplicate Verification
- CLAHE
- Unsharp Masking
- Data Augmentation
- Smooth Balancing
- Dataset Splitting

Dataset format:

```
dataset/
│
├── train/
├── valid/
└── test/
```

---

# 🏋 Training

Training configuration:

| Parameter | Value |
|------------|---------|
| Epoch | 40 |
| Batch Size | 12 |
| Image Size | 512 × 512 |
| Optimizer | AdamW |
| Scheduler | Cosine Learning Rate |
| Warmup Epoch | 3 |

Training command

```bash
python train.py
```

or execute the notebook:

```
notebooks/02_training.ipynb
```

---

# 📊 Results

Performance comparison

| Model | mAP50 | Precision | Recall | F1-score |
|--------|--------|-----------|---------|-----------|
| YOLOV12 + CBAM | **0.917** | **0.916** | **0.857** | **0.886** |
| YOLOV12 + ECA | 0.884 | - | - | 0.860 |

Evaluation includes:

- Precision Curve
- Recall Curve
- F1 Curve
- Precision-Recall Curve
- Confusion Matrix
- Grad-CAM Visualization

---

# 📁 Project Structure

```
Anterior-Eye-Disease-Detection
│
├── dataset/
├── notebooks/
├── preprocessing/
├── deployment/
├── models/
├── docs/
├── results/
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

- **Big Data Laboratory**
- **Information Systems Study Program**
- **Faculty of Engineering and Informatics**
- **Universitas Multimedia Nusantara**

Special thanks to:

- Ultralytics
- Kaggle Dataset Provider
- OpenCV Community

---

# 📧 Contact

**Author**

Nurfajriah Oktaviani

Universitas Multimedia Nusantara

GitHub:
https://github.com/NurfajriahOktaviani

---

# 📜 License

This project is released under the MIT License.
