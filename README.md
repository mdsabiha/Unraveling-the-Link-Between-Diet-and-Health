# Capstone Project — Unraveling the Link Between Diet and Health (NHANES 2009–2020)

This repository contains the exported report of my capstone project:  
**`Capstone_Capstone1_Report.pdf`**

The project investigates how **dietary habits, physical activity, and body measures** influence chronic health outcomes such as **hypertension, cholesterol, diabetes, and inflammation**, using large-scale health survey data from the **National Health and Nutrition Examination Survey (NHANES)**.

---

## 📚 Data Source

- **Dataset**: National Health and Nutrition Examination Survey (**NHANES**) by the CDC.  
- **Period covered**: 2009–2020.  
- **Design**: Cross-sectional, nationally representative of the U.S. population.  
- **Modules used**:
  - **Demographics**: age, gender, ethnicity, socioeconomic factors.  
  - **Dietary intake**: 24-hour recall (Day 1 & Day 2).  
  - **Physical activity**: vigorous, moderate, walking/biking, sedentary minutes.  
  - **Body measures**: weight, height, BMI, waist circumference.  
  - **Clinical data**: blood pressure, cholesterol, fasting glucose, inflammation (CRP).  
  - **Questionnaires**: medical history, self-reported conditions.  

All raw NHANES `.XPT` files were processed into analysis-ready datasets.

---

## 🔬 Methodology

### 1. Data Processing
- Built a reusable function to load and standardize NHANES modules.  
- Merged datasets by **SEQN** (unique respondent ID).  
- Combined Day 1 & Day 2 dietary intake to calculate averages.  

### 2. Feature Engineering
- **Dietary features**: average calories, protein, carbs, fats, cholesterol, fiber, vitamins, minerals.  
- **Ratios**: % protein, % carbs, % fat.  
- **Nutrient density**: nutrients per 1000 kcal.  
- **Physical activity**: total weekly activity, sedentary ratio, activity categories (*Highly Active, Moderate, Low, Sedentary*).  
- **Body measures**: BMI and weight categories (*Underweight, Normal, Overweight, Obese*).  
- **Clinical outcomes**:
  - Hypertension: average systolic/diastolic → Normal, Elevated, Stage 1, Stage 2.  
  - Cholesterol: HDL, LDL, triglycerides, medication use.  
  - Diabetes: fasting glucose, insulin use, self-report, prediabetes.  
  - Inflammation: CRP levels.  

### 3. Data Cleaning
- Addressed **missing values** (selective imputation/removal).  
- Removed **duplicates**.  
- Flagged/capped **outliers** (e.g., extreme nutrient intake).  

### 4. Analysis Approach
- Descriptive statistics & distribution checks.  
- Risk classification per health outcome.  
- Cross-tabulations (e.g., sodium vs. hypertension categories).  
- Comparative analysis of diet types (low-fat, diabetic, weight-loss).  
- Visualizations (histograms, box plots, bar charts).  

---

## 📊 Key Findings

### Hypertension
- High **sodium** + low **potassium** diets → strongly associated with elevated BP.  
- **Fiber-rich diets** → protective effect.  
- Inactivity worsened outcomes across all BMI groups.  

### Cholesterol
- **Saturated fat** → higher LDL.  
- **Polyunsaturated fats & fiber** → improved lipid profiles.  
- Medication lowered cholesterol, but dietary balance remained critical.  

### Diabetes
- High **carbohydrate density** → elevated fasting glucose.  
- Sedentary lifestyle increased risk even with normal BMI.  
- Balanced macronutrients reduced prevalence.  

### Inflammation
- High **CRP** more common in obese + sedentary individuals.  
- Diets rich in **antioxidant vitamins (C, E, K)** linked to lower inflammation.  

### Cross-Cutting Insight
- **Balanced nutrient density + consistent activity** were the strongest protectors across all outcomes.  

---

## 📂 Repository Structure

- nhanes-capstone-report
- 
  ├─ README.md 
  
  └─ Capstone_Capstone1_Report.pdf

  ---
  
---

## 💡 Contributions & Impact
- Designed a pipeline for **multi-module NHANES integration**.  
- Created interpretable **derived features** (ratios, densities, categories).  
- Generated insights that align with **public health recommendations**.  
- Provides a **framework for predictive modeling** and health dashboards.  

---

## 🚀 Future Work
- Develop **machine learning models** (logistic regression, random forest, LightGBM).  
- Build an **interactive dashboard** (Power BI, Tableau).  
- Deploy a **Flask app** for live health risk predictions.  
- Extend findings to **personalized diet recommendation systems**.  

---

## 🙏 Acknowledgments
- **CDC NHANES** for open-access health data.  
- Tools: **Python, Pandas, NumPy, scikit-learn, Matplotlib**.  
- Google Colab for providing the environment.  

---

## 📄 License
This project is for **educational purposes only**.  
NHANES data is **public, de-identified, and open**.

