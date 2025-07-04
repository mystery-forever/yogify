# Yoga-82 Pose Classification

This repository provides a complete pipeline to download, process, and train classification models on the **Yoga-82 dataset**. It includes utilities for building both a **mini dataset** (15 selected poses) and a **full dataset** (82 poses), along with corresponding TensorFlow models.

---

## 📁 Repository Structure
Yoga-82/  
├── yoga_dataset_links/ # Contains .txt files with URLs for each pose  
│ ├── Bakasana.txt  
│ ├── Tadasana.txt  
│ └── ... (total 82 poses)  
├── requirements.txt # Requirements for model  
├── script_dataset.py # Downloads and organizes the full Yoga-82 dataset  
├── script_mini_dataset.py # Filters out only 15 selected poses into a mini dataset  
├── mini_model.ipynb # TensorFlow model for 15-pose classification  
├── model.ipynb # TensorFlow model for full 82-pose classification  
├── Main_Dataset/ # Downloaded images organized by pose name  
├── Main_Dataset_extra/ # Automatically created to store unused pose folders  


---

## 🧾 Project Summary

| Component        | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| 📥 Data Download | Downloads images from provided URLs and organizes them into pose folders    |
| 🧹 Data Cleanup  | Deduplicates images using content hash and handles missing/broken links     |
| ✂️ Mini Dataset  | Retains only 15 essential yoga poses; others are moved to a separate folder |
| 🤖 Mini Model    | Light classification model suitable for small-scale training                |
| 🧠 Full Model    | Deep learning model trained on the complete Yoga-82 dataset                 |

---

## 🚀 Getting Started

### 1. Install Required Libraries

Install dependencies with:

```bash
pip install -r requirements.txt
```

### 2.  Download the Dataset

You can download and organize the Yoga-82 dataset using one of the following methods:

---

Use the `script_dataset.py` script to automatically download images from the URLs listed in `yoga_dataset_links/*.txt` files.

```bash
python script_dataset.py
```

### 3: Create a Mini Dataset (15 Poses)

To work with a smaller subset of poses (e.g., for lightweight models or faster experimentation), run:

```bash
python script_mini_dataset.py
```

###  4: Train the Model

You can now train classification models on the prepared dataset. Two options are available:

---
####  Option 1: Mini Model (15 Poses)

Open and run the notebook:

```bash
mini_model.ipynb
```
####  Option 2: Full Model (82 Poses)

Open and run the notebook:

```bash
model.ipynb
```

## 📊 Model Performance Metrics

Below are the training and validation metrics for both the **Full Model** (trained on 82 poses) and the **Mini Model** (trained on 15 poses).

---

### 🧠 Full Model – `model.ipynb`

| Metric                | Value     |
|-----------------------|-----------|
| ✅ Train Accuracy     | 71.67%    |
| 📉 Train Loss         | 1.3309    |
| 🧪 Validation Accuracy| 71.24%    |
| 📉 Validation Loss    | 1.3109    |

---

### ⚡ Mini Model – `mini_model.ipynb`

| Metric                | Value     |
|-----------------------|-----------|
| ✅ Train Accuracy     | 88.83%    |
| 📉 Train Loss         | 0.7853    |
| 🧪 Validation Accuracy| 90.43%    |
| 📉 Validation Loss    | 0.7151    |

---

> ℹ️ The mini model achieved higher accuracy due to fewer classes and more separation between pose categories. The full model can be improved using augmentation, regularization, or advanced architectures (e.g., MobileNet, EfficientNet).

