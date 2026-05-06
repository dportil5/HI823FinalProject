# COVID-19 Prediction AI System Using Causal Symptom Analysis and Machine Learning

## Project Overview
This project develops a COVID-19 diagnostic AI system using the COVIDCARE Phase II dataset and DEMI causal analysis. The goal is to predict PCR-confirmed COVID-19 positivity using symptoms, demographics, vaccination variables, exposure information, and at-home testing information.

## Dataset
The project uses:
- COVIDCARE Phase II patient dataset
- COVIDCARE DEMI knowledgebase

The original patient dataset included 822 patients and 472 variables. After excluding records with missing PCR results, the final analytic sample included 559 patients, including 501 PCR-negative patients and 58 PCR-positive patients.

## Methods
The project workflow includes:
- Data cleaning
- Leakage variable removal
- Mutual information feature selection
- Interaction term creation
- Logistic regression
- LASSO regression
- Gradient boosting
- DEMI total effect analysis
- DEMI diagnostic network
- Patient-level prediction function

## Main Results
LASSO was the best-performing model by AUC.

| Model | Accuracy | AUC | F1 | McFadden R2 |
|---|---:|---:|---:|---:|
| LASSO | 0.9286 | 0.9171 | 0.7059 | 0.1542 |
| Logistic Regression | 0.9357 | 0.9091 | 0.6897 | -0.2349 |
| Gradient Boosting | 0.9286 | 0.9091 | 0.6429 | 0.1562 |

## Patient Scenario Demo
The final prediction function used the LASSO model. For the example patient scenario, the model predicted a 59.47% probability of PCR-positive COVID-19.

## Files Included
- `COVID_Symptoms_Causal_Analysis (1).ipynb`: Main Jupyter notebook
- `COVIDCARE_FORSUBMISSION_MIT_CLEANED_Phase_II_2021-12-03.csv`: Patient dataset
- `COVIDCARE_DEMI_knowledgebase_v4.csv`: DEMI knowledgebase
- `requirements.txt`: Python package requirements
- Output CSV files
- Figure PNG files

## How to Run
1. Download or clone this repository.
2. Install dependencies:

```bash
pip install -r requirements.txt
