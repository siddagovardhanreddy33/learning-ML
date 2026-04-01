# 📊 Data Profiling & YData-Profiling

---

## 🧠 What is Data Profiling?

**Data Profiling** is the process of examining and understanding a dataset before applying Machine Learning or analysis.

It helps answer questions like:

- What type of data do we have?
- Are there missing values?
- Are there errors or duplicates?
- Which features are important?
- How are variables related?
- Is the data suitable for ML?

👉 **In short:**  
**Data Profiling = Understanding your data deeply**

---

## 🎯 Why Data Profiling is Important?

Before building ML models, we must check data quality.

**Bad data → Bad model ❌**  
**Clean data → Better accuracy ✅**

---

## 🔍 Example Problems Data Profiling Detects

| Problem | Example |
|--------|--------|
| Missing values | salary column has null values |
| Duplicates | same customer repeated |
| Outliers | salary = 999999999 |
| Wrong datatype | age stored as text |
| Imbalance | 95% values are same |
| High correlation | duplicate information |

---

## 📊 What Data Profiling Analyzes

### 1. Basic Information
- number of rows
- number of columns
- data types
- memory usage

---

### 2. Statistical Summary (Numerical Data)
- mean
- median
- mode
- min / max
- standard deviation
- quartiles

---

### 3. Missing Values
- identifies null values
- shows percentage of missing data
- helps decide filling or removing data

---

### 4. Data Distribution
- normal distribution
- skewed distribution
- uniform distribution

Helps in:
- scaling
- transformation
- normalization

---

### 5. Correlation Between Features
Shows relationship between variables.

Example:
- experience ↑ → salary ↑
- height ↑ → weight ↑

Helps in feature selection.

---

### 6. Outlier Detection
Detects unusual extreme values.

Example:
salary = 9999999

---

### 7. Data Quality Warnings
Profiling tools automatically detect:

- high correlation
- missing values
- skewed data
- constant columns
- imbalance in dataset

---

# 🤖 What is YData-Profiling?

**YData-Profiling** is a Python library that automatically performs **Data Profiling** and generates a detailed **EDA report**.

Earlier name:
**pandas-profiling** (deprecated)

---

## ⚡ What YData-Profiling Does

Automatically analyzes:

- data types
- missing values
- distributions
- correlations
- outliers
- duplicates
- feature interactions
- data quality issues

Generates interactive HTML report.

---

## 🧪 Example Code

```python
from ydata_profiling import ProfileReport

profile = ProfileReport(df)

profile.to_file("report.html")