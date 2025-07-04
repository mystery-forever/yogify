# Yoga-82 Pose Classification

This repository provides a complete pipeline to download, process, and train classification models on the **Yoga-82 dataset**. It includes utilities for building both a **mini dataset** (15 selected poses) and a **full dataset** (82 poses), along with corresponding TensorFlow models.

---

## 📁 Repository Structure
Yoga-82/  
├── yoga_dataset_links/ # Contains .txt files with URLs for each pose  
│ ├── Bakasana.txt  
│ ├── Tadasana.txt  
│ └── ... (total 82 poses)  
├── script_dataset.py # Downloads and organizes the full Yoga-82 dataset  
├── script_mini_dataset.py # Filters out only 15 selected poses into a mini dataset  
├── mini_model.ipynb # TensorFlow model for 15-pose classification  
├── model.ipynb # TensorFlow model for full 82-pose classification  
├── Main_Dataset/ # Downloaded images organized by pose name  
├── Main_Dataset_extra/ # Automatically created to store unused pose folders  

