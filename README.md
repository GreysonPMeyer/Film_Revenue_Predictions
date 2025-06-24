# Film Revenue Prediction
This repository contains a data science project aimed at predicting the gross revenue of films using the TMDB 5000 Movie Dataset from Kaggle. The objective is to evaluate a suite of regression models and determine which performs best in forecasting a movie’s box office performance.

## Project Overview
The "data" folder contains all of the relevant data
Data cleaning & feature engineering are handled in the feature_engineering.ipynb file. The following are some of the features I created/altered in order to enhance predictive capabilities:
* One-hot encoded the 10 most common genres
* Created "summer blockbuster", "award season" and "winter low season" buckets
* Created a one-hot encoded column for whether a film is a sequel
* Counted the number of previous films by each director
* One-hot encoded the film distributors
* Average revenue for the director and top 3 cast members of each film (being careful of data leakage in the process)

Modeling: The following models were trained on the dataset and had their prediction power evaluated.
* Ridge
* Lasso
* Elastic Net
* Random Rorest Regressor
* XGBoost Regressor
* LightGBM regressor
* K-Nearest Neighbors Regressor

All models were tuned using cross-validation to ensure fair and robust comparisons.

Evaluation: Comparing models using Root Mean Squared Error (RMSE), Mean Absolute Error (MAE) and R² score.
Summary results and visual comparisons are included in the Jupyter notebooks.

## Repository Structure

* data/                      # Contains the relevant datasets
* feature_engineering.ipynb  # Notebook for cleaning and preparing the data
* model_selection.ipynb      # Notebook for training and evaluating regression models
* README.md                  # Project overview


## Getting Started
Clone this repository:

* git clone https://github.com/GreysonPMeyer/Film_Revenue_Predictions.git
* cd film_revenue_prediction
  
Install required packages:
* pip install -r requirements.txt

Open and run the Jupyter notebooks in order to explore the full workflow.

📌 Future Plans
* Expand exploratory and model analysis using Tableau
* Investigate ensemble techniques or stacked models
* Deploy a simple app or dashboard for real-time prediction
