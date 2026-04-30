# Crime Hotspot Prediction Using Python & Machine Learning (2024 Dataset)

This project performs crime analysis and next‑month hotspot prediction using the **London_Crimes_2024_Expanded** dataset. It applies Python‑based data science techniques to identify crime patterns, engineer lagged features, and build predictive models using Logistic Regression and Random Forest.

---

## 📌 Project Overview

- Analyses crime distribution across time, crime types, and LSOA regions  
- Aggregates data at **LSOA‑month** level  
- Creates **lagged features** to avoid data leakage  
- Defines hotspots using the **top 10% crime threshold**  
- Predicts **Hotspot Next Month** using ML models  
- Evaluates using:
  - Accuracy  
  - Precision  
  - Recall  
  - F1‑score  
  - Confusion matrices  

This project demonstrates structured reasoning, data cleaning, feature engineering, and predictive modelling for real‑world decision support.

---

## 🧠 Methodology

### **1. Data Cleaning**
- Removed missing or invalid entries  
- Standardised date formats  
- Filled missing outcome categories  
- Ensured required fields (crime type, LSOA, coordinates) were present  

### **2. Aggregation**
Data grouped by:


Generated:
- Total crime count  
- Crime‑type pivot table  
- Month‑to‑month ordering  

### **3. Hotspot Definition**
Hotspots = LSOA‑months in the **top 10%** of crime counts.

### **4. Lagged Features**
Created previous‑month:
- Crime counts  
- Crime‑type counts  
- Hotspot status  

This prevents leakage and simulates real prediction.

### **5. Modelling**
Models used:
- **Logistic Regression**
- **Random Forest Classifier**

Train/test split based on **time**, not random shuffle.

---

## 📊 Results Summary

### **Logistic Regression**
- Accuracy: **0.916**
- Precision: **0.577**
- Recall: **0.908**
- F1‑score: **0.706**

### **Random Forest**
- Accuracy: **0.939**
- Precision: **0.681**
- Recall: **0.850**
- F1‑score: **0.756**

Random Forest performed best due to non‑linear relationships in crime patterns.

---

## 📂 Repository Structure

---

## 📈 Visual Outputs

The **figures/** folder includes:
- Crime type distribution  
- Monthly crime trends  
- Spatial clustering  
- Confusion matrices  
- Feature importance  
- Model comparison table
- ## 📂 Figures

The `figures/` folder contains all visual outputs used in this project, including:

### 🔹 Top 10 Crime Types (Bar Chart)
![Top Crime Types](figures/top_crime_types.png)

### 🔹 Monthly Crime Trend (Line Chart)
![Monthly Crime Trend](figures/monthly_trend.png)

### 🔹 Spatial Distribution of Crime Incidents (Scatter Plot)
![Spatial Distribution](figures/spatial_distribution.png)

### 🔹 Top 10 LSOAs by Crime Count
![Top LSOAs](figures/top_lsoas.png)

### 🔹 Confusion Matrix – Logistic Regression
![Confusion Matrix Logistic Regression](figures/confusion_matrix_logreg.png)

### 🔹 Confusion Matrix – Random Forest
![Confusion Matrix Random Forest](figures/confusion_matrix_rf.png)

### 🔹 Top 10 Feature Importances – Random Forest
![Feature Importances](figures/feature_importance_rf.png)


---

## 📘 Full Report

The complete academic report is included in the **report/** folder, covering:
- Research questions  
- Stakeholder analysis  
- Data cleaning  
- Feature engineering  
- Modelling  
- Ethical considerations  
- Limitations  
[DataScience Assaignment 2.docx](https://github.com/user-attachments/files/27245011/DataScience.Assaignment.2.docx)

---

## 🔗 Google Colab Notebook

Add your Colab link here:
https://colab.research.google.com/drive/1BK3TsgQQ5m9_oOCCO9z0o3RfrotDEy5I?usp=sharing[DataScience Assaignment 2.docx](https://github.com/user-


---

## ⚖️ Ethical Considerations

- Predictive policing may reinforce historical bias  
- Crime data reflects police activity, not true crime  
- Models should support—not replace—human decision‑making  

---

## 👩‍💻 Author

**Samira Patel**  
BSc (Hons) Computer Science  
University of Central Lancashire (UCLan)
