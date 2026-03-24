# Global Cancer Trends, Outcomes, and Treatment Cost Analysis 

## Overview
This project presents an exploratory and statistical analysis of a global cancer patient dataset containing **50,000 records** from **2015 to 2024**. The objective was to examine how **demographic, lifestyle, environmental, and clinical factors** relate to **cancer severity, survival, and treatment cost**.

The project combines **data cleaning, exploratory data analysis (EDA), hypothesis testing, correlation analysis, and Random Forest modeling** to extract meaningful patterns from healthcare data.

---

## Dataset Description
The dataset includes the following categories of variables:

### Demographic Variables
- Age
- Gender
- Country/Region
- Year of diagnosis

### Genetic, Lifestyle, and Environmental Factors
- Genetic risk
- Smoking
- Alcohol use
- Obesity level
- Air pollution exposure

### Clinical and Economic Variables
- Cancer type
- Cancer stage
- Treatment cost (USD)

### Outcome Variables
- Survival years
- Target severity score

---

## Project Objectives
The analysis was designed to answer the following questions:

1. What patterns exist across age, gender, country, cancer type, and stage?
2. Which lifestyle or genetic factors are most associated with cancer severity?
3. Do some cancer types show a higher proportion of early-stage diagnosis?
4. Which factors are the strongest predictors of severity and survival?
5. Does treatment cost have any relationship with survival years?
6. Do higher cancer stages lead to higher treatment costs or lower survival?
7. Does genetic risk amplify the negative effect of smoking on severity?

---


## Workflow
### 1. Data Understanding and Inspection
- Loaded the dataset and reviewed structure, data types, and summary statistics
- Explored the distribution of numerical variables such as age and treatment cost
- Checked category balance across gender, country, cancer type, and stage

### 2. Exploratory Data Analysis
Performed descriptive analysis to understand:
- Age distribution
- Gender and country distribution
- Cancer type and stage distribution
- Treatment cost patterns
- Relationships between risk factors and severity

### 3. Statistical and Inferential Analysis
Used statistical methods to validate analytical questions, including:
- Correlation analysis
- Linear trend analysis
- Kruskal-Wallis test
- Interaction effect testing using OLS regression

### 4. Predictive Analysis
Built Random Forest regression models to evaluate predictors of:
- **Cancer severity score**
- **Survival years**

---

## Key Analyses Performed
### A. Descriptive Analysis
- Examined overall patient demographics and variable distributions
- Found the dataset to be broadly balanced across major categories
- Example summary from the notebook:
  - **Rows:** 50,000
  - **Age range:** 20 to 89 years
  - **Mean age:** 54.42 years

### B. Risk Factors vs. Cancer Severity
Studied the relationship between:
- Genetic risk
- Smoking
- Alcohol use
- Air pollution
- Obesity level

The analysis showed that **smoking** and **genetic risk** had the strongest relationship with severity among the available factors.

### C. Early-Stage Diagnosis by Cancer Type
Calculated the proportion of cases diagnosed at **Stage 0** or **Stage I** for each cancer type.

Examples from the notebook:
- Liver cancer: **40.61%**
- Colon cancer: **40.42%**
- Prostate cancer: **40.19%**
- Lung cancer: **38.43%**

The proportions were relatively similar across cancer types, indicating limited variation in early-stage diagnosis within this dataset.

### D. Predictors of Severity and Survival
Used Random Forest regression to identify important predictors.

#### Severity Model
- **Train R²:** 0.969
- **Test R²:** 0.775

This suggests the model captured meaningful signal for predicting severity, with **smoking** and **genetic risk** emerging as strong contributors.

#### Survival Model
The selected features showed weak predictive power for survival on unseen data, suggesting that the available variables were not sufficient to explain survival duration well.

### E. Economic Burden of Treatment
Explored treatment cost across:
- Countries
- Age groups
- Gender

This analysis helped compare average treatment costs across patient segments and highlighted differences in economic burden across groups.

### F. Treatment Cost vs. Survival
Tested whether higher treatment cost was associated with longer survival.

Results from the notebook:
- **Pearson correlation:** -0.00043
- **Pearson p-value:** 0.9235
- **Spearman correlation:** -0.00045
- **Spearman p-value:** 0.9207

**Conclusion:** No significant relationship was found between treatment cost and survival years in this dataset.

### G. Cancer Stage vs. Cost and Survival
Used the Kruskal-Wallis test to compare treatment cost and survival across cancer stages.

Results:
- **Treatment cost p-value:** 0.4254
- **Survival years p-value:** 0.6033

**Conclusion:** No statistically significant difference was observed in treatment cost or survival across stages.

### H. Interaction Effect: Genetic Risk × Smoking
Used OLS regression to test whether genetic risk amplified the effect of smoking on severity.

Result:
- **Interaction p-value:** 0.6283

**Conclusion:** The interaction effect was not statistically significant in this dataset.

---

## Key Findings
- **Smoking** and **genetic risk** were the strongest predictors of cancer severity.
- Early-stage diagnosis rates were fairly similar across different cancer types.
- Treatment cost showed **no meaningful correlation** with survival years.
- Cancer stage did **not** show a statistically significant effect on treatment cost or survival in this dataset.
- Survival years were much harder to predict than severity, indicating weaker signal in the available features.

---

If you found this project useful, feel free to star the repository.
