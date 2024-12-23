# **Machine Learning Projects: Supervised and Unsupervised Approaches**

This repository showcases two distinct projects, each applying machine learning techniques to solve real-world problems in different domains. The repository is organized into two sections:

1. **Supervised Learning**: **Predicting Concrete Compressive Strength**
   - Focused on regression modeling to predict the compressive strength of concrete mixtures.
   - Code: `Predicting_Concrete_Strength.ipynb`
2. **Unsupervised Learning**: **Clustering Housing Data**
   - Employed clustering techniques to segment housing data based on economic and geographical attributes.
   - Code: `Clustering_Housing_data.ipynb`

---

## **1. Predicting Concrete Compressive Strength**

### **Objective**
Predicting the 28-day compressive strength of concrete, a critical metric for the design and safety of civil engineering projects. This project applies supervised machine learning techniques to model the relationship between concrete composition and its compressive strength.

### **Dataset**
- **Source**: `concrete.csv`
- **Attributes**:
  - **Inputs**: Cement, Blast Furnace Slag, Fly Ash, Water, Superplasticizer, Coarse Aggregate, Fine Aggregate, and Age (1–365 days).
  - **Target**: Compressive Strength (in MPa).

### **Methodology**
1. **Exploratory Data Analysis (EDA)**:
   - Uncovered patterns through histograms, boxplots, pair plots, and heatmaps.
   - Identified significant predictors: Cement, Superplasticizer, and Age.

2. **Data Preparation**:
   - Cleaned data and handled missing values.
   - Replaced zeros in skewed variables with median/mean values.
   - Scaled features using Quantile Transformer for robust model performance.

3. **Modeling and Evaluation**:
   - Models Used: KNN, Random Forest, XGBoost.
   - Ensemble Learning: Combined models using a Voting Regressor.
   - Metrics: RMSE, MAE, MSE, R².

### **Results**
- **XGBoost** and **Voting Regressor** outperformed other models, delivering the most accurate predictions.
- Highlighted the importance of preprocessing in small datasets and demonstrated the value of ensemble learning.

---

## **2. Clustering Housing Data**

### **Objective**
Identify distinct economic segments across a state using clustering techniques on housing data. This unsupervised learning project focuses on grouping regions with similar economic and geographical attributes.

### **Dataset**
- **Source**: `housing.csv`
- **Attributes Used**: Median Income, Longitude, Latitude.

### **Methodology**
1. **K-Means Clustering**:
   - Performed clustering with `k=6` and visualized results in 3D space.
2. **Elbow Method**:
   - Plotted WCSS to identify the optimal number of clusters.
   - Observed that the optimal `k` is 2.
3. **Silhouette Analysis**:
   - Evaluated clustering quality using the Silhouette Coefficient.
   - Found that `k=2` produces well-defined and meaningful clusters.

### **Results**
- Clustering revealed distinct regional economic segments.
- Optimal clusters (`k=2`) provided high-quality, interpretable groupings, supported by Silhouette Coefficient analysis.



