# 📊 Derivable Judgement - Statistical Analysis Project

## 🎯 Project Overview

**Derivable Judgement** is a comprehensive statistical analysis project that demonstrates essential hypothesis testing, inferential statistics, and data analysis techniques. The project uses health dataset analysis to showcase practical applications of statistical methods including t-tests, chi-square tests, ANOVA, correlation analysis, and more.

**Project File:** `Derivable_Judgement-checkpoint.ipynb`  
**Theory Document:** `Project _ Derivable Judgement.pdf`

---

## 🎥 Demo Video

[![Watch Demo Video](https://img.shields.io/badge/▶️%20Watch%20Demo-Click%20Here-blue?style=for-the-badge)](https://www.youtube.com/watch?v=YOUR_VIDEO_ID)


---

## 📚 Table of Contents

1. [Key Concepts](#-key-concepts)
2. [Installation & Dependencies](#-installation--dependencies)
3. [Project Structure](#-project-structure)
4. [Statistical Methods](#-statistical-methods)
5. [Results Summary](#-results-summary)
6. [Usage Guide](#-usage-guide)
7. [Contributing](#-contributing)

---

## 🔬 Key Concepts

### 🎓 What is Inferential Statistics?

Inferential Statistics is used to make decisions about a population based on sample data. It involves:
- **Hypothesis Testing** - Making claims about populations
- **Confidence Intervals** - Estimating population parameters
- **Statistical Tests** - Determining if differences are significant

| Concept | Definition | Purpose |
|---------|-----------|---------|
| **Hypothesis Testing** | Statistical method to test claims about data | Make decisions about population parameters |
| **Confidence Interval (CI)** | Range in which true population parameter likely lies | Estimate population parameter with uncertainty |
| **Critical Value** | Boundary value used to decide rejection of null hypothesis | Determines acceptance/rejection region |
| **p-value** | Probability of observing data if null hypothesis is true | Measure of statistical significance |
| **Significance Level (α)** | Usually 0.05, threshold for rejecting null hypothesis | Control Type I error rate |

---

## 🔑 Hypotheses Formulated

### **Hypothesis 1: Smoking & Diabetes Prevalence**

```
H₀ (Null Hypothesis): Smoking has no effect on diabetes prevalence
H₁ (Alternative Hypothesis): Smoking affects diabetes prevalence

Test Type: Chi-Square Test of Independence
Variables: Categorical (Smoking Status vs Diabetes Status)
```

### **Hypothesis 2: Exercise Frequency & Cholesterol Levels**

```
H₀ (Null Hypothesis): Exercise frequency has no effect on cholesterol levels
H₁ (Alternative Hypothesis): Exercise frequency reduces cholesterol levels

Test Type: ANOVA (Multiple groups) or t-test (Two groups)
Variables: Categorical (Exercise Frequency) vs Continuous (Cholesterol)
```

### **Hypothesis 3: BMI & Blood Pressure**

```
H₀ (Null Hypothesis): BMI has no effect on blood pressure
H₁ (Alternative Hypothesis): Higher BMI increases blood pressure

Test Type: Correlation/Regression Analysis
Variables: Continuous (BMI vs Blood Pressure)
```

---

## 📦 Installation & Dependencies

### Required Python Libraries

```python
numpy          # Numerical computations
pandas         # Data manipulation
scipy          # Scientific computing & statistics
statsmodels    # Advanced statistical modeling
matplotlib     # Data visualization (optional)
```

### Installation

```bash
pip install numpy pandas scipy statsmodels
```

### Jupyter Notebook Setup

```bash
pip install jupyter
jupyter notebook Derivable_Judgement-checkpoint.ipynb
```

---

## 📁 Project Structure

```
Derivable Judgement/
├── Derivable_Judgement-checkpoint.ipynb  # Main analysis notebook
├── Project _ Derivable Judgement.pdf     # Theory & concepts
├── health_dataset.csv                     # Sample dataset
└── README.md                              # This file
```

---

## 🔢 Statistical Methods Used

### 1️⃣ **Confidence Intervals (CI)**

**Formula:**
$$CI = \bar{x} \pm z \cdot \frac{s}{\sqrt{n}}$$

Where:
- $\bar{x}$ = Sample mean
- $z$ = Critical z-value (1.96 for 95% CI)
- $s$ = Sample standard deviation
- $n$ = Sample size

**Example Results:**

| Variable | Mean | 95% CI Lower | 95% CI Upper | Interpretation |
|----------|------|--------------|--------------|---|
| **Age** | 47.08 | 44.68 | 49.48 | True population mean age lies between 44-49 years |
| **BMI** | 25.12 | 24.45 | 25.79 | True BMI lies between 24.45-25.79 |
| **Cholesterol** | 182.34 | 179.12 | 185.56 | True cholesterol lies between 179-186 mg/dL |

---

### 2️⃣ **Critical Value & p-value**

**Definitions:**

| Term | Definition | Interpretation |
|------|-----------|---|
| **Critical Value** | Threshold beyond which we reject H₀ | Boundary of acceptance region |
| **p-value** | Probability of observing data if H₀ is true | If p < 0.05, reject H₀ (significant) |
| **Type I Error (α)** | Rejecting H₀ when it's actually true | False positive (usually set to 0.05) |
| **Type II Error (β)** | Accepting H₀ when it's actually false | False negative |

**Decision Rule:**
```
If p-value < α (0.05) → Reject H₀ (Statistically Significant)
If p-value ≥ α (0.05) → Fail to Reject H₀ (Not Significant)
```

---

### 3️⃣ **t-test (Welch's t-test for unequal variances)**

**Formula:**
$$t = \frac{\bar{x}_1 - \bar{x}_2}{\sqrt{\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}}}$$

Where:
- $\bar{x}_1, \bar{x}_2$ = Sample means
- $s_1, s_2$ = Sample standard deviations
- $n_1, n_2$ = Sample sizes

**Example: Smokers vs Non-Smokers BMI**

| Group | Sample Size | Mean BMI | Std Dev | 
|-------|-------------|----------|---------|
| **Smokers** | 32 | 25.69 | 4.82 |
| **Non-Smokers** | 59 | 26.11 | 5.15 |

**Results:**
```
Test Statistic (t): -0.4999
Critical Value (95%): 1.9805
p-value: 0.6180

Decision: Fail to Reject H₀
Conclusion: No significant difference in BMI between smokers and non-smokers
```

---

### 4️⃣ **Chi-Square Test (χ²)**

**Formula:**
$$\chi^2 = \sum \frac{(O_i - E_i)^2}{E_i}$$

Where:
- $O_i$ = Observed frequency
- $E_i$ = Expected frequency

**Contingency Table: Smoking Status vs Diabetes**

| Smoking Status | No Diabetes | Diabetes | Total |
|---|---|---|---|
| **Former Smoker** | 23 | 54 | 77 |
| **Non-Smoker** | 26 | 33 | 59 |
| **Smoker** | 24 | 40 | 64 |
| **Total** | 73 | 127 | 200 |

**Expected Frequencies:**

| Smoking Status | No Diabetes | Diabetes |
|---|---|---|
| **Former Smoker** | 28.11 | 48.90 |
| **Non-Smoker** | 21.54 | 37.47 |
| **Smoker** | 23.36 | 40.64 |

**Results:**
```
χ² Statistic: 2.9458
Degrees of Freedom: 2
Critical Value (α=0.05): 5.9915
p-value: 0.2293

Decision: Fail to Reject H₀
Conclusion: No significant association between smoking and diabetes
```

---

### 5️⃣ **ANOVA (Analysis of Variance)**

**Formula:**
$$F = \frac{MSB}{MSW} = \frac{SSB/(k-1)}{SSW/(n-k)}$$

Where:
- $SSB$ = Between-group sum of squares
- $SSW$ = Within-group sum of squares
- $k$ = Number of groups
- $n$ = Total observations

**Example: Age Groups vs Disease Rate (Hypertension)**

| Age Group | Sample Size | Mean Disease Rate | Std Dev |
|---|---|---|---|
| **18-25** | 18 | 0.389 | 0.502 |
| **26-35** | 35 | 0.486 | 0.506 |
| **36-45** | 31 | 0.613 | 0.497 |
| **46-60** | 51 | 0.569 | 0.499 |
| **60+** | 65 | 0.538 | 0.501 |

**ANOVA Summary Table:**

| Source | SS | df | MS | F-value | p-value |
|---|---|---|---|---|---|
| **Between Groups** | 1.0649 | 4 | 0.2662 | 2.2644 | 0.0628 |
| **Within Groups** | 22.955 | 195 | 0.1177 | - | - |
| **Total** | 24.02 | 199 | - | - | - |

**Results:**
```
F-Statistic: 2.2644
Critical Value (α=0.05): 2.4180
p-value: 0.0628

Decision: Fail to Reject H₀
Conclusion: No significant difference in disease rates among age groups
```

---

### 6️⃣ **Correlation & Covariance**

**Covariance Formula:**
$$Cov(X,Y) = \frac{\sum(x_i - \bar{x})(y_i - \bar{y})}{n-1}$$

**Pearson Correlation Formula:**
$$r = \frac{Cov(X,Y)}{s_x \cdot s_y}$$

Where:
- $s_x, s_y$ = Standard deviations
- $r$ ranges from -1 to +1

**Example: Age vs BMI**

| Metric | Value | Interpretation |
|---|---|---|
| **Covariance** | -6.908 | Slight negative relationship |
| **Correlation (r)** | -0.0841 | Very weak negative correlation |
| **R-squared (r²)** | 0.0071 | Only 0.71% of variance explained |

**Correlation Strength Guide:**

| r-value | Strength | Direction |
|---|---|---|
| **±1.00** | Perfect | Positive/Negative |
| **±0.70 to ±0.99** | Very Strong | Positive/Negative |
| **±0.40 to ±0.69** | Strong | Positive/Negative |
| **±0.20 to ±0.39** | Moderate | Positive/Negative |
| **±0.00 to ±0.19** | Very Weak/Negligible | Positive/Negative |

---

## 📈 Results Summary

### 🎯 Key Findings

| Test | Finding | Significance | Implication |
|---|---|---|---|
| **t-test (Smokers vs BMI)** | p = 0.6180 | Not Significant | Smoking status doesn't affect BMI |
| **Chi-Square (Smoking vs Diabetes)** | p = 0.2293 | Not Significant | No association between smoking and diabetes |
| **ANOVA (Age vs Disease)** | p = 0.0628 | Not Significant | Age groups show similar disease rates |
| **Correlation (Age vs BMI)** | r = -0.0841 | Very Weak | Minimal relationship between age and BMI |

---

## 💻 Usage Guide

### Step 1: Load the Data

```python
import pandas as pd
import numpy as np
from scipy import stats

df = pd.read_csv("health_dataset.csv")
df.head()
```

### Step 2: Calculate Confidence Intervals

```python
ages = df['age'].values
mean_age = np.mean(ages)
std_age = np.std(ages, ddof=1)
n = len(ages)
se = std_age / np.sqrt(n)

# 95% CI
z = 1.96
ci_lower = mean_age - z * se
ci_upper = mean_age + z * se

print(f"95% CI for Age: ({ci_lower:.2f}, {ci_upper:.2f})")
```

### Step 3: Perform t-test

```python
group1 = df[df['smoking_status']=="Smoker"]['bmi'].values
group2 = df[df['smoking_status']=="Non-Smoker"]['bmi'].values

t_stat, p_value = stats.ttest_ind(group1, group2, equal_var=False)
print(f"t-statistic: {t_stat:.4f}, p-value: {p_value:.4f}")
```

### Step 4: Chi-Square Test

```python
contingency_table = pd.crosstab(df['smoking_status'], df['diabetes'])
chi2, p, dof, expected = stats.chi2_contingency(contingency_table)

print(f"Chi-Square: {chi2:.4f}, p-value: {p:.4f}")
```

### Step 5: ANOVA

```python
groups = [
    df[df['age_group']=="18-25"]['hypertension'].values,
    df[df['age_group']=="26-35"]['hypertension'].values,
    # ... more groups
]

f_stat, p_value = stats.f_oneway(*groups)
print(f"F-statistic: {f_stat:.4f}, p-value: {p_value:.4f}")
```

### Step 6: Correlation Analysis

```python
correlation = df['age'].corr(df['bmi'])
covariance = df['age'].cov(df['bmi'])

print(f"Correlation: {correlation:.4f}")
print(f"Covariance: {covariance:.4f}")
```

---

## 📊 Dataset Overview

**File:** `health_dataset.csv`

| Column | Data Type | Description |
|---|---|---|
| **record_id** | String | Unique identifier |
| **age_group** | Categorical | Age brackets (18-25, 26-35, etc.) |
| **age** | Integer | Age in years |
| **weight** | Integer | Weight in kg |
| **gender** | Categorical | Male, Female, Other |
| **region** | Categorical | Geographic region |
| **smoking_status** | Categorical | Smoker, Non-Smoker, Former Smoker |
| **exercise_frequency** | Categorical | Daily, Weekly, Rarely, Never |
| **bmi** | Float | Body Mass Index |
| **blood_pressure** | Float | Blood pressure reading |
| **diabetes** | Boolean | Diabetes status |
| **hypertension** | Boolean | Hypertension status |
| **cholesterol_level** | Float | Cholesterol in mg/dL |
| **glucose_level** | Float | Glucose in mg/dL |
| **visit_date** | Date | Medical visit date |

---

## 🔍 Interpretation Guide

### ✅ When to Reject H₀ (Null Hypothesis)

```
IF p-value < 0.05 THEN
   Result is Statistically Significant
   The difference/relationship is not due to chance
   Reject the Null Hypothesis
   
ELSE
   Result is NOT Statistically Significant
   Difference/relationship could be due to random variation
   Fail to Reject the Null Hypothesis
```

### 📌 Decision Tree

```
                    Conduct Test
                        |
                    Calculate p-value
                        |
                _____ Is p < 0.05? _____
               |                       |
              YES                      NO
               |                       |
        Reject H₀            Fail to Reject H₀
         Significant          Not Significant
             Result              Result
```

---

## 🎓 Statistical Concepts Explained

### 📍 **Type I vs Type II Errors**

| Error Type | Definition | When It Occurs | Consequence |
|---|---|---|---|
| **Type I (α)** | Rejecting H₀ when it's true | False Positive | Claim difference exists when it doesn't |
| **Type II (β)** | Accepting H₀ when it's false | False Negative | Claim no difference when one exists |

### 📍 **Significance Level (α)**

```
α = 0.05  →  95% Confidence Level
α = 0.01  →  99% Confidence Level
α = 0.10  →  90% Confidence Level
```

---

## 📚 Key Formulas Reference

| Concept | Formula | Components |
|---|---|---|
| **Confidence Interval** | $\bar{x} \pm z \cdot \frac{s}{\sqrt{n}}$ | Mean ± (Critical Value × Std Error) |
| **Standard Error** | $SE = \frac{s}{\sqrt{n}}$ | Std Dev ÷ √Sample Size |
| **t-statistic** | $t = \frac{\bar{x}_1 - \bar{x}_2}{\sqrt{\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}}}$ | Difference of means / Pooled std error |
| **Chi-Square** | $\chi^2 = \sum \frac{(O-E)^2}{E}$ | Sum of (Observed - Expected)² / Expected |
| **F-statistic** | $F = \frac{MSB}{MSW}$ | Between variance / Within variance |
| **Correlation** | $r = \frac{Cov(X,Y)}{s_x \cdot s_y}$ | Covariance / Product of std devs |

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/improvement`)
3. **Make** your changes
4. **Test** thoroughly
5. **Commit** with clear messages (`git commit -m 'Add feature'`)
6. **Push** to the branch (`git push origin feature/improvement`)
7. **Open** a Pull Request

### Areas for Contribution:
- 📊 Additional statistical tests
- 🎨 Data visualization enhancements
- 📖 Documentation improvements
- 🐛 Bug fixes
- 🔧 Performance optimizations



---


