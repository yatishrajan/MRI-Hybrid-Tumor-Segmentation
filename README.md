# MRI-Hybrid-Tumor-Segmentation

### 🧠 Project Overview
This project focuses on the precise segmentation of brain tumors in **Lower-Grade Glioma (LGG) MRI slices**. 

The core innovation is a **Hybrid Framework** that evaluates:
1. **Baseline Model:** A standard U-Net architecture.
2. **Heatmap-guided Model:** A U-Net that uses VAE-generated **Anomaly Heatmaps** as spatial priors to guide the segmentation process.

### 📊 Performance Results
The following metrics represent the mean scores and standard deviation across the test dataset:

| Metric | Baseline | Heatmap-guided |
| :--- | :--- | :--- |
| **Dice Score** | 0.7940 ± 0.21 | 0.7717 ± 0.25 |
| **IoU Score** | 0.7010 ± 0.23 | 0.6825 ± 0.26 |

### 🚀 Technical Insights
* **High Performance:** Both models achieved Dice scores near 0.80, indicating high overlap with ground-truth masks.
* **Architecture:** Implemented in PyTorch using the LGG Segmentation Dataset.
* **Compute:** Trained using NVIDIA GPU acceleration on Kaggle.

### 📁 Repository Structure
* `VAE_notebook.ipynb`: Anomaly detection and heatmap generation.
* `UNet_notebook.ipynb`: Comparative segmentation training and evaluation.
