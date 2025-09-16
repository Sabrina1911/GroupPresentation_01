## Introduction To Data Structure (Titanic 9 Challenges)

## Team Details

| Team #      | Member                          | ID (if applicable) |
| ----------- | ------------------------------- | ------------------ |
| **Group 1** | Andrew Silveira                 | **5077086**        |
|             | Rohit Krishnamurthy Iyer        | **8993045**        |
|             | Sabrina Ronnie George Karippatt | **8991911**        |

---

## 📘 Project Abstract

This project explores the **Titanic dataset** through a structured sequence of **9 challenges**, focusing on descriptive statistics, exploratory data analysis (EDA), and object-oriented programming (OOP) in Python.  

The notebook is written as a **story**:
- Each challenge begins with a short **conceptual explanation**.  
- Code is implemented with reusable **helper functions** and **OOP classes**.  
- Results are paired with **plain-language interpretations**.  

The final output demonstrates how statistics (mean, median, mode, variance, std, IQR, plots) can provide insights into the Titanic dataset and lay the foundation for more advanced analysis and modeling.

---

## Table of Contents
1. Environment Setup
2. Install Dependencies
3. Project Structure
4. Data Sources
5. Notebook Outline (1-13)
6. How to Run
7. Exports
8. Reproducibility
9. Troubleshooting

---

## Environment Setup 
```bash
   # Windows (PowerShell)
    cd C:\Users\Sabrina\1557_VSC\DataAnalysis\Group_Presentation_1
    python -m venv .venv
    .venv\Scripts\Activate
    python -m pip install --upgrade pip

   # macOS / Linux
    cd path/to/Group_Presentation_1
    python -m venv .venv
    source .venv/bin/activate
    python -m pip install --upgrade pip
```
---    

## Install dependencies
The notebook uses:
   * Core: NumPy, Pandas, Matplotlib, Jupyter
   * Optional: Seaborn (Titanic dataset), Matplotlib-Venn (Venn diagrams), SciPy (stats utilities)

             pip install numpy pandas matplotlib jupyter seaborn matplotlib-venn scipy

---             

## Project Structure
Group_Presentation_1/
├─ data/
│  └─ titanic_data.csv
├─ notebook/
│  ├─ outputs/
│  │  └─ numerical_summary_YYYYMMDD-HHMMSS.csv
│  └─ Challenges_Solution.ipynb
├─ README.md
└─ requirements.txt

---

## Data Sources

We can load Titanic either from Seaborn or from a local CSV (use only one at a time):
- Seaborn: sns.load_dataset("titanic")
    Quick and consistent; pre-cleaned columns (requires internet on first fetch)..
- Local CSV: pd.read_csv("data/titanic_data.csv")
    Works offline, matches your provided file, may include extra columns (requires cleaning).

---

## Notebook Outline with Challenges

1) Setup & Imports — modern typing, core libs, plotting; guarded Venn import (HAS_VENN).
2) Data Loading — Seaborn or CSV; defines X1=age, X2=fare, Y=survived.
3) Helpers — clean_series() (drop NaNs), format_number() (pretty output).
4) Challenge 1 – Mean — clear explanations + interpretations; NaN-safe.
5) Challenge 2 – Median — consistent structure with interpretation.
6) Challenge 3 – Mode — handles multimodal outputs, includes context.
7) Challenge 4a – Data Exploration — shape, dtypes, missing values, summaries.
8) Challenge 4b – Summary of Use Case — bridges dataset context with analysis goals.
9) Challenge 5 – OOP Central Tendency — CentralTendency class with report().
10) Challenge 6 – OOP Dispersion — DispersionMeasures class with variance, std, IQR, interpretation.
11) Challenge 7 – Numerical Summary & Plots — summary table + histogram, boxplot, scatter, optional Venn.
12) Challenge 8 – NumericalSummary (Compose + Export) — combines Central Tendency + Dispersion; exports CSV/Excel
13) Challenge 9 – Conclusions, Limitations & Next Steps — concise wrap-up + unit checks.

---

## How to Run
- Activate the virtual environment.
- Launch Jupyter Notebook.
- Open Challenges_Solution.ipynb and run cells top-to-bottom.
- Keep only one data loading option active (Seaborn or CSV).
- Review the printed interpretations for talking points in class.

---

## Exports

- Numerical summaries are saved in the notebook/outputs/ folder.
- File formats:
    * CSV (numerical_summary_*.csv) → always generated.
    * Excel (numerical_summary_*.xlsx) → generated if openpyxl is installed.
---   

## Reproducibility

- Global random seed: RANDOM_SEED = 42.
- Helper functions ensure consistent NaN handling and formatting.
- Assertions in Challenges 6, 8, 9 provide lightweight unit checks.

---

## Troubleshooting

- ImportError: seaborn not found -> pip install seaborn
- ImportError: openpyxl not found -> pip install openpyxl
- Plots look odd for Fare -> use the log-scale boxplot (added in Challenge 7).
- Dataset columns differ from Seaborn -> switch to the CSV loader and align column names (age, fare, survived).

