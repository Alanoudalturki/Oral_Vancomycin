# **Oral Vancomycin in *Clostridium difficile* Infection (CDI)**
## **Retrospective Cohort Analysis at xxx (2024)**

**Analysis and code conducted by:** Alanoud Alturki  
**Language & stack:** Python 3.11 (pandas, numpy, scipy, statsmodels, lifelines, matplotlib, seaborn)

---

## **Project Overview**
CDI is a major healthcare-associated infection, with vancomycin as a first-line therapy. While 125 mg every 6 hours is standard, higher doses are sometimes prescribed for severe cases. The impact of higher dosing strategies on **recurrence**, **time-to-resolution**, and **mortality** remains unclear.

This project uses electronic health record (EHR) data from **xxx, Riyadh (2024)** to compare outcomes across oral vancomycin dose groups (125 mg, 250 mg, 500 mg).

---

## **Objectives**
- **Primary Objective:** Compare 90-day CDI recurrence rates across vancomycin doses (125, 250, 500 mg).
- **Secondary Objectives:**
  - Compare time to symptom resolution (days 3, 7, 10, 14, 28).
  - Assess 90-day mortality across dose groups.
  - Explore dose changes and sensitivity analyses (max-dose, time-varying models).

---

## **Methods**
- **Study Design:** Retrospective cohort study (**n = 198** patients).
- **Inclusion Criteria:** Adults ≥18 years with confirmed CDI treated with oral vancomycin ≥72 h.
- **Exclusion Criteria:** Complicated CDI (toxic megacolon, perforation), rectal vancomycin, fecal microbiota transplant, multiple CDI courses in the same year.
- **Outcomes Measured:** 90-day recurrence, time to symptom resolution, 90-day mortality, adverse events (if recorded).

---

## **Statistical Analyses**
- **Descriptive Statistics**
  - Continuous: mean ± SD, median [IQR]
  - Categorical: counts (n) and percentages
- **Group Comparisons**
  - Kruskal–Wallis for continuous variables
  - χ² / Fisher’s exact test for categorical variables
- **Survival Analysis**
  - Kaplan–Meier curves with log-rank tests
  - Cox proportional hazards models
- **Multivariable Models**
  - Logistic regression for 90-day mortality
  - Cox models for time to resolution
- **Sensitivity Analyses**
  - Maximum-dose and time-varying dose modeling
  - IPTW (propensity weighting) for confounding control

---

## **Repository Contents**
- `oral_vancomycin.ipynb` — full analysis notebook (Python 3.11)
- `oral_vancomycin_results.pdf` — compiled report with tables, figures, and statistical output
- `cdi_outputs/tables/` — publication-ready tables (Excel export)
- `cdi_outputs/figures/` — high-resolution figures (histograms, Kaplan–Meier, forest plots)

---

## **Figures**
- **Figure 1–3:** Distributions for age, weight, and time-to-resolution (gray histograms with red median lines)
- **Figure 4:** Time-to-resolution by dose (stacked %)
- **Figure 5:** Kaplan–Meier survival curves by dose
- **Figure 6:** 90-day mortality by dose
- **Figure 7–8:** Forest plots (logistic regression and Cox models; 95% CIs; red reference at 1)

---

## **Software & Dependencies**
- **Python:** 3.11  
- **Libraries:** `pandas`, `numpy`, `scipy`, `statsmodels`, `lifelines`, `matplotlib`, `seaborn`  
- **Export tools:** `nbconvert`, `jupyter`, `pyppeteer`

---

## **Skills Demonstrated**
- EHR curation and cohort construction; reproducible data pipelines
- Data cleaning, feature engineering, and clinical rule mapping (CDI severity, WBC/SCr categories)
- Nonparametric testing (Kruskal–Wallis), χ²/Fisher’s exact tests
- Survival analysis (Kaplan–Meier, log-rank), Cox PH; time-varying Cox setup
- Multivariable modeling (logistic regression, GLMs) with model diagnostics
- Causal inference sensitivity (IPTW via multinomial propensity scores)
- Publication-quality visualization (Matplotlib/Seaborn; blue palette; reference lines)
- Automated reporting (Excel tables, figure export, notebook → PDF with `nbconvert`)
- Version control and documentation for research transparency

---

## **Author**
**Alanoud Alturki**  
Health Data Analyst | Health Informatics Specialist | Pharmacist  
MS in Health Informatics · MS in Health Data Analysis · PhD Student  
[LinkedIn](https://www.linkedin.com/in/alanoud-alturki-5601b2b5)

