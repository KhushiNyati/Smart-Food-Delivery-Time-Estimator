Smart-Food-Delivery-Time-Estimator
==============================

# 🍽️ Smart Food Delivery Time Estimator

Smart Food Delivery Time Estimator is a machine learning-based project that predicts the estimated delivery time for food orders. This model utilizes features such as weather, traffic density, restaurant location, and delivery distance to provide accurate predictions, improving customer experience in food delivery services.

## 🚀 Project Overview

The goal of this project is to estimate the delivery time of food orders based on various factors that influence delivery time. By leveraging machine learning models, the system can provide accurate delivery time predictions and optimize delivery routes for food delivery platforms.

### Key Features:
- **Prediction:** Delivery time estimation based on multiple features.
- **Models Used:** Linear Regression, Random Forest, XGBoost, LightGBM, and Stacking Regressor.
- **Data Cleaning:** Handling missing data, outlier detection, and feature engineering.
- **Hyperparameter Tuning:** Extensive tuning of Random Forest, LightGBM, and Stacking Regressor models.
- **Model Selection:** Choosing the best performing model based on evaluation metrics like MAE, RMSE, and R².

## 🧠 Tech Stack

- **Language:** Python
- **Libraries:** Pandas, NumPy, Scikit-learn, MLFlow, XGBoost, LightGBM, Matplotlib
- **Version Control:** Git, DVC
- **IDE:** VS Code
- **Modeling:** Regression models, Hyperparameter tuning, Stacking models

## 📁 Project Structure


------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io

    
## 📊 Model Performance

The following models were trained and evaluated on the data:

- **Linear Regression**
- **Random Forest**
- **XGBoost**
- **LightGBM**
- **Stacking Regressor**

### Hyperparameter Tuning:
- **Random Forest**: Optimized the number of trees (`n_estimators`), max depth, and other important hyperparameters.
- **LightGBM**: Tuned parameters like `learning_rate`, `num_leaves`, and `max_depth`.
- **Stacking Regressor**: Combined multiple models with tuned hyperparameters to improve prediction accuracy.

## ✅ Features

- **Data Cleaning**: Missing data handling, feature scaling, and outlier detection.
- **Exploratory Data Analysis (EDA)**: In-depth analysis of the dataset to find insights and trends.
- **Model Selection**: Comparison of different regression models using metrics like MAE, RMSE, and R².
- **Hyperparameter Tuning**: Use of grid search and random search techniques for fine-tuning models.
- **Final Estimator**: A stacked model that combines the best of Random Forest, XGBoost, and LightGBM.

## 🏁 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Smart-Food-Delivery-Time-Estimator.git
   cd Smart-Food-Delivery-Time-Estimator
2. Install dependencies:
   ```bash
   pip install -r requirements-dev.txt
3. Pull the dataset (via DVC):
   ```bash
   dvc pull
   
4. Run the Jupyter Notebooks for EDA, model training, and evaluation:


Swiggy.csv - https://raw.githubusercontent.com/KhushiNyati/Smart-Food-Delivery-Time-Estimator/refs/heads/main/swiggy.csv

Food-Delivery-Data-Cleaning - https://github.com/KhushiNyati/Smart-Food-Delivery-Time-Estimator/blob/main/Food_Delivery_Data_Cleaning.ipynb

Food Delivery EDA - https://github.com/KhushiNyati/Smart-Food-Delivery-Time-Estimator/blob/main/Food_Delivery_EDA.ipynb

Data-clean-utils.py - https://github.com/KhushiNyati/Smart-Food-Delivery-Time-Estimator/blob/main/data_clean_utils.py

Food Delivery Baseline Mode -  https://github.com/KhushiNyati/Smart-Food-Delivery-Time-Estimator/blob/main/Food_Delivery_Baseline_Model.ipynb

Food Delivery Exp 1 drop vs impute.ipynb - https://github.com/KhushiNyati/Smart-Food-Delivery-Time-Estimator/blob/main/Food_Delivery_Exp_1_drop_vs_impute.ipynb
![Screenshot 2025-04-14 000302](https://github.com/user-attachments/assets/07b06994-89a3-4868-a765-b1e5b577da4d)


Food_Delivery_Exp_2_missing_indicator.ipynb - https://github.com/KhushiNyati/Smart-Food-Delivery-Time-Estimator/blob/main/Food_Delivery_Exp_2_missing_indicator.ipynb
![Screenshot 2025-04-14 000113](https://github.com/user-attachments/assets/d9c14971-f3ed-499e-9dc1-0a3eac885089)


Food Delivery Model Selection - https://github.com/KhushiNyati/Smart-Food-Delivery-Time-Estimator/blob/main/Food_Delivery_Model_Selection.ipynb

Food_Delivery_LGBM_HP_Tuning - https://github.com/KhushiNyati/Smart-Food-Delivery-Time-Estimator/blob/main/Food_Delivery_LGBM_HP_Tuning.ipynb
![Screenshot 2025-04-14 003254](https://github.com/user-attachments/assets/0bc4fa8e-c827-4d45-944e-d15e3ebd55aa)
![Screenshot 2025-04-14 003309](https://github.com/user-attachments/assets/6d955e70-60a7-40bd-beae-a8a3b3ad56a9)

Food Delivery RF HP Tuning.ipynb - https://github.com/KhushiNyati/Smart-Food-Delivery-Time-Estimator/blob/main/Food_Delivery_RF_HP_Tuning.ipynb
![Screenshot 2025-04-14 011526](https://github.com/user-attachments/assets/064e71d6-3bb5-428c-a361-d8337faa2f37)

Food Delivery Stacking Regressor HP Tuning.ipynb - https://github.com/KhushiNyati/Smart-Food-Delivery-Time-Estimator/blob/main/Food_Delivery_Stacking_Regressor_HP_Tuning.ipynb

Food Delivery Final Estimator - https://github.com/KhushiNyati/Smart-Food-Delivery-Time-Estimator/blob/main/Food_Delivery_Final_Estimator.ipynb


<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
