# Airline Ticket Price Prediction using Machine Learning

## Project Overview

This project focuses on analyzing and predicting airline ticket prices using machine learning techniques. Airline prices vary depending on several factors such as duration of the flight, airline, number of stops, departure time, and route. The goal of this project is to build a predictive model that can estimate ticket prices based on these features.

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

### 1. Data Cleaning and Exploratory Data Analysis (EDA)

The initial step involved understanding and cleaning the dataset. Missing values were handled and unnecessary columns were removed to improve data quality.

Several visualizations were created to explore relationships between variables:

A correlation matrix was plotted for all numerical columns to analyze relationships between variables. It was observed that flight duration had the highest correlation with ticket price, indicating that longer flights generally have higher prices.

A linear regression plot (lmplot) between duration and price was created to visually confirm this strong positive relationship.The departure time (Dep_Time) column was transformed into meaningful categories such as Morning, Afternoon, Evening, Night, and Late Night using conditional logic (if-else).
A bar chart was used to visualize the distribution of flights across these time categories. The analysis showed that night flights had the highest number of departures.

### 2. Feature Engineering and Encoding
* Categorical variables were converted into numerical form so that they could be used in machine learning models.
* Different encoding techniques were used depending on the nature of the variable:
* One-Hot Encoding was applied to categorical variables with no ordinal relationship.
* Target Encoding was applied to the Airline column using the median ticket price of each airline.
* Label Encoding was applied to the Total Stops column using a map() function to preserve its natural order.

### 3. Outlier Detection and Treatment
* Outliers were identified using histograms and boxplots.
* The upper bound for price was calculated as 23017.
* Values above this threshold were treated as outliers.
* Instead of removing them, they were replaced with the median price to prevent distortion of the model.

### 4. Feature Selection
* A Random Forest model was used to calculate feature importance.
##### The most important features were:
###### Feature	Importance
* Duration	0.54
* Airline	0.14
* This confirms that flight duration is the most influential factor affecting ticket prices.

### 5. Model Building
* The dataset was split into 80% training and 20% testing data using Train-Test Split.
* A Random Forest Regressor model was trained to predict flight ticket prices.
* Initial model performance:
R² Score: 0.76
MAPE: 14.2
MAE: 1238.39

### 6. Hyperparameter Tuning
To improve model performance, RandomizedSearchCV was used for hyperparameter tuning.
##### Best parameters obtained:
n_estimators = 550
min_samples_split = 10
max_depth = 17
After tuning, the model achieved:
R² Score: 0.81

### 7. Final Model
Using the best hyperparameters, the final model was trained.
Final performance:
R² Score: 0.799
MAPE: 13.78
This indicates that the model can predict airline ticket prices with good accuracy.

### 8. Model Saving
Finally, the trained model was saved using Python Pickle so that it can be reused later without retraining.

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
