# Predicting AI Adoption Among University Students Using a Multilayer Perceptron

A Python-based research data analysis project for **CSC 0315: Intelligent System** at the **Pamantasan ng Lungsod ng Maynila (PLM)**.

## Overview

This project investigates factors associated with AI adoption among university students and evaluates the predictive performance of two approaches:

- **Multilayer Perceptron (MLP)** – A neural network with two hidden layers.
- **Multiple Linear Regression (MLR)** – A statistical regression model used as a baseline.

Both models use six predictor variables to predict students' AI Adoption Scores.

The project uses Jupyter Notebooks (`.ipynb`) as its primary development and analysis environment. Each notebook contains its own code, explanations, tables, and visualizations. All cells are executed manually to allow step-by-step analysis and inspection of results.

## Research Variables

### Predictor Variables

The study uses six independent variables:

1. AI Familiarity
2. Perceived Usefulness
3. Perceived Ease of Use
4. Trust
5. Accessibility
6. Digital Literacy

Each variable is measured using five Likert-scale survey items. A composite score is calculated using the mean of its five items.

### Target Variable

**AI Adoption Score**

Calculated as the mean of seven academic activity frequency items.

| Response | Score |
|---|---:|
| Never | 0 |
| Once | 1 |
| Two or three times | 2 |
| About once a week | 3 |
| Several times a week | 4 |
| Daily or almost daily | 5 |

The resulting score ranges from 0 to 5.

## Project Structure

```text
ai-adoption-analysis/
│
├── notebooks/
│   ├── 01_data_preprocessing.ipynb
│   ├── 02_scoring.ipynb
│   ├── 03_reliability_analysis.ipynb
│   ├── 04_descriptive_analysis.ipynb
│   ├── 05_mlp_model.ipynb
│   ├── 06_regression_model.ipynb
│   └── 07_model_evaluation.ipynb
│
├── modules/
│   └── __init__.py
│
├── data/
│   └── .gitkeep
│
├── results/
│   ├── graphs/
│   └── .gitkeep
│
├── requirements.txt
├── README.md
└── .gitignore
```
git
## Notebook Guide

| Notebook | Purpose |
|---|---|
| `01_data_preprocessing.ipynb` | Load, validate, clean, and prepare survey responses. |
| `02_scoring.ipynb` | Reverse-code negatively worded items and calculate composite scores. |
| `03_reliability_analysis.ipynb` | Calculate Cronbach's alpha for the six predictor constructs. |
| `04_descriptive_analysis.ipynb` | Generate descriptive statistics and response distributions. |
| `05_mlp_model.ipynb` | Build and train the two-hidden-layer MLP model. |
| `06_regression_model.ipynb` | Build and evaluate the Multiple Linear Regression model. |
| `07_model_evaluation.ipynb` | Compare MLP and MLR predictive performance. |

### Notebook Execution

Notebooks are executed manually in VS Code using the Jupyter extension.

Each notebook is organized into individual cells containing code and Markdown explanations. This allows the researcher to:

- Execute code one cell at a time.
- Inspect intermediate outputs.
- Review generated tables and visualizations.
- Identify and correct errors before proceeding.
- Document findings alongside the corresponding analysis.

There is no central execution script. Each notebook is responsible for its respective research task.

## Research Questions and Analysis

The project addresses five research questions:

1. Determine the levels of AI familiarity, perceived usefulness, perceived ease of use, trust, accessibility, and digital literacy.
2. Determine the extent of AI adoption using the composite AI Adoption Score.
3. Evaluate the predictive performance of the MLP model.
4. Evaluate the predictive performance of the MLR model.
5. Compare the predictive performance of MLP and MLR.

## Methodology

The analysis follows this workflow:

1. **Data Validation** – Check eligibility, consent, incomplete responses, duplicate entries, and invalid scale values.
2. **Data Preprocessing** – Clean and prepare survey responses.
3. **Reverse Coding** – Reverse-code negatively worded Trust and Accessibility items.
4. **Composite Scoring** – Calculate the six predictor scores and AI Adoption Score.
5. **Reliability Analysis** – Calculate Cronbach's alpha for each predictor construct.
6. **Descriptive Analysis** – Calculate means, standard deviations, and response distributions.
7. **Model Training** – Train the MLP and MLR models using the same six predictor variables.
8. **Model Evaluation** – Apply repeated five-fold cross-validation using the same data splits and appropriate training-fold preprocessing.
9. **Model Comparison** – Compare the models using their evaluation metrics.

### Evaluation Metrics

| Metric | Purpose | Preferred Result |
|---|---|---|
| RMSE | Measures prediction error while penalizing larger errors. | Lower |
| MAE | Measures average absolute prediction error. | Lower |
| R² | Measures how well the model explains variation in the target variable. | Higher |

Results will be interpreted as exploratory findings, considering the limitations of the available sample size.

## Requirements

- Python 3.10 or later
- Visual Studio Code
- Python extension for VS Code
- Jupyter extension for VS Code

### Python Libraries

| Library | Purpose |
|---|---|
| Pandas | Data loading, cleaning, and manipulation. |
| NumPy | Numerical computations. |
| SciPy | Statistical calculations. |
| Scikit-learn | Machine learning, cross-validation, preprocessing, and evaluation. |
| Matplotlib | Data visualization. |
| Seaborn | Statistical visualization. |
| Jupyter | Notebook execution support. |
| IPykernel | Python kernel for Jupyter notebooks. |

## Setup

### 1. Clone the Repository

```cmd
git clone https://github.com/YOUR_USERNAME/ai-adoption-analysis.git
cd ai-adoption-analysis
```

### 2. Create a Virtual Environment

```cmd
py -m venv .venv
```

### 3. Activate the Virtual Environment

```cmd
.venv\Scripts\activate
```

### 4. Install Dependencies

```cmd
pip install -r requirements.txt
```

### 5. Configure VS Code

1. Open the project folder in VS Code.
2. Install the Python and Jupyter extensions.
3. Open any notebook inside the `notebooks/` directory.
4. Select the Python interpreter from the project's `.venv` environment.
5. Select the corresponding Jupyter kernel.

## Dataset

Place the Google Forms CSV export inside the `data/` directory.

```text
data/
└── survey_responses.csv
```

**Data Privacy:** Raw survey data may contain personally identifiable information. Do not commit raw datasets, names, email addresses, or other confidential respondent information to the repository. Only validated and anonymized data should be used for analysis.

## Expected Outputs

Generated reports and visualizations will be stored in the `results/` directory.

```text
results/
├── descriptive_statistics.csv
├── reliability_results.csv
├── mlp_results.csv
├── regression_results.csv
├── model_comparison.csv
│
└── graphs/
    ├── predictor_distributions.png
    ├── adoption_distribution.png
    └── model_comparison.png
```

These are planned outputs and will be generated as the corresponding notebooks are implemented.

