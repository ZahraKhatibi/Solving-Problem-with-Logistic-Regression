# Titanic Survival Prediction with Logistic Regression

This project focuses on predicting survival on the Titanic using logistic regression. The goal is to determine whether a passenger survived or not based on passenger information.

## Assignment

In this problem, we intend to solve the binary classification problem of survival on the Titanic using Logistic Regression. The dataset for this task is located in the 'Dataset' directory, with the 'Survived' column being the dependent variable, and the other columns representing independent features.

1. Determine the data type (numeric or non-numeric) of each column.

2. Upon initial inspection, are all features necessarily needed for prediction? If not, specify which ones are not needed and remove them from the dataset. (For example, the 'PassengerId' feature is a random value assigned to each person and may not have any direct relationship with a person's survival chances.)

3. Since the Logistic Regression algorithm only accepts numerical input, provide a solution for non-numeric columns and explain it.

4. Standardize the values in the dataset 

5. Implement Logistic Regression along with regularization (weight decay). Optimize the learning rate and weight decay rate using 5-fold Cross-Validation with 10 repetitions. Analyze the impact of changes in these rates in terms of bias and variance and provide a written report.

6. Finally, report the results on the test dataset.

## Dataset

The dataset is divided into two parts:
- `train.csv`: Used for training the logistic regression model.
- `test.csv`: Used for making predictions.

## Data Exploration

The `data_explore` function provides insights into the dataset:
- Displays the first few rows of the dataset.
- Shows the dataset's size (number of instances and features).
- Lists the columns (features) in the dataset.
- Displays the data types of each column.
- Provides summary statistics for numerical features.
- Shows unique values and their counts for categorical features like "Embarked" and "Sex."

## Data Preprocessing

Key preprocessing steps include:
1. Handling missing values: Filling missing values in the "Embarked" column with the mode and in the "Age" column with the mean.
2. Converting categorical features: Using one-hot encoding to convert categorical features like "Embarked" and "Sex" into numerical format.
3. Standardizing numerical features: Standardizing "Age" and "Fare" to have zero mean and unit variance.

## Logistic Regression

Logistic regression is used to model the probability of survival based on the preprocessed data. Key steps include:
1. Cost Function: Defining the cost function for regularized logistic regression with a regularization term.
2. Gradient Descent: Using gradient descent to minimize the cost function and update model parameters (weights and bias).
3. Prediction: Making predictions on the test dataset using the trained logistic regression model with a threshold of 0.5 for classification.

## Hyperparameter Tuning

Hyperparameters (learning rate alpha and regularization parameter lambda) are tuned using 5-fold cross-validation. Different combinations are tested to optimize the model's performance and balance bias and variance.

## Results

The project concludes by making predictions on the test dataset using the best-trained logistic regression model. These predictions help identify passengers likely to have survived the Titanic disaster.
