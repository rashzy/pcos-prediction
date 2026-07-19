# pcos-prediction

# PCOS Prediction Using Machine Learning: An India Focus



A comprehensive, deployment-ready machine learning framework engineered to address the critical **PCOS diagnostic crisis in India**, where up to **70% of cases remain undiagnosed** and patients face an average **18-month diagnostic delay**. 

This project transitions diagnostics from resource-heavy ultrasound reliance to clinical, metabolic, and lifestyle pattern recognition, aligning with the **SAHI Framework (March 2026)** and the **Ayushman Bharat Digital Mission (ABDM)** ecosystem for equitable rural and urban deployment.

---

##  Table of Contents
* [The Problem & India Context](#-the-problem--india-context)
* [Dataset Structure](#-dataset-structure)
* [Model Training & Performance](#-model-training--performance)


---

##  The Problem & India Context

* **The Epidemic Trajectory:** India records the highest PCOS prevalence among South Asian countries ($269.8$ per $100,000$), with a Total Percentage Change (TPC) of **+86.9%**.
* **The Diagnostic Odyssey:** Traditional Rotterdam criteria face structural barriers in India: strict specialist shortages ($1$ gynecologist per $15,000$ women), high ultrasound dependency in infrastructure-starved rural zones, and profound societal stigmas.
* **Systemic Metabolic Burden:** Clinical data reveals that among Indian women with PCOS, **91.9% present with dyslipidemia**, **43.2% with obesity**, and **37.5% with metabolic syndrome**. It is fundamentally a systemic metabolic crisis, not merely a reproductive condition.

* 1. **Data Collection & Cleaning:** Ingests $541$ patient profiles encompassing $45$ distinct clinical, hormonal, physical, and lifestyle features.
2. **Feature Engineering:** Automated BMI/WHR parsing, categorical encoding, standard scaling, and feature selection utilizing Random Forest Importance and SHAP values.
3. **Predictive Modeling:** Stratified $k$-fold cross-validation across Random Forest, SVM, Gradient Boosting, and Logistic Regression.
4. **Edge Deployment Target:** Low-footprint screening scripts optimized for deployment at Primary Health Centres (PHCs) and integrated with ASHA worker workflows.

---

##  Dataset Structure

The model ingests 45 feature vectors categorized across four key domains:

| Category | Targeted Parameters |
| :--- | :--- |
| **Clinical & Cycle** | Age, BMI, Blood Pressure, Pulse Rate, Cycle Length, Cycle Regularity |
| **Hormonal Profiles** | FSH, LH, TSH, AMH, PRL, Vitamin D3, PRG, $\beta$-HCG |
| **Physical/Ultrasound** | Hip/Waist ratio, Follicle Numbers (Inf/Sup), Endometrium thickness |
| **Lifestyle & Dermatological** | Weight gain, Hirsutism, Skin darkening, Hair loss, Fast food intake |

1. **Data Collection & Cleaning:** Ingests 541 patient profiles encompassing 45 distinct clinical, hormonal, physical, and lifestyle features[cite: 1].
2. **Feature Engineering:** Automated BMI/WHR parsing, categorical encoding, standard scaling, and feature selection utilizing Random Forest Importance and SHAP values[cite: 1].
3. **Predictive Modeling:** Stratified $k$-fold cross-validation across Random Forest, SVM, Gradient Boosting, and Logistic Regression[cite: 1].
4. **Edge Deployment Target:** Low-footprint screening scripts optimized for deployment at Primary Health Centres (PHCs) and integrated with ASHA worker workflows[cite: 1].

---


---

##  Model Training & Performance

The core architecture prioritizes **Sensitivity (Recall)** alongside overall Accuracy to minimize false negatives in critical early-stage evaluations[cite: 1].

* **Random Forest Baseline Accuracy:** **88.07%**[cite: 1]
* **Target Clinical Sensitivity:** **>85%** using non-ultrasound, lifestyle-centric features alone[cite: 1].

> ⚠️ **Implication for ML Engineering:** Urban vs. Rural metabolic profiles vary heavily in India (e.g., varying inflammatory markers and localized insulin resistance profiles)[cite: 1]. Models must be deployed with multi-site calibration weights to eliminate demographic or regional bias[cite: 1].
