# Machine-Learning-Loan-Default

Loan default prediction using machine learning models (logistic regression, random forest, gradient boosting, neural network, stacked classifier).

# Dataset

The Excel file (```data_loan_default.xlsx```) contains a dataset of 8929 loans issued between January 2007 and September 2017. There are 20 independent variables and one dependent variable. The dataset is imbalanced with about 15% of defaulting loans. 

# Methodology

Five models are compared:

- logistic regression,
- random forest,
- gradient boosting (XGBoost),
- neural network,
- stacked classifier (with the four above models as base models and a random forest as meta model).

## Data preprocessing

First, the data is made ready for analysis with the following steps:

- feature engineering,
- dealing with missing values,
- encoding categorical variables,
- splitting the dataset,
- feature scaling.

Then, for each model, hyperparameters are found with cross-validation (grid search or bayesian optimization methods are used) and the optimization metric is the macro recall. Class imbalance is mitigated by balancing the class weights. The models are fit and predictions are made on out-of-sample data. For each model we provide various performance metrics as well as an estimate of feature importance. 
