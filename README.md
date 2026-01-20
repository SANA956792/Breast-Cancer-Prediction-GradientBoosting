# Breast Cancer Classification with Gradient Boosting

## 📌 Project Overview
This project implements a **Gradient Boosting Classifier** for breast cancer diagnosis using the Wisconsin Breast Cancer dataset. The model predicts whether a tumor is **Malignant (0)** or **Benign (1)** based on 30 numerical features extracted from cell nuclei measurements.

## 📊 Dataset
- **Source**: `sklearn.datasets.load_breast_cancer()`
- **Samples**: 569 instances
- **Features**: 30 numerical features (mean, error, and worst values for 10 characteristics)
- **Target**: Binary (0 = Malignant, 1 = Benign)
- **Data Quality**: No missing values, no duplicates

## 🏗️ Model Architecture
- **Algorithm**: GradientBoostingClassifier
- **Hyperparameters**:
  - `n_estimators`: 200
  - `learning_rate`: 0.05
  - `max_depth`: 3
  - `subsample`: 0.8
  - `min_samples_leaf`: 10
  - `random_state`: 42

## 📈 Performance Metrics
| Metric | Score |
|--------|-------|
| **Accuracy** | 96.49% |
| **Precision** | 95.89% |
| **Recall** | 98.59% |
| **F1-Score** | 97.22% |

## 🚀 Deployment
The model is deployed as an interactive web application using **Gradio** with the following features:

### Input Interface
- **30 Input Fields**: Accepts all 30 feature values from the dataset
- **Real-time Prediction**: Instant classification results
- **Probability Display**: Shows confidence scores for both classes

### Output Features
- **Prediction Label**: "Malignant" or "Benign"
- **Probability Scores**: Malignant and Benign probabilities

### Launch Instructions
```bash
# Run the Gradio interface
inter.launch()
