Board Games Data Processing

This repository contains shell scripts for data quality checking and data cleaning of board game datasets. The scripts are designed to process raw data files and convert them into a cleaned format for further analysis.

Scripts

1. empty_cell - Data Quality Checking

The empty_cell script checks the dataset for empty cells in each column and reports the count of missing values.

To Run:
1. Give execute permissions to the script:
   chmod +x empty_cell
2. Run the script with your dataset:
   ./empty_cell sample.txt

Output:
The script will output the count of empty cells in each column of the dataset.

---

2. preprocess1 - Data Cleaning

The preprocess1 script is responsible for cleaning the dataset. It:
- Converts semicolons to tabs.
- Removes Windows line endings (\r).
- Converts commas to dots in the Rating Average column.
- Removes non-ASCII characters (e.g., "CO2" -> "CO").

To Run:
1. Give execute permissions to the script:
   chmod +x preprocess1
2. Run the script with your dataset:
   ./preprocess1 sample.txt

Output:
The script will generate a cleaned file named sample.tsv.

---

Requirements

Ensure that you have the necessary permissions to execute the scripts and that you are using a Unix-like environment (Linux, macOS, etc.).

---
