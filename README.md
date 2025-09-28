# Job Transition Analytics Project

This repository contains a complete data‑science project designed to showcase analytical and predictive modeling skills for roles such as **business analyst**, **program manager** and **data analyst**.  It is intended to be an out‑of‑the‑box example that demonstrates how to generate data, explore it, build models, and draw insights in a professional, reproducible way.

## Project Overview

Modern career paths often involve moving between roles and departments.  Understanding what factors contribute to a successful transition can inform training programmes, hiring strategies and personal career planning.  Since real employee data is sensitive and often unavailable, this project uses a **synthetic dataset** that simulates employees attempting to move into target roles like **Business Analyst**, **Program Manager** or **Data Analyst**.  The project contains:

- **Synthetic dataset (`synthetic_job_transition.csv`)** – 500 rows of simulated employee data with attributes such as current role, years of experience, education, performance rating, satisfaction level, training hours, certifications, last promotion interval, projects completed, and departmental assignment.  A binary target variable (`target_role_success`) indicates whether the simulated employee successfully moved into their desired role.  The data is generated via a logistic function to produce realistic correlations between features and the target.
- **Jupyter notebook (`analysis.ipynb`)** – A step‑by‑step analysis that loads the dataset, performs exploratory data analysis (EDA) with visualisations, preprocesses categorical variables, builds three classification models (Logistic Regression, Decision Tree, Random Forest) and evaluates their performance.  It also reports feature importances from the Random Forest model and summarises findings.
- **Requirements file (`requirements.txt`)** – Lists the Python packages needed to run the notebook.

The project is structured to illustrate an increasing level of difficulty: it begins with basic data exploration, progresses to more advanced visualisations and correlation analysis, and culminates in building and comparing multiple predictive models.

## Getting Started

### Prerequisites

To run the analysis notebook locally you need Python 3.8+ and the packages listed in `requirements.txt`.  If you use a virtual environment (recommended), create one and install the dependencies:

```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
pip install -r requirements.txt
```

### Files

| File | Description |
| --- | --- |
| `synthetic_job_transition.csv` | Synthetic dataset with 500 samples and 13 columns (see below). |
| `analysis.ipynb` | Jupyter notebook performing EDA, preprocessing, and predictive modeling. |
| `requirements.txt` | List of Python packages required to run the notebook. |

### Dataset Fields

The dataset columns are described below.  All values are synthetic and generated for demonstration purposes:

| Column | Type | Description |
| --- | --- | --- |
| `employee_id` | integer | Unique identifier for each synthetic employee. |
| `current_role` | categorical | The employee's current role (Analyst, Engineer, Consultant, Manager). |
| `target_role` | categorical | The role the employee wants to transition into (Business Analyst, Program Manager, Data Analyst). |
| `years_experience` | float | Total years of professional experience. |
| `education_level` | categorical | Highest degree obtained (High School, Bachelor, Master, Doctorate). |
| `performance_rating` | float | Recent performance rating (1–5 scale). |
| `satisfaction_level` | float | Current job satisfaction (0–1 scale). |
| `training_hours` | integer | Hours of training completed in the past year. |
| `certifications_count` | integer | Number of professional certifications held. |
| `last_promotion_years` | integer | Years since the last promotion. |
| `projects_completed` | integer | Number of projects completed in the past year. |
| `department` | categorical | Department where the employee currently works (Sales, Engineering, HR, Marketing, Finance, Operations). |
| `target_role_success` | binary | **Target variable**: 1 if the employee successfully transitioned into their desired role, 0 otherwise. |

## Running the Notebook

1. Open the `analysis.ipynb` notebook in JupyterLab, Jupyter Notebook or VS Code.
2. Run the cells sequentially.  The notebook will:
   - Load the `synthetic_job_transition.csv` dataset.
   - Display dataset information and summary statistics.
   - Visualise distributions of numeric features and the target variable.
   - Plot a correlation heatmap for numeric variables.
   - Preprocess categorical variables using one‑hot encoding and split the data into training and test sets.
   - Train and evaluate Logistic Regression, Decision Tree and Random Forest classifiers.
   - Show feature importance for the Random Forest model.
3. Review the conclusions section for a high‑level summary of insights.

## Notes

- This dataset is **entirely synthetic** and is not derived from any real personal or company data.
- The synthetic generation process uses a logistic function to ensure certain features (such as performance rating, satisfaction level and certifications) have a positive influence on the success variable.  This helps illustrate how relationships between variables can be modeled.
- The project can be extended by experimenting with other algorithms (e.g. Gradient Boosting), tuning hyperparameters, or creating additional synthetic features to simulate more complex scenarios.

## License


## Future Work

This project can be expanded by exploring additional machine learning algorithms, performing cross-validation, and experimenting with hyperparameter tuning. You could also use real-world datasets or integrate data from public sources to further validate the models and compare them against the synthetic data results.

This repository is provided for demonstration and educational purposes.  Feel free to fork and modify it for your own portfolio projects.
