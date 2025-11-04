# 🧠 Stroke Risk Prediction System

A Machine Learning–based system designed to predict whether a patient is **“At Risk”** or **“Not at Risk”** of stroke using health-related tabular data.

---

## 🚀 Project Highlights

- 🧩 **Model:** Tuned **XGBoost** model for stroke risk prediction  
- 📊 **Data Type:** Tabular health data (~35,000 patient records with clinical and behavioral features)  
- ⚙️ **Preprocessing:** Comprehensive data cleaning and feature engineering, including:
  - Categorical encoding  
  - Outlier detection and removal  
  - Feature scaling and selection  
  - Handling class imbalance  
- 🩺 **Prediction:** Binary classification — *At Risk* / *Not at Risk*  
- 🎯 **Goal:** Support healthcare professionals in **early detection**, **prioritization**, and **data-driven decision-making**  

---

## 🩸 1. Introduction

Stroke is a critical medical emergency and one of the leading causes of death and long-term disability worldwide. It occurs when blood flow to the brain is disrupted, depriving cells of oxygen and nutrients. Early detection of stroke risk is vital to prevent severe outcomes.

Traditional diagnosis methods (clinical tests, imaging, etc.) can be costly and time-consuming. With **AI and ML**, it’s now possible to predict stroke risk using patient data efficiently.

**Objective:**  
Build a machine learning model that accurately classifies patients as **“At Risk”** or **“Not at Risk”** based on measurable health attributes.

---

## ❓ 2. Problem Statement

Stroke risk is influenced by a combination of physiological, behavioral, and psychological factors such as:
- Blood pressure  
- Irregular heartbeat  
- Fatigue  
- Anxiety  
- Sleep apnea  

Manual assessments can be inconsistent and non-scalable. Therefore, this project aims to create a **supervised ML model** that automates and improves stroke risk prediction accuracy.

---

## 📂 3. Dataset Description

The **Stroke Risk Prediction Dataset** contains ~35,000 records, capturing clinical, behavioral, and demographic factors.

**Target Variable:**  
`at_risk` → **Yes = At Risk**, **No = Not at Risk**

| Attribute | Description |
|------------|-------------|
| age | Age of the patient |
| gender | Male/Female |
| chest_pain | Presence of chest pain (Yes/No) |
| high_blood_pressure | Indicates elevated blood pressure |
| irregular_heartbeat | Abnormal heart rhythm |
| shortness_of_breath | Difficulty in breathing |
| fatigue_weakness | General fatigue or muscle weakness |
| dizziness | Feeling lightheaded or dizzy |
| swelling_edema | Swelling in body parts |
| neck_jaw_pain | Pain in neck or jaw |
| excessive_sweating | Unusual sweating patterns |
| persistent_cough | Long-lasting cough |
| nausea_vomiting | Nausea or vomiting |
| chest_discomfort | Chest tightness or pressure |
| cold_hands_feet | Poor blood circulation |
| snoring_sleep_apnea | Sleep-related breathing disorder |
| anxiety_doom | Anxiety, fear, or stress-related symptoms |
| stroke_risk_percentage | Quantitative stroke risk (0–100%) |
| at_risk | Target variable: Yes/No |

**Data Type:**  
- Numerical and categorical features  
- Binary classification problem  

---

## 🔍 4. Preprocessing & Exploratory Data Analysis (EDA)

Key preprocessing steps performed:

1. Encoding categorical variables  
2. Outlier detection and removal  
3. Feature engineering  
4. Feature scaling using `StandardScaler`  
5. Feature selection  
6. Handling class imbalance with **Random UnderSampling**

These steps ensured a **clean, balanced, and high-quality** dataset for robust model training.

---

## ⚙️ 5. Model Design & Implementation

**Algorithms Evaluated:**
- Support Vector Machine (SVM)  
- Logistic Regression (LR)  
- **XGBoost (Tuned)** ✅  
- Random Forest (RF)  
- K-Nearest Neighbors (KNN)  
- Decision Tree  

**Hyperparameter Tuning:**  
Used **GridSearchCV** and **RandomizedSearchCV**, optimizing primarily for **F1-score** and **Recall** due to class imbalance.

**Final Model:**  
- **XGBoost (Tuned)** achieved the highest performance across all major metrics.  
- Strong predictive power on tabular health data, making it ideal for stroke risk prediction.

---

## 📊 6. Model Performance (Tuned)

### 🏆 Best Model — XGBoost

| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|--------|-----------|------------|----------|------------|-----------|
| **XGBoost** | **0.9360** | **0.8997** | **0.9298** | **0.9145** | **0.9857** |

---

### ⚖️ Comparison — Other Tuned Models

| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|--------|-----------|------------|----------|------------|-----------|
| SVM | 0.9309 | 0.8872 | 0.9305 | 0.9083 | 0.9844 |
| Logistic Regression | 0.9224 | 0.8723 | 0.9247 | 0.8977 | 0.9825 |
| Random Forest | 0.9354 | 0.8966 | 0.9321 | 0.9140 | 0.9854 |
| KNN | 0.8657 | 0.7426 | 0.9720 | 0.8420 | 0.9384 |
| Decision Tree | 0.9306 | 0.8950 | 0.9193 | 0.8780 | 0.9780 |

---

### 📈 Insights

- 🥇 **Best Model:** XGBoost  
- 🥈 **Strong Alternatives:** Random Forest and SVM  
- ✅ **Observation:** XGBoost achieves the best balance between **precision** and **recall**, with the highest **ROC-AUC** value, indicating excellent discriminatory power.

---

## ⚖️ 7. Ethical Considerations & Bias Mitigation

- Focused on **high recall** to reduce false negatives (critical in healthcare).  
- Ensured **data privacy** — no personally identifiable information (PII) used.  
- Addressed **class imbalance** via under-sampling.  
- Applied **feature scaling and encoding** to avoid algorithmic bias.  
- Maintained **model transparency** using interpretable models (Logistic Regression, Decision Tree) alongside XGBoost.

---

## 🧠 8. Future Enhancements

- Integrate **real-time monitoring systems** in healthcare environments.  
- Implement **explainability tools** (e.g., SHAP, LIME) for feature interpretation.  
- Deploy as a **web or mobile application** for clinicians.  
- Expand dataset diversity for **fairness and generalization testing**.  

---

## 🧰 Tech Stack

| Category | Tools |
|-----------|-------|
| **Language** | Python 🐍 |
| **Libraries** | scikit-learn, XGBoost, pandas, numpy, seaborn, matplotlib |
| **Development** | Jupyter Notebook / Google Colab |
| **Version Control** | Git & GitHub |

---

## 📜 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**Sisuru Disnaka Samarathunga**  
📧 sisurudisnaka001.com  
🌐 [GitHub Profile](https://github.com/SisuruDisnaka)

---

> 💬 *"Empowering healthcare through intelligent, data-driven stroke risk prediction."*
