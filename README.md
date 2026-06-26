# Mental Health in Tech — Data Analysis

Exploratory data analysis on mental health in tech workplaces, focused on identifying patterns, risk factors, and intervention opportunities for HR and Clinical Advisory teams.

This project is actively in development. Analyses and findings are updated as the work progresses.

---

## Project Context

This project analyzes survey data from 1,259 tech professionals about mental health at work. The goal is to transform raw data into actionable insights for HR decision-making, with a Clinical AI and Medical Advisory perspective.

Dataset: [OSMI Mental Health in Tech Survey](https://www.kaggle.com/datasets/osmi/mental-health-in-tech-survey)

---

## Research Questions

The following questions guide this analysis:

- Does access to mental health benefits reduce work interference?
- Which gender group is more likely to seek treatment — and why does volume mislead?
- Which age group reports the most frequent work interference?
- Does family history amplify work interference, and in which age groups?
- Do companies treat mental and physical health with equal seriousness?
- Can we predict which employees are most likely to seek treatment?

---

## Work in Progress

| # | Analysis | Status |
|---|---|---|
| 01 | EDA checklist — initial exploration and data cleaning | Done |
| 02 | Gender and treatment-seeking — volume vs proportional rate | Done |
| 03 | Correlation heatmap — relationships between key variables | Done |
| 04 | Age distribution and treatment rate by age group | Done |
| 05 | Age and work interference — which group is most affected | Done |
| 06 | Family history and work interference by age group | Done |
| 07 | Psychological safety culture — segmentation by company type and size | In progress |
| 08 | Parity between mental and physical health | Planned |
| 09 | Predictive model for treatment-seeking | Planned |

---

## Key Questions Under Investigation

### Gender and Treatment
- In absolute volume, men appear more affected
- But the dataset is 78% male — does proportional rate tell a different story?

### Age and Work Interference
- Which age group reports the most frequent interference?
- Does having a family history of mental illness amplify this effect?

### Benefits and Performance
- Do mental health benefits actually reduce work interference?
- Is having benefits enough, or does access to resources matter more?

---

## Repository Structure

```
mental-health-tech-analysis/
|
|-- README.md
|-- requirements.txt
|-- data/
|   |-- survey.csv
|
|-- notebooks/
|   |-- mental_health_eda.ipynb
|
|-- outputs/
    |-- graficos/
        |-- grafico_genero_tratamento.png
        |-- heatmap_correlacao.png
        |-- age_distribution.png
        |-- age_treatment.png
        |-- age_work_interference.png
        |-- family_history_interference.png
```

---

## Technologies Used

- Python 3.10+
- pandas
- matplotlib
- seaborn
- scipy
- scikit-learn
- shap
- jupyter

---

## How to Run

```bash
# 1. Clone the repository
git clone https://github.com/juksilva/mental-health-tech-analysis.git
cd mental-health-tech-analysis

# 2. Install dependencies
pip install -r requirements.txt

# 3. Open the notebook
jupyter notebook notebooks/mental_health_eda.ipynb
```

---

## Methodology

### EDA Approach

Before any analysis or model, a strict checklist is followed:

1. Shape, types and null values verification
2. Group balance check — critical to avoid wrong volume-based conclusions
3. Unique values inspection to detect inconsistencies
4. Text column cleaning (e.g. Gender column had 49 variations, Age had outliers below 0)
5. Descriptive analysis with absolute volume and proportional rate

Note: The dataset is 78% male. All gender analyses use proportional rate, not absolute volume.

### Statistical Validation

All associations validated with Chi-square Test:
- p < 0.05: statistically significant association
- p < 0.001: very strong association

---

## Author

Portfolio project developed with focus on Clinical AI, Medical Advisory, and HR Analytics.

Dataset provided by Open Sourcing Mental Illness (OSMI).

Last updated: June 2026
