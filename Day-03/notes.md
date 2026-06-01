# Day 3 Notes — Statistics for Machine Learning 📊

# Why Statistics Matters in Machine Learning

Machine Learning models learn patterns from data.

Statistics helps us:
- understand data
- identify patterns
- detect anomalies
- summarize information
- make data-driven decisions

Statistics is one of the core foundations of Machine Learning.

---

# Mean (Average)

Mean represents the average value of a dataset.

Formula:

Mean = Sum of Values / Number of Values

Example:

Data:
[10, 20, 30, 40, 50]

Mean:

(10 + 20 + 30 + 40 + 50) / 5

= 30

Python:

```python
np.mean(data)
```

---

# Median

Median is the middle value after sorting data.

Example:

[10, 20, 30, 40, 50]

Median = 30

Python:

```python
np.median(data)
```

---

# Why Median is Important

Median is resistant to outliers.

Example:

[10, 20, 30, 40, 1000]

Mean becomes very large due to 1000.

Median remains:

30

Therefore:

- Mean is sensitive to outliers
- Median is robust against outliers

---

# Mode

Mode is the most frequently occurring value.

Example:

[10, 10, 20, 20, 20, 30]

Mode = 20

Python:

```python
from scipy import stats

stats.mode(data)
```

---

# Range

Range measures the spread of data.

Formula:

Range = Maximum Value - Minimum Value

Example:

[10, 20, 30, 40, 50]

Range:

50 - 10 = 40

Python:

```python
data.max() - data.min()
```

---

# Variance

Variance measures how far data points are spread from the mean.

Low Variance:

[50, 50, 50, 50]

High Variance:

[10, 30, 50, 70, 90]

Python:

```python
np.var(data)
```

---

# Standard Deviation

Standard Deviation is the square root of variance.

It measures the average distance of values from the mean.

Low Standard Deviation:
- values are close together

High Standard Deviation:
- values are spread out

Python:

```python
np.std(data)
```

---

# Histogram

Histogram helps visualize data distribution.

Python:

```python
plt.hist(data)
```

Histogram helps identify:
- spread
- concentration
- skewness
- unusual values

---

# Outliers

Outliers are values that are significantly different from the rest of the dataset.

Example:

[25, 30, 35, 40, 45, 200]

Here:

200 is an outlier.

Outliers can:
- distort averages
- affect model performance
- create misleading conclusions

---

# Boxplot

Boxplots help visualize:

- Median
- Spread
- Quartiles
- Outliers

Python:

```python
plt.boxplot(data)
```

Boxplots are commonly used during Exploratory Data Analysis (EDA).

---

# Quartiles

Quartiles divide data into four equal parts.

Q1 → 25th Percentile

Q2 → Median (50th Percentile)

Q3 → 75th Percentile

Python:

```python
Q1 = np.percentile(data, 25)

Q3 = np.percentile(data, 75)
```

---

# Interquartile Range (IQR)

IQR measures the spread of the middle 50% of the data.

Formula:

IQR = Q3 - Q1

Python:

```python
IQR = Q3 - Q1
```

---

# Outlier Detection using IQR

Lower Bound:

Q1 - 1.5 × IQR

Upper Bound:

Q3 + 1.5 × IQR

Values outside these bounds are considered outliers.

Python:

```python
outliers = data[
    (data < lower_bound) |
    (data > upper_bound)
]
```

---

# Salary Dataset Analysis

Dataset:

```python
salary = np.array([
    25000,
    30000,
    35000,
    40000,
    45000,
    50000,
    200000
])
```

Results:

Q1 = 32500

Q3 = 47500

IQR = 15000

Lower Bound = 10000

Upper Bound = 70000

Detected Outlier:

200000

---

# Mean vs Median

When outliers exist:

Use Median

Reason:

Median is not heavily affected by extreme values.

Example:

Employee salaries often contain:
- Managers
- Directors
- CEOs

Their salaries can significantly increase the mean.

Median usually provides a more realistic representation of a typical employee salary.

---

# Key Learnings from Day 3

Today I learned:

- Mean
- Median
- Mode
- Range
- Variance
- Standard Deviation
- Histograms
- Outliers
- Boxplots
- Quartiles
- IQR
- Outlier Detection
- Mean vs Median Analysis

---

# Machine Learning Connection

Statistics helps Machine Learning by:

- Understanding data distributions
- Detecting anomalies
- Identifying outliers
- Improving data quality
- Making better preprocessing decisions

Strong statistics foundations lead to better Machine Learning models.

---

# Day 3 Conclusion

Today I learned how to summarize, analyze, and understand datasets using statistical techniques.

I also learned how outliers affect data and how to detect them using boxplots and the IQR method.

These concepts form an important foundation for Machine Learning, Data Analysis, and Exploratory Data Analysis (EDA).