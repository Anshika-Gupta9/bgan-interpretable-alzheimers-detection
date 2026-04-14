# Biomarker-Guided Attention Network (BGAN) for Alzheimer’s Disease Detection

 A deep learning + explainable AI (XAI) project for early detection and classification of Alzheimer’s Disease using MRI scans.
## Live Project Website  
🔗 https://anshika-gupta9.github.io/bgan-interpretable-alzheimers-detection/
---

## Overview
Alzheimer’s Disease (AD) is a progressive neurodegenerative disorder affecting millions worldwide. Early detection is critical but challenging due to subtle structural brain changes.

This project proposes a **Biomarker-Guided Attention Network (BGAN)** that:
- Improves interpretability of deep learning models  
- Aligns model attention with clinically relevant brain regions  
- Balances accuracy and medical reliability  

---

## Key Idea
Traditional CNNs act as black boxes.

BGAN introduces:
- Biomarker Prior Knowledge  
- Attention Mechanisms (SE + CBAM)  
- Explainability Metric (BAS)  

This ensures the model focuses on actual Alzheimer’s-affected regions (hippocampus, ventricles, etc.)

---

## Dataset

- Alzheimer’s MRI Multiclass Dataset (Kaggle)  
- 44,000 images  
- 4 classes:
  - Non-Demented  
  - Very Mild Demented  
  - Mild Demented  
  - Moderate Demented  

### Preprocessing

- MD5 duplicate removal  
- Perceptual hash clustering  
- Group-level train/val/test split (**no data leakage**)  
- Data augmentation (flip, rotation, crop, jitter)  

---

## Models Used

- DenseNet121  
- ResNet50  
- VGG16  
- **Proposed: BGAN**  

---

## Results

| Model        | Accuracy | F1 Score | AUC   | BAS (Interpretability) |
|-------------|---------|---------|------|------------------------|
| DenseNet121 | 91.49%  | 0.925   | 0.987 | 1.37 |
| ResNet50    | 99.22%* | 0.993   | 0.999 | 3.95 |
| VGG16       | 94.14%  | 0.949   | 0.994 | 0.00 |
| **BGAN**    | 90.81%  | 0.918   | 0.986 | **11.58** ✅ |

*BGAN achieves the best interpretability while maintaining competitive accuracy.*

---

## Biomarker Alignment Score (BAS)

A novel metric proposed in this project:

- BAS > 1 → Good alignment  
- Higher BAS → More medically meaningful model  

---

## Key Contributions

- ✅ Biomarker-guided attention mechanism  
- ✅ Learnable blending of prior + learned attention  
- ✅ Composite loss for alignment  
- ✅ Novel interpretability metric (BAS)  
- ✅ Leak-free dataset splitting strategy  

---

## 🛠️ Tech Stack

- Python  
- PyTorch  
- NumPy, Pandas  
- OpenCV  
- Matplotlib / Seaborn  
- Google Colab (GPU: Tesla T4)  

---


