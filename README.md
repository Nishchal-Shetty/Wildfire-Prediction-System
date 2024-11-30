# Integrated Wildfire Risk Prediction and Monitoring System

Welcome to the **Integrated Wildfire Risk Prediction and Monitoring System** repository! This project integrates multi-source datasets and employs advanced machine learning techniques to predict wildfire risks and monitor occurrences effectively.

---

## 🚀 Project Overview
This project focuses on building a comprehensive wildfire risk prediction and monitoring system by leveraging data from NASA FIRMS and OpenMeteo. The system is designed to process diverse data, extract meaningful patterns, and predict wildfire risks with high accuracy. 

### Key Features:
- Unified data lake combining wildfire and weather datasets.
- Advanced exploratory data analysis (EDA) to extract spatial-temporal insights.
- Machine learning pipeline using XGBoost with hyperparameter optimization for high prediction accuracy.
- Visualization tools for better understanding wildfire trends and intensities.

---

## 📊 Datasets Used

### 1. **NASA FIRMS (Fire Information for Resource Management System)**
   - **Attributes**:
     - Latitude/Longitude (Numeric)
     - Detection Time/Date (Date/Time)
     - Fire Radiative Power (Numeric)
     - Confidence Level (Categorical/Numeric, standardized to low/nominal/high)
     - Satellite and Land Cover Information
   - **Details**:
     - Real-time global fire data within 3 hours of satellite detection.

### 2. **OpenMeteo Weather Data**
   - **Attributes**:
     - Temperature, Dew Point, Wind Speed/Direction, Pressure, Air Quality (Numeric)
     - Timestamp (Temporal)
   - **Details**:
     - Open-source, high-resolution weather data with 80 years of historical records.

---

## 🔍 Data Processing and Visualization

### **Dataset Consolidation:**
- Unified FIRMS and weather data, addressing inconsistencies and aligning timestamps.
- Standardized confidence values for better interpretability.

### **Exploratory Data Analysis (EDA):**
- Fire activity and intensity mapping across Australia.
- Seasonal and yearly wildfire frequency trends using bar charts.
- Correlation analysis between fire presence and weather attributes.

### **Visualization Highlights:**
- Heatmaps for spatial fire distribution.
- Temporal trend analysis using line graphs and pair plots.

---

## 🤖 Machine Learning Pipeline

### **Modeling Approach:**
- Preprocessed and scaled features for uniformity.
- Built and optimized an XGBoost classifier to predict wildfire risks.

### **Model Performance:**
- **Baseline Accuracy:** 74.83%
- **Optimized Accuracy:** 80.33%
- **Precision:** 76.98%  
- **Recall:** 86.60%  
- **F1 Score:** 81.51%

### **Key Insights:**
- Fires are more likely when:
  - Temperature > 30°C
  - Relative Humidity > 50%
  - Precipitation ≈ 0 mm

### **Feature Importance:**
- Evapotranspiration, soil temperature, relative humidity, and wind speed were the most impactful factors.

---

## 📈 How to Use This Repository

### Prerequisites:
- Python 3.8+
- Libraries: `numpy`, `pandas`, `matplotlib`, `seaborn`, `scikit-learn`, `xgboost`, `bayesian-optimization`

### Steps:
1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/wildfire-risk-prediction.git
   cd wildfire-risk-prediction
