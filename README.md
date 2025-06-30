# 📊 Life Satisfaction and Willingness to Protest – A Regression Analysis (Stata)

This project investigates the interplay between **life satisfaction** and **willingness to protest**, using **primary survey data** and statistical analysis conducted in **Stata**. The study focuses on understanding how life satisfaction affects protest willingness, and whether this relationship varies across different demographic groups through **interaction terms** in regression models.

---

## 🎯 Objectives

- Examine how life satisfaction influences willingness to protest
- Identify demographic factors (e.g., age, income, education, etc.) related to protest behavior
- Use interaction terms to assess how the effect of life satisfaction varies by subgroup

---

## 🧩 Data

- **Type**: Primary data collected via structured survey  
- **Sample Size**: (Add your number here, e.g., *n = 300 respondents*)  
- **Key Variables**:
  - `willingness_to_protest`: Binary or Likert-scale measure
  - `life_satisfaction`: Self-reported measure of subjective well-being
  - Demographics: `age`, `gender`, `education`, `income`, etc.

---

## 🛠️ Tools Used

- **Stata** for statistical analysis
- `regress`, `logit`, and `margins` commands used for estimation and marginal effects

---

## 📈 Methodology

1. **Descriptive Statistics**  
   Basic summaries of life satisfaction, protest willingness, and demographics.

2. **Regression Analysis**  
   - Ordinary Least Squares (OLS) and/or Logistic Regression used to estimate effects
   - Main independent variable: `life_satisfaction`  
   - Dependent variable: `willingness_to_protest`

3. **Interaction Terms**  
   - Examined how the relationship between life satisfaction and protest varies by subgroups (e.g., life satisfaction × education)
   - Used `margins` and `marginsplot` for interpretation

---

## 📊 Sample Stata Code Snippet

```stata
logit willingness_to_protest life_satisfaction##i.education age gender income
margins education, at(life_satisfaction=(1(1)10))
marginsplot
