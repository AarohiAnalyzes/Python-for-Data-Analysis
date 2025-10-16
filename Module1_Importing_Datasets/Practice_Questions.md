# Python for Data Analysis - Quiz

## Question 1
You want to apply classification and regression techniques in Python. Which library would you choose?

- [ ] Pandas  
- [x] scikit-learn  
- [ ] Numpy  
- [ ] matplotlib  

---

## Question 2
Ravi is working with a DataFrame named `df` and a list called `headers_list` that contains three column names. What command should he use to rename the DataFrame’s columns?

- [ ] df.tail(headers_list)  
- [x] df.columns = headers_list  
- [ ] df.tail() = headers_list  
- [ ] df.head(headers_list)  

---

## Question 3
Which Python command loads data from a CSV file named `"A.csv"` into a DataFrame?

- [ ] df.head("A.csv")  
- [x] df = pandas.read_csv("A.csv")  
- [ ] read.dataframe("A.csv")  
- [ ] df = pandas.write_csv("A.csv")  

---

## Question 4
You are analyzing a used car dataset in Pandas. The column “cylinders” contains numeric values like 4, 6, and 8 to represent engine configuration. What data type is most appropriate for this column?

- [ ] float64  
- [ ] string  
- [ ] object  
- [x] int64  

---

## Question 5
Zoya wants to view summary statistics—including non-numeric columns—for her DataFrame `df`. Which command should she use?

- [ ] df.info()  
- [ ] df.statistics(include = "all")  
- [x] df.describe(include = "all")  
- [ ] df.describe()  

---

## Question 6
A data analyst has loaded a dataset of used cars and noticed that the first row contains numeric values rather than column names. What does this imply about the dataset?

- [x] The dataset has no header row and treats the first row as data.  
- [ ] The file format is incompatible with Pandas in the column.  
- [ ] The dataset is in Excel format in a Pandas column.  
- [ ] The dataset contains missing values in the first row.  

---

## Question 7
You’ve created a connection to a database using `sqlite3.connect()`. Which of the following correctly describes the role of the `connect()` function?

- [ ] It defines the SQL query to run  
- [ ] It exports the data to a CSV file  
- [ ] It fetches query results  
- [x] It opens a connection to the specified database file  

---

## Question 8
You’re tasked with visualizing trends in used car prices over time. Which Python library would be the best choice for this task?

- [ ] Scikit-learn  
- [ ] Pandas  
- [x] Matplotlib  
- [ ] Numpy  

---

## Question 9
Roma’s dataset, Pandas used 0, 1, 2… as column headers. What is a valid way to set appropriate labels from a separate list named `cols`?

- [ ] Run df.rename(cols)  
- [x] Set df.columns = cols  
- [ ] Set cols = df.labels  
- [ ] Assign df.index = cols  

---

## Question 10
After importing the database module, what is the correct next step to begin querying a database?

- [ ] Call disconnect() on the database  
- [ ] Use cursor() without connection  
- [ ] Use commit() before reading  
- [x] Call connect() to open a session  
