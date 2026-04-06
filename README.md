# ICU Mortality Prediction System – Documentation (Dataset Included)

## 1. Project Overview

This project focuses on predicting ICU patient mortality using machine learning techniques. The model analyzes patient clinical data and predicts whether the patient will survive or not during their hospital stay.

The dataset used is **`icu_mortality_train.csv`**, which contains patient-level medical records collected from ICU settings.

---

## 2. Dataset Description

The dataset consists of multiple features related to ICU patients.

### Input Features (Independent Variables)

- **Demographic details:**
  - Age
  - Gender

- **Vital signs:**
  - Heart Rate
  - Blood Pressure
  - Temperature

- **Laboratory values:**
  - pH
  - PaCO2
  - PaO2

- Other clinical measurements

### Target Variable (Dependent Variable)

- **In-hospital_death**
  - `0` → Patient survived  
  - `1` → Patient died  

---

## 3. Idea of the Project

The main idea is to build a predictive healthcare system that:

- Takes patient medical data as input  
- Uses machine learning to analyze patterns  
- Predicts the risk of death in ICU  

This helps doctors make early decisions and improve patient care.

---

## 4. Use Case

This system can be used in:

- ICU monitoring systems  
- Hospital decision-support tools  
- Healthcare analytics platforms  

### Example Flow

1. Patient admitted to ICU  
2. Patient data entered into system  
3. Model predicts mortality risk  
4. Doctors take necessary action  

---

## 5. Approach

### Step 1: Data Loading
- Load dataset using `pandas`
- Inspect structure and columns  

### Step 2: Data Preprocessing
- Handle missing values:
  - Rows with missing values removed using `dropna()`
- Convert categorical data:
  - One-hot encoding using `get_dummies()`

### Step 3: Feature Selection
- `X` → All input features  
- `y` → Target column (`In-hospital_death`)  

### Step 4: Train-Test Split
- 80% training data  
- 20% testing data  

### Step 5: Model Building
- Algorithm used: **Random Forest Classifier**

**Reason:**
- Works well with structured data  
- Handles multiple features efficiently  
- Reduces overfitting  

### Step 6: Model Training
- Fit model on training dataset  

### Step 7: Prediction
- Predict on test data  
- Predict on new patient input  

---

## 6. Solution

### System Workflow

1. Input patient data  
2. Preprocess data  
3. Pass to trained model  
4. Output prediction:
   - `0` → Survival  
   - `1` → Death  

### Handling New Data

- Align features using `reindex()`  
- Apply same preprocessing steps  

---

## 7. Python Modules Used

- `pandas` → Data handling  
- `numpy` → Numerical operations  
- `sklearn.model_selection` → Train-test split  
- `sklearn.ensemble` → Random Forest  
- `sklearn.preprocessing` → Encoding  
- `sklearn.metrics` → Evaluation  

---

## 8. Model Evaluation

The model performance is measured using:

### 1. Accuracy
- Percentage of correct predictions  

### 2. Confusion Matrix
- Shows correct and incorrect predictions  

### 3. Classification Report

Includes:
- Precision  
- Recall  
- F1-score  

---

## 9. Conclusion

This project successfully demonstrates how machine learning can be applied in healthcare for ICU mortality prediction.

### Future Improvements

- Use advanced models (XGBoost, Neural Networks)  
- Improve missing value handling (imputation techniques)  
- Deploy as a web application  
- Integrate with hospital systems  

---
