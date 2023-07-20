# ⚡⚡ Diabetes_Prediction 🩺🩺
![Python version](https://img.shields.io/badge/Python%20version-3.10%2B-lightgrey)
![GitHub last commit](https://img.shields.io/github/last-commit/Taweilo/Diabetes_Prediction)
![GitHub repo size](https://img.shields.io/github/repo-size/Taweilo/Diabetes_Prediction)
![Type of ML](https://img.shields.io/badge/Type%20of%20ML-Binary%20Classification-red)
![License](https://img.shields.io/badge/License-MIT-green)

Badge [source](https://shields.io/)

 <img src="https://meddo.in/blog/wp-content/uploads/2020/09/onpage_Book-diagnostic-test-online-1024x575.jpeg" width="1100" height="450">
This project will follow the Business Analysis (BA) workflow to address diabetes diagnosis using data mining techniques. By leveraging modeling, we aim to classify and predict the disease based on input features. The health industry can consult this model for more informed decision-making.

```
├── Image
│   ├── 2.1 Dataset.jpg                           <- dataset image used in the README.
│   ├── 2.2 Statistics.jpg                        <- data statistics summary used in the README.
│   ├── 2.3 Outcome distribution.jpg              <- outcome distribution image used in the README.
│   ├── 2.4 Pairplot.jpg                          <- pairplot image used in the README.
│   ├── 5.1 Evaluation.jpg                        <- model summary table used in the README.                            
│
├── Code_Diabetes_Prediction.ipynb                <- code
├── Data_diabetes.csv                             <- dataset
├── LICENSE                                       <- MIT license
├── README.md                                     <- read me
```

## 1. Business Understanding

## 2. Data Understanding 
The Diabetes dataset was loaded via Colab. The dataset is from Kaggle: https://www.kaggle.com/datasets/akshaydattatraykhare/diabetes-dataset (also please see Data_diabetes.csv attached). Basic data analysis was performed to identify the shape of data, get column names, find missing values, and generate descriptive statistics. [[The Pearson correlation matrix was calculated to find the pairwise correlation of the columns in the data. All columns in the data are visually represented as histograms. A correlation heatmap figure was generated to represent the correlation matrix.]]

* Original Dataset
 <img src="https://github.com/Taweilo/Diabetes_Prediction/blob/main/Image/2.1%20Dataset.jpg" width="600">
 
| Name | Modeling Role | Measurement Level| Description|
| ---- | ------------- | ---------------- | ---------- |
| **Pregnancies** | input | int64 | To express the Number of pregnancies of the patient |
| **Glucose** | input | int64 | To express the Glucose level in the blood of the patient|
| **BloodPressure** | input | int64 | To express the Blood pressure measurement of the patient |
| **SkinThickness** | input | int64 | To express the thickness of the skin of the patient |
| **Insulin** | input | int64 | To express the Insulin level in the blood of the patient |
| **BMI** | input | float64 | To express the Body mass index of the patient |
| **DiabetesPedigreeFunction** | input | float64  | To express the Diabetes percentage of the patient |
| **Age** | input | int64 | To express the age of the patient |
| **Outcome** | target | binary | To express the final result 1 is Yes and 0 is No Diabetes of the patient |

* Statistics
 <img src="https://github.com/Taweilo/Diabetes_Prediction/blob/main/Image/2.1%20Dataset.jpg" width="600">
 
* Pairplot
 <img src="https://github.com/Taweilo/Diabetes_Prediction/blob/main/Image/2.4%20Pairplot.png" width="1000">

* Outcome Distribution
 <img src="https://github.com/Taweilo/Diabetes_Prediction/blob/main/Image/2.3%20Outcome%20distribution.jpg" width="600">
 
## 3. Data Preparation 
1. Define variables (X and y) 
2. Split the data into train and test datasets <br>
   train: **2727 data<br>
   test:  **1819 data<br>
  
## 4. Modeling   
Several machine learning models were included. Among all, KNN, Regression Tree, and Random Forest proceeded hyperparameter tuning for better performance:
* Logistic regression
* Gaussian model
* SVM
* KNN
* Regression Tree
* Random Forest with Tuning
  
## 5. Evaluation
 <img src="https://github.com/Taweilo/Diabetes_Prediction/blob/main/Image/5.1%20Evaluation.jpg" width="500" >
 * Random Forest has the best performance. The best hyperparameter is: 
```
 {'n_estimators': 200,
 'min_samples_split': 10,
 'min_samples_leaf': 4,
 'max_features': 'log2',
 'max_depth': 5,
 'bootstrap': True}
```
 * Out-of-sample Accuracy of Random Forest:  0.76; Out-of-sample AUC:  0.83; True Positive Rate: 54.1% and False Positive Rate 11.7%.
 <img src="https://github.com/Taweilo/Diabetes_Prediction/blob/main/Image/5.2%20RF%20Confusion%20Matrix.jpg" width="500" >
 
 * Feature importance can be shown: Glucose in the blood is the most important feature. 
 <img src="https://github.com/Taweilo/Diabetes_Prediction/blob/main/Image/5.3%20Feature%20importance.jpg" width="500" >
 
 

 

