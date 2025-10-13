# 📘 Lesson 4: Getting Started Analyzing Data in Python

---

## 🧠 1. Overview
Before analyzing data, you need to **understand it**.  
Check data types, data distribution, and look for possible issues like missing values.

---

## 🔍 2. Basic Checks

When exploring data, always:
- Check **data types**
- Look at **data distribution**
- Find **missing or incorrect values**

---

## 🧩 3. Data Types

Data types tell what kind of data each column has.

| Pandas Type | Python Type | Description |
|--------------|--------------|-------------|
| **object**   | `string`     | Text or mixed data |
| **int64**    | `int`        | Whole numbers |
| **float64**  | `float`      | Numbers with decimals |

### Why it matters:
- Avoid type mismatches  
- Ensure data works with functions  
- Helps when cleaning or converting data  

```python
# Check data types
df.dtypes
```
---

## 📊 4. Quick Data Summary


| Function | Purpose |
|--------------|--------------|
| **df.describe()**   |  Stats for numeric columns  | 
| **df.describe(include = "all")**   | Summary for all cols |
| **df.info()**  | Data Types, Missing values and Memory use | 

### Example:

```python
print(df.dtypes)          # Check data types
print(df.describe())      # Numeric summary
print(df.info())          # Basic info
```
---

## ✅ 5. Summary

- Always explore your data first.
- Use df.dtypes, df.describe(), and df.info() to learn about it.
- Knowing your data helps avoid errors later in analysis
