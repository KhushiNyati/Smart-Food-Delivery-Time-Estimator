# Smart-Food-Delivery-Time-Estimator

##  Introduction  

Running a food delivery service comes with the challenge of keeping customers happy by ensuring their meals arrive on time and in good condition. However, factors like traffic congestion and bad weather can cause unpredictable delays, affecting the delivery schedule.  

To address this challenge, we have developed a **Food Delivery Time Prediction System** that utilizes **machine learning**. Our goal is to predict delivery times with high accuracy by analyzing past delivery data, current traffic conditions, and real-time weather updates.  

Additionally, we have built a **Command Line Interface (CLI)** that allows users to input key delivery parameters and receive estimated delivery times. The system categorizes delivery time predictions into the following ranges:  

-  Very Quick: ≤ 15 minutes  
-  Quick: 15–30 minutes  
-  Moderate: 30–45 minutes  
-  Slow: 45–60 minutes  
-  Very Slow: ≥ 60 minutes  

This tool helps food delivery services optimize logistics, improve customer satisfaction, and enhance operational efficiency.  


==============================

Build ML projects thatpredicts  fooddelivery time in minutes

Project Organization
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

##  Setting Up Datasets  

The datasets used in this project are available on **Kaggle**.  
Place the dataset files in the **datasets/** directory before running the model.  

##  Data Preprocessing  

The preprocessing steps include:  
1. Standardizing columns into appropriate formats: **strings, integers, and floats**.  
2. Converting **order date** to `datetime` format.  
3. Extracting time from **Time Ordered** and **Time Order Picked**.  
4. Dropping rows with **null values**.  
5. Encoding categorical variables using **label encoding**.  

##  Feature Selection  

Feature selection was performed using **SelectKBest**, which retains only the most significant predictors.  
The implementation is available in `kbest.py`.  

##  Model Improvement  

The following techniques were applied to enhance model performance:  
- **Hyperparameter Tuning**: Optimized model parameters using **GridSearchCV**.  

##  Command Line Interface (CLI)  

To use the CLI for predictions:  

1. Navigate to the project directory.  
2. Run the CLI script:  
   ```bash
   python main.py

Follow the prompts to input the delivery parameters and obtain predictions.

## Model Evaluation Results  

| Model                        | MSE   | R² Score |
|------------------------------|-------|----------|
| **Linear Regression**        | 42.80 | 0.51     |
| **Decision Tree**            | 41.14 | 0.53     |
| **Decision Tree (Bagging)**  | 21.67 | 0.75     |
| **Random Forest**            | 21.21 | 0.75     |
| **Elastic Net Regularization** | 47.35 | 0.46     |
| **LightGBM**                 | 16.88 | 0.80     |
| **XGBoost**                  | 18.41 | 0.79     |

The developed **LightGBM model** demonstrates promising accuracy and generalization capabilities, making it a reliable choice for **predicting delivery times** in food delivery services.  

##  Conclusion  

The **LightGBM model** achieves the high accuracy and strong generalization, making it the **most suitable model** for predicting food delivery times effectively.  

