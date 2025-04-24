# 🚀 Excavate 2025 – Band Gap Prediction in Perovskite Oxides

🔗 **Live Demo**: [Click here to view the hosted application](https://excavate-2025-1.onrender.com/)

This project was developed for **Excavate 2025**, hosted by **IIT Kharagpur**, where our team **Krantikari Techies** tackled a materials informatics challenge using machine learning to predict and classify the **band gaps of perovskite oxides**.

---

## 🧩 Problem Statement

Participants were provided with a dataset of **5,152 perovskite compositions**, each with structural, atomic, and electronic features. The tasks were:

1. **Binary Classification (Model 1)**  
   - **Goal:** Classify each material as an **Insulator** or **Non-Insulator**  
   - **Criterion:**  
     - `Eg ≥ 0.5 eV` → **Insulator**  
     - `Eg < 0.5 eV` → **Non-Insulator**

2. **Regression (Model 2)**  
   - **Goal:** Predict the **exact band gap value (Eg in eV)**  
   - **Condition:** Only for materials classified as **insulators**

---

## ⚙️ Our Approach

### 🔹 Data Preprocessing
- Handled missing values and noise
- Removed outliers using IQR method
- One-hot encoded categorical features (like A, B, A', B')
- Normalized/standardized feature values

### 🔹 Feature Engineering
- Analyzed physical/electronic significance of each feature
- Focused on properties like electronegativity, atomic radius, and HOMO/LUMO energies

### 🔹 Modeling
- **Model 1 (Classification):**
  - XGBoost Classifier ✅ *(Best Performance)*
  - Decision Tree Classifier
- **Model 2 (Regression):**
  - XGBoost Regressor ✅ *(Best Performance)*
  - Random Forest Regressor

---

## 📈 Results

### 🟢 Classification (XGBoost Classifier)
- **Accuracy:** 92.8%
- **Insights:** High precision and recall in distinguishing insulators vs non-insulators

### 🔵 Regression (XGBoost Regressor)
- **MAE:** 0.2213  
- **MSE:** 0.1249  
- **R² Score:** 0.8206  
- **Inference:** The model effectively captured the nonlinear relationships between features and band gap values
