# Lesson 4: Data Normalization

### What is Data Normalization?
Data normalization means changing the values of features (columns) in a dataset so they have a similar scale or range.  
This helps machine learning models work better and faster because all data is treated fairly.

---

## Why Normalize Data?
- To make all features (columns) have similar ranges.  
- To improve the accuracy and performance of machine learning models.  
- To make sure one feature doesn’t dominate others due to larger values.

---

## Types of Normalization Methods

## 1. Simple Feature Scaling

This method divides each value by the maximum value of that column.

**Formula:**

```
x_new = x_old / x_max
```

**In Pandas:**

```python
df['length'] = df['length'] / df['length'].max()
```

**Example:**
If the maximum value is 100 and a data point is 50, then the new value = 50 / 100 = 0.5

---

## 2. Min-Max Normalization

This method changes values so they are between 0 and 1.

**Formula:**

```
x_new = (x_old - x_min) / (x_max - x_min)
```

**In Pandas:**

```python
df['length'] = (df['length'] - df['length'].min()) / (df['length'].max() - df['length'].min())
```

**Example:**
If min = 20, max = 100, and value = 60, then (60 - 20) / (100 - 20) = 40 / 80 = 0.5

**Range:** 0 to 1

---

## 3. Z-Score Normalization (Standardization)

This method shows how far a value is from the average (mean).

**Formula:**

```
x_new = (x_old - mean) / standard_deviation
```

**In Pandas:**

```python
df['length'] = (df['length'] - df['length'].mean()) / df['length'].std()
```

**Range:** Around -3 to +3

---

## Summary Table

| Method         | Formula                 | Range | Pandas Code                             |
| -------------- | ----------------------- | ----- | --------------------------------------- |
| Simple Scaling | x / x(max)              | 0 → 1 | df['col'] = df['col'] / df['col'].max() |
| Min-Max        | (x - min) / (max - min) | 0 → 1 | df['col'] =                             |

