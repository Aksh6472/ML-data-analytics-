# ML-data-analytics-
# Energy Consumption Prediction Using Linear Regression

## Overview

This project develops a machine learning model to predict energy consumption based on building operational and environmental features. The dataset is preprocessed by handling duplicates, encoding categorical variables, and standardizing numerical features before training a Linear Regression model. The model's performance is evaluated using multiple regression metrics and validated through 5-fold cross-validation.

## Objectives

* Preprocess and clean the dataset.
* Encode categorical features for machine learning.
* Standardize input features.
* Train a Linear Regression model.
* Evaluate model performance using standard regression metrics.
* Validate model generalization using cross-validation.

## Technologies Used

* Python
* Google Colab
* Pandas
* NumPy
* Scikit-learn

## Dataset

The project uses the **Energy_consumption.csv** dataset.

### Target Variable

* **EnergyConsumption**

### Feature Variables

The dataset includes features such as:

* HVACUsage
* LightingUsage
* DayOfWeek
* Holiday
* Timestamp (removed before training if present)
* Additional numerical attributes related to energy consumption

## Methodology

### Data Preprocessing

The following preprocessing steps were performed:

* Loaded the dataset using Pandas.
* Checked for missing values.
* Removed duplicate records.
* Encoded categorical variables using `LabelEncoder`.
* Removed the `Timestamp` column before training (if available).
* Standardized the feature set using `StandardScaler`.

### Model Development

The processed dataset was divided into training and testing sets using an 80:20 split. A Linear Regression model from Scikit-learn was trained on the training data and used to predict energy consumption on the test set.

### Model Evaluation

The model was evaluated using the following metrics:

* Mean Absolute Error (MAE)
* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)
* Coefficient of Determination (R² Score)

To assess model stability and generalization, 5-fold cross-validation was performed.

## Project Structure

```text
Energy-Consumption-Prediction/
│
├── Energy_consumption.csv
├── Energy_Consumption_Prediction.ipynb
├── README.md
└── requirements.txt
```

## Installation

Clone the repository:

```bash
git clone https://github.com/<your-username>/Energy-Consumption-Prediction.git
```

Navigate to the project directory:

```bash
cd Energy-Consumption-Prediction
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

## Running the Project

1. Place `Energy_consumption.csv` in the project directory.
2. Open `Energy_Consumption_Prediction.ipynb` in Google Colab or Jupyter Notebook.
3. Execute all cells sequentially.
4. Review the generated predictions and evaluation metrics.

## Future Enhancements

Potential improvements include:

* Comparing multiple regression algorithms such as Random Forest, XGBoost, and Gradient Boosting.
* Performing feature engineering and feature selection.
* Applying hyperparameter optimization.
* Building a web application using Streamlit or Flask for interactive predictions.
* Deploying the trained model as a REST API.
