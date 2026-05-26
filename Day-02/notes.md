# Day 2 Notes — Pandas & Exploratory Data Analysis (EDA) 🚀

# What is Pandas?

Pandas is a Python library used for:
- data analysis
- data manipulation
- handling structured datasets

It is one of the most important libraries in:
- Machine Learning
- Data Science
- Data Analytics

---

# Why Pandas is Important

Real-world datasets are usually:
- large
- messy
- incomplete
- structured in rows and columns

Pandas helps:
- organize data
- clean datasets
- filter information
- analyze patterns

---

# What is a DataFrame?

A DataFrame is a table-like structure in Pandas.

Example:

| Name | Marks | Attendance |
|------|------|------|
| Aman | 90 | 92 |
| Priya | 85 | 95 |

Rows represent records.

Columns represent features or attributes.

---

# Creating a DataFrame

```python
import pandas as pd

data = {
    "Name": ["Aman", "Priya"],
    "Marks": [90, 85]
}

df = pd.DataFrame(data)
```

---

# Important DataFrame Operations

## head()

```python
df.head()
```

Displays first few rows.

---

## shape

```python
df.shape
```

Returns:
```python
(rows, columns)
```

---

## columns

```python
df.columns
```

Shows column names.

---

## info()

```python
df.info()
```

Provides:
- column information
- data types
- missing values

Very important in ML preprocessing.

---

# Selecting Data

## Single Column

```python
df["Marks"]
```

---

## Multiple Columns

```python
df[["Name", "Marks"]]
```

---

# Filtering Data

```python
df[df["Marks"] > 80]
```

Used to filter rows based on conditions.

This is heavily used in:
- analytics
- preprocessing
- ML pipelines

---

# Sorting Data

```python
df.sort_values(by="Marks", ascending=False)
```

Used to sort datasets.

---

# Aggregation Functions

## Mean

```python
df["Marks"].mean()
```

---

## Maximum

```python
df["Marks"].max()
```

---

## Minimum

```python
df["Marks"].min()
```

---

## Sum

```python
df["Marks"].sum()
```

Aggregation functions help summarize data.

---

# Feature Engineering

Feature engineering means creating new useful columns from existing data.

Example:

```python
df["Total"] = df["Math"] + df["Science"] + df["English"]
```

This is very important in Machine Learning.

---

# apply() Function

Used to apply custom functions to columns.

Example:

```python
df["Grade"] = df["Average"].apply(assign_grade)
```

This is useful for:
- transformations
- preprocessing
- categorization

---

# Missing Values

Missing values are represented as:

```python
NaN
```

Meaning:
```python
Not a Number
```

Real datasets commonly contain missing values.

---

# Detecting Missing Values

```python
df.isnull()
```

Returns:
- True → missing
- False → not missing

---

# Counting Missing Values

```python
df.isnull().sum()
```

Very important during preprocessing.

---

# Handling Missing Values

Example:

```python
df["Marks"] = df["Marks"].fillna(df["Marks"].mean())
```

This replaces missing values using average values.

Common preprocessing technique.

---

# CSV Handling

## Save CSV

```python
df.to_csv("data.csv", index=False)
```

---

## Read CSV

```python
pd.read_csv("data.csv")
```

CSV files are commonly used in:
- Machine Learning
- Data Analysis
- Real-world datasets

---

# What is EDA?

EDA = Exploratory Data Analysis

EDA means:
- understanding data
- finding patterns
- identifying trends
- detecting relationships
- checking missing values
- visualizing data

EDA happens before building ML models.

---

# Data Visualization

Visualization helps understand data patterns visually.

---

# Bar Graph

```python
plt.bar()
```

Used for comparisons.

---

# Histogram

```python
plt.hist()
```

Used to understand data distribution.

---

# Heatmap

```python
sns.heatmap()
```

Used for correlation analysis.

---

# Correlation

Correlation measures relationship between variables.

Example:
- higher attendance → higher marks

---

# Correlation Values

| Value | Meaning |
|------|------|
| 1 | Strong Positive Relationship |
| 0 | No Relationship |
| -1 | Strong Negative Relationship |

---

# Correlation Matrix

```python
df.corr(numeric_only=True)
```

Used heavily in:
- feature selection
- ML preprocessing
- analytics

---

# groupby()

One of the most important Pandas operations.

Example:

```python
df.groupby("Brand")["Sales"].sum()
```

Used for:
- grouping categories
- aggregating values
- business analytics

---

# Key Learnings from Day 2

Today I learned:
- DataFrames
- filtering datasets
- sorting data
- feature engineering
- apply() functions
- handling missing values
- CSV operations
- EDA concepts
- correlation analysis
- heatmaps
- groupby()
- business-style analytics

---

# Day 2 Conclusion

Today I moved from:
- numerical arrays
to
- structured real-world datasets.

I practiced:
- data cleaning
- analysis
- visualization
- preprocessing
- exploratory data analysis

This forms the foundation of real-world Machine Learning workflows.