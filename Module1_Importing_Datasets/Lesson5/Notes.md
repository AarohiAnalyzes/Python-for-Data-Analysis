# 📘 Lesson 5: Accessing Databases with Python

---

## 🧠 1. What This Lesson Is About
You will learn how Python connects to a database and gets data from it — just like how Excel connects to a data file.  

Python uses something called a **Database API (DB-API)** to talk to databases.

---

## 🔗 2. How It Works (The Flow)

```
User → Python Program → API Calls → Database (DBMS)
```

Let’s break this down:
- 👤 **User**: You (the person writing Python code)  
- 🐍 **Python Program**: Your code or Jupyter Notebook  
- 🔌 **API Calls**: Special functions that send messages to the database  
- 🗄️ **DBMS**: The actual database (like MySQL, SQLite, etc.)

---

## ❓ 3. What Is an API?

**API = Application Programming Interface**

➡️ It’s a *set of functions* that lets one program talk to another.  
For example:
- You use a **database API** to ask the database for data.
- The database sends the answer back to Python.

So, a **SQL API** is simply the way Python talks to a SQL database.

---

## ⚙️ 4. Steps to Work with a Database in Python

When Python connects to a database, it follows these 5 basic steps:

1. **Connect** → Open a link to the database  
2. **Create a cursor** → Think of it like a pen to write SQL commands  
3. **Execute SQL** → Run SQL commands (like `SELECT`, `INSERT`, etc.)  
4. **Fetch results** → Get the data back from the database  
5. **Close** → Always close the connection when done  

---

## 🔌 5. How to Connect (Examples)

| Database | Python Library | Example Connection |
|-----------|----------------|--------------------|
| SQLite | `sqlite3` | `sqlite3.connect("data.db")` |
| MySQL | `mysql.connector` | `mysql.connector.connect(host="localhost", user="root", password="1234", database="test")` |
| PostgreSQL | `psycopg2` | `psycopg2.connect("dbname=test user=postgres password=1234")` |

---

## 💻 6. Simple Example (Using SQLite)

```python
import sqlite3

# 1. Connect to the database (creates it if not found)
conn = sqlite3.connect("students.db")

# 2. Create a cursor
cur = conn.cursor()

# 3. Create a table
cur.execute("""
CREATE TABLE IF NOT EXISTS students (
    id INTEGER PRIMARY KEY,
    name TEXT,
    marks REAL
)
""")

# 4. Insert data
cur.execute("INSERT INTO students (name, marks) VALUES (?, ?)", ("Alice", 90))
cur.execute("INSERT INTO students (name, marks) VALUES (?, ?)", ("Bob", 75))

# 5. Save the changes
conn.commit()

# 6. Read data
cur.execute("SELECT * FROM students")
rows = cur.fetchall()
for row in rows:
    print(row)

# 7. Close connection
conn.close()
```
🧩 What happens here:

1. Python connects to a new file students.db
2. It creates a table called students
3. It adds two students (Alice and Bob)
4. It reads all data and prints it
5. Then closes the connection

---

## ✅ 7. Summary

- API: A way for Python to talk to databases
- DB-API: Python’s system for connecting to any SQL database
- SQLite: Easiest database to start with (no setup needed)
- Always:Connect, Execute, Fetch, Close
