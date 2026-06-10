# Student Performance Predictor

## Introduction About the Data

The goal of this project is to predict a student's **Math Score** based on various demographic and academic factors using Machine Learning Regression techniques.

### Independent Variables

* **gender** : Gender of the student
* **race_ethnicity** : Ethnic group of the student
* **parental_level_of_education** : Education qualification of parents
* **lunch** : Type of lunch received by the student
* **test_preparation_course** : Completion status of test preparation course
* **reading_score** : Reading score obtained by the student
* **writing_score** : Writing score obtained by the student

### Target Variable

* **math_score** : Mathematics score obtained by the student

### Dataset Source

Dataset Link:
https://www.kaggle.com/datasets/spscientist/students-performance-in-exams

### Prediction Page

<img width="938" height="499" alt="image" src="https://github.com/user-attachments/assets/da4d3c85-53a8-4b6c-9a6a-8d48cccade0e" />


---

## Azure API Link

Prediction Endpoint:

[https://student-score-predictor-rashu-2026.azurewebsites.net/predictdata](https://student-score-predictor-rashu-2026-fufjgjcbf5erbjg8.centralindia-01.azurewebsites.net/predictdata)

---

# Approach for the Project

## Data Ingestion

* Dataset is loaded as CSV.
* Data is split into Training and Testing datasets.
* Raw, Train, and Test datasets are stored inside the artifacts folder.

## Data Transformation

In this phase a preprocessing pipeline is created.

### Numerical Features

* Missing value handling using SimpleImputer
* Standard Scaling using StandardScaler

### Categorical Features

* Missing value handling using SimpleImputer
* Ordinal Encoding
* Feature Scaling

The preprocessing object is saved as a pickle file.

## Model Training

Various regression models are trained and evaluated.

Models Tested:

* Linear Regression
* Decision Tree Regressor
* Random Forest Regressor
* Gradient Boosting Regressor
* XGBoost Regressor
* CatBoost Regressor
* AdaBoost Regressor

The best performing model is selected based on evaluation metrics and saved as a pickle file.

## Prediction Pipeline

The prediction pipeline:

* Accepts user input from the web interface
* Converts input data into DataFrame format
* Loads trained model and preprocessor
* Performs prediction
* Returns predicted Math Score

## Flask Application

A Flask web application is created to provide an interactive user interface for score prediction.

Users can:

* Enter student information
* Submit the form
* Get predicted Math Score instantly

---

## Project Structure

```text
MLProject/
│
├── artifacts/
├── notebook/
├── src/
│   ├── components/
│   ├── pipeline/
│   ├── exception.py
│   ├── logger.py
│   └── utils.py
│
├── templates/
│   ├── home.html
│   └── index.html
│
├── application.py
├── requirements.txt
├── setup.py
└── README.md
```

## Technologies Used

* Python
* Flask
* Scikit-Learn
* Pandas
* NumPy
* CatBoost
* XGBoost
* Azure App Service
* GitHub Actions

## Author

Rashmitha  Nakirikanti

Machine Learning Project - Student Performance Predictor
