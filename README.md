# Titanic Survival Analysis and Prediction

This project explores the Titanic dataset, cleans and prepares the data, trains machine learning models, and predicts whether a passenger is likely to survive.

I built this project as a full mini-pipeline:

- inspect and visualize passenger data
- encode categorical features
- train/test split
- train classification models
- evaluate model accuracy
- run an interactive survival predictor

## What I Did

### 1) Loaded and checked the cleaned dataset

- Read `clean_data.csv` with pandas
- Verified missing values

### 2) Explored data visually

I created quick plots to understand patterns:

- Survival count plot
- Survival by gender
- Age distribution

### 3) Prepared features for modeling

- Used `LabelEncoder` to convert `sex` from text into numeric values
- Selected core features:
  - `pclass`
  - `sex`
  - `age`
  - `fare`
- Target column used for prediction:
  - `survived`

### 4) Trained machine learning models

I trained two classifiers:

- Logistic Regression
- Random Forest Classifier

### 5) Evaluated model performance

- Split data into train and test sets
- Computed accuracy using `accuracy_score`

### 6) Built an interactive predictor in notebook

Using `ipywidgets`, I added controls for:

- passenger class
- sex
- age
- fare

When you click the button, the notebook predicts:

- survival result (Yes/No)
- survival probability (percentage)

## What This Project Predicts

The model predicts whether a passenger with given characteristics would likely survive the Titanic disaster.

Input features:

- Passenger class (`pclass`)
- Sex (`sex`)
- Age (`age`)
- Ticket fare (`fare`)

Output:

- Class prediction: survived or not survived
- Confidence/probability of survival

## What It Is Expected To Do

Given realistic passenger details, the trained model should:

- estimate survival likelihood based on learned patterns
- perform reasonably well on similar Titanic-like data
- provide quick interactive predictions through the notebook interface

Important note:
This is an educational machine learning project. Predictions are pattern-based estimates from historical data, not guaranteed truths.

## Project Files

- `clean_data.csv` -> cleaned input dataset
- `train_and_test2.csv` -> additional data file used during the workflow
- `cleaning.ipynb` -> data cleaning notebook
- `cleaned.ipynb` -> analysis, modeling, and interactive prediction notebook

## How To Run

1. Open `cleaned.ipynb`
2. Run all cells from top to bottom
3. Train the model cells
4. Use the widget panel to test custom passenger inputs

## Main Libraries Used

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- ipywidgets
