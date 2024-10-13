# Loan_Prediction_Analyisis Project

This project utilizes the Naive Bayes machine learning algorithm to predict whether a loan will be repaid based on historical data. It covers data collection, cleaning, model training, testing, and visualization.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Data Collection](#data-collection)
3. [Data Cleaning](#data-cleaning)
4. [Model Training](#model-training)
5. [Testing and Prediction](#testing-and-prediction)
6. [Data Visualization](#data-visualization)

## Project Overview
The goal of this project is to predict loan repayment outcomes using the Naive Bayes algorithm. This involves:
- Collecting and preparing loan data
- Training a Naive Bayes model on the processed data
- Testing the model's accuracy and making predictions
- Visualizing results with various charts for easier interpretation

## Data Collection
Loan data is collected in `.csv` format and includes columns like `id`, `issue date`, `loan amount`, `funded amount`, `term`, `interest rate`, and `installment`. 

- **Libraries used**: `pandas`, `numpy`
- **Data Import Methods**: `np.genfromtxt()` to load the dataset.

## Data Cleaning
Data cleaning steps ensure the dataset is ready for modeling:
1. **Handling Missing Values**: Missing values are identified using `.isnan()` and filled with `.nanmax()` and `.nanmin()`.
2. **Dataset Splitting**: Splitting the data into numeric and text components for better handling.
3. **Creating Checkpoints**: Saving intermediate results to allow recovery in case of system interruptions.
4. **Processing String Data**: Unique values in text columns are identified with `.unique()`, and missing values are filled.
5. **Data Conversion**: Converting all text data to numeric format for consistency.
6. **Sorting and Saving Data**: Sorting by `id` and saving the cleaned dataset as a new `.csv` file using `.savetxt()`.

## Model Training
The cleaned data is then used to train a Naive Bayes model:
1. **Reading Cleaned Data**: Importing the cleaned dataset for modeling.
2. **Feature Splitting**: Dividing the data into independent and dependent variables.
3. **Data Splitting**: Splitting the data into 80% for training and 20% for testing to evaluate the model's performance.
4. **Training with Naive Bayes**: Using the Naive Bayes algorithm to predict loan repayment.

## Testing and Prediction
1. **Predicting with the Model**: Using the trained Naive Bayes model to predict loan repayment outcomes on the test data.
2. **Accuracy Calculation**: Evaluating model performance by calculating the accuracy based on the confusion matrix results.

## Data Visualization
To interpret the results, several visualizations are created:
1. **Bar Chart**: Compares data between groups to track changes over time.
2. **Pie Chart**: Visualizes the accuracy and error rate of the model based on the confusion matrix.
3. **Confusion Matrix**: Displays the model's classification performance with true positives, false positives, true negatives, and false negatives.
