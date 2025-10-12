# 📘 Lesson 3: Importing and Exporting Data in Python

---

## 🧠 1. Overview
This lesson explains how to **import and export data in Python** using the `pandas` library.  
You'll learn to read data from multiple sources (CSV, JSON, Excel, SQL, web URLs) and export it into different formats.

---

## 🗂️ 2. Importing Data

### 2.1 Definition
**Importing data** means reading and loading external data into Python from local files or online sources.

### 2.2 Important Properties

| Property | Description | Example |
|-----------|--------------|----------|
| **Format** | How the data is encoded | CSV, JSON, XLSX |
| **File Path** | Where the data is stored | Local path or URL |

---

## 📥 3. Importing a CSV File into Python

```python
import pandas as pd

# URL of the dataset (Iris dataset)
url = "https://raw.githubusercontent.com/mwaskom/seaborn-data/master/iris.csv"

# Read the CSV file into a DataFrame
iris_df = pd.read_csv(url)

# Display data
print(iris_df.head())        # Prints first 5 rows
print(iris_df.head(10))      # Prints first 10 rows
print(iris_df.tail())        # Prints last 5 rows
```
⚠️ Avoid using print(iris_df) for large datasets — it prints the entire file.

---

## 🧾 4. Common Pandas Import Functions

| Format    | Function          | Example                                    |
| :-------- | :---------------- | :----------------------------------------- |
| **CSV**   | `pd.read_csv()`   | `pd.read_csv("data.csv")`                  |
| **JSON**  | `pd.read_json()`  | `pd.read_json("data.json")`                |
| **Excel** | `pd.read_excel()` | `pd.read_excel("data.xlsx")`               |
| **SQL**   | `pd.read_sql()`   | `pd.read_sql("SELECT * FROM table", conn)` |

---

## 💾 5. Exporting Data from Python

Once you’ve processed or cleaned your data, you can save it in various formats.

### 5.1 Export Example — CSV
```
# Export the DataFrame to a CSV file
iris_df.to_csv("iris_exported.csv", index=False)
```
This creates a file named iris_exported.csv in your working directory.

---

✅ 6. Summary

- Use Pandas to import and export datasets easily.
- Always verify file paths and formats before loading.
- Use .head() and .tail() to safely preview data.
- Export data with to_csv(), to_json(), to_excel(), or to_sql().
- When importing from the web, make sure URLs are direct links to raw data.
