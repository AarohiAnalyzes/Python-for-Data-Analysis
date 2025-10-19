# Lesson 1: Preprocessing Data in Python

Data preprocessing is the process of converting or mapping data from its initial **raw** form into another form suitable for analysis.  
It is also known as **data cleaning** or **data wrangling**.

---

## 🎯 Learning Objectives

1. **Identify and handle missing values**  
2. **Data Formatting**  
3. **Data Normalization** (Centering / Scaling)  
4. **Data Binning**  
5. **Turning categorical to numerical variables**  

---

## 🧠 Concept Overview

In Python, the **pandas** library is commonly used for data preprocessing tasks.  
Operations are usually performed **along columns**, where **each row represents a sample**.

For example, suppose we have a database called `students` with the following columns:

- `Student_Id`  
- `Student_Name`  
- `Student_Surname`  
- `Student_Marks`  

---

## 🔍 Accessing Data in Pandas

To access a specific column in a DataFrame, use the column name in square brackets:

```python
df["Student_Name"]
```
---

## 🛠️ Manipulating DataFrames

You can easily manipulate data in pandas.
For example, to add one mark to all students' marks, you can write:

```python
df["Student_Marks"] = df["Student_Marks"] + 1
```

This command increases every student's marks by 1.

## 📘 Summary

- Data preprocessing involves cleaning, transforming, and organizing data for analysis.
- By mastering pandas operations, you can efficiently prepare your datasets for machine learning and data science tasks
