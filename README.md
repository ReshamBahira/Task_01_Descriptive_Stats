# Task 01 — Descriptive Statistics

## Overview

This project analyzes a real-world dataset of Facebook political advertisements from the **2024 U.S. Presidential Election**. The goal is to explore and summarize the dataset using two distinct approaches:

- **Pure Python (Standard Library Only)** — to understand how descriptive statistics are computed manually
- **Pandas** — to perform the same analysis using a data analysis library

The purpose is not just to compute statistics, but to understand how data is structured, how missing values and inconsistencies affect analysis, and how different tools approach the same problem.

---

## Dataset

**Source:** Facebook Political Ads Dataset — 2024 U.S. Election

Each row represents a single advertisement and includes:

- Ad metadata (page name, platform, timestamps)
- Spend, impressions, and audience size (stored as ranges)
- Messaging and topic indicators (binary columns)

> ⚠️ **Note:** The dataset is not included in this repository. Download it and place it in the project directory before running any scripts.

---

## Project Structure
```
Task_01_Descriptive_Stats/
│
├── pure_python_stats.py       # Analysis using standard library only
├── pandas_stats.py            # Analysis using Pandas + visualizations
├── README.md
├── requirements.txt
└── visualizations/            # Generated output from Pandas script
```

---

## How to Run

### 1. Pure Python Script

Runs descriptive statistics using only Python's standard library — no external dependencies required.
```bash
python pure_python_stats.py
```

### 2. Pandas Script

Runs the same analysis using Pandas and generates visualizations saved to the `visualizations/` folder.
```bash
python pandas_stats.py
```

---

## Key Findings

- Ad spending is **highly concentrated** among a small number of major political campaigns
- Most ads have **very low or zero spend**, creating a heavily right-skewed distribution
- Advertising activity **spikes around key political events** such as debates and election day
- Messaging is largely focused on **policy issues** (economy, governance, social topics) rather than candidate promotion alone
- A small number of ads with **very high impressions and spend** significantly pull up averages
- Several columns contain **missing or incomplete data**, which affects analysis results

---

## Comparison of Approaches

Both scripts produce similar overall results but differ in how the analysis is performed.

| Aspect | Pure Python | Pandas |
|---|---|---|
| Missing value handling | Manual | Automatic (`isna()`, `dropna()`) |
| Range-based column parsing | Manual string parsing | Handled with custom or built-in methods |
| Summary statistics | Computed from scratch | `describe()`, `value_counts()` |
| Speed | Slower | Faster |
| Depth of understanding | Higher | Lower |

**Small differences in results** may occur due to:

- Rounding behavior
- Missing value treatment
- Standard deviation method (population vs. sample)
- Automatic type inference in Pandas

Overall, pure Python provided a deeper understanding of the underlying data and computations, while Pandas made the analysis faster and more efficient.
