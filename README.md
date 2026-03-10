# Airline Ticket Price Prediction using Machine Learning

## Project Overview

This project focuses on predicting airline ticket prices using machine learning techniques. Airline prices vary depending on several factors such as duration of the flight, airline, number of stops, departure time, and route. The goal of this project is to build a predictive model that can estimate ticket prices based on these features.

The project follows a complete machine learning workflow including data cleaning, feature engineering, feature selection, model training, hyperparameter tuning, and model evaluation.

## Problem Statement

Airline ticket prices fluctuate due to multiple factors and are often difficult for customers to predict. This project aims to develop a machine learning model that can analyze historical flight data and predict ticket prices with good accuracy.

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn

## Machine Learning Model

The main model used in this project is Random Forest Regressor. Random Forest is an ensemble learning algorithm that builds multiple decision trees and combines their predictions to improve accuracy and reduce overfitting.

Hyperparameter tuning was performed using RandomizedSearchCV to find the optimal parameters for the model.


## Project Workflow

The project follows these steps:

1. Data Cleaning
   Handling missing values and removing unnecessary columns.

2. Feature Engineering
   Transforming and creating meaningful features such as flight duration and time-related variables.

3. Feature Encoding
   Converting categorical variables into numerical form so that they can be used in machine learning models.

4. Train-Test Split
   Splitting the dataset into training and testing sets.

5. Model Training
   Training a Random Forest model on the training dataset.

6. Model Evaluation
   Evaluating the model using regression metrics such as:

   * MAE (Mean Absolute Error)
   * MAPE (Mean Absolute Percentage Error)
   * R² Score

7. Hyperparameter Tuning
   Using RandomizedSearchCV to find the best parameters for the model.

8. Final Model Selection
   The best model was selected and saved using pickle for future predictions.


## Feature Importance

Feature importance analysis showed that flight duration is the most influential factor affecting airline ticket prices. This insight makes sense because longer flights generally cost more than shorter flights.

Other important factors include airline type, number of stops, and departure time.



## Model Performance

The final model achieved good performance on the test dataset.

Evaluation metrics used:

* R² Score
* MAE
* MAPE

These metrics indicate that the model can explain a large portion of the variance in airline ticket prices.


## Model Saving

The trained model was saved using Python's pickle library so that it can be reused later without retraining.

## Future Improvements

Possible improvements for this project include:

* Trying other machine learning models such as Gradient Boosting or XGBoost
* Building a web application for real-time predictions
* Deploying the model using Flask or FastAPI
* Using more real-world airline datasets

## Conclusion

This project demonstrates how machine learning can be applied to predict airline ticket prices. By analyzing historical flight data and using ensemble learning techniques like Random Forest, it is possible to build a model that can provide useful price predictions.

The project highlights the importance of data preprocessing, feature engineering, and hyperparameter tuning in building effective machine learning models.

## Author
Deepak Kumar
Aspiring Data Scientist
