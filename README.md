## Introduction To Data Structure (Titanic 9 Challenges)

## Team Details
| Team #      | Member                          | ID (if applicable) |
| ----------- | ------------------------------- | ------------------ |
| **Group 2** | Andrew Silveira                 | **5077086**               |
|             | Rohit Krishnamurthy Iyer        | **8993045**        |
|             | Sabrina Ronnie George Karippatt | **8991911**        |

## Table of Contents
1. Environment Setup
2. Install Dependencies
3. Project Structure
4. Data Sources
5. Notebook Outline (0–9)
6. How to Run
7. Exports
8. Reproducibility
9. Troubleshooting

## Environment Setup 
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

## Install dependencies
The notebook uses NumPy, Pandas, Matplotlib, Jupyter, Seaborn (optional for loading Titanic), and Matplotlib-Venn (optional).

    pip install numpy pandas matplotlib jupyter seaborn matplotlib-venn scipy

## Project Structure
Group_Presentation_1/
├─ Include/                 # venv dirs live at project root (not in .venv/)
├─ Lib/
├─ Scripts/
├─ etc/
├─ share/
├─ pyvenv.cfg
├─ data/
│  └─ titanic_data.csv
├─ notebook/
│  ├─ outputs/
│  │  └─ numerical_summary_20250916-043806.csv
│  └─ Challenges_Solution.ipynb
├─ README.md
└─ requirements.txt

## Data Sources

We can load Titanic either from Seaborn or from a local CSV (use only one at a time):
- Seaborn: sns.load_dataset("titanic")
Quick and consistent; pre-cleaned columns; internet required for first fetch.
- Local CSV: pd.read_csv("data/titanic_data.csv")
Matches your file; works offline; may include extra columns; might need cleaning.

## Notebook Outline with Challenges

0) Setup & Imports — modern typing, core libs, plotting; guarded Venn import (HAS_VENN).
1) Data Loading — Seaborn or CSV; defines X1=age, X2=fare, Y=survived.
2) Helpers — clean_series() (drop NaNs), format_number() (pretty output).
3) Mean / 4) Median / 5) Mode — clear explanations + interpretations; NaN-safe.
5) OOP Central Tendency — CentralTendency with mean/median/mode/report.
6) OOP Dispersion — DispersionMeasures with variance, std, five-number, IQR, interpret(); ddof=1 vs 0.
7) Numerical Summary & Plots — one-row summaries; histogram (Age), boxplot (Fare), scatter (Age vs Fare), optional Venn.
8) OOP NumericalSummary + Export — composes (5)+(6); exports CSV/Excel; optional extra numeric cols.
9) Conclusions, Limitations & Next Steps + Final Unit Checks — concise wrap-up + assertions.

## How to Run
- Activate the virtual environment.
- Launch Jupyter.
- Open the notebook and run cells top to bottom the first time.
- Keep only one data loading option active (Seaborn or CSV).
- Review printed interpretations after each section for talk tracks.

## Reproducibility

- The notebook sets a global random seed (RANDOM_SEED = 42) for any sampling.
- Helper functions ensure consistent NaN handling and formatting.
- Assertions in Challenges 6, 8, 9 provide lightweight unit checks to prove correctness.

## Troubleshooting

- ImportError: seaborn not found
    pip install seaborn
- Plots look odd for Fare
    Use the log-scale boxplot (added in Challenge 7 add-ons).
- Dataset columns differ from Seaborn
    Switch to the CSV loader and adjust column names (age, fare, survived) accordingly.
