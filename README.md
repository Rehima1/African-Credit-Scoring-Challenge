# African-Credit-Scoring-Challenge

## Project Overview

This project aimed to develop a Deep learning model to predict loan defaults in African financial markets. The goal is to build a model that accurately assesses the likelihood of loan defaults for both existing and new customers.

## Data

The project utilizes three datasets:

- **Train.csv:** Contains historical loan data with features like customer demographics, loan details, and target variable indicating default status.
- **Test.csv:** Contains loan data for which predictions need to be made.
- **economic_indicators.csv:** Contains macroeconomic indicators for different countries.

## Methodology

1. **Data Loading and Preprocessing:**
    - Load the train, test, and economic indicators datasets using pandas.
    - Merge economic indicators with train and test data based on country ID.
    - Handle missing values using imputation techniques (e.g., mean imputation).
    - Convert date columns to datetime objects and extract relevant features (e.g., month, day, year).
    - Encode categorical features using label encoding.
    - Create new features based on domain knowledge (e.g., interest rate, total amount to repay, loan repayment days).

2. **Exploratory Data Analysis:**
    - Analyze data distributions, correlations, and patterns using visualizations (e.g., histograms, scatter plots, heatmaps).
    - Identify key features that influence loan default.
    - Understand the relationship between economic indicators and loan defaults.

3. **Feature Engineering:**
    - Create new features based on existing features to improve model performance.
    - Examples include interaction terms, polynomial features, and aggregated features.

4. **Model Selection and Training:**
    - Select a sequantial deep learning model.
    - Split the train data into training and validation sets.
    - Train the model using the training data and evaluate its performance on the validation set.
    - I used features with strong correlation to the taget (corr > 3).

5. **Prediction and Submission:**
    - Use the trained model to predict loan defaults on the test data.
    - Create a submission file with predictions in the required competition format.


## Results

The model achieved an F1 score of 0.7123 on the validation set, and 0.628571428 on testing set, indicating acceapted performance in predicting loan defaults. The credit scoring function provides a scalable solution to evaluate risk and improve lending decisions.

## Conclusion

This project was conducted as part of my Deep Learning subject. While machine learning could potentially provide better performance, deep learning was the required approach for addressing this challenge. The developed model and credit scoring function aim to help financial institutions mitigate risk and make more informed lending decisions in African financial markets.

## Future Work

- Use machine learning models and feature engineering techniques to further improve performance.
- Incorporate external data sources, such as credit bureau data, to enhance the model's predictive power.
- Develop a more sophisticated credit scoring function with finer risk categories and scores.
- Balance the target.
