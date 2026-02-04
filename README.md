This project implements an end-to-end Exploratory Data Analysis (EDA) system in Python that analyzes a user-provided CSV dataset and automatically generates meaningful insights. The pipeline loads the dataset, performs data quality checks, infers column types, computes descriptive statistics, produces visualizations, and summarizes key patterns observed in the data. The goal is to help users quickly understand the structure, quality, and characteristics of a dataset with minimal manual effort.

The primary analysis is implemented in a Jupyter Notebook (EDA_new.ipynb) designed to run from top to bottom without requiring manual intervention. The system accepts a required CSV file and optionally a schema or data dictionary file that may describe column meanings, data types, or missing-value codes. The analysis is robust and produces results even when no schema file is provided.

Requirements

Python 3.10 or higher

pip (Python package manager)

All required Python packages are listed in requirements.txt
Project Structure

The repository is organized as follows:

EDA_new.ipynb — End-to-end exploratory data analysis notebook

requirements.txt — Python dependencies required to run the project

README.md — Project documentation

output/ — Automatically generated analysis outputs (tables, plots, insights)

Setup Instructions

First, clone the repository and navigate into the project directory:
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
python -m venv venv
source venv/bin/activate      # macOS/Linux
venv\Scripts\activate         # Windows
Install the required dependencies:
pip install -r requirements.txt
How to Run the Project

Launch Jupyter Notebook:
Open EDA_new.ipynb and select Run All to execute the complete analysis pipeline from start to finish.

Input

Required: A CSV file containing tabular data

Optional: A schema or data dictionary file (CSV or JSON) describing column meanings or missing-value codes

Dataset paths are specified directly in the notebook using a configuration list.

Output

When executed, the notebook automatically creates an output/ directory and generates:

Dataset structure and data type summaries

Missing value and data quality reports

Descriptive statistics for numeric and categorical variables

Multiple visualizations (distributions, relationships, trends)

A concise insights summary based on computed results

The number and type of outputs adapt to the dataset provided.
Optional LLM-Based Insights

The notebook supports optional large language model (LLM)–based insight generation. When enabled and provided with an OpenAI API key, the model generates natural-language insights strictly from computed statistics and plots. If no API key is available, the system automatically falls back to deterministic, rule-based insights.

This behavior is controlled directly within the notebook and does not affect the core analysis pipeline.

Reproducibility and Notes

The notebook is designed to run end-to-end without manual code edits.

All dependencies are explicitly specified to ensure reproducibility.

The analysis produces results even when optional schema files or LLM access are not available.

Outputs are deterministic unless optional LLM functionality is enabled.