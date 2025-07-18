# Employee Performance Analysis

## 1. Project Background and Overview

**KiwiLearn** is a leading education provider in Aotearoa New Zealand that supports students across the tertiary sector through digital learning resources and institutional partnerships. As KiwiLearn expands, it faces increasing pressure to maintain high service standards while optimising staff performance across departments.

This project aims to uncover trends in employee performance data across multiple variables such as training hours, years of experience, department, gender, and salary. The goal is to assist KiwiLearn’s HR and executive leadership in making data-informed decisions that improve workforce outcomes.

---

## Table of Contents

1. [Project Background and Overview](#1-project-background-and-overview)  
2. [Data Structure Overview](#2-data-structure-overview)  
3. [Executive Summary](#3-executive-summary)  
4. [Insights Deep Dive](#4-insights-deep-dive)  
5. [Recommendations](#5-recommendations)  
6. [Full Report](#6-full-report)  
7. [Environment Setup](#7-environment-setup)  

---

## Quick Access

- [Raw Dataset](https://github.com/itsLucas-h/employee-performance-analysis/tree/main/data/raw)  
- [Full Report (PDF)](https://github.com/itsLucas-h/employee-performance-analysis/tree/main/reports)  
- [View Analysis Notebook](https://github.com/itsLucas-h/employee-performance-analysis/blob/main/notebooks/01_data_analysis.ipynb)

---

## 2. Data Structure Overview

The dataset contains **700 records** of anonymised employees at KiwiLearn and serves as the foundation for this performance analysis. It is stored under `data/raw/Employee_Performance.csv`.

Each row represents one employee, with columns capturing demographic, departmental, and performance-related attributes:

| Column Name           | Description                                                                 |
|-----------------------|-----------------------------------------------------------------------------|
| `Employee_ID`         | Unique identifier for each employee                                         |
| `Department`          | Department the employee works in: Sales, Marketing, IT, or HR              |
| `Gender`              | Gender of the employee: Male or Female                                      |
| `Years_of_Experience` | Total number of years the employee has worked professionally                |
| `Monthly_Salary`      | Employee’s gross monthly income in NZD                                      |
| `Training_Hours`      | Total number of training hours completed during the year                    |
| `Performance_Rating`  | A numeric rating from 1 to 5.5 indicating the employee’s annual performance |

### Key Characteristics:
- `Performance_Rating` is the **target variable** for this analysis.
- The dataset is **fully populated** with no missing values.
- All features are either **numerical** or **categorical**.
- Data is **balanced across departments and genders**, enabling fair comparative analysis.

**Raw Dataset:**  
[View `Employee_Performance.csv`](https://github.com/itsLucas-h/employee-performance-analysis/tree/main/data/raw)

---

## 3. Executive Summary

This analysis investigated 700 anonymised KiwiLearn employee records to identify the drivers of performance across key demographic and work-based factors.

- **Performance ratings** show a normal distribution centred around 3.5, suggesting a tendency toward moderate performance.
- **Sales** is the largest department and displays a wide range of performance scores.
- **No strong correlation** was found between monthly salary and performance.
- **Years of experience** and **training hours** showed weak but positive associations with performance.
- Female employees slightly outperformed males on average.
- HR had the highest median performance score among departments.

These findings suggest that performance is likely influenced by a combination of qualitative factors not captured in the dataset, alongside modest contributions from experience and training.

---

## 4. Insights Deep Dive

### Sales Department Trends
The Sales team has the most employees but the widest spread of performance. While some top performers exist, others lag significantly. This points to inconsistent practices or unclear KPIs.

### Salary vs Performance
There is no evidence that higher salaries directly correspond to higher performance. Some high earners underperform, and some low earners outperform, suggesting salary is not an effective standalone motivator or indicator.

### Training and Experience
While a positive relationship exists between training hours and performance, the correlation is weak. Years of experience also show a similar low-strength positive relationship, implying that experience alone does not guarantee improved performance.

### Department-Level Summary
- **HR** had the highest median performance.
- **Marketing** showed a narrower spread in ratings.
- **IT** had the lowest mean performance score.
- Performance disparities suggest department-specific challenges or leadership differences.

---

## 5. Recommendations

1. **Review Sales department strategy**  
   High variation in performance suggests inconsistent training, management, or role clarity. Introduce coaching and set clear expectations.

2. **Rebalance training allocation**  
   Focus training efforts on departments (e.g., IT) with lower average performance to lift consistency across the organisation.

3. **Explore qualitative factors**  
   Conduct employee surveys or interviews to identify non-numeric factors (e.g., motivation, engagement, work environment) impacting performance.

4. **Redesign incentive models**  
   Current salary structures do not align clearly with performance. Consider revising performance-based bonus schemes instead of fixed raises.

---

## Full Report

The complete report with visuals, statistical summaries, and interpretation is available here:

[View Full Report (PDF)](https://github.com/itsLucas-h/employee-performance-analysis/tree/main/reports)

---

## Environment Setup

To run the analysis locally:

```bash
git clone https://github.com/itsLucas-h/employee-performance-analysis.git
cd employee-performance-analysis

# Set up virtual environment
python -m venv .venv
.venv\Scripts\activate  # Windows
# or
source .venv/bin/activate  # macOS/Linux

# Install required packages
pip install -r requirements.txt

# Start Jupyter Notebook
jupyter notebook notebooks/analysis.ipynb
