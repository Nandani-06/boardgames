# 🧩 Board Games Dataset Analysis

This project analyzes a dataset of board games to uncover trends in game mechanics, domains, and how they relate to rating and complexity.

> **Course**: CITS4407 – Open Source Tools and Scripting
> **Version**: 1.0  
> **Author**: Nandani Patel
> **Student ID**: 24055729

---

## 📂 Project Overview

This project includes three Bash scripts:

### 1. `empty_cells` 
- Indicates how many empty cells there are in each column of a data set that is separated by semicolons.
- enables the identification of flaws in data quality prior to analysis.

### 2. `preprocess`
The raw data set is cleaned and transformed:
Tabs are used in place of semicolon delimiters.
In numeric columns, it substitutes dots for commas.
- Eliminates non-ASCII characters and Windows carriage returns.
- Automatically adds new, distinct values to missing IDs.
Sanitised `.tsv` is printed out for analysis. 

### 3. `analysis`

The sanitised data is subjected to statistical analysis:

- Identifies the most frequent **game mechanic** and **game domain** (based on occurrence counts).
- Calculates the **Pearson correlation** between:
  - Year of publication and average rating.
  - Complexity and average rating.
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

---
## 🔗 Project Repository
You can view or clone the project on GitHub:  
👉 [https://github.com/Nandani-06/boardgames](https://github.com/Nandani-06/boardgames)

