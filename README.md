# Data Preprocessing and Model Evaluation

## Overview

This project involves preprocessing and evaluating a dataset related to fraud detection. The dataset includes information about various transactions and user details. The steps include data loading, preprocessing, and evaluating different models to predict fraud, ultimately selecting XGBoost for its performance.

## Data Loading

The dataset consists of the following files:
- **Train Data**: `train.csv` - Contains features and target labels for training.
- **Test Data**: `test.csv` - Contains features for testing.
- **Sample Submission**: `sample_submission.csv` - Template for submitting predictions.

The data was loaded from CSV files with specific columns selected for analysis.

## Data Preprocessing

The preprocessing steps applied to the data are as follows:

1. **Gender Encoding**:
   - Transformed gender descriptions into binary values (Male=1, Female=0).

2. **Occupation and Education Encoding**:
   - Encoded categorical values for occupation and education level into numerical values.

3. **Marital Status Encoding**:
   - Converted marital status into numerical values.

4. **Age Transformation**:
   - Extracted the first two digits of age.

5. **Device Type Encoding**:
   - Mapped various device types to numerical values and handled missing values.

6. **Location Encoding**:
   - Replaced location abbreviations with full names and encoded them into numerical values.

7. **Transaction Time Conversion**:
   - Converted transaction times into a 24-hour format and categorized them into time periods (Morning, Afternoon, Evening, Late Night).

8. **Transaction Type Encoding**:
   - Encoded transaction types into numerical values.

9. **Merchant ID Extraction**:
   - Extracted the last digit from MerchantID.

10. **Email Domain Encoding**:
    - Extracted and encoded email domains into numerical values.

11. **Handling Missing Values**:
    - Imputed missing values using the mean strategy for numerical columns.

## Data Processing Results

- **Processed Training Data**: Saved as `x_train_processed.csv`.
- **Processed Test Data**: Saved as `x_test_processed.csv`.

The processed data is now ready for model training and evaluation.

## Model Evaluation

### Models Tried

1. **Random Forest**:
   - Tested with default parameters and evaluated using various metrics.

2. **XGBoost**:
   - Initial hyperparameter tuning was performed to optimize performance.

3. **PCA Techniques**:
   - Applied Principal Component Analysis (PCA) to reduce dimensionality and improve model performance.

### Final Model

After experimenting with various models, including Random Forest and applying hyperparameter tuning with XGBoost, we selected XGBoost as the final model due to its superior performance in predicting fraud.

- **Model Parameters**:
       -  n_estimators=1000,
        - max_depth=10,
       -  learning_rate=0.1,


- **Evaluation Metrics**:
  - **Log Loss**: Measures the model's prediction accuracy.
  - **AUC (Area Under Curve)**: Represents the model's ability to distinguish between classes.
  - **F1 Score**: A measure of the model's accuracy considering both precision and recall.

### Results

- **Validation Log Loss**: Value not available in this summary.
- **Validation AUC**: Value not available in this summary.
- **Validation F1 Score**: Value not available in this summary.

- **Test Predictions**:
  - The final predictions were saved in `predictions.csv`.

## Conclusion

The preprocessing steps ensured that the data was cleaned and transformed appropriately for model training. Various models were evaluated, and XGBoost was selected for its performance and effectiveness in predicting fraud.

