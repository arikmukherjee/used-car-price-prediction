# Used Car Price Prediction

This repository contains a reproducible notebook-based workflow for exploring and modeling used car prices. The project demonstrates end-to-end steps: data loading, exploratory data analysis (EDA), feature engineering, model training, and evaluation.

Files
- [15-Used_Car_Price_Prediction_Spring_2026.ipynb](15-Used_Car_Price_Prediction_Spring_2026.ipynb) — Jupyter notebook with the full analysis and modeling pipeline.
- [used_cars.csv](used_cars.csv) — Dataset used for experiments.

Quick start

1. Create and activate a Python virtual environment (recommended):

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS / Linux
source .venv/bin/activate
```

2. Install the common data science packages used in the notebook:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyterlab
```

3. Open the notebook and run the cells interactively:

```bash
jupyter lab  # or `jupyter notebook`
```

What the notebook contains
- Data loading and basic validation of [used_cars.csv](used_cars.csv).
- Exploratory data analysis (distributions, correlations, missing values).
- Feature engineering and preprocessing (encoding, scaling, date handling).
- Model training examples (linear models, tree-based models, ensemble methods).
- Model evaluation using RMSE and R², plus residual analysis.

Reproducibility
- The notebook is self-contained and aims to run top-to-bottom when the required packages are installed.
- If you want repeatable results, set random seeds where noted in the notebook before training.

Suggestions & next steps
- Add a `requirements.txt` or `environment.yml` for exact dependencies.
- Extract modeling code into scripts or a small package for experiments and hyperparameter tuning.
- Log experiments (e.g., with MLflow or Weights & Biases) for systematic comparison.

License & contact
- This project is provided for learning and experimentation.

Notebook summary

This project notebook ([15-Used_Car_Price_Prediction_Spring_2026.ipynb](15-Used_Car_Price_Prediction_Spring_2026.ipynb)) contains a step-by-step workflow and the following highlights:

- Objective: Predict used car prices using regression models and demonstrate basic ML engineering steps.
- Author: Suprava Das (internship project for IDEAS Summer 2026).
- Data: `used_cars.csv` is loaded, shuffled, and inspected for missing values and data types.
- Cleaning & feature engineering: standardizes string placeholders, creates `car_age` from `model_year`, converts `milage` and `price` to numeric types, and removes the `clean_title` column.
- Categorical handling: groups rare categories (<1%) in `transmission` and `ext_col` as `others`, then label-encodes categorical columns.
- Outliers: filters out prices above the 99th percentile.
- Modeling: trains a `RandomForestRegressor` (n=100) with an 80/20 train-test split; evaluates using R², MSE, and MAE (run the notebook to see numeric results).
- Additional tasks: demonstrates loading the MNIST dataset, applies K-Means clustering (k=10), and evaluates clustering with a mapped-label macro F1 score.
- Visualizations: price distribution, mileage vs price scatter, average price by car age, correlation heatmap, and transmission-type bar chart.

Reproduce results by opening the notebook and running the cells; metric values depend on the dataset and preprocessing steps.

