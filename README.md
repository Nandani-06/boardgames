# 🧩 Board Games Dataset Analysis

This project analyzes a dataset of board games to uncover trends in game mechanics, domains, and how they relate to rating and complexity.

> **Course**: CITS4407 – Open Source Tools and Scripting
> **Version**: 1.0  
> **Author**: Nandani Patel
> **Student ID**: 24055729

---

## 📂 Project Overview

This project includes three Bash scripts:

**`empty_cells`**: Scans a raw board game dataset and counts missing values per column     
**`preprocess`**: Cleans the dataset by standardizing formats and filling missing IDs     
**`analysis`**: Performs statistical analysis on the cleaned data                       

---

## 🛠 How to Use

### 1. Check for Missing Values

```bash
./empty_cells bgg_dataset.txt
````

Outputs a count of empty cells for each column in the dataset.

---

### 2. Preprocess the Dataset

```bash
./preprocess bgg_dataset.txt
```

Creates a cleaned TSV file `bgg_dataset.tsv` with:

* Semicolon (`;`) replaced by tabs
* Carriage return characters removed
* Commas in decimal numbers replaced with dots
* Non-ASCII characters removed
* Missing `/ID` values filled with new unique IDs

---

### 3. Run Analysis on Cleaned Data

```bash
./analysis bgg_dataset.tsv
```

Outputs:

* Most popular **game mechanic**
* Most popular **game domain**
* Pearson correlation between **Year** and **Average Rating**
* Pearson correlation between **Complexity** and **Average Rating**
