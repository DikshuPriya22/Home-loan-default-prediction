# Home Loan Default Prediction

## Objective
To predict whether a customer will default on a home loan using machine learning techniques, enabling financial institutions to identify high-risk applicants and minimize potential losses.

---

## Dataset
The project uses multiple datasets including:
- Application Data
- Bureau Data
- Previous Applications
- Installment Payments

These datasets are merged and processed to create a comprehensive dataset for analysis.

---

## Data Preprocessing
- Handled missing values using median (numerical) and mode (categorical)
- Removed highly correlated features to reduce multicollinearity
- Performed feature engineering:
  - AGE
  - EMPLOYMENT_YEARS
  - INCOME_CREDIT_RATIO
  - ANNUITY_INCOME_RATIO
- Applied log transformation to handle skewed distributions
- Outliers treated using capping (winsorization)

---

## Exploratory Data Analysis (EDA)
- Identified class imbalance in target variable
- Observed skewness in income and loan amount distributions
- Analyzed relationships between income, loan amount, and default
- Studied categorical variables with respect to default behavior
- Correlation analysis showed no single dominant predictor

### Key Insights
- Customers with high loan-to-income ratio are more likely to default
- Lower income and shorter employment duration increase default risk
- Financial stability is a key factor in loan repayment
- Default risk depends on multiple combined factors

---

## Model Building
Implemented multiple models:
- Logistic Regression
- Random Forest
- Tuned Random Forest
- Gradient Boosting (optional)

---

## Model Evaluation
Evaluated models using:
- Accuracy
- Precision
- Recall 
- ROC-AUC Score
- Confusion Matrix

---

## Final Model
**Tuned Random Forest** was selected as the final model because:
- It achieved significantly higher **recall**, effectively identifying defaulters
- It provided better **ROC-AUC score**
- It balances prediction performance with business impact

This project focuses on **recall optimization to minimize financial risk**, as missing defaulters can lead to significant losses.

---

## Overfitting Check
- Train and test scores are closely aligned
- Indicates good generalization and model stability

---

## Business Impact
- Helps banks identify high-risk customers
- Enables better credit decision-making
- Reduces financial losses due to loan defaults

---

## Project Risks & Mitigation
- **Class imbalance** → handled using class weights
- **Overfitting** → checked using train-test comparison
- **Data quality issues** → handled via preprocessing
- **Model bias** → evaluated using multiple metrics

---

## Future Improvements
- Implement advanced models like XGBoost or LightGBM
- Perform deeper feature engineering
- Deploy model using a web application
- Monitor model performance in real-time

---

## Tech Stack
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn

---

## Conclusion
The project successfully builds a predictive model to identify loan defaulters. By focusing on recall and business impact, the model provides a practical solution for financial risk management.
