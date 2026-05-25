# Day 1 Notes — NumPy Foundations 

# What is NumPy?

NumPy is a Python library used for numerical computing and working with arrays efficiently.

It is widely used in:
- Machine Learning
- Data Science
- Deep Learning
- Data Analysis

NumPy is faster and more optimized than normal Python lists.

---

# Why NumPy is Important in ML

Machine Learning works heavily with:
- numbers
- datasets
- matrices
- tensors

NumPy helps perform operations efficiently on large amounts of numerical data.

---

# Topics Learned

## 1. Creating Arrays

```python
import numpy as np

arr = np.array([1,2,3,4,5])
```

NumPy arrays are optimized containers for numerical data.

---

## 2. Indexing

```python
arr[0]
arr[2]
```

Used to access specific elements inside arrays.

---

## 3. Vectorized Operations

```python
arr + 10
arr * 2
```

NumPy can apply operations to all elements at once without loops.

This is called vectorization.

---

## 4. Statistical Operations

```python
arr.mean()
arr.max()
arr.min()
arr.sum()
```

These functions help analyze numerical datasets.

---

## 5. Boolean Masking / Filtering

```python
arr[arr > 50]
```

Used to filter values based on conditions.

Very important in data analysis and ML preprocessing.

---

## 6. Multiple Conditions

```python
(arr > 50) & (arr < 90)
```

Used for advanced filtering.

---

## 7. 2D Arrays

```python
data = np.array([
    [78,92],
    [45,70]
])
```

2D arrays represent rows and columns similar to tables or spreadsheets.

---

# Shape

```python
data.shape
```

Used to understand dimensions of data.

Example:
- (5,2) → 5 rows and 2 columns

---

# Axis Concept

## axis = 0
Column-wise operation

## axis = 1
Row-wise operation

Example:

```python
data.sum(axis=1)
```

Calculates row totals.

---

# Aggregation Functions

```python
sum()
mean()
max()
min()
argmax()
```

Used to summarize and analyze data.

---

# Random Data Generation

```python
np.random.randint(40,100,size=20)
```

Used to generate random numerical datasets.

---

# Data Visualization

## Bar Plot

```python
plt.bar()
```

Used to compare values.

---

## Histogram

```python
plt.hist()
```

Used to visualize data distribution.

---

# Key Learnings

- NumPy is the foundation of ML computation
- Arrays are faster than normal Python lists
- Vectorized operations make computations efficient
- Filtering and masking are important for data preprocessing
- Data analysis starts with understanding patterns in datasets
- Visualization helps understand distributions and trends

---

# Debugging Lesson Learned

Using:
```python
{}
```

creates a set, not a list.

Correct:
```python
[]
```

Lists maintain order and work properly with visualization libraries like Matplotlib.

---

# Day 1 Conclusion

Today I learned the foundations of numerical computing and data analysis using NumPy.

I practiced:
- arrays
- filtering
- conditions
- multidimensional data
- aggregation
- visualization
- debugging

This forms the foundation for future ML and Deep Learning concepts.