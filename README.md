# Predicting AI Adoption Among University Students Using a Multilayer Perceptron

A Python-based research data analysis project for **CSC 0315: Intelligent System** at the **Pamantasan ng Lungsod ng Maynila (PLM)**.

## Overview

This project investigates factors associated with AI adoption among university students and evaluates the predictive performance of two approaches:

- **Multilayer Perceptron (MLP)** – A neural network with two hidden layers.
- **Multiple Linear Regression (MLR)** – A statistical regression model used as a baseline.

Both models use six predictor variables to predict students' AI Adoption Scores.

The project uses Jupyter Notebooks (`.ipynb`) as its primary development and analysis environment. Each notebook contains its own code, Markdown explanations, tables, and visualizations. All cells are executed manually to allow step-by-step analysis and inspection of results.

## Research Variables

### Predictor Variables

The study uses six independent variables:

1. AI Familiarity
2. Perceived Usefulness
3. Perceived Ease of Use
4. Trust
5. Accessibility
6. Digital Literacy

Each construct is measured using **three five-point Likert-scale items**, for a total of 18 predictor items.

A composite score is calculated by taking the mean of the three items belonging to each construct.

Two negatively worded items are reverse-coded before calculating their respective construct scores:

- Trust Item 12
- Accessibility Item 15

### Target Variable

**AI Adoption Score**

The target variable is calculated as the mean of seven academic activity frequency items.

| Response | Score |
|---|---:|
| Never | 0 |
| Once | 1 |
| Two or three times | 2 |
| About once a week | 3 |
| Several times a week | 4 |
| Daily or almost daily | 5 |

The resulting score ranges from 0 to 5. A higher score indicates more frequent reported use of generative AI across the selected academic activities.

### Total Measurement Items

| Component | Number of Items |
|---|---:|
| Six predictor constructs (3 items each) | 18 |
| AI Adoption activities | 7 |
| **Total** | **25** |

## Project Structure

```text
ai-adoption-analysis/
│
├── notebooks/
│   ├── 01_data_preprocessing.ipynb
│   ├── 02_scoring.ipynb
│   ├── 03_descriptive_statistics.ipynb
│   ├── 04_mlp_model.ipynb
│   ├── 05_regression_model.ipynb
│   └── 06_model_evaluation.ipynb
│
├── modules/
│   └── __init__.py
│
├── data/
│   └── .gitkeep
│
├── results/
│   ├── tables/
│   │   └── .gitkeep
│   │
│   ├── graphs/
│   │   └── .gitkeep
│   │
│   └── .gitkeep
│
├── requirements.txt
├── README.md
└── .gitignore
```

## Notebook Guide

| Notebook | Purpose |
|---|---|
| `01_data_preprocessing.ipynb` | Load the Google Forms export, rename survey columns, and convert responses into numerical values. |
| `02_scoring.ipynb` | Validate responses, reverse-code negatively worded items, and calculate the six predictor scores and AI Adoption Score. |
| `03_descriptive_statistics.ipynb` | Generate descriptive statistics, frequency distributions, summary tables, and visualizations for SOP 1 and SOP 2. |
| `04_mlp_model.ipynb` | Build and evaluate the two-hidden-layer Multilayer Perceptron model. |
| `05_regression_model.ipynb` | Build and evaluate the Multiple Linear Regression model. |
| `06_model_evaluation.ipynb` | Compare MLP and MLR predictive performance using the same evaluation procedure. |

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

1. Determine the levels of AI familiarity, perceived usefulness, perceived ease of use, trust, accessibility, and digital literacy among surveyed university students.
2. Determine the extent of AI adoption using the composite AI Adoption Score.
3. Evaluate the predictive performance of the MLP model.
4. Evaluate the predictive performance of the MLR model.
5. Compare the predictive performance of MLP and MLR.

## Methodology

The analysis follows this workflow:

1. **Data Validation** – Check respondent eligibility, consent, incomplete responses, duplicate entries, and invalid scale values.
2. **Data Preprocessing** – Rename survey columns and convert responses into numerical values.
3. **Reverse Coding** – Reverse-code the negatively worded Trust and Accessibility items.
4. **Composite Scoring** –