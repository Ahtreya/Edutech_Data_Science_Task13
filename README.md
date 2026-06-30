# Edutech_Data_Science_Task13
## Project Overview
This repository contains the hyperparameter tuning and model optimisation task using a Random Forest Classifier on the Breast Cancer Wisconsin dataset.

## Best Parameters Found
* **GridSearchCV**: `{'max_depth': None, 'n_estimators': 200}` (Achieved 96% Accuracy)
* **RandomizedSearchCV**: `{'n_estimators': 100, 'max_depth': 5}` (Achieved 96% Accuracy)

## Files Included
* `Edutech_Data_Science_Task13.ipynb`: Complete code workflow with data preprocessing, scaling, and tuning pipelines.
* `data.csv`: Source dataset used.
* `grid_search_report.txt`: Exported classification report metrics for the Grid Search configuration.
* `random_search_report.txt`: Exported classification report metrics for the Randomised Search configuration.

## Interview Questions Related To This Task

### Q1: What is the core difference between GridSearchCV and RandomizedSearchCV?
* **GridSearchCV:** It performs an exhaustive search over a specified parameter grid. It evaluates every single permutation of the parameters, making it thorough but computationally expensive and slow for large spaces ($O(N)$ combination complexity).
* **RandomizedSearchCV:** It samples a fixed number of parameter combinations randomly from specified distributions or lists based on the `n_iter` budget. It is significantly faster and resource-efficient while exploring sprawling search spaces effectively.

### Q2: What is Cross-Validation (CV) and why is it essential during hyperparameter tuning?
* **Definition:** Cross-validation is a data resampling technique where the training dataset is partitioned into $K$ equal folds. The model training pipeline runs iteratively $K$ times; in each iteration, $K-1$ folds are used for training and the remaining 1 fold is utilized as the unseen validation reference.
* **Importance:** Tuning parameters on a single train/test split introduces selection bias and causes the hyperparameters to overfit to that specific validation set. Native 5-fold cross-validation (`cv=5`) ensures performance stability and guarantees the selected model configuration generalizes cleanly to completely unseen production metrics without data leakage.
  
