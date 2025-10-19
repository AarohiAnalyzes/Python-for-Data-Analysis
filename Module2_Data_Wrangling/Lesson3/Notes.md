# Lesson 3: Data Formatting in Python

## 💡 What is Data Formatting?

Data is often collected from **different sources** and stored in **different formats**.  
To make meaningful comparisons and perform accurate analysis, we must bring data into a **common standard of expression** - this process is called **data formatting**.

---

## ⚖️ Why Data Formatting Matters

| Non-Formatted Data | Formatted Data |
|---------------------|----------------|
| Confusing | Clear |
| Hard to aggregate | Easy to aggregate |
| Hard to compare | Easy to compare |

---

### 🧩 Example

**Non-Formatted:**

NY, ny, N.Y, NEW YORK

**Formatted:**

New York

---

## 🧮 Applying Calculations to an Entire Column

In pandas, you can apply operations to entire columns easily.

### Example:
Converting total marks into percentage (assuming 6 subjects):

```python
df["Student_Marks"] = df["Student_Marks"] / 6
```
After performing the calculation, it’s a good practice to rename the column for clarity:

```python
df.rename(columns={"Student_Marks": "Student_Percentage"}, inplace=True)
```

---

## ⚙️ Incorrect Data Types

Sometimes, incorrect data types are assigned to columns (features).
For example, a numeric column may be mistakenly stored as a string (object type).

Common Data Types in pandas

| Data Type | Description                      |
| --------- | -------------------------------- |
| `object`  | Text or mixed data               |
| `int64`   | Integer numbers                  |
| `float64` | Decimal (floating-point) numbers |

---

## 🔍 Identifying and Correcting Data Types

To check the data types of all columns:

```python
df.dtypes
```
To convert a column’s data type:
If the data type of the Student_Marks column is stored as object but should be numeric (int or float):

```python
df["Student_Marks"] = df["Student_Marks"].astype("int")
```

---

## 📘 Summary

| Task                       | Function / Example                                |
| -------------------------- | ------------------------------------------------- |
| Apply operations to column | `df["col"] = df["col"] / value`                   |
| Rename columns             | `df.rename(columns={"old": "new"}, inplace=True)` |
| Check data types           | `df.dtypes`                                       |
| Convert data type          | `df["col"].astype("int")`                         |

