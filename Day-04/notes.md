# Day 04 - Statistics for Machine Learning + First ML Model

# Why are we learning Statistics?

Machine Learning is not magic.

A machine learns patterns from data.

To understand whether the machine is learning correctly, we need Statistics.

Think of Statistics as the language of data.

Without Statistics:

```text
Data = Random Numbers
```

With Statistics:

```text
Data = Information
```

---

# 1. Probability

Probability tells us how likely an event is to happen.

Formula:

Probability = Favorable Outcomes / Total Outcomes

---

## Example 1: Coin Toss

Possible Outcomes:

* Heads
* Tails

Total Outcomes = 2

Probability of getting Heads:

P(Heads) = 1 / 2 = 0.5 = 50%

Meaning:

If we toss a coin many times, roughly half of the tosses should be Heads.

---

## Example 2: Dice Roll

Possible Outcomes:

1, 2, 3, 4, 5, 6

Total Outcomes = 6

Probability of getting 3:

P(3) = 1 / 6

≈ 16.67%

---

## Why ML Uses Probability

Suppose Gmail receives an email.

The ML model may predict:

Spam = 95%

Not Spam = 5%

The model is using probability.

---

# 2. Normal Distribution (Bell Curve)

Many real-world datasets follow a Bell-shaped pattern.

Examples:

* Student Marks
* Human Heights
* Human Weights
* IQ Scores

Most values are near the center.

Very high values are rare.

Very low values are rare.

Example:

Marks of students:

```text
20 40 50 60 70 75 80 90 100
```

Most students are around:

60 - 80

Very few score:

20 or 100

This creates a Bell Curve.

---

# Mean, Median and Mode

For a perfect Normal Distribution:

Mean ≈ Median ≈ Mode

All three are located near the center.

---

# 3. Standard Deviation

Standard Deviation tells us:

"How spread out the data is."

Small Standard Deviation:

Data is close to the mean.

Large Standard Deviation:

Data is spread out.

---

Example:

Mean Marks = 70

Standard Deviation = 10

Most students are expected near:

70 ± 10

Which means:

60 to 80

---

# The Famous 68-95-99.7 Rule

For Normal Distribution:

Within 1 Standard Deviation:

68% of data lies here.

Example:

70 ± 10

60 to 80

---

Within 2 Standard Deviations:

95% of data lies here.

70 ± 20

50 to 90

---

Within 3 Standard Deviations:

99.7% of data lies here.

70 ± 30

40 to 100

---

# Why Is This Important?

It helps us identify unusual values.

These unusual values are often called:

Outliers

---

# 4. Z-Score

Z-Score tells us:

"How far a value is from the mean."

Formula:

Z = (Value - Mean) / Standard Deviation

---

Example:

Mean = 50

Standard Deviation = 5

Value = 55

Z = (55 - 50) / 5

Z = 1

Meaning:

The value is 1 standard deviation above the mean.

---

Example:

Value = 40

Z = (40 - 50) / 5

Z = -2

Meaning:

The value is 2 standard deviations below the mean.

---

Outlier Rule:

If:

|Z| > 3

the value may be considered unusual.

---

# 5. Percentiles

Percentiles tell us how a value compares to the rest of the data.

---

Example:

You are in the 90th percentile.

Meaning:

You performed better than 90% of people.

Only 10% performed better than you.

---

Example:

85th percentile means:

85% of observations lie below that value.

---

Important Percentiles:

25th Percentile = Q1

50th Percentile = Median

75th Percentile = Q3

---

# Machine Learning Begins

Until now:

We were understanding data.

Now:

We will make the computer learn from data.

---

# Dataset

Hours Studied vs Marks

| Hours | Marks |
| ----- | ----- |
| 1     | 35    |
| 2     | 40    |
| 3     | 50    |
| 4     | 55    |
| 5     | 65    |
| 6     | 70    |
| 7     | 80    |
| 8     | 90    |

Question:

Can a machine learn this relationship?

Answer:

Yes.

---

# Feature (X)

Feature means:

Input to the model.

Example:

Hours Studied

If we know:

Hours = 5

We want to predict Marks.

Therefore:

X = Hours

---

# Target (y)

Target means:

Output we want to predict.

Example:

Marks

Therefore:

y = Marks

---

Think Like This

Hours Studied
↓
Machine Learning Model
↓
Marks

---

# Linear Regression

Linear Regression learns a straight-line relationship.

Example:

More Hours Studied
↓
More Marks

The model learns:

Marks ≈ m × Hours + c

where:

m = slope

c = intercept

---

# Training a Model

Code:

model.fit(X, y)

Meaning:

Learn the relationship between X and y.

Think:

Teacher gives examples.

Student learns patterns.

The model is the student.

---

# Making Predictions

Code:

model.predict([[9]])

Meaning:

Predict marks for 9 study hours.

Our Result:

95.71

---

# Important Lesson

The model predicted:

10 hours → 103.5 marks

But exam marks cannot exceed 100.

Why?

Because:

Machine Learning learns patterns.

Machine Learning does NOT use common sense.

---

# Train-Test Split

Question:

How do we know the model actually learned?

Answer:

Test it on unseen data.

---

Training Data

Used for learning.

Testing Data

Used for evaluation.

---

Our Split:

75% Training

25% Testing

Result:

Training Rows = 6

Testing Rows = 2

---

# Model Evaluation

Predictions:

41.7
72.9

Actual:

40
70

---

# Mean Absolute Error (MAE)

Formula:

Average of all prediction errors.

Example:

Error 1 = 1.7

Error 2 = 2.9

Average Error:

2.3

---

Interpretation

MAE = 2.3

Meaning:

The model is wrong by approximately 2.3 marks on average.

Smaller MAE = Better Model

---

# What I Learned Today

✓ Probability

✓ Normal Distribution

✓ Standard Deviation

✓ 68-95-99.7 Rule

✓ Z-Score

✓ Percentiles

✓ Features (X)

✓ Target (y)

✓ Linear Regression

✓ Train-Test Split

✓ Predictions

✓ MAE

✓ Machine Learning learns patterns, not common sense

This was my first complete Machine Learning workflow.
