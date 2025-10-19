# Lesson 2: Dealing with Missing Values in Python

---

## 💡 What is a Missing Value?

A **missing value** occurs when **no data value** is stored for a variable (column or feature) in an observation (row).  

Missing values can appear in several forms, such as:

- `"?"`
- `"N/A"`
- `0`
- Blank cell (`""`)
- `"NaN"`

---

## ⚙️ How to Deal with Missing Values

There are several strategies to handle missing data depending on the context and dataset.

### 1. ✅ Check with the Data Collection Source
Before making assumptions, verify whether missing data is due to:
- Data entry errors
- Technical issues
- Non-response or data not applicable

---

### 2. 🗑️ Drop the Missing Values

You can remove missing values by **dropping rows or columns** containing them.

**Options:**
- **Drop the variable (column)**
- **Drop the data entry (row)**

#### Example in Python:

```python
df.dropna(subset=['Student_Marks'], axis=0, inplace=True)
```

- axis=0 → drop the row
- axis=1 → drop the column
- If inplace=True is not mentioned, it does not modify the original DataFrame

---

### 3. 🔄 Replacing the Missing Values

Instead of deleting, you can **replace** missing values using several strategies:

1. Replace with the average (mean) of similar data points
2. Replace by frequency (mode)
3. Replace based on other functions or logic

#### Example in Python:

```python
mean_marks = df["Student_Marks"].mean()
df["Student_Marks"].replace(np.nan, mean_marks, inplace=True)
```

---

### 4. 🚫 Leave It as Missing Data

In some cases, it’s better to leave missing values as they are -
especially when the missingness itself carries meaning (e.g., a skipped survey question).

--- 

### 5. 🧠 Summary

| Method           | Description                    | Example                    |
| ---------------- | ------------------------------ | -------------------------- |
| Check Source     | Verify reason for missing data | Contact data provider      |
| Drop Values      | Remove rows/columns            | `df.dropna()`              |
| Replace Values   | Use mean, mode, or logic       | `df.replace(np.nan, mean)` |
| Leave as Missing | Keep as-is if meaningful       | —                          |

---

### 6. 📘 Key Functions Recap

| Function                           | Description                               |
| ---------------------------------- | ----------------------------------------- |
| `df.dropna()`                      | Drop rows or columns with missing values  |
| `df.replace(missing_val, new_val)` | Replace specific missing values           |
| `df.isnull()`                      | Detect missing values                     |
| `df.fillna(value)`                 | Fill missing values with a specific value |
