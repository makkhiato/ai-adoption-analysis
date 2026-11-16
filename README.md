# Predicting AI Adoption Among University Students Using a Multilayer Perceptron

A Python-based research data analysis project for **CSC 0315: Intelligent System** at the **Pamantasan ng Lungsod ng Maynila (PLM)**.

## Overview

This project analyzes the factors associated with AI adoption among university students and evaluates the predictive performance of two machine learning approaches:

- **Multilayer Perceptron (MLP)** – A neural network with two hidden layers.
- **Multiple Linear Regression (MLR)** – A statistical regression model used as a baseline.

The models use six predictor variables to predict students' AI Adoption Scores.

## Research Variables

### Predictor Variables

The study uses six independent variables:

1. AI Familiarity
2. Perceived Usefulness
3. Perceived Ease of Use
4. Trust
5. Accessibility
6. Digital Literacy

Each variable is measured using five Likert-scale survey items. The corresponding composite score is calculated using the mean of its five items.

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
├── modules/
│   ├── __init__.py
│   ├── preprocessing.py
│   ├── scoring.py
│   ├── reliability.py
│   ├── descriptive.py
│   ├── mlp_model.py
│   ├── regression_model.py
│   └── evaluation.py
│
├── data/
│   └── .gitkeep
│
├── results/
│   ├── graphs/
│   └── .gitkeep
│
├── main.py
├── config.py
├── requirements.txt
├── README.md
└── .gitignore
```

## Analysis Modules

| File | Responsibility |
|---|---|
| `main.py` | Executes and coordinates the analysis pipeline. |
| `config.py` | Stores project settings, column mappings, and model configurations. |
| `preprocessing.py` | Validates, cleans, and prepares survey data. |
| `scoring.py` | Performs reverse coding and calculates composite scores. |
| `reliability.py` | Calculates Cronbach's alpha for the six predictor constructs. |
| `descriptive.py` | Generates descriptive statistics and response distributions. |
| `mlp_model.py` | Defines the Multilayer Perceptron model. |
| `regression_model.py` | Defines the Multiple Linear Regression model and diagnostics. |
| `evaluation.py` | Performs cross-validation, calculates evaluation metrics, and compares models. |

## Research Questions and Analysis

The project addresses five research questions:

1. Determine the levels of AI familiarity, perceived usefulness, perceived ease of use, trust, accessibility, and digital literacy.
2. Determine the extent of AI adoption using the composite AI Adoption Score.
3. Evaluate the predictive performance of the MLP model.
4. Evaluate the predictive performance of the MLR model.
5. Compare the predictive performance of MLP and MLR.

## Methodology

The analysis follows this general workflow:

1. **Data Validation** – Check eligibility, consent, incomplete responses, duplicate entries, and invalid scale values.
2. **Data Preprocessing** – Clean and prepare the survey responses.
3. **Reverse Coding** – Reverse-code negatively worded Trust and Accessibility items.
4. **Composite Scoring** – Calculate the six predictor scores and AI Adoption Score.
5. **Reliability Analysis** – Calculate Cronbach's alpha for each predictor construct.
6. **Descriptive Analysis** – Calculate means, standard deviations, and response distributions.
7. **Model Training** – Train the MLP and MLR models using the same six predictor variables.
8. **Model Evaluation** – Apply repeated five-fold cross-validation.
9. **Model Comparison** – Compare the models using their evaluation metrics.

### Evaluation Metrics

| Metric | Purpose | Preferred Result |
|---|---|---|
| RMSE | Measures prediction error while penalizing larger errors. | Lower |
| MAE | Measures the average absolute prediction error. | Lower |
| R² | Measures how well the model explains variation in the target variable. | Higher |

Results will be interpreted as exploratory findings, considering the limitations of the available sample size.

## Requirements

- Python 3.10 or later
- Required Python packages listed in `requirements.txt`

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

## Dataset

Place the Google Forms CSV export inside the `data/` directory.

```text
data/
└── survey_responses.csv
```

**Data Privacy:** Raw survey data may contain personally identifiable information. Do not commit raw datasets, names, email addresses, or other confidential respondent information to the public repository. Only validated and anonymized data should be used for analysis.

## Running the Project

Once the analysis pipeline has been implemented:

```cmd
python main.py
```

Generated reports and visualizations will be stored in the `results/` directory.

## Expected Outputs

```text
results/
├── descriptive_statistics.csv
├── reliability_results.csv
├── mlp_results.csv
├── regression_results.csv
├── model_comparison.csv
│
└── graphs/
```

These outputs will contain the descriptive statistics, reliability results, model evaluation metrics, model comparison, and relevant visualizations.

## Project Status

<em>Under Development</em>

The project structure and analysis modules are being developed incrementally. Final results will be added after data processing, model training, and evaluation are completed.

---

**Course:** CSC 0315 – Intelligent System  
**Institution:** Pamantasan ng Lungsod ng Maynila (PLM)