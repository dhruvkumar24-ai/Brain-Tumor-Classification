# Brain Tumor Classification using CNN & Transfer Learning

## Overview
This project implements a brain tumor detection and classification system using Convolutional Neural Networks (CNN) and transfer learning techniques (VGG16, InceptionV3) on MRI scan images. The model classifies images into four categories: No Tumor, Meningioma, Glioma, and Pituitary Tumor.

## Features
- Custom CNN and fine-tuned pretrained models (VGG16, InceptionV3)
- Data augmentation, BatchNormalization, and Dropout for robust training
- Optimized with Adam optimizer
- Evaluation using ROC-AUC, precision, recall, and F1-score
- Achieved up to 90% accuracy with InceptionV3

## Dataset
- Source: [Kaggle - Brain Tumor MRI Dataset](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset)
- Four classes: No Tumor, Meningioma, Glioma, Pituitary Tumor

## Quick Start

1. **Clone the repository**
   ```powershell
   git clone https://github.com/dhruvkumar24-ai/Brain-Tumor-Classification.git
   ```

2. **Install dependencies**
   - Python 3.10+
   - Required packages: tensorflow, keras, scikit-learn, matplotlib, seaborn, Pillow, opencv-python, kagglehub

3. **Download the dataset**
   - The notebook automatically downloads the dataset using `kagglehub`.

4. **Run the notebook**
   - Open `notebooks/Brain_tumor_detection_using_CNN.ipynb` in VS Code or Jupyter.
   - Follow the instructions in the notebook cells.

## Training Speed Optimizations
- Adjustable image size and batch size for faster training
- Mixed precision training (if supported)
- Optimized data pipeline using `tf.data`
- Quick testing mode for rapid experimentation

## Results
- Custom CNN, VGG16, and InceptionV3 models compared
- InceptionV3 achieved highest accuracy (~90%)
- Detailed evaluation metrics provided in the notebook

## Project Structure
```
BRAIN-TUMOUR-CLASSIFICATION/
│
├── Brain_tumor_detection_using_CNN.ipynb
├── README.md
└── (Dataset downloaded automatically)
```

## Credits
- Developed by Dhruv Kumar Sahu
- Dataset by Masoud Nickparvar (Kaggle)

## License
This project is for educational purposes.

---

## 📊 Results & Evaluation

The models were evaluation based on accuracy, precision, and recall. **InceptionV3** emerged as the top performer due to its ability to capture multi-scale features in medical imagery.

| Model | Accuracy | Precision | Recall |
| :--- | :---: | :---: | :---: |
| **InceptionV3** | **90.2%** | **0.89** | **0.91** |
| VGG16 | 84.5% | 0.83 | 0.85 |
| Custom CNN | 76.0% | 0.74 | 0.72 |

> **Key Insight:** The use of Inception modules allowed the network to choose the optimal kernel size for feature extraction, which was critical for identifying the subtle textures of Glioma vs. Meningioma tumors.
![ROC-AUC Curve](images/"C:\Users\dhruv\OneDrive - IIT Kanpur\Pictures\Screenshots\Screenshot 2026-04-20 221014.png")
