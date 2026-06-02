# Python Data Analysis Foundations: NumPy & Pandas

A comprehensive, hands-on guide demonstrating the fundamentals of Python's primary data science libraries: NumPy and Pandas. This repository covers foundational operations ranging from multi-dimensional array manipulation to complex tabular data engineering, sorting, and merging.

---

## 📌 Repository Overview
The purpose of this project is to build and document a rock-solid understanding of Python core data analysis libraries. Rather than just writing scripts, the notebook focuses on solving programmatic micro-challenges to master memory efficiency, indexing syntax, conditional item selection, and dataframe joins.

---

## 🛠️ Core Tech Stack & Concepts
* **NumPy:** Used as a high-performance linear algebra library for multidimensional arrays, combining C/Fortran computational efficiency with easy Python syntax.
* **Pandas:** Utilized as a powerful data manipulation and analysis tool built on top of NumPy, leveraging `Series` (single columns) and `DataFrames` (multi-dimensional tables).

---

## 🔄 Technical Breakdown & Tasks Covered

### 1. NumPy Array & Matrix Engineering
* **Dimensional Definition:** Creating 1-D arrays from lists and setting up precise multi-dimensional matrices.
* **Built-in Generative Methods:** Leveraging functions like `np.random.rand()` for uniform distributions, `np.random.randint()` for bounded integers, `np.arange()` for intervals, and `np.eye()` to produce identity matrices.
* **Vectorized Mathematical Operations:** Executing high-speed element-wise additions, array squaring, square roots (`np.sqrt()`), and exponential scaling (`np.exp()`).
* **Slicing & Indexing:** Accessing specific element coordinates, broadcasting universal modifications across index ranges, and conditionally filtering data subsets (e.g., extracting only odd numbers or clipping negative elements to zero).

### 2. Pandas Tabular Data Operations
* **DataFrame Generation:** Constructing structural dataframes directly out of Python dictionary objects.
* **Web Scraping Tabular Data:** Using `pd.read_html()` to instantly scrape and parse structural market data directly into working dataframes.
* **Advanced Data Engineering & Pipeline Simulation:**
    * Simulating real-world relational database tasks by concatenating discrete dataset rows (`pd.concat()`).
    * Combining disparate text and financial features using relational database-style matching tables via column-based keys (`pd.merge()`).
    * Programmatically applying custom logical transformations over structural columns using `.apply()` lambda/method mapping.
    * Managing memory states permanently using `inplace=True` operations during value sorting.

---

## 📈 Key Code Examples & Challenges Solved

#### Relational Data Pipeline Simulation
The repository concludes with a practical mock enterprise pipeline where separate client name blocks, dynamic salary tables, and newly onboarded client entries are systematically processed, joined, and verified:

```python
# Concatenating separate dataframes and merging complementary features on a common key
bank_df_all = pd.concat([Bank_df_1, Bank_df_2])
bank_df_all = pd.merge(bank_df_all, bank_df_salary, on='Bank Client ID')

# Appending a fresh single-row observation matrix to the main ledger
new_df = pd.concat([bank_df_all, new_client_df], axis=0)

---



## 🎓 Acknowledgments
* **Platform:** Coursera
* **Course Curriculum:** Python for Data Analysis: Pandas & NumPy
* **Course Instructor:** Ryan Ahmed
* **Skills Developed:** High-performance vector math, Boolean array masking, data structural alignment, web-based table extraction, and data validation pipelines.
