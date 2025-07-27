# StackOverflow Data Pipeline: Wrangling, Feature Engineering, and ML Modeling

This project presents an end-to-end pipeline for working with raw StackOverflow XML data, involving extensive data wrangling, feature engineering, and supervised machine learning. It showcases practical data science techniques for turning noisy, unstructured data into meaningful predictive insights.

## Project Goals

- Convert StackOverflow XML files to structured CSV format
- Perform in-depth data wrangling and exploratory data analysis
- Engineer predictive features to enrich post metadata
- Train and evaluate multiple ML models to:
  - Predict whether a post will receive an accepted answer
  - Estimate the number of views a post will get

---

## Dataset

Data comes from the official [StackExchange Data Dump](https://archive.org/details/stackexchange), including:

- Posts.xml
- Users.xml
- Comments.xml
- Badges.xml, Votes.xml, Tags.xml, etc.

---

## Data Wrangling Workflow

- Parsed XML files using `ElementTree`
- Converted XML to CSV with consistent headers
- Loaded data into pandas DataFrames
- Merged relevant datasets (`Posts`, `Users`, `Comments`)
- Filtered for questions and cleaned missing or irrelevant entries

---

## Feature Engineering

Created features to enhance prediction quality:

- `TitleLength` and `BodyLength` from post content
- `NumTags` to capture tag richness
- `IsAnswered` (classification target)
- Log transformation of skewed numerical features
- Imputed missing values (e.g., `ViewCount`) using regression

---

## Machine Learning

### Models Implemented:

- Logistic Regression
- Random Forest Classifier
- Histogram-based Gradient Boosting (HGB)
- XGBoost Classifier
- LightGBM Classifier

### Techniques Used:

- **Handling Class Imbalance**: SMOTE, ADASYN, SMOTEENN, SMOTETomek
- **Model Tuning**: RandomizedSearchCV for hyperparameter optimization
- **Dimensionality Reduction**: PCA, t-SNE
- **Evaluation**:
  - Accuracy, Precision, Recall, F1
  - Confusion Matrices
  - ROC-AUC Score
  - SHAP for feature importance

---

## Visualizations

- Word and character length distributions
- t-SNE plots to visualize clustering
- Decision boundary plots
- SHAP summary and dependence plots

---

## Tools & Libraries

- Python (3.9+)
- pandas, numpy, matplotlib, seaborn
- scikit-learn
- imbalanced-learn
- XGBoost, LightGBM
- SHAP
- t-SNE, PCA

---

## Author

**Sehar Aejaz**  
seharaejaz@gmail.com  

---

##  Highlights

 End-to-end pipeline: from messy XML to clean ML-ready dataset  
 Feature engineering and missing value treatment  
 Multiple ML models with evaluation and explainability  
 A strong demonstration of data wrangling and predictive modeling skills

---

