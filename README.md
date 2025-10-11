# SC5002_Lab_Assignment_2
This project explores Linear Regression and Ridge Regression models using a real-world diamond dataset.
Our goal is to understand how regularization (Ridge) helps prevent overfitting compared to the standard Linear model and to demonstrate the use of k-fold cross-validation for robust model evaluation.

## Dataset Description

Source: Kaggle – Diamonds Dataset
Size: 50,000 rows × 10 columns
Features:
1. Numerical: carat, depth, table, x, y, z (dimensions of the diamond)
2. Categorical: cut, color, clarity
3. Target Variable: price — continuous numerical variable representing diamond cost.

Preprocessing:
1. Removed 126 duplicates (final: 49,874 rows).
2. Removed rows with zero dimensions.
3. Applied StandardScaler to normalize features so that mean = 0 and SD = 1.


## Steps Taken
Data Preprocessing  
  1. Checked dataset shape and duplicates.
  2. Dropped duplicates and invalid (zero) values.
  3. Encoded categorical features (Label Encoding).
  4. Scaled numerical features using StandardScaler.

Exploratory Data Analysis
  1. Used boxplots to observe the relationship between cut, color, clarity, and price.
  2. Generated a correlation heatmap to identify strong predictors (e.g., carat has the highest correlation with price).

Model Training
  1.   Split data into 80% training and 20% test.
  2.   Implemented K-Fold (k=5) cross-validation to ensure stable evaluation.
  3.   Trained:
       - Linear Regression as the baseline model.
       - Ridge Regression for comparison, tuning alpha values to reduce overfitting.

Evaluation Metrics
  1. Calculated values:
       - Mean Squared Error (MSE) - to measure prediction error
       - R^2 score - to measure the fitting of the model
  2. Compared both LR and RR models' training and test performances

Analysis and Comparison
  1. Both LR and RR have identical results in terms of MSE and R^2
  2. LR was chosen to be more suitable due to its simplicity and interpretability
  3. Explain the different alpha values in RR and their corresponding results
  4. Explain examples where LR and RR are more suited for

## Insights & Conclusion
  1. Carat is the most significant predictor of price; physical dimensions (x, y, z) also contribute strongly.
  2. Categorical variables like cut, color, and clarity influence price but less directly — they interact with carat size.

Section 1 and 2 is done by Manville
Section 3 is done by Elizabeth
Section 4 and 5 is done by Jevons
