# Early-Game Match Outcome Prediction in League of Legends

Can the outcome of a League of Legends match be predicted using only the first 10 minutes of gameplay?

This project explores the predictive power of early-game performance metrics in high-ranked League of Legends matches using dimensionality reduction, clustering, and supervised machine learning techniques.

---

## Project Overview

The dataset contains approximately 10,000 ranked matches and includes a variety of features describing the state of the game at the 10-minute mark, such as:

- Gold and experience differences
- Kills and deaths
- Objective control (e.g., buffs)
- Lane and jungle performance metrics

Each observation represents a single match, with 38 features capturing early-game dynamics.  
The target variable (`blueWins`) indicates whether the blue team ultimately won the match.

The goal of this analysis is to determine how informative early-game performance is with respect to the final match outcome.

---

## Methods

The analysis includes:

- Exploratory Data Analysis (EDA)
- Feature scaling and preprocessing
- Principal Component Analysis (PCA)
- K-Means clustering in reduced feature space
- Random Forest classification
- Stratified K-Fold cross-validation
- Model evaluation via confusion matrix and ROC curve

---

## Results

The final Random Forest classifier achieved:

- **Accuracy:** ~72% on held-out test data  
- **ROC-AUC:** 0.81  

These results suggest that early-game performance metrics contain meaningful predictive information about the final outcome of a match, despite predictions being made using only the first 10 minutes of gameplay.

---

## Repository Contents

- `early_game_win_prediction_LoL.ipynb` – Full analysis pipeline, including preprocessing, dimensionality reduction, clustering, and classification.

---

## Reproducibility

To reproduce the analysis locally:

1. Install the required Python libraries
2. Obtain the kaggle dataset from https://www.kaggle.com/datasets/bobbyscience/league-of-legends-diamond-ranked-games-10-min

