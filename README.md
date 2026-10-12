# Customer Shopping Trends Analysis

### Exploratory Data Analysis · Customer Behaviour · Machine Learning · Python

Analysed **3,900 shopping records across 50 US states** to investigate purchasing patterns, explore geographic similarities, and compare machine learning approaches to customer spending analysis.

This academic project demonstrates data preparation, visualisation, clustering, classification, regression, and critical evaluation of model results.

- **Author:** Darren Alexander
- **Course:** Machine Learning | University of London, SIM Global Education
- **Period:** January–April 2026

## Project Objectives

- Explore purchasing patterns across product categories, payment methods, and locations.
- Group states with similar shopping characteristics using K-Means clustering.
- Compare models for classifying above-median spending and predicting purchase amounts.
- Evaluate whether the results support reliable business conclusions.

## Key Findings

| Finding | Result | Interpretation |
| --- | --- | --- |
| Most frequently purchased category | Clothing represented **1,737 records (44.5%)** | Clothing was the largest category in this dataset. |
| Digital payment usage | PayPal and Venmo accounted for **1,291 records (33.1%)** | These two methods represented approximately one-third of recorded purchases. |
| Geographic coverage | **50 US states** | State-level summaries enabled comparison of spending and purchasing characteristics. |
| Predictive modelling | Compared **5 classification and 5 regression models** | Explored alternative approaches to spending classification and prediction. |

These findings describe the dataset; they do not establish population-wide consumer behaviour or proven commercial impact.

## Analytical Approach

### 1. Data Preparation and Exploration

- Used pandas and NumPy to inspect, transform, and summarise shopping records.
- Encoded categorical variables and applied feature scaling for relevant models.
- Created visualisations of product preferences, payment methods, and geographic patterns.

### 2. Geographic Segmentation

- Aggregated purchase amounts and customer characteristics by state.
- Applied Min-Max scaling and K-Means clustering.
- Used the elbow method and silhouette analysis to evaluate clustering.
- Created an interactive Folium map of regional purchase counts.

### 3. Classification and Regression

- Compared Random Forest, AdaBoost, K-Nearest Neighbours, Support Vector Machine, and Decision Tree classifiers.
- Compared Linear Regression, Random Forest, AdaBoost, Support Vector Regression, and Decision Tree regression.
- Used an **80/20 training–test split**.
- Applied **3-fold cross-validation** through GridSearchCV to tune the Random Forest classifier.

## Model Limitations and Next Steps

The current notebook includes a target-derived feature, `Avg_Purchase_Amount`, calculated using `Purchase Amount (USD)`. Because purchase amount is also the regression target and determines the classification label, this introduces **target leakage into both modelling tasks**.

The reported predictive scores therefore should not be interpreted as reliable performance on unseen customers. A corrected evaluation would remove this feature, fit preprocessing only on training data, and rerun model comparison and validation.

State-level clusters should also be treated as exploratory groupings, with their usefulness assessed before informing targeting decisions.

## Tools and Skills

**Python · pandas · NumPy · scikit-learn · Matplotlib · Seaborn · Folium · Jupyter Notebook**

Skills demonstrated include:

- Exploratory data analysis
- Data preprocessing and feature engineering
- Data visualisation
- K-Means clustering
- Classification and regression
- Hyperparameter tuning
- Model evaluation and identification of target leakage

## Project Files

| File | Contents |
| --- | --- |
| Analysis notebook (`.ipynb`) | Python workflow, visualisations, and model comparisons |
| Project report (`.pdf`) | Detailed methodology, findings, and discussion |
| Shopping dataset (`.csv`) | Shopping records used in the analysis |
| Regional map (`.html`) | Interactive map; download and open in a browser |

## How to Explore This Project

1. Start with the PDF report for the methodology and findings.
2. Open the notebook to review the analytical workflow.
3. To run the notebook locally, keep the dataset named `shopping_trends.csv` in the same folder as the notebook and install the imported Python libraries.
4. Download the HTML map and open it in a browser to explore regional purchase counts.
5. Read the model limitations before interpreting predictive scores.

## Data Source

[Customer Shopping Trends Dataset — Kaggle, Sourav Banerjee](https://www.kaggle.com/datasets/iamsouravbanerjee/customer-shopping-trends-dataset)

---

Created as academic coursework and presented as a data analytics portfolio project.
