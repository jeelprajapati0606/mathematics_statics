<div align="center">
 
 #                                        📊 Expectation_Decider

</div>

> **A Comprehensive Statistical Analysis of Student Performance Using Probability Theory & Bayes Theorem**

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Project Features](#-project-features)
- [Dataset](#-dataset)
- [Key Concepts](#-key-concepts)
- [Probability Fundamentals](#-probability-fundamentals)
- [Random Variables & Distributions](#-random-variables--distributions)
- [Venn Diagrams](#-venn-diagrams)
- [Contingency Analysis](#-contingency-analysis)
- [Event Independence & Relationships](#-event-independence--relationships)
- [Bayes Theorem Application](#-bayes-theorem-application)
- [Key Findings](#-key-findings)
- [Installation & Usage](#-installation--usage)
- [Demo](#-demo)
- [Technologies Used](#-technologies-used)
- [Author](#-author)

---

## 🎯 Overview

**Expectation_Decider** is a statistical analysis project that uses **Probability Theory** and **Bayes Theorem** to predict student exam performance based on multiple factors including:
- Study hours
- Attendance percentage
- Group discussion participation
- Previous test scores

This project demonstrates how probability concepts can be applied to real-world educational data to make informed decisions about student success.

---

## ✨ Project Features

✅ **Empirical & Theoretical Probability Analysis**  
✅ **Random Variable & Probability Distribution Calculations**  
✅ **Venn Diagram Visualization**  
✅ **Contingency Table Analysis**  
✅ **Joint, Marginal & Conditional Probability**  
✅ **Event Independence Testing**  
✅ **Bayes Theorem Application**  
✅ **Data-Driven Insights & Predictions**  

---

## 📁 Dataset

| Column | Type | Description |
|--------|------|-------------|
| `study_hours` | Integer | Number of hours spent studying |
| `attendance` | Integer | Attendance percentage (0-100) |
| `group_discussion` | Categorical | Participation in group discussions (Yes/No) |
| `previous_test_score` | Integer | Score from previous test (0-100) |
| `final_exam_pass` | Categorical | Final exam result (Pass/Fail) |

**Dataset Size:** 200 student records

**Sample Data:**

| study_hours | attendance | group_discussion | previous_test_score | final_exam_pass |
|---|---|---|---|---|
| 4 | 72 | Yes | 89 | Fail |
| 16 | 72 | Yes | 93 | Pass |
| 4 | 79 | No | 61 | Fail |
| 4 | 65 | Yes | 61 | Fail |
| 20 | 76 | Yes | 50 | Pass |

---

## 🔑 Key Concepts

### What is Probability?

**Probability** is the measure of the likelihood that an event will occur. It ranges from **0 to 1** (or **0% to 100%**).

$$P(Event) = \frac{\text{Number of Favorable Outcomes}}{\text{Total Number of Possible Outcomes}}$$

#### Key Terminology:

| Term | Definition | Example |
|------|-----------|---------|
| **Experiment** | An activity that produces an outcome | Selecting a student from the dataset |
| **Outcome** | The result of an experiment | The selected student passes the exam |
| **Event** | A specific outcome or group of outcomes | Student has attendance > 80% |
| **Sample Space** | All possible outcomes | All 200 students in the dataset |

#### Three Probability Events from Our Dataset:

| Event | Description |
|-------|-------------|
| **Event A** | A student passes the final exam |
| **Event B** | A student has attendance above 80% |
| **Event C** | A student participates in group discussions |

---

## 📈 Probability Fundamentals

### 1️⃣ Empirical Probability

**Empirical probability** is based on actual observed data.

$$P(\text{Event}) = \frac{\text{Number of Times Event Occurred}}{\text{Total Number of Trials}}$$

**Example from our dataset:**
- Total students: 200
- Students who passed: 140

$$P(\text{Pass}) = \frac{140}{200} = 0.70 \text{ (70%)}$$

**Interpretation:** The probability of a student passing the exam is **70%** based on actual data.

---

### 2️⃣ Theoretical Probability

**Theoretical probability** is based on expected outcomes under ideal conditions.

$$P(\text{Event}) = \frac{\text{Number of Favorable Outcomes}}{\text{Total Number of Possible Outcomes}}$$

**Example:**
If a student can either Pass or Fail with equal likelihood:

$$P(\text{Pass}) = \frac{1}{2} = 0.50 \text{ (50%)}$$

**Real-life Example:** When tossing a coin:
$$P(\text{Heads}) = \frac{1}{2} = 0.50 \text{ (50%)}$$

---

## 🎲 Random Variables & Distributions

### Definition

A **random variable** is a function that assigns numerical values to the outcomes of a random experiment.

**In our case:**
$$X = \text{Number of students passing the final exam out of 3 randomly selected students}$$

### Possible Values:

| X (Number of Passes) | Interpretation |
|---|---|
| 0 | No student passes |
| 1 | One student passes |
| 2 | Two students pass |
| 3 | All three students pass |

### Probability Distribution

**Given:** $p = 0.7$ (probability of passing), $n = 3$ (number of trials)

Using **Binomial Distribution:**

$$P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}$$

| X | P(X) |
|---|---|
| 0 | 0.027 |
| 1 | 0.189 |
| 2 | 0.441 |
| 3 | 0.343 |

### Mean and Variance

$$\mu = np = 3 \times 0.7 = 2.1$$

$$\sigma^2 = np(1-p) = 3 \times 0.7 \times 0.3 = 0.63$$

**Interpretation:** On average, 2.1 out of 3 randomly selected students will pass the exam.

---

## 🔄 Venn Diagrams

### Analysis: Study Hours vs Attendance

| Condition | Count |
|-----------|-------|
| **Study > 10 Hours** | 109 |
| **Attendance > 80%** | 74 |
| **Both Conditions Met** | 37 |

### Venn Diagram Formula:

$$|A \cup B| = |A| + |B| - |A \cap B|$$

$$= 109 + 74 - 37 = 146$$

**Interpretation:** 146 students either study more than 10 hours OR have attendance above 80% (or both).

---

## 📊 Contingency Analysis

### Contingency Table: Group Discussion vs Final Exam Result

|  | **Fail** | **Pass** | **Total** |
|---|---|---|---|
| **No Discussion** | 58 | 48 | 106 |
| **Yes Discussion** | 32 | 62 | 94 |
| **Total** | 90 | 110 | **200** |

---

## 🔗 Event Independence & Relationships

### 1️⃣ Joint Probability

**Joint probability** is the probability that two events both occur.

$$P(A \cap B) = P(\text{Group Discussion YES AND Pass})$$

$$P(A \cap B) = \frac{62}{200} = 0.31 \text{ (31%)}$$

**Interpretation:** 31% of students both participate in group discussions AND pass the exam.

---

### 2️⃣ Marginal Probability

**Marginal probability** is the probability of a single event occurring.

$$P(B) = P(\text{Pass}) = \frac{110}{200} = 0.55 \text{ (55%)}$$

**Interpretation:** 55% of all students pass the exam.

---

### 3️⃣ Conditional Probability

**Conditional probability** is the probability of an event occurring given that another event has already occurred.

$$P(A|B) = \frac{P(A \cap B)}{P(B)}$$

**Example: Probability of Passing GIVEN Group Discussion Participation**

$$P(\text{Pass | Group Discussion Yes}) = \frac{62}{94} = 0.6596 \text{ (65.96%)}$$

**Interpretation:** If a student participates in group discussions, their probability of passing increases to **65.96%** (compared to overall 55%).

---

### 4️⃣ Independence Test

Two events are **independent** if:
$$P(A|B) = P(A)$$

**Test Results:**

| Probability | Value |
|---|---|
| $P(\text{Pass \| Group Discussion Yes})$ | 0.6596 |
| $P(\text{Pass})$ | 0.5500 |
| **Equal?** | ❌ **NO** |

**Conclusion:** ✅ **Dependent Events**

Group discussion participation and passing the exam are **DEPENDENT** - they are related to each other.

---

### 5️⃣ Mutual Exclusivity Test

Two events are **mutually exclusive** if they cannot occur together:
$$P(A \cap B) = 0$$

**Test Results:**

| Metric | Value |
|---|---|
| $P(\text{Group Discussion Yes AND Pass})$ | 0.31 |
| **Can both occur?** | ✅ **YES** |

**Conclusion:** ✅ **NOT Mutually Exclusive**

A student can both participate in group discussions AND pass the exam.

---

## 🧠 Bayes Theorem Application

### Bayes Theorem Formula

$$P(B|A) = \frac{P(A|B) \times P(B)}{P(A)}$$

Where:
- $P(B|A)$ = Probability of B given A (Posterior)
- $P(A|B)$ = Probability of A given B (Likelihood)
- $P(B)$ = Probability of B (Prior)
- $P(A)$ = Probability of A (Evidence)

### Application: Probability of Passing Given High Attendance

**Given:**
- $P(\text{High Attendance | Pass})$ = 0.70
- $P(\text{Pass})$ = 0.70
- $P(\text{High Attendance})$ = 0.60

**Calculate:**
$$P(\text{Pass | High Attendance}) = \frac{0.70 \times 0.70}{0.60} = \frac{0.49}{0.60} = 0.8167$$

### Result Table

| Component | Value |
|---|---|
| **Probability of High Attendance** | 60% |
| **Probability of Pass** | 70% |
| **P(High Attendance \| Pass)** | 70% |
| **P(Pass \| High Attendance)** | **81.67%** |

**Interpretation:** 
> 📌 A student with **high attendance (>80%)** has an **81.67%** chance of passing the exam.

This demonstrates that attendance is a strong predictor of exam success!

---

## 🎓 Key Findings

### Summary of Insights

| Finding | Impact | Confidence |
|---------|--------|-----------|
| Higher study hours increase pass probability | 🟢 Strong Positive | ✅ High |
| Attendance > 80% correlates with passing | 🟢 Strong Positive | ✅ High |
| Group discussion participation improves performance | 🟢 Positive | ✅ High |
| Previous test score influences final exam | 🟢 Positive | ✅ High |
| Group discussion & Passing are dependent events | 🔵 Dependent | ✅ Confirmed |

### Critical Success Factors

🏆 **Top 3 Factors for Exam Success:**

1. **Group Discussion Participation**
   - Pass probability: **65.96%** vs **55%** (overall)
   - Improvement: **+10.96%**

2. **High Attendance (>80%)**
   - Pass probability: **81.67%** (via Bayes)
   - Improvement: **+26.67%**

3. **Study Hours (>10 hours)**
   - Positive correlation with passing
   - Supports exam preparation

---

## 🚀 Installation & Usage

### Prerequisites

```bash
Python 3.7+
pip
```

### Required Libraries

```bash
pip install numpy pandas matplotlib seaborn matplotlib-venn
```

## 🎥 Demo

### 🔴 Watch the Full Project Walkthrough

[![Watch Demo Video](https://img.shields.io/badge/▶_WATCH_DEMO-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/watch?v=YOUR_VIDEO_ID)

### 📺 Interactive Visualization Guide

The notebook includes:
- ✅ Venn Diagrams
- ✅ Probability Distribution Charts
- ✅ Contingency Table Heatmaps
- ✅ Statistical Summary Plots

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| **Python 3** | Programming Language |
| **Jupyter Notebook** | Interactive Development |
| **NumPy** | Numerical Computations |
| **Pandas** | Data Manipulation & Analysis |
| **Matplotlib** | Data Visualization |
| **Seaborn** | Advanced Data Visualization |
| **Matplotlib-Venn** | Venn Diagram Creation |

---

## 📋 Project Structure

```
mathematics_statics/
├── README.md
├── student.csv
├── Expectation_Decider.ipynb
├── requirements.txt
└── images/
    ├── venn_diagram.png
    ├── probability_distribution.png
    └── contingency_heatmap.png
```

---


## 👤 Author

**Jeel Prajapati**

- GitHub: [@jeelprajapati0606](https://github.com/jeelprajapati0606)
- Repository: [mathematics_statics](https://github.com/jeelprajapati0606/mathematics_statics)

---
<div align="center">
   
###  ⭐ If you found this project helpful, please consider giving it a star! ⭐

### Made with ❤️ by Jeel Prajapati

</div>
