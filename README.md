# Heart_disease_prediction
# Heart Disease Prediction

A beginner-friendly Machine Learning project that predicts the risk of heart disease from selected patient health parameters. The project covers the complete ML workflow, from exploratory data analysis and data preprocessing to model training, evaluation, model serialization, and deployment through a Streamlit web application.

> **Note:** This project is for educational purposes only and should not be used as a medical diagnostic tool.

## Project Overview

The project uses patient-related features such as age, sex, chest pain type, resting blood pressure, cholesterol, fasting blood sugar, resting ECG, maximum heart rate, exercise-induced angina, oldpeak, and ST slope to predict whether the input indicates a higher or lower risk of heart disease.

The trained Logistic Regression model is integrated into a Streamlit application where users can enter these values and receive a prediction.

## Workflow

1. Load the heart disease dataset using Pandas.
2. Perform Exploratory Data Analysis (EDA).
3. Check dataset shape, information, statistics, duplicates, and missing values.
4. Visualize important feature distributions and relationships with the target.
5. Handle zero values in `Cholesterol` and `RestingBP` using mean-based replacement.
6. Convert categorical variables into numerical features using one-hot encoding.
7. Standardize numerical features using `StandardScaler`.
8. Split the dataset into training and testing sets.
9. Train and compare multiple classification models.
10. Evaluate models using Accuracy and F1 Score.
11. Save the trained Logistic Regression model and preprocessing information using Joblib.
12. Build a Streamlit interface for making predictions on new user input.

## Machine Learning Models

The notebook experiments with the following classification algorithms:

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Gaussian Naive Bayes
- Decision Tree Classifier
- Support Vector Machine (SVM with RBF Kernel)

The deployed application uses **Logistic Regression**.

## Input Features

The Streamlit application accepts the following inputs:

| Feature | Description |
|---|---|
| Age | Age of the person |
| Sex | Biological sex value used by the dataset |
| Chest Pain Type | Type of chest pain |
| Resting BP | Resting blood pressure |
| Cholesterol | Cholesterol level |
| Fasting BS | Whether fasting blood sugar is above 120 mg/dL |
| Resting ECG | Resting electrocardiogram result |
| Max HR | Maximum heart rate |
| Exercise Angina | Exercise-induced angina |
| Oldpeak | ST depression value |
| ST Slope | Slope of the ST segment |

## Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Streamlit

## Project Structure

```text
heart-disease-prediction/
│
├── heart.ipynb
├── app.py
├── heart.csv
│
├── Logistic_Regression.pkl
├── heart_scaler.pkl
├── heart_columns.pkl
│
└── README.md
```

The exact filenames of the saved model/preprocessing files should match the filenames referenced in `app.py`.

## Running the Project Locally

### 1. Clone the repository

```bash
git clone <your-github-repository-url>
cd heart-disease-prediction
```

### 2. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib streamlit
```

### 3. Run the Streamlit application

```bash
streamlit run app.py
```

The application will open in your browser.

## Model Evaluation

The notebook evaluates the classification models using:

- **Accuracy Score**
- **F1 Score**
- Classification report

The project compares multiple models before selecting Logistic Regression for the deployed application.

## What I Learned

Through this project, I practiced:

- Exploratory Data Analysis
- Data cleaning and preprocessing
- Handling categorical variables
- Feature scaling
- Train-test splitting
- Classification algorithms
- Model evaluation
- Saving ML models with Joblib
- Connecting a trained ML model with a Streamlit frontend
- Building an end-to-end beginner Machine Learning project

