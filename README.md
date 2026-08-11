# 🩺 MultiFusion Breast Cancer Detection Framework

<div align="center">

**A Deep Learning Framework for Breast Cancer Image Classification Across Multiple Imaging Modalities**

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Key Features](#-key-features)
- [Datasets](#-datasets)
- [Methodology](#-methodology)
- [Experimental Results](#-experimental-results)
- [Application](#️-application)
- [Model Security & Deployment](#-model-security--deployment)
- [Project Structure](#-project-structure)
- [Live Deployment](#-live-deployment)
- [Limitations](#️-limitations)
- [Future Work](#-future-work)
- [Research](#-research)
- [Author](#️-author)
- [License](#-license)

---

## 📖 Overview

**MultiFusion Breast Cancer Detection Framework** is a deep learning-based framework for automated breast cancer image classification across multiple medical imaging modalities.

The framework combines **Self-Supervised Learning (SSL)** with **Swin Transformer-based feature learning** to explore robust visual representation learning in scenarios where large-scale annotated medical imaging data can be difficult and expensive to obtain.

The framework is evaluated across three diverse breast cancer imaging datasets:

- **BUSI** — Breast Ultrasound Images
- **BreakHis** — Breast Histopathology Images
- **INbreast** — Digital Mammography

By evaluating the framework across different imaging modalities, the project investigates the robustness and generalization of deep learning-based breast cancer classification beyond a single dataset or imaging modality.

> ⚠️ **Disclaimer:** This project is intended for educational and research purposes only. It is not a medical diagnostic system and should not be used for clinical decision-making.

---

## ✨ Key Features

- 🧠 **Self-Supervised Learning** using SimCLR
- 🔬 **Swin Transformer-based visual feature learning**
- 🩻 Support for multiple breast imaging modalities
- 📊 Evaluation across BUSI, BreakHis, and INbreast datasets
- 🔄 Focus on cross-dataset generalization
- 🖥️ Interactive Streamlit-based application
- 🔐 Private model-weight hosting using Hugging Face
- ⚡ Efficient inference using trained deep learning models
- 🌐 Cloud deployment through Streamlit Community Cloud

---

## 🗂️ Datasets

The framework was evaluated using three publicly available breast cancer imaging datasets representing different medical imaging modalities.

### 🩻 BUSI

**Breast Ultrasound Images Dataset**

- **Modality:** Ultrasound
- **Classes:** Benign, Malignant, Normal
- **Task:** Breast lesion classification

---

### 🔬 BreakHis

**Breast Cancer Histopathological Image Dataset**

- **Modality:** Histopathology
- **Classes:** Benign, Malignant
- **Task:** Breast cancer classification from histopathological images

---

### 🩺 INbreast

**INbreast Digital Mammography Dataset**

- **Modality:** Mammography
- **Task:** Breast cancer-related image analysis

---

The use of multiple datasets enables evaluation across substantially different imaging modalities and helps investigate the generalization of the proposed learning approach.

---

## 🧠 Methodology

The framework follows a learning pipeline combining self-supervised representation learning with transformer-based visual feature extraction.

### 1. Self-Supervised Representation Learning

The framework incorporates **SimCLR-based self-supervised learning** to learn meaningful visual representations from medical images without relying exclusively on manually annotated data during representation learning.

The learned representations are intended to capture useful visual characteristics that can subsequently support downstream classification.

### 2. Transformer-Based Feature Learning

**Swin Transformer** is utilized for hierarchical visual feature extraction.

The transformer-based representation learning stage enables the framework to capture both local and broader spatial characteristics present in breast medical images.

### 3. Classification

The learned visual representations are used for downstream classification across the supported breast imaging datasets.

### High-Level Pipeline

```text
Medical Images
       │
       ▼
Self-Supervised Representation Learning
       │
       ▼
Learned Visual Representations
       │
       ▼
Swin Transformer-based Feature Learning
       │
       ▼
Dataset-Specific Classification
       │
       ▼
Prediction