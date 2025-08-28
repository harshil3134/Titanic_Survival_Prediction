Titanic Survival Prediction
Project Overview
This project is a comprehensive machine learning workflow to predict passenger survival on the Titanic, based on data from the classic Kaggle competition. It demonstrates a full data science pipeline, including data preprocessing, feature engineering, and model optimization to build a robust and accurate classification model.

Key Features
Data Preprocessing Pipeline: Uses scikit-learn's ColumnTransformer and Pipeline to handle missing values and encode categorical features, ensuring a clean and reproducible workflow.

Feature Engineering: Creates a new, more predictive Family_Size feature by combining the SibSp and Parch columns.

Model Selection: Employs a RandomForestClassifier for robust classification.

Hyperparameter Tuning: Uses GridSearchCV with cross-validation to systematically find the optimal model parameters.

Final Submission: Generates a formatted CSV file ready for submission to the Kaggle competition.

Methodology
The project follows a standard machine learning workflow:

Data Loading and Exploration: The train.csv and test.csv datasets were loaded and explored to understand the data types, distributions, and presence of missing values.

Feature Engineering: New features like Family_Size were created from existing columns to provide more predictive power to the model.

Data Preprocessing: A ColumnTransformer was used to apply different preprocessing steps to different columns:

Missing Age and Fare values were imputed with the mean.

Categorical features like Sex and Embarked were one-hot encoded.

Model Training and Tuning: A RandomForestClassifier was trained on the preprocessed data. GridSearchCV was then used to find the best combination of hyperparameters (n_estimators, max_depth, min_samples_split) to maximize the model's accuracy.

Prediction and Submission: The final, optimized model was used to make predictions on the unseen test dataset. These predictions were then saved in the required Kaggle submission format (submission.csv).

How to Run the Code
Clone this repository to your local machine.

Ensure you have all the required libraries installed (see requirements.txt).

Open the titanic-dataset.ipynb notebook in a Jupyter environment.

Run all the cells in the notebook sequentially.

Requirements
The following libraries are required to run this notebook:

pandas

numpy

scikit-learn

seaborn

matplotlib

You can install all of them using:

Bash

pip install -r requirements.txt

Final Results
The final model achieved a cross-validation accuracy of 0.789. The submission.csv file contains the final predictions from this model.
