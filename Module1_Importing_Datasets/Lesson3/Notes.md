# Lesson 3: Importing and Exporting  Data in Python

## Key Concepts

### Importing Data
- It's a process of reading and loading the data into python from various resources
- Two Important properties:
  1. format : It's a way data is encoded. eg. CSV, JSON, XLSx
  2. file path : It's where the data is stored. Usually it's on computer or on internet
 
Importing a csv into python

import pandas as pd

url = "https://archive.ics.uci.edu/dataset/53/iris"

iris_df = pd.read_csv(url, header = None)
