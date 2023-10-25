# FrankensteinsMonster
How to build Frankenstein himself

This code performs a machine learning workflow to build a logistic regression model on a classification dataset. Here are the key steps:

1. Load and preprocess the dataset:
- Remove duplicates
- Handle missing values 
- Remove highly correlated features
- Normalize continuous features
- Encode categorical features

2. Split data into train/validation folds using StratifiedKFold

3. For each fold:
- Tune hyperparameters using GridSearchCV
- Evaluate model performance using accuracy, precision, recall, F1, ROC AUC
- Address class imbalance using class weights 

4. Average metrics across folds to evaluate overall performance

5. Plot ROC curve using decision function values on validation set

6. Save predictions on test set to CSV file

The main goal is to build an optimized logistic regression model that generalizes well across multiple cross-validation folds. Performance is evaluated using various classification metrics. The model is tuned using grid search on hyperparameters like C and penalty type. Class imbalance is handled by computing class weights. The end result is a model that can make predictions on new unseen data. The workflow demonstrates a systematic process for developing and evaluating a classification model.
