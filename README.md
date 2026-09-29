# Ames Housing Data Preprocessing & EDA

## Overview
This project demonstrates an end-to-end data preprocessing and exploratory data analysis (EDA) pipeline using the Ames Housing dataset. It focuses on cleaning, transforming, and visualizing residential home sale records to prepare the data for machine learning models. 

This repository also contains the original assignment brief (`Ames_Housing_Assignment_Brief.pdf`), which outlines the specific preprocessing requirements and methodologies implemented in this project.

## Repository Structure
* `data_preprocessing.ipynb`: The main Jupyter Notebook containing all code, visualizations, and markdown explanations.
* `Ames_Housing_Assignment_Brief.pdf`: The original assignment requirements and guidelines.
* `requirements.txt`: The list of Python dependencies required to run the notebook.
* `.gitignore`: Specifies intentionally untracked files (such as the raw dataset and local environments).

## Dataset
The dataset contains 1,460 residential home sale records from Ames, Iowa, featuring 80 independent variables and 1 target variable (`SalePrice`). It includes a mix of numerical and categorical variables describing every aspect of the homes.

## Key Techniques Applied
* **Missing Value Handling:** Differentiated between MCAR, MAR, and MNAR data. Applied median imputation for geographical features and categorical labeling for structural absences (e.g., "None" for missing PoolQC).
* **Outlier Treatment:** Utilized Z-score and IQR statistical methods, coupled with visual scatter plot detection, to remove erroneous extremes and winsorize heavily skewed features like LotArea.
* **Feature Engineering:** Created composite variables (TotalSF, TotalBathrooms, HouseAge) and applied conditional logic for binary flags (IsRemodeled).
* **Categorical Encoding:** Applied label encoding for ordinal quality metrics and one-hot encoding for nominal variables (Neighborhood, HouseStyle).
* **Feature Scaling:** Implemented and compared Min-Max Scaling and Standard Scaling on continuous variables.
* **Correlation Analysis:** Computed Pearson and Spearman correlation matrices to identify multicollinearity and the strongest positive/negative predictors of SalePrice.

## Technologies Used
* Python
* Pandas & NumPy (Data Manipulation)
* Matplotlib & Seaborn (Data Visualization)
* Scikit-Learn (Imputation, Scaling)

## How to Run
1. Clone this repository.
2. Install the required dependencies: `pip install -r requirements.txt`
3. Download the `train.csv` dataset from [Kaggle](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data) and place it in the root directory.
4. Execute `data_preprocessing.ipynb` top-to-bottom.
