# 🚲 Bike Rental Demand Prediction – Azure ML Studio Project

Hi, I'm **Asanda Ndlela**, a final-year Applied Mathematics and Statistics student at UKZN and an aspiring Data Scientist. This is an entry-level machine learning project developed using **Azure Machine Learning Studio**, where I trained and evaluated a model to predict bike rental demand based on various environmental and seasonal features.

---

## 🧠 Project Overview

The goal of this project was to predict the **number of bikes rented** on a given day using historical data and machine learning models within **Azure ML Studio**. This end-to-end workflow involved data preprocessing, feature engineering, model training, and evaluation – all done in a code-free, drag-and-drop environment.

---

## 🔧 Tools & Technologies
- **Azure Machine Learning Studio (Classic)** – cloud-based environment for building and deploying ML models
- **Bike Rental UCI Dataset** – open dataset containing daily records of bike rental counts and associated weather/seasonal features
- **Regression Models** – such as Linear Regression and Decision Forest Regression
- **Data Preprocessing** – feature selection, normalization, data splitting

---

## 📊 Key Features in the Workflow

1. **Data Cleaning and Preparation**
   - Removed irrelevant columns (e.g. index, casual vs. registered counts)
   - Handled null or inconsistent values
   - Converted categorical variables where necessary

2. **Feature Selection**
   - Included key predictors like temperature, humidity, season, holiday indicators, and working day flags

3. **Model Training**
   - Trained multiple regression models:
     - Linear Regression
     - Decision Forest Regression
     - Boosted Decision Tree Regression
   - Tuned hyperparameters using drag-and-drop modules

4. **Model Evaluation**
   - Compared model performance using:
     - **RMSE** (Root Mean Squared Error)
     - **MAE** (Mean Absolute Error)
     - **R² Score**
   - Best-performing model selected based on lowest RMSE

5. **Deployment Readiness**
   - Prepared trained model for scoring and possible web service deployment (optional stage in Azure ML)

---

## 📈 What I Learned
- How to navigate and use Azure ML Studio’s visual interface
- Key concepts in model evaluation (e.g. RMSE, R²)
- Data preprocessing techniques like normalization and feature selection
- The importance of testing different models and comparing results

---

## 📂 Project Files
> _Note: Due to Azure ML Studio being cloud-based, most of the workflow is saved in the Azure workspace. Screenshots or exported pipeline images can be included here._

- `Pipeline_Screenshot_1.png` – Azure pipeline structure
- `Model_Comparison.png` – Evaluation metrics for selected models
- `Feature_Schema.png` – Final features used in training

---

## 📝 Still a Work in Progress

This is one of my early explorations into machine learning using cloud tools. I plan to later recreate this pipeline using Python (scikit-learn) in Jupyter Notebooks to deepen my understanding of the same workflow with code.

> 🙌 Thank you for checking out this project!

