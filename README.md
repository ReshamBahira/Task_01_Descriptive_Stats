
# Task_01_Descriptive_Stats

## Project Description

This project analyzes a real-world dataset of Facebook political advertisements from the 2024 U.S. Presidential election. The goal is to explore and summarize the dataset using two different approaches:

1. **Pure Python (Standard Library Only)** – to understand how descriptive statistics are computed manually  
2. **Pandas** – to perform the same analysis using a data analysis library  

The purpose of this task is not just to compute statistics, but to understand how data is structured, how missing values and inconsistencies affect analysis, and how different tools approach the same problem.

---

## Dataset

Source: Facebook Political Ads Dataset (2024 U.S. Election)

Each row represents an advertisement and includes:
- Ad metadata (page name, platform, timestamps)
- Spend, impressions, and audience size (stored as ranges)
- Messaging and topic indicators (binary columns)

⚠️ **Note:**  
The dataset is not included in this repository.  
Download it and place it in the project directory before running scripts.

---

## Project Structure
Task_01_Descriptive_Stats/
│
├── pure_python_stats.py
├── pandas_stats.py
├── README.md
├── requirements.txt
└── visualizations/ (generated from Pandas script)


---

## How to Run the Scripts

### 1. Pure Python Script

Runs descriptive statistics using only standard Python libraries.

```bash
python pure_python_stats.py

### 2. Pandas Script

Runs the same analysis using Pandas and generates visualizations.


---

## Summary of Findings and Insights

- Ad spending is highly concentrated among a small number of major political campaigns  
- Most ads have very low or zero spend, creating a highly skewed distribution  
- Advertising activity increases around key political events such as debates and elections  
- Messaging is largely focused on issues (economy, governance, social topics) rather than only candidate promotion  
- A small number of ads have very high impressions and spend, which strongly affects averages  
- Some columns contain missing or incomplete data, which impacts analysis  

---

## Comparison of the Two Approaches

Both the pure Python and Pandas scripts produce similar overall results, but differ in how the analysis is performed.

- Pure Python required manual handling of:
  - missing values  
  - parsing range-based columns (spend, impressions)  
  - computing statistics like mean, median, and standard deviation  

- Pandas handled many of these automatically using built-in functions like:
  - `describe()`  
  - `value_counts()`  
  - `isna()`  

Small differences in results occur due to:
- rounding differences  
- missing value handling  
- standard deviation calculations (population vs sample)  
- automatic type inference in Pandas  

Overall, pure Python provided a deeper understanding of the data and computations, while Pandas made the analysis faster and more efficient.
