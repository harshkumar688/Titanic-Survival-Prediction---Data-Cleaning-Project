# 🚢 Titanic Survival Prediction – Data Cleaning & Exploratory Analysis

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-Data%20Visualization-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Preprocessing-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)

## 📌 Project Overview
This repository contains the solution for **Week 1: ML Fundamentals + Data Preprocessing**. The project focuses on data cleaning, missing value imputation, feature engineering, categorical encoding, and extracting meaningful demographic insights from the classic **Titanic Dataset**.

---

## 🛠️ Key Tasks Completed
1. **Exploratory Data Analysis (EDA)**: Summarized statistical properties using `.info()` and `.describe()`.
2. **Missing Data Handling**:
   * Imputed missing `Age` using median values (global and title-granular).
   * Imputed missing `Embarked` values using the mode (`'S'`).
   * Dropped the `Cabin` column due to high missingness (>75%).
3. **Categorical Encoding**:
   * Applied `LabelEncoder` to transform `Sex` into numerical values (`female`: 0, `male`: 1).
   * Applied One-Hot Encoding (`pd.get_dummies`) to convert `Embarked` into binary columns.
4. **Feature Engineering**:
   * **`TitleGroup`**: Extracted titles (`Mr`, `Mrs`, `Miss`, `Master`, `Rare`) from passenger names.
   * **`FamilySize` & `IsAlone`**: Derived total family size and solo travel indicators.
   * **`AgeGroup` & `FareBin`**: Categorized age spans and ticket fare tiers.
5. **Data Export**:
   * Cleaned dataset exported as `titanic_cleaned.csv`.
   * Feature-engineered dataset exported as `titanic_advanced_cleaned.csv`.

---

## 📊 Key Findings & Insights

| Feature Category | Group / Dimension | Total Passengers | Survived | Survival Rate (%) |
| :--- | :--- | :---: | :---: | :---: |
| **Gender** | Female | 314 | 233 | **74.20%** |
| | Male | 577 | 109 | **18.89%** |
| **Passenger Class** | 1st Class | 216 | 136 | **62.96%** |
| | 2nd Class | 184 | 87 | **47.28%** |
| | 3rd Class | 491 | 119 | **24.24%** |
| **Family Dynamics** | Small Family (2-4 members) | 292 | 173 | **59.25%** |
| | Solo Passenger (`IsAlone`) | 537 | 163 | **30.35%** |
| | Large Family (5+ members) | 62 | 9 | **14.52%** |

### 💡 Takeaways:
* **"Women & Children First"**: Female passengers survived at nearly 4x the rate of male passengers (74.2% vs 18.9%).
* **Socioeconomic Advantage**: 1st Class passengers had a 63.0% survival rate compared to 24.2% in 3rd Class.
* **Family Size Impact**: Passengers travelling in small families (2–4 members) had the highest survival rates (~59%), whereas large families (5+) experienced severe drop-offs (14.5%).

---

## 📂 Project Structure

```text
.
├── Titanic-Dataset.csv            # Original raw dataset
├── titanic_cleaned.csv            # Basic cleaned dataset
├── titanic_advanced_cleaned.csv   # Feature-engineered dataset
├── age_distribution.png           # Visual output plot
├── main.py                        # Python script executing data preprocessing
└── README.md                      # Project documentation
