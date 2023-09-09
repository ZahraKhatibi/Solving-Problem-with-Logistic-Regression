# Titanic Survival Prediction with Logistic Regression

## Zara Khatibi - 610398119 - Deep Learning Homework

This project focuses on predicting survival on the Titanic using logistic regression. The goal is to determine whether a passenger survived or not based on passenger information.

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

The project demonstrates the entire process of using logistic regression for binary classification, from data exploration and preprocessing to model training and hyperparameter tuning. It emphasizes the importance of handling missing data, encoding categorical features, and finding the right hyperparameters for optimal model performance.

Feel free to explore the code and adapt it for your own classification tasks.
