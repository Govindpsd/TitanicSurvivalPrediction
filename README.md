# Titanic Survival Prediction Project

## Overview

This repository contains code for predicting survival on the Titanic using machine learning techniques. The project involves data preprocessing, model building with RandomForestClassifier, cross-validation, hyperparameter tuning, and generating predictions for submission.

## Project Structure

- **train.csv**: Training dataset containing passenger information.
- **test.csv**: Test dataset for which survival predictions are to be made.
- **gender_submission.csv**: Sample submission file for Kaggle competition.

## Code Overview

### Dependencies

- Python 3.x
- Required Python libraries:
  - pandas
  - matplotlib
  - seaborn
  - scikit-learn

### Data Preprocessing

1. **Loading Data**: Reading `train.csv`, `test.csv`, and `gender_submission.csv` using Pandas.
2. **Handling Missing Values**: Filling missing values in `Age` and `Fare` with medians.
3. **Feature Engineering**:
   - Creating `Family` feature by combining `SibSp` and `Parch`.
   - Dropping irrelevant columns (`Name`, `Ticket`, `Cabin`).

4. **Scaling**: Standardizing numeric features (`Age`, `Fare`) using StandardScaler.
5. **Encoding Categorical Variables**: Label encoding `Sex` and one-hot encoding `Embarked`.

### Model Building

- **RandomForestClassifier**: Training the classifier on preprocessed data.
- **Evaluation**: Assessing model performance using confusion matrix and accuracy score.

### Cross-Validation

- **ShuffleSplit**: Implementing ShuffleSplit for cross-validation with 5 splits.

### Hyperparameter Tuning

- **RandomizedSearchCV**: Searching optimal hyperparameters (`n_estimators`, `max_features`, `max_depth`, `criterion`) using randomized search.

### Making Predictions

- Generating predictions on `test_data` using the best estimator from `RandomizedSearchCV`.

### Submission

- Creating a submission file (`Submission.csv`) containing `PassengerId` and predicted `Survived` values.


4. **Check the submission file (`Submission.csv`) generated in the project directory.**

## Contributing

- Contributions to improve the project are welcome. Feel free to submit issues and pull requests.

## Contact
- Govind
- pgovind887@gmail.com


