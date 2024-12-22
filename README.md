# Predicting Concrete Compressive Strength Using Machine Learning

This project focuses on leveraging supervised machine learning techniques to predict the **28-day compressive strength** of concrete, a critical metric in civil engineering. The compressive strength of concrete reflects its ability to resist failure under pressure and is fundamental to the design and safety of civil infrastructure.

Accurate prediction of concrete strength is vital to balancing cost-efficiency, environmental sustainability, and structural integrity. This project addresses this challenge by analyzing and modeling the relationship between concrete mixture proportions and strength using a dataset (`concrete.csv`) representative of real-world scenarios.

---

## Problem Statement

Concrete strength prediction is essential to prevent under-designed structures that risk failure and over-designed structures that result in increased costs and environmental impact. The dataset used for this analysis presents the **small dataset problem**, a common challenge in machine learning, where limited data availability demands careful preprocessing and feature engineering to achieve reliable predictions.

---

## Dataset Description

The dataset contains the following attributes:

- **Cement, Blast Furnace Slag, Fly Ash, Water, Superplasticizer, Coarse Aggregate, Fine Aggregate**: Quantities of respective components in kg/m³ of the concrete mixture.
- **Age**: Age of the concrete (in days) ranging from 1 to 365.
- **Compressive Strength (Target)**: Measured in MPa, representing the 28-day compressive strength of the concrete.

---

## Project Workflow

### 1. Exploratory Data Analysis (EDA)

Performed univariate and multivariate analyses to understand data distributions and relationships:
- **Histograms**: Revealed distributions and central tendencies.
- **Boxplots**: Identified potential outliers in key variables.
- **Pair plots**: Examined relationships between features.
- **Heatmaps**: Analyzed correlations, highlighting significant predictors like **Cement**, **Superplasticizer**, and **Age**.

### 2. Data Preparation & Feature Engineering
- **Data Cleaning**: Removed duplicates and handled missing values.
- **Zero Value Handling**: Replaced zeros in skewed variables with median values or mean where appropriate.
- **Outlier Mitigation**: Used **Quantile Transformer** for robust scaling and reducing outlier impact.
- **Feature Scaling**: Standardized the dataset for consistent model performance.

### 3. Modeling & Evaluation

Trained the dataset on three regression models:
- **K-Nearest Neighbors (KNN)**
- **Random Forest**
- **XGBoost**

Combined individual models using a **Voting Regressor** for ensemble learning.

**Evaluation Metrics**:
- **RMSE (Root Mean Squared Error)**
- **MAE (Mean Absolute Error)**
- **MSE (Mean Squared Error)**
- **R² Accuracy**

### Results
- **XGBoost** and the **Voting Regressor** outperformed other models across all metrics, showcasing their robustness in predicting compressive strength.
- **KNN Regressor** demonstrated the weakest performance, likely due to its sensitivity to feature scaling and data sparsity.

---

## Key Learnings and Contributions
- Highlighted the importance of preprocessing in dealing with small datasets.
- Demonstrated the value of ensemble learning in improving predictive accuracy.
- Provided a reproducible workflow for similar regression tasks in the engineering domain.

---
