# Predicting High Return on Investment Among U.S. College Graduates

## Project Overview
This machine learning classification project analyzes 30,000 synthetic U.S. college graduate records to predict whether a graduate belongs to the high-return-on-investment (ROI) category. Using Python, the project compares Decision Tree and K-Nearest Neighbors (KNN) classifiers to evaluate their ability to identify high-ROI graduates.

The analysis follows the Cross-Industry Standard Process for Data Mining (CRISP-DM) framework and was developed as a Group 3 academic project for CISA 5381.

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
- [Jupyter Notebook](notebooks/College_Graduate_ROI_Analysis.ipynb) — complete Python analysis and model evaluation.

## Attribution
Group 3 academic Machine Learning project, CISA 5381. This repository presents the group's work for portfolio purposes; individual contributions should be distinguished from collaborative work.
## Individual Contributions

This Machine Learning project was completed collaboratively as part of Group 3 for CISA 5381.

My contributions focused on the initial stages of the Cross-Industry Standard Process for Data Mining (CRISP-DM) framework, including:

- **Business Understanding:** Defined the research problem and objectives for predicting high return on investment among U.S. college graduates.
- **Data Understanding:** Examined the dataset's structure, variables, and data quality to support the analysis.
- **Data Preparation:** Contributed to data cleaning and preparation in Python.
- **Exploratory Data Analysis:** Explored patterns in graduate outcomes and educational characteristics to support the group's research questions.
- **Jupyter Notebook Development:** Developed the initial sections of the notebook, establishing the analytical foundation for subsequent modeling.

Group 3 completed model development, evaluation, and final conclusions collaboratively.

## Data Source
**Dataset:** [College Major ROI](https://www.kaggle.com/datasets/sergionefedov/college-major-roi)

**Kaggle publisher:** sergionefedov

The dataset, *College Major ROI*, was obtained from Kaggle and contains 30,000 synthetic graduate records calibrated using published college return-on-investment research.

**License:** Creative Commons CC0 1.0 (Public Domain).

The dataset is included in the `data` folder for reproducibility. Results describe patterns within synthetic data and should not be interpreted as verified outcomes for actual U.S. college graduates.

## How to Run This Project

1. Download the repository using **Code → Download ZIP** on GitHub.
2. Extract the ZIP file to your computer.
3. Open a terminal or Anaconda Prompt in the extracted repository folder.
4. Install the required Python packages:

   ```bash
   pip install -r requirements.txt
   ```

5. Start Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

6. Open `notebooks/College_Graduate_ROI_Analysis.ipynb`.
7. Run the notebook cells in order to reproduce the analysis.

The dataset is stored in `data/college_major_roi.csv`. The notebook uses the relative path `../data/college_major_roi.csv` when run from the `notebooks` directory.
