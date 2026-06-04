# Big Mountain Resort — Ski Resort Pricing Model

A guided data science capstone project following the full data science pipeline to build a pricing recommendation model for **Big Mountain Resort** in Montana. The project answers a real business question: *given the resort's facilities, what ticket price does the market support?*

---

## Business Problem

Big Mountain Resort recently added a new chairlift, increasing operating costs by $1.54M per year. Management needs to determine whether current ticket prices reflect the resort's value in the market, and whether strategic facility changes could justify a price increase — or allow cuts to reduce costs without impacting perceived value.

---

## Project Pipeline

The project follows a structured, notebook-driven workflow:

| Step | Notebook | Description |
|------|----------|-------------|
| 1 | [`02_data_wrangling.ipynb`](Notebooks/02_data_wrangling.ipynb) | Data loading, missing value analysis, feature inspection, state-level market summary statistics |
| 2 | [`03_exploratory_data_analysis.ipynb`](Notebooks/03_exploratory_data_analysis.ipynb) | Distribution analysis of resort features and ticket prices; correlation exploration; market segmentation |
| 3 | [`03_exploratory_data_analysis2.ipynb`](Notebooks/03_exploratory_data_analysis2.ipynb) | Extended EDA with additional feature relationships |
| 4 | [`04_preprocessing_and_training.ipynb`](Notebooks/04_preprocessing_and_training.ipynb) | Train/test split, missing value imputation (median/mean), feature scaling, baseline and initial model evaluation (R², MAE, MSE) |
| 5 | [`05_modeling.ipynb`](Notebooks/05_modeling.ipynb) | Final model deployment; Big Mountain ticket price prediction; scenario analysis for facility changes |

---

## Key Results

The trained regression model was used to:
- Estimate Big Mountain Resort's **market-supported ticket price** relative to competitors
- Evaluate **4 business scenarios** (e.g., adding/removing runs, increasing vertical drop, closing chairlifts) and their projected revenue impact
- Identify which resort features have the **strongest influence on ticket price**

A serialized model is saved at [`models/ski_resort_pricing_model.pkl`](models/ski_resort_pricing_model.pkl) for reproducibility.

An executive summary of findings is available in [`Big_Mountain_Resort_Executive_Presentation.pptx`](Big_Mountain_Resort_Executive_Presentation.pptx).

---

## Methods & Skills

| Category | Details |
|----------|---------|
| **Data wrangling** | Missing value analysis, imputation, feature derivation, state-level aggregation |
| **EDA** | Distribution plots, correlation analysis, market segmentation by region/state |
| **Modeling** | Regression modeling, train/test split, cross-validation, feature scaling |
| **Model evaluation** | R², Mean Absolute Error (MAE), Mean Squared Error (MSE) |
| **Business analysis** | Scenario modeling, pricing sensitivity analysis |

---

## Tools & Libraries

- **Language:** Python 3
- **Data manipulation:** pandas, NumPy
- **Machine learning:** scikit-learn
- **Visualization:** Matplotlib, seaborn
- **Environment:** Jupyter Notebook
- **Other:** pickle (model serialization), os, Pipenv

---

## Repository Structure

```
DataScienceGuidedCapstone/
├── Notebooks/
│   ├── 02_data_wrangling.ipynb               # Data loading, cleaning, missing values
│   ├── 03_exploratory_data_analysis.ipynb    # EDA: distributions, price by state/region
│   ├── 03_exploratory_data_analysis2.ipynb   # Extended EDA
│   ├── 04_preprocessing_and_training.ipynb   # Imputation, scaling, baseline models
│   ├── 05_modeling.ipynb                     # Final model, price prediction, scenarios
│   └── library/sb_utils.py                  # Shared utility functions
├── data/
│   ├── ski_data_cleaned.csv                  # Cleaned dataset after wrangling
│   ├── ski_data_step3_features.csv           # Feature-engineered dataset
│   └── state_summary.csv                    # State-level market summary statistics
├── models/
│   └── ski_resort_pricing_model.pkl          # Serialized trained model
├── raw_data/
│   └── ski_resort_data.csv                  # Original source dataset
├── library/sb_utils.py                      # Project utility functions
├── Big_Mountain_Resort_Executive_Presentation.pptx
├── Frequentist_Inference_Case_Study_Part_A.ipynb
├── Pipfile / Pipfile.lock
└── .gitignore
```

---

## Dataset

US ski resort data including features such as vertical drop, skiable terrain acreage, snowmaking area, number of chairs, fast quads, runs, and weekend/weekday ticket prices. Source: Springboard Guided Capstone dataset.

---

## Author

**Esref Selvi**

[![GitHub](https://img.shields.io/badge/GitHub-YatoSnow-181717?style=flat&logo=github)](https://github.com/YatoSnow)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-esrefselvi-0A66C2?style=flat&logo=linkedin)](https://linkedin.com/in/esrefselvi)

---

*Completed as the Guided Capstone Project for the Springboard Data Science Fellowship.*
