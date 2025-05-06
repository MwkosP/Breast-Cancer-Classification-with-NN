# 🩺 Breast Cancer Binary Classifiction Using Ultrasound Images

## 🎯 **Objective**  
The project aims at the Classification of breast cancer through the processing of ultrasound images into benign or malignant cases. The goal is to develop a reliable binary classification model that can identify diagnostic decisions.

## 📚 **Dataset**  
- **Name:** Breast Ultrasound Images Dataset  
- **Source:** Kaggle  
- **Description:** Contains ultrasound images labeled as:
  - Benign  
  - Malignant  
  - Normal  
- **Usage in this project:** Only benign and malignant categories were used for binary classification.

## 📊 **Exploratory Data Analysis (EDA)**  
- Mean Picture per class
- Heatmaps  
- Pixel value histograms  
- PCA (2D projection)

## ⚙️ **Preprocessing**  
- Dataset split: 80% training, 10% validation, 10% test  
- Image resizing to 224×224  
- Normalization to [0, 1] range  
- Data augmentation:
  - Horizontal/vertical flips  
  - Brightness and contrast adjustments  
  - Zooming  
  - Small rotations

## 🤖 **Models Used**  
- Custom Convolutional Neural Network (CNN)  
- VGG16 (pretrained on ImageNet)  
- ResNet50 (pretrained on ImageNet)

## 🧪 **Training & Evaluation**  
- **Cross-validation:** 3-fold cross-validation was used to ensure robust evaluation of each model.  
- **Early Stopping:** Training was monitored using `val_loss`, and the best model weights were saved automatically.  
- **Evaluation Metrics:**  
  - Accuracy  
  - Precision  
  - Recall  
  - F1-score  
  - Confusion Matrix
  - Loss Curves 

- **Metrics were calculated on the test set and individually for each fold** during k-fold cross-validation.

## 📈 **Visualizations Included:**  
- Training/validation **loss curves** for all models  
- Training/validation **accuracy curves**  
- **Confusion Matrix** visualized as a heatmap  
- **Classification Report** showing precision, recall, and F1-score per class

## 🏆 **Best Model:**  
- **VGG16 (Fine-Tuned)** achieved the best performance with:
  - **Accuracy:** 90.24%  
  - **Loss:** 0.2399  
- Although the custom CNN showed the largest relative improvement during fine-tuning, VGG16 outperformed all models in final evaluation.

## 📊 **Statistical Test (One-Way ANOVA):**  
To quantitatively assess performance differences between the three models, a one-way ANOVA test was conducted using accuracy scores from a 3-fold cross-validation.  
- **F-statistic:** 10.060  
- **p-value:** 0.0121  
- The low p-value suggests statistically significant differences between model performances.

## 🧑‍💻 Author

Created by Panagiotis Mokos  
GitHub: [@MwkosP](https://github.com/MwkosP)

