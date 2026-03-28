🛒 Retail Expiry Reduction — End-to-End Machine Learning Project
📌 Overview
A retail grocery chain loses revenue every month due to product expiry — stock that hits its sell-by date before being sold. This project builds a complete machine learning pipeline on real retail transaction data to:
🔴 Predict which product-store combinations are likely to expire (Classification)
📊 Estimate how much expiry value will be incurred (Regression)
💡 Surface actionable insights for supply chain and merchandising teams
---
📁 Project Structure
```
.
├── expiry_reduction_ml.ipynb      # Main notebook — full walkthrough
├── Expiry_Reduction___Case_Study_.xlsx  # Source data (place here)
├── requirements.txt               # Python dependencies
└── README.md                      # This file
```
---
🗂️ Dataset
Column	Description
`month`	Reporting month
`store_type`	Offline / Hybrid
`division_name`	Business division
`dept`	Department
`family`	Product family
`shelf_life_flag`	Shelf life bucket
`mtd`	MTD / Rest (timing period)
`offer_type`	Liquidation offer type
`expiry`	Expiry value in ₹ (target)
`net_sales`	Net sales value in ₹
Size: 24,821 rows × 10 columns | Period: Jan 2023 & Jan 2024
---
🗺️ Notebook Sections
#	Section	Description
1	Setup & Data Loading	Library imports, data quality audit
2	EDA	Target distribution, category analysis, correlations
3	Feature Engineering	9 new features: ordinal encoding, log transforms, risk scores
4	Classification	Predict whether expiry occurs — 4-5 models compared
5	Regression	Predict expiry value — two-stage approach
6	Feature Importance	What drives expiry — model interpretability
7	Model Summary	Head-to-head leaderboard
8	Recommendations	5 data-backed business actions
---
📊 Key Results
Task	Best Model	Metric
Classification	Gradient Boosting / XGBoost	AUC-ROC ≈ 0.88+
Regression	Gradient Boosting / XGBoost	R² ≈ 0.75+
---
💡 Key Insights
Bakery has a 4.87% expiry rate — 5× the chain average
Deep discounting (>30% off) reduces expiry rate to 1.06% vs 2.8–3.1% for lighter offers
Month-end (last 5-6 days) has 40% higher expiry rate — ordering discipline needed
Offline stores generate 51% more expiry than Hybrid stores
Short-Life Dairy & Bread dominate absolute expiry losses
---
🚀 How to Run
```bash
# 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/retail-expiry-ml.git
cd retail-expiry-ml

# 2. Install dependencies
pip install -r requirements.txt

# 3. Place the dataset in the project root
#    File: Expiry_Reduction___Case_Study_.xlsx

# 4. Launch Jupyter
jupyter notebook expiry_reduction_ml.ipynb
```
---
📦 Requirements
```
pandas>=1.5.0
numpy>=1.23.0
matplotlib>=3.6.0
seaborn>=0.12.0
scikit-learn>=1.2.0
xgboost>=1.7.0
openpyxl>=3.0.0
jupyter>=1.0.0
```
---
🛠️ Skills Demonstrated
Data Wrangling — null handling, skewed distributions, datetime processing
EDA — business-framed visual storytelling with matplotlib/seaborn
Feature Engineering — domain-driven features, ordinal encoding, target encoding
ML Pipelines — sklearn `Pipeline` + `ColumnTransformer` best practices
Model Evaluation — AUC-ROC, R², 5-fold cross-validation, confusion matrices
Business Translation — ML findings → executive-ready recommendations
---
📈 Next Steps
[ ] Hyperparameter tuning with Optuna
[ ] SHAP values for prediction explainability
[ ] Monthly retraining pipeline
[ ] FastAPI deployment for real-time scoring
[ ] A/B testing framework for business impact measurement
---
Built by [Your Name] | LinkedIn | Portfolio
