# Data Analysis with Python - Cheat Sheet: Importing Data Sets

| **Task** | **Description** | **Code Example** |
|-----------|-----------------|------------------|
| **Read CSV data set** | Read the CSV file containing a data set into a pandas DataFrame. | 
```
df = pd.read_csv(<CSV_path>, header=None)  
# load without header 
df = pd.read_csv(<CSV_path>, header=0)  
# load using first row as header |
| **Print first few entries** | Print the first few entries (default 5) of the pandas DataFrame. | ```python<br>df.head(n)  # n = number of entries; default 5<br>``` |
| **Print last few entries** | Print the last few entries (default 5) of the pandas DataFrame. | ```python<br>df.tail(n)  # n = number of entries; default 5<br>``` |
| **Assign header names** | Assign appropriate header names to the DataFrame. | ```python<br>df.columns = headers<br>``` |
| **Replace "?" with NaN** | Replace entries `"?"` with `NaN` using NumPy. | ```python<br>df = df.replace("?", np.nan)<br>``` |
| **Retrieve data types** | Retrieve the data types of all DataFrame columns. | ```python<br>df.dtypes<br>``` |
| **Retrieve statistical description** | Retrieve statistical description of the data set (default: numeric only). Use `include="all"` for all variables. | ```python<br>df.describe()  # or df.describe(include="all")<br>``` |
| **Retrieve data set summary** | Retrieve the summary information of the DataFrame. | ```python<br>df.info()<br>``` |
| **Save data frame to CSV** | Save the processed DataFrame to a CSV file at a specified path. | ```python<br>df.to_csv(<output_CSV_path>)<br>``` |

> 📝 **Note:**  
> In **JupyterLite**, you need to **download the file locally** and use the local path as `<CSV_path>`.  
> In **JupyterLab** or other Python environments, you can use a **URL** directly as `<CSV_path>`.

