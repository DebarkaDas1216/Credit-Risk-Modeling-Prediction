# Credit Risk Modeling Prediction

This project focuses on building a Credit Risk Prediction Model to classify customers into different approval categories (P1, P2, P3, P4) based on their internal banking data and external CIBIL credit history. The solution integrates data preprocessing, feature engineering, statistical analysis, and machine learning to optimize the credit approval process.

# Key Highlights

Dataset size: Internal + External + Unseen datasets (~65,000+ rows)

Data Cleaning: Removal of invalid values (-99999), null handling, and feature reduction.

Feature Selection:

Chi-Square Test for categorical features.

VIF (Variance Inflation Factor) for multicollinearity check.

ANOVA (F-test) for numerical features.

Encoding: Ordinal encoding for EDUCATION, One-Hot Encoding for other categorical features.

# Models Used:

Random Forest Classifier

Decision Tree Classifier

XGBoost Classifier **(best performing)**

Hyperparameter Tuning: GridSearchCV and custom grid for fine-tuning XGBoost.

Scaling: StandardScaler applied to key numerical features.

Unseen Data Prediction: Applied final tuned XGBoost model on unseen dataset for real-world validation.

#Tools & Libraries

Python, Pandas, NumPy

Scikit-learn, XGBoost, Statsmodels, SciPy

Matplotlib for visualization

OpenPyXL for Excel data handling

# Results

XGBoost outperformed other models with the highest accuracy and balanced Precision, Recall, and F1 scores across all classes (P1, P2, P3, P4).

Final model tuned with parameters (colsample_bytree=0.9, learning_rate=1, max_depth=3, alpha=10, n_estimators=100).

Successfully predicted Target Variable for unseen dataset.

Business Problems Solved

Automated credit approval classification.

Identified high-risk vs. low-risk customers.

Reduced reliance on manual verification.

Provided interpretable insights from financial and behavioral features.

Delivered a scalable ML pipeline that can be retrained on new data.

# How to Run

Clone the repository:

git clone https://github.com/yourusername/credit-risk-modeling.git
cd credit-risk-modeling


# Install dependencies:

pip install -r requirements.txt


# Place datasets inside the Data/ folder:

Internal_Bank_Dataset.xlsx

External_Cibil_Dataset.xlsx

Unseen_Dataset.xlsx

Run the notebook/script to train models and generate predictions.
