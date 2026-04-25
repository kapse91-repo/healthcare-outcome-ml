# Healthcare Outcome Prediction

## Project Overview
This project predicts **patient outcomes** (Recovered, Referred, Deceased) using a synthetic healthcare dataset containing demographic and clinical variables.

**Author:** Data Science Intern  
**Domain:** Healthcare  
**Task:** Multi-class Classification  
**Target Variable:** Outcome

---

## Dataset Description
The dataset contains 500 patient records with the following features:
- **Patient_ID**: Unique identifier
- **Age**: Patient age in years
- **Gender**: Male/Female
- **BMI**: Body Mass Index
- **Blood_Pressure**: Systolic/Diastolic reading
- **Cholesterol_Level**: Cholesterol measurement
- **Smoker**: Yes/No
- **Diabetic**: Yes/No
- **Diagnosis**: Medical condition (Diabetes, Hypertension, Flu, Pneumonia, Heart Disease)
- **Treatment_Cost**: Cost of treatment in rupees
- **Admission_Date & Discharge_Date**: Hospital stay dates
- **Outcome**: Recovered / Referred / Deceased

---

## Problem Statement
**Goal:** Predict the **Outcome** of a patient's hospital visit based on demographic and clinical features.

This is a **multi-class classification** problem with 3 classes: Recovered, Referred, Deceased.

---

## Features Engineered
- **Length_of_Stay**: Days between admission and discharge
- **Systolic_BP** and **Diastolic_BP**: Split from Blood_Pressure
- **Age_Group**: Young (<30), Middle (30-49), Senior (50-64), Elderly (65+)
- **High_Cost**: Flag for expensive treatments (above median)
- **High_BP**: Flag for high blood pressure (Systolic > 140 or Diastolic > 90)

---

## Models Used
1. **Logistic Regression** (baseline) - Accuracy: 39%, Macro F1: 37.5%
2. **Random Forest** (tree-based ensemble) - Accuracy: 32%, Macro F1: 31%

**Best Model:** Logistic Regression

---

## Top Important Features
| Feature | Importance |
|---------|------------|
| BMI | 0.112 |
| Treatment_Cost | 0.110 |
| Cholesterol_Level | 0.101 |
| Age | 0.101 |
| Systolic_BP | 0.098 |
| Diastolic_BP | 0.098 |

---

## Files
- `Healthcare_Outcome_Prediction.ipynb` - Jupyter notebook with full code
- `requirements.txt` - Python dependencies
- `.gitignore` - Python gitignore

---

## How to Run
```bash
# Clone the repository
git clone https://github.com/kapse91-repo/healthcare-outcome-ml.git
cd healthcare-outcome-ml

# Install dependencies
pip install -r requirements.txt

# Run the notebook
jupyter notebook Healthcare_Outcome_Prediction.ipynb
```

---

## Limitations
- Dataset is synthetic and simplified
- No temporal or longitudinal patient history
- Limited external factors (no detailed lab values or medications)

---

## Future Improvements
- Hyperparameter tuning for Random Forest
- Try XGBoost, LightGBM, or neural networks
- Address class imbalance with SMOTE
- Add SHAP interpretability
- Use real-world healthcare data

---

## Colab Link
[Open in Google Colab](https://colab.research.google.com/drive/1DdGoZvj34eyab73HL7IvZ2eIjq5FQqae)
