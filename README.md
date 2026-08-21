# Cardiovascular Risk Prediction & Model Evaluation Benchmark

An end-to-end Machine Learning study benchmarking **XGBoost** and **LightGBM** on tabular clinical data, incorporating Scikit-Learn preprocessing pipelines, Cross-Validation, and Explainable AI (SHAP).

## 📂 Repository Contents
- `cardio_risk_modeling_and_evaluation.ipynb` : End-to-end data preprocessing, training, cross-validation, and SHAP interpretability code.
- `Cardiovascular_Risk_Prediction_Report.pdf` : Full academic report detailing methodology, experimental setups, and medical discussions.
- `cardiovascular_dataset.csv` : Processed tabular dataset (~68,000 records).

## ⚙️ Methodology & Pipeline
- **Preprocessing:** Leakage-free transformations using Scikit-Learn `ColumnTransformer` (`StandardScaler` and `OneHotEncoder`).
- **Feature Engineering:** Derived clinical indicators including `bp_mean`, `pulse_pressure`, and interaction feature `age_x_bmi`.
- **Hyperparameter Optimization:** `RandomizedSearchCV` with 4-Fold Stratified Cross-Validation.

## 📊 Key Evaluation Results
| Metric | XGBoost (Tuned) | LightGBM (Tuned) |
| :--- | :--- | :--- |
| **ROC-AUC (Test Set)** | **0.8034** | **0.8032** |
| **PR-AUC (Average Precision)** | **0.7867** | **0.7877** |
| **5-Fold Stratified CV ROC-AUC** | **0.8010 ± 0.0034** | **0.8012 ± 0.0033** |

## 🔍 Explainable AI (XAI) with SHAP
- Identified systolic blood pressure (`ap_hi`), mean arterial pressure (`bp_mean`), and `age_x_bmi` as primary risk drivers.
- Analyzed feature behavior and non-linear interactions using `TreeExplainer`, SHAP Beeswarm, and Dependence plots.

## 🛠️ Tech Stack
Python, Scikit-Learn, XGBoost, LightGBM, SHAP, Pandas, NumPy, Matplotlib, Seaborn
