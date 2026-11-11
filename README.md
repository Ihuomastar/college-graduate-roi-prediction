# Predicting High Return on Investment Among U.S. College Graduates

## Project Overview
This machine learning classification project analyzes 30,000 U.S. college graduate records to predict whether a graduate belongs to the high-return-on-investment (ROI) category. Using Python, the project compares Decision Tree and K-Nearest Neighbors (KNN) classifiers to evaluate their ability to identify high-ROI graduates.

Developed as a Group 3 academic project for CISA 5381, following the CRISP-DM framework.

## Research Objectives
- Predict high-ROI classification using graduate and educational characteristics.
- Explore associations involving college major, institution tier, internships, and geographic region.
- Compare model performance using accuracy, precision, recall, and F1-score.

## Dataset and Preparation
- 30,000 records and 18 original variables.
- High ROI defined as the top 25% of net ROI values.
- Data quality checks and categorical encoding.
- Stratified 80/20 training and testing split.
- Standardization for KNN.

## Machine Learning Methods
Two supervised classification models were evaluated:
- Decision Tree: maximum depth of 4.
- K-Nearest Neighbors: 21 neighbors.

Five-fold cross-validation on training data guided parameter selection using F1-score. Standardization was performed within each KNN cross-validation fold.

## Model Performance

| Model | Accuracy | Precision (High ROI) | Recall (High ROI) | F1-score (High ROI) |
|---|---:|---:|---:|---:|
| Decision Tree | 81.75% | 61.81% | 70.67% | 65.94% |
| KNN | 82.40% | 64.32% | 66.47% | 65.38% |

The majority-class accuracy baseline was 75%.

## Key Findings
- Electrical Engineering had a 66.32% high-ROI rate in the dataset.
- Ivy/Elite institutions had a 38.47% high-ROI rate.
- Graduates with internships had a 31.31% high-ROI rate, compared with 20.12% for those without internships.
- Regional differences were modest, with 25.73% in the Midwest and 24.21% in the South.

These are descriptive associations, not evidence of causation.

## Model Selection
Although KNN achieved slightly higher overall accuracy, Decision Tree achieved higher recall and F1-score for the high-ROI class. Decision Tree was selected because identifying high-ROI graduates was the primary classification objective.

## Tools and Skills
Python, pandas, scikit-learn, Jupyter Notebook, data cleaning, exploratory data analysis, classification, cross-validation, feature standardization, model evaluation, and analytical reporting.

## Limitations
The dataset may not represent all U.S. college graduates. High-ROI graduates account for only 25% of observations, and the findings should not be interpreted as causal relationships. External validation would be needed before real-world use.

## Project Files
- [Jupyter Notebook](College_Graduate_ROI_Analysis.ipynb) — complete Python analysis and model evaluation.

## Attribution
Group 3 academic Machine Learning project, CISA 5381. This repository presents the group's work for portfolio purposes; individual contributions should be distinguished from collaborative work.

