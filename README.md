# Machine Learning Journey

My personal repository for learning and practicing Machine Learning.

This repository contains my notes, implementations, experiments, competition workflows, and projects throughout my learning journey.


## Machine Learning Competition Workflow

A general workflow I follow when participating in Machine Learning competitions, such as Kaggle.

### 1. Understand the Competition
- Identify the problem type: Classification, Regression, or Ranking.
- Understand the evaluation metric (Accuracy, F1, AUC, RMSE, MAE, Log Loss, QWK, etc.).
- Read competition rules, submission limits, and data restrictions.

### 2. Exploratory Data Analysis (EDA)
- Inspect dataset shape, data types, and statistical summaries.
- Check missing values, duplicates, and outliers.
- Analyze target distribution and class imbalance.
- Explore feature-target relationships and correlations.
- Compare train and test distributions.

### 3. Validation Strategy
- Choose an appropriate validation method:
  - K-Fold
  - StratifiedKFold
  - GroupKFold
  - TimeSeriesSplit
- Ensure validation reflects the competition's evaluation setting.
- Fix random seeds for reproducibility.

### 4. Baseline Model
- Build a simple preprocessing pipeline.
- Train an initial model.
- Establish a baseline CV score.
- Generate an initial submission to verify the pipeline.

### 5. Data Preprocessing
- Handle missing values.
- Encode categorical variables.
- Scale numerical features when necessary.
- Handle outliers and skewed distributions.
- Prevent data leakage by fitting preprocessing only on training folds.

### 6. Feature Engineering
- Create interaction features and feature combinations.
- Generate statistical features using groupby.
- Extract date and time features.
- Apply frequency encoding, binning, and polynomial features.
- Validate every new feature using cross-validation.

### 7. Feature Selection
- Analyze feature importance.
- Use permutation importance or SHAP when appropriate.
- Remove irrelevant or redundant features.
- Check for data leakage.

### 8. Model Training
For tabular data, explore models such as:

1. Gradient Boosting: LightGBM, XGBoost, CatBoost.
2. Random Forest and ExtraTrees.
3. Linear Models: Ridge, Lasso, Logistic Regression.
4. SVM and KNN when appropriate.

Use cross-validation and early stopping where applicable.

### 9. Hyperparameter Tuning
- Use Optuna or Randomized Search.
- Tune important model parameters.
- Compare tuned models against the baseline.
- Avoid excessive tuning before establishing a reliable validation pipeline.

### 10. Special Techniques
- Class imbalance: class weights, threshold optimization, and SMOTE when appropriate.
- Skewed regression targets: log transformation and inverse transformation.
- Special metrics: optimize decision thresholds or prediction cutoffs when necessary.

### 11. Ensemble Learning
- Averaging and weighted averaging.
- Stacking with out-of-fold predictions.
- Combine diverse models and feature sets.
- Evaluate whether ensembling actually improves CV performance.

### 12. Prediction & Submission
- Generate test predictions using trained fold models.
- Check submission format, column names, IDs, and row count.
- Save experiment results and compare different submissions.
- Track CV and leaderboard scores.

## Tools

### Languages & Libraries

Reference libraries for machine learning and AI competitions, based on the OlpAI'25 guidelines and the expected OlpAI'26 environment.

| Category | Libraries |
|---|---|
| Machine Learning / NLP | PyTorch, TensorFlow, Scikit-learn, XGBoost, CatBoost, Transformers, spaCy, NLTK, Gensim, FastText |
| Data Processing | Pandas, NumPy, SciPy, CSV, JSON, Pickle |
| Image Processing | OpenCV, Pillow, Torchvision, Scikit-image |
| Visualization | Matplotlib, Seaborn, Plotly, AutoViz |
| Utilities | Joblib, Datasets, Evaluate, OS, Sys, Re, Itertools, Collections, Time, PDB, PyTorch Lightning, TensorBoard, tqdm |

*Note: The OlpAI'26 environment and supported library versions may differ from this reference.*

## Goals

- Understand Machine Learning fundamentals.
- Practice implementing ML algorithms.
- Improve model evaluation and optimization skills.
- Build practical Machine Learning projects.
- Develop better problem-solving skills through competitions.

