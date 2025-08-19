# 🚗 BMW Car Sales Prediction
## 📝 Project Description

This project aims to analyze and predict BMW car sales based on various vehicle and market characteristics. The dataset includes information on Model, Year, Region, Color, Fuel Type, Transmission, Engine Size, Mileage, Price, and Sales Volume.

The main goal was to identify the variables that most influence car sales, both considering the Sales_Volume variable and without it, and to develop a predictive model to classify sales as High or Low.

## 🧹 Data Preprocessing

Categorical Variables Conversion: Columns Model, Region, Color, Fuel_Type, and Transmission were converted to categorical data types.

Target Variable: A categorical variable Sales_Classification was created based on sales volume (High vs Low) and encoded as numeric (0 and 1).

One-Hot Encoding: Applied to all categorical variables to prepare the dataset for modeling.

Train/Test Split: Dataset was split into 70% training and 30% testing data.

## 🏗️ Models Used
### 🌲 Random Forest

A Random Forest Classifier was trained to classify car sales.

Predictions were evaluated using a classification report and confusion matrix.

Limitation: Attempting to apply SHAP for model explainability caused compatibility issues and errors (AssertionError), preventing a satisfactory explanation.

### ⚡ XGBoost

An XGBoost Classifier was used as an alternative.

Key parameters:

n_estimators=200

max_depth=6

learning_rate=0.1

eval_metric='logloss'

Model evaluation performed with classification report and confusion matrix.

SHAP worked correctly, allowing visualization of the importance of each feature in predicting sales.

## 📊 Results

The most influential variables for predicting sales (according to SHAP) include:

Price_USD

Engine_Size_L

Mileage_KM

Model

Transmission

The impact of Sales_Volume was studied through the Sales_Classification variable, showing that it is possible to predict high or low sales using vehicle and market characteristics.

## ✅ Conclusion

We successfully preprocessed and prepared the data, trained predictive models, and evaluated their performance.

Although Random Forest did not allow explainability via SHAP due to technical limitations, XGBoost provided clear interpretability.

The developed workflow identifies the most impactful features on BMW car sales, providing valuable insights for sales and marketing strategies.
