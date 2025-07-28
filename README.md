# 🏥 Clinical Data Dashboard – Patient Risk Stratification

## Overview

This project presents a structured health data analysis workflow designed to assess patient risk based on vital signs and demographic information.  
Using real-world-inspired clinical datasets (`patients.csv` and `vitals.csv`), we perform data preprocessing, exploratory analysis, and unsupervised learning to identify patient profiles that may require medical attention.

The analysis simulates part of what a health informatics system or clinical decision support tool would perform in a hospital or primary care environment.

---

## Methodology

### Preprocessing
- Merging of `patients` and `vitals` data based on `patient_id`
- BMI computation using weight and height
- Detection of hypertensive cases based on systolic and diastolic thresholds

### Exploratory Analysis
- Correlation matrix across key vitals (`bp`, `spo2`, `bmi`, `glucose`, etc.)
- Heatmap visualization to highlight potential relationships

### Clustering (K-Means)
- Patient grouping using:
  - Age
  - BMI
  - Systolic Blood Pressure
  - Glucose
- 3 clusters identified (interpreted as low, medium, and high risk)
- Visual comparison via scatterplots

### Risk Scoring
- Custom rule-based `risk_score` assigned based on thresholds:
  - High BP, BMI > 30, glucose > 126, age > 65
- Patients with `risk_score >= 2` flagged as high-risk

---

## Key Visuals
- BMI vs Systolic BP scatterplot with K-Means clusters
- Correlation heatmap of vitals and BMI
- Distribution of risk scores across the patient population

---

## Technologies Used

- Python 3.x
- Pandas, Seaborn, Matplotlib
- Scikit-learn (for clustering)
- Jupyter Notebook

---

## 👤 Author

**Evmorfia Anastasiou**  
BSc Computer Science | HealthTech Enthusiast  
*Exploring the intersection of data, technology, and human health.*
