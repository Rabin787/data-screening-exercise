# Data Scientist Screening Exercise – Relevant Research

## Overview

This repository contains my submission for the **Data Scientist screening exercise** at Relevant Research.
The objective is to clean, analyze, and visualize a messy real-world administrative dataset related to ICE immigration detention facilities and to identify the **top 10 largest facilities by total population**.

The emphasis of this exercise is on **data quality assessment, transparent cleaning decisions, and reproducible analysis**.

---

## Repository Structure

```text
relevant-research-screening/
├── data/
│   ├── processed/
│   │   ├── cleaned_ice_detention.csv
|   |   └── top_10_detention_facilities.csv
│   └── raw/
|       └── messy_ice_detention.csv
├── notebooks/
│   └── detention_analysis.ipynb
├── output/
│   └── top_10_detention_facilities.png
├── README.md
```

---

## Analysis Workflow

All analysis is documented in the Jupyter Notebook:

```
notebooks/detention_analysis.ipynb
```

### Key steps include:

1. **Data Loading**

   * Importing a non-UTF-8 CSV file using a fallback encoding

2. **Data Cleaning**

   * Removing metadata rows preceding the true header
   * Cleaning facility names by removing special characters and normalizing whitespace
   * Converting population columns (Levels A–D) to numeric values
   * Converting date columns to datetime format

3. **Analysis**

   * Computing total population by summing Levels A–D
   * Identifying the top 10 facilities by total population

4. **Visualization**

   * Creating and saving a bar chart of the top 10 detention facilities

---

## Reproducibility

* Raw data is loaded from `data/raw/`.
* Cleaned outputs are written to `data/processed/`.
* Figures are saved to `output/`.
* All file paths are relative, allowing the notebook to be run end-to-end.

---

## Requirements

* Python
* pandas
* matplotlib

---
## How to Run

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/repo-name.git
   cd repo-name
2. **Install dependencies:**
   Make sure Python is installed, then run:
   ```bash
   pip install pandas matplotlib
3. **Run the analysis notebook:**
   
    * Open notebooks/detention_analysis.ipynb in Jupyter Notebook or JupyterLab.
    * Execute the cells from top to bottom to reproduce the data cleaning, analysis, and visualization.

4. **Outputs:**
   
    * Cleaned CSV files are saved in data/processed/.
    * The top 10 detention facilities chart is saved in output/top_10_detention_facilities.png.


## AI Usage Disclosure

ChatGPT was used as a support tool to assist with:

* Diagnosing CSV encoding issues
* Reasoning about Excel-style datetime serial values and their conversion to datetime
* Improving code comments and documentation

The ChatGPT prompt history used during this exercise can be reviewed here:
**(https://chatgpt.com/share/696e4e53-4310-8000-bcf7-275a966da08f)**

---

## Author

Rabin Karki
