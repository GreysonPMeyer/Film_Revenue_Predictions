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
bash
Copy
Edit
.
├── data/                   # (Not committed) Raw and cleaned TMDB 5000 data
├── notebooks/              # Jupyter notebooks for EDA, modeling, and evaluation
├── models/                 # Saved model artifacts (optional)
├── results/                # Plots, tables, and metrics
├── requirements.txt        # Environment dependencies
└── README.md               # Project overview
🔍 The notebooks are organized so that running them in order (top to bottom) will reproduce the full analysis and modeling pipeline.

## Getting Started
Clone this repository:

bash
Copy
Edit
git clone https://github.com/yourusername/film-revenue-prediction.git
cd film-revenue-prediction
Install required packages:

bash
Copy
Edit
pip install -r requirements.txt
Download the dataset from Kaggle and place it in the data/ directory.

Open and run the Jupyter notebooks in order to explore the full workflow.

📌 Future Plans
* Expand exploratory and model analysis using Tableau
* Investigate ensemble techniques or stacked models
* Deploy a simple app or dashboard for real-time prediction
