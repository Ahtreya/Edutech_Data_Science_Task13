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
