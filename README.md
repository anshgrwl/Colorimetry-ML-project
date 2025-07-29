# Colorimetry-ML-project
# Copper Ion Concentration Classification Using Machine Learning

This project presents a machine learning-based system for classifying copper ion concentrations in water using dual-mode biosensor images (colorimetric and fluorometric). The system supports real-time water quality assessment and risk-level categorization, integrated with a Flask-based web application for user interaction.

## 🧪 Problem Statement

Copper, while an essential micronutrient, becomes toxic at high concentrations and poses a serious threat to public health, especially in mining regions or areas with aging infrastructure. Existing detection methods are expensive, lab-bound, and not field-deployable. This project aims to automate copper ion concentration detection using low-cost optical biosensors and machine learning.

## 🧠 ML-Based Solution Overview

- **Input**: Images of biosensors exposed to various Cu²⁺ concentrations
- **Output**: Classified water quality level based on copper concentration
- **Modes**:
  - Colorimetric (visible light)
  - Fluorometric (UV light)

## 💻 Features

- RGB-based image classification
- Multiple ML models (SVM, Logistic Regression, XGBoost, Random Forest, etc.)
- 6-fold cross-validation with metrics: Accuracy, Precision, Recall, F1-score, Specificity
- Flask-based web app for:
  - User authentication
  - Uploading images
  - Displaying results
  - Risk level visualization
  - Historical data tracking

## 🔬 Methodology

### 📊 Dataset
- 6 base copper concentrations: 0, 20, 50, 100, 200, 500 µM
- Interpolated to generate 501 levels (0–500 µM)
- Image augmentation: rotation, flipping, brightness, cropping
- Total: **5010 images per modality**

### 🎯 Risk Categories

| Risk Level              | Copper (µM) |
|-------------------------|-------------|
| Safe                    | 0–19        |
| Slightly Contaminated   | 20–39       |
| Moderately Contaminated | 40–59       |
| Unsafe                  | 60–99       |
| Heavily Contaminated    | 100–500     |

### 🛠️ ML Models Used
- Logistic Regression
- Support Vector Machine (SVM)
- Random Forest
- XGBoost
- Decision Tree
- K-Nearest Neighbors
- Naive Bayes
- Neural Network (MLP)

### 🧪 Evaluation Metrics
- Accuracy
- Precision
- Recall (Sensitivity)
- Specificity
- F1-Score

### 🏆 Best Model
**SVM** on **fluorometric images**:
- Accuracy: 96.77%
- Precision: 97.15%
- Recall: 97.00%
- Specificity: 99.88%

## 🌐 Web Application Overview

| Feature                  | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| User Authentication      | Sign-up, Login, Session Handling                                            |
| Sample Upload            | Upload biosensor image for analysis                                         |
| ML Integration           | Real-time prediction using pretrained SVM model                             |
| Visualization            | Risk gauge, risk level badges                                               |
| History Dashboard        | View all past analyses with timestamps and results                          |
