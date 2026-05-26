# Mental Health in Tech — Data Analysis

Data analysis on mental health in tech workplaces, focused on identifying patterns, risk factors, and intervention opportunities for HR and Clinical Advisory teams.

---

## Project Context

This project analyzes survey data from **1,259 tech professionals** about mental health at work. The goal is to transform raw data into actionable insights for HR decision-making, with a **Clinical AI and Medical Advisory** perspective.

Dataset: [OSMI Mental Health in Tech Survey](https://www.kaggle.com/datasets/osmi/mental-health-in-tech-survey)

---

## Business Problems Investigated

| # | Problem | Techniques |
|---|---|---|
| 01 | EDA Checklist — initial dataset exploration | Descriptive analysis, value_counts, info() |
| 02 | Impact of mental health benefits on performance | Crosstab, Chi-square, Proportional rate |
| 03 | Psychological safety culture | Heatmap, Segmentation, Seaborn |
| 04 | Parity between mental and physical health | Logistic Regression, Odds Ratio |
| 05 | Predictive model for treatment-seeking | Random Forest, SHAP, ROC-AUC |

---

## Key Findings

### Gender and Treatment
- 76.5% of women sought treatment vs 49.8% of men
- In absolute volume, men seem more affected — but the dataset is 78% male
- Conclusion: men are underdiagnosed, not less affected

### Benefits and Work Interference
- Companies without mental health benefits: 18% frequent interference
- Companies with benefits: 14.3% frequent interference
- Statistically significant association: chi2 = 23.6, p = 0.0006

### Access to Support Resources
- seek_help is the factor with the strongest association (chi2 = 30.1, p < 0.0001)
- Only 19.8% of employees know where to seek help
- Employees without access to resources: 18.3% frequent interference

### Correlation Heatmap
- wellness_program vs seek_help = 0.47 (strongest correlation)
- family_history vs treatment = 0.38 (strongest clinical predictor)
- benefits vs seek_help = 0.38 (policies drive awareness)

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
|   |-- 01_eda_checklist.ipynb
|   |-- 02_beneficios_interferencia.ipynb
|   |-- 03_seguranca_psicologica.ipynb
|   |-- 04_paridade_saude.ipynb
|   |-- 05_modelo_preditivo.ipynb
|
|-- outputs/
    |-- graficos/
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

# 3. Open notebooks in order
jupyter notebook notebooks/
```

---

## Methodology

### EDA Approach

Before any analysis or model, a strict checklist is followed:

1. Shape, types and null values verification
2. Group balance check — critical to avoid wrong volume-based conclusions
3. Unique values inspection to detect inconsistencies
4. Text column cleaning (e.g. Gender column had 49 variations)
5. Descriptive analysis with absolute volume and proportional rate

Note: The dataset is 78% male. All gender analyses use proportional rate, not absolute volume.

### Statistical Validation

All associations validated with Chi-square Test:
- p < 0.05: statistically significant association
- p < 0.001: very strong association

---

## Recommendations for HR and Clinical Advisory

**1. Investing in mental health programs reduces work interference**
Companies with active benefits have 3.7 percentage points less frequent interference. In a 1,000-person company, that represents approximately 37 fewer employees with compromised performance.

**2. Men are underdiagnosed, not less vulnerable**
The proportional rate shows nearly half of men (49.8%) needed treatment. Male awareness programs have high impact potential.

**3. Access to resources matters more than having benefits on paper**
seek_help has a stronger association than benefits. It is not enough to offer — companies must communicate and facilitate access.

**4. Companies without wellness programs concentrate the highest risk**
84% of companies in the dataset have no active wellness program. This is the priority group for intervention.

---

## Next Steps

- Mental vs physical health parity analysis by sector
- Predictive model with Random Forest and SHAP values
- Interactive dashboard with Streamlit
- Text analysis of comments column with NLP

---

## Author

Portfolio project developed with focus on Clinical AI, Medical Advisory, and HR Analytics.

Dataset provided by Open Sourcing Mental Illness (OSMI).
