


\



# Stroke Risk Prediction System

## 🚀 Project Highlights

- **ML Model:** Includes a fully trained **XGBoost** model for stroke risk prediction.  
- **Data Type:** Works with **tabular health data** (~35,000 patient records, clinical and behavioral features).  
- **Preprocessing:** Comprehensive preprocessing and feature engineering completed:
  - Categorical encoding
  - Outlier detection and removal
  - Feature scaling and selection
  - Handling class imbalance  
- **Prediction:** Predicts whether a patient is **“At Risk”** or **“Not at Risk”** of stroke.  
- **Goal:** Assist healthcare providers with **early detection**, prioritization of high-risk patients, and data-driven decision-making.  

---

## 1. Introduction

Stroke is a critical medical emergency and a leading cause of death and long-term disability worldwide. It occurs when blood flow to part of the brain is interrupted or significantly reduced, preventing brain cells from receiving oxygen and nutrients. Early detection of stroke risk can save lives and improve recovery outcomes.

Traditional diagnosis often requires clinical evaluations, lab tests, and imaging, which can be time-consuming, expensive, or unavailable in resource-limited settings. With advancements in **Artificial Intelligence (AI)** and **Machine Learning (ML)**, automated systems can now assist healthcare professionals in identifying individuals at high risk of stroke.

**Objective:**  
Develop a Machine Learning-based system that predicts whether a patient is **“At Risk”** or **“Not at Risk”** of stroke using health-related tabular data.

---

## 2. Problem Statement

Stroke risk identification is challenging due to complex interactions between physiological, lifestyle, and psychological factors (e.g., blood pressure, irregular heartbeat, anxiety, fatigue, sleep apnea). Manual assessment is prone to human error and lacks scalability.

**Goal:**  
Create a supervised ML model that accurately predicts stroke risk based on measurable attributes such as age, blood pressure, chest pain, irregular heartbeat, fatigue, anxiety, and other medical indicators.

---

## 3. Dataset Description

The **Stroke Risk Prediction Dataset** contains ~35,000 patient records with clinical, behavioral, and demographic features.  

**Target variable:** `at_risk` (binary: Yes = At Risk, No = Not at Risk)

| Attribute | Description |
|-----------|-------------|
| age | Age of the patient |
| gender | Male/Female |
| chest_pain | Presence of chest pain (Yes/No) |
| high_blood_pressure | Indicates high blood pressure |
| irregular_heartbeat | Abnormal heart rhythm |
| shortness_of_breath | Difficulty in breathing |
| fatigue_weakness | General fatigue or muscle weakness |
| dizziness | Feeling lightheaded or dizzy |
| swelling_edema | Swelling in body parts |
| neck_jaw_pain | Pain in neck or jaw region |
| excessive_sweating | Unusual sweating patterns |
| persistent_cough | Long-lasting cough |
| nausea_vomiting | Nausea or vomiting |
| chest_discomfort | Chest tightness or pressure |
| cold_hands_feet | Poor blood circulation symptoms |
| snoring_sleep_apnea | Sleep-related breathing disorder |
| anxiety_doom | Anxiety, fear, or stress-related symptoms |
| stroke_risk_percentage | Quantitative stroke risk level (0–100%) |
| at_risk | Target variable: Yes/No |

**Data Composition:**  
- Numerical & categorical features  
- Binary classification problem  

---

## 4. Preprocessing & Exploratory Data Analysis (EDA)

Key preprocessing steps completed by me:  

1. Encoding categorical variables  
2. Outlier detection and removal  
3. Feature engineering  
4. Feature scaling (StandardScaler)  
5. Feature selection  
6. Handling class imbalance (Random UnderSampling)  

This ensures the dataset is clean, balanced, and ready for robust ML modeling.

---

## 5. Model Design & Implementation

**Algorithms Tested:**  
- Support Vector Machines (SVM)  
- Logistic Regression (LR)  
- **XGBoost (Tuned)** ✅  
- Random Forest (RF)  
- K-Nearest Neighbors (KNN)  
- Decision Tree  

**Hyperparameter Tuning:** GridSearchCV / RandomizedSearchCV focusing on maximizing F1-score and Recall due to class imbalance.

**Final Model:**  
- **XGBoost (Tuned)**: Best overall performance across Accuracy, Recall, F1 Score, and ROC-AUC  
- Provides strong predictive power for stroke risk with tabular patient data.

---

## 6. Sample Model Performance (Tuned)

| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|-------|---------|----------|--------|----------|---------|
| XGBoost | 0.9360 | 0.8997 | 0.9298 | 0.9145 | 0.9857 |


### Sample Other Model Performance (Tuned)



| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC |

|-------|---------|----------|--------|----------|---------|

| SVM | 0.9309 | 0.8872 | 0.9305 | 0.9083 | 0.9844 |

| Logistic Regression | 0.9224 | 0.8723 | 0.9247 | 0.8977 | 0.9825 |

| Random Forest | 0.9354 | 0.8966 | 0.9321 | 0.9140 | 0.9854 |

| KNN | 0.8657 | 0.7426 | 0.9720 | 0.8420 | 0.9384 |

| Decision Tree | 0.9306 | 0.8950 | 0.9193 | 0.9780 | 0.9780 |

---

## 7. Ethical Considerations & Bias Mitigation

- High **Recall** to minimize false negatives for patient safety.  
- **Data privacy** ensured; no PII used.  
- **Class imbalance** handled with Random UnderSampling.  
- **Feature scaling and encoding** prevent algorithmic bias.  
- Transparent models like Logistic Regression & Decision Tree used for explainability alongside XGBoost.

---







