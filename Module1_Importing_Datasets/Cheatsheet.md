# Data Analysis with Python - Cheat Sheet: Importing Data Sets

| **Task** | **Description** | **Code Example** |
|-----------|-----------------|------------------|
| **Read CSV data set** | Read the CSV file containing a data set into a pandas DataFrame. | ```# load without header                           df = pd.read_csv(<CSV_path>, header=None)         # load using first row as header                     df = pd.read_csv(<CSV_path>, header=0)  ``` |
| **Print first few entries** | Print the first few entries (default 5) of the pandas DataFrame. | ```df.head(n)  # n = number of entries;``` |
| **Print last few entries** | Print the last few entries (default 5) of the pandas DataFrame. | ```df.tail(n)  # n = number of entries;``` |
| **Assign header names** | Assign appropriate header names to the DataFrame. | ```df.columns = headers``` |
| **Replace "?" with NaN** | Replace entries `"?"` with `NaN` using NumPy. | ```df = df.replace("?",np.nan)``` |
| **Retrieve data types** | Retrieve the data types of all DataFrame columns. | ```df.dtypes``` |
| **Retrieve statistical description** | Retrieve statistical description of the data set (default: numeric only). Use `include="all"` for all variables. | ```df.describe()  # or df.describe(include="all")``` |
| **Retrieve data set summary** | Retrieve the summary information of the DataFrame. | ```df.info()``` |
| **Save data frame to CSV** | Save the processed DataFrame to a CSV file at a specified path. | ```df.to_csv(<output_CSV_path>)``` |

> 📝 **Note:**  
> In **JupyterLite**, you need to **download the file locally** and use the local path as `<CSV_path>`.  
> In **JupyterLab** or other Python environments, you can use a **URL** directly as `<CSV_path>`.
