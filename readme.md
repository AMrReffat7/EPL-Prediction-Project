# ⚽ Premier League EDA & Match Outcome Prediction

A complete exploratory and predictive analysis of English Premier League (EPL) matches using post-match data, enriched with engineered features and optimized ML models.

---

## 📌 Project Overview

This project blends in-depth **EDA** and **machine learning** to uncover match trends and predict full-time results (Home Win, Draw, Away Win). It spans over 20 seasons of EPL data and extracts key tactical, offensive, and defensive insights.

---

## 📊 EDA Highlights

- **Defensive strength** ≠ stronger teams: Many efficient defensive teams use low-blocks and don't score much.
- **Draws** are strategic: Top teams often draw tough matches—an underrated success trait.
- **Goal ratios** indicate dominance: High scoring-to-conceding ratios reflect title contenders.
- **Disciplinary trends**: Away teams are consistently more aggressive and card-prone.
- **Shot volume ≠ more goals**: Increase in shots per game doesn’t translate to scoring booms.

---

## 🤖 ML Model Summary

- **Target:** `FullTimeResult` (H/D/A)
- **Features:** Match stats + engineered features like `AvgGoalsScored`, `WinRate`, `ShotConversion`, `DisciplinaryIndex`, `SeasonProgress`, etc.
- **Handling Imbalance:** SMOTE oversampling significantly improved draw classification.
- **Best Models:**

  - `MLPClassifier` (F1-Score: \~0.94 with SMOTE)
  - `GradientBoostingClassifier`
  - `Logistic Regression` (optimized via GridSearch)

---

## 📈 Engineered Features

- Team historical averages (goals scored/conceded, shot conversion)
- Tactical discipline (fouls, cards)
- Match context (season progress, end-of-season flag)
- Team encodings
- Shot, corner, and card differences

---

## 🔬 Tools Used

- **Python**, `pandas`, `seaborn`, `matplotlib`, `scikit-learn`, `imblearn`
- GridSearchCV for hyperparameter tuning
- Confusion matrices, classification reports, and precision/recall analysis

---

## 📁 Dataset

Structured match-level dataset including:

- `Season`, `MatchDate`, `HomeTeam`, `AwayTeam`
- Full-time & half-time goals
- Shots, fouls, cards, corners

---

## 📦 Output

- Trained models saved as `.pkl` files for deployment
- Classification metrics and confusion matrix visualizations
- Ready for extension into betting models or predictive dashboards
