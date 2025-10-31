# Lesson 5: Binning

## What is Binning?

Binning is the process of **grouping numeric values into bins**. It converts numeric variables into categorical variables.

**Example:**
If a feature `price` ranges from 5000 to 50000, we can create bins like:

* Low
* Medium
* High

## How to Do Binning in Python

```python
import numpy as np
import pandas as pd

# Define bins
bins = np.linspace(min(df['price']), max(df['price']), 4)

# Define labels
group_names = ['low', 'medium', 'high']

# Create a new binned column
df['binned_price'] = pd.cut(df['price'], bins, labels=group_names, include_lowest=True)
```

## Visualizing Binned Data

Binned data can be visualized using a **histogram**:

```python
import matplotlib.pyplot as plt

df['binned_price'].value_counts().plot(kind='bar')
plt.xlabel('Price Category')
plt.ylabel('Count')
plt.title('Histogram of Binned Prices')
plt.show()
```

## Summary

* Binning converts continuous numeric data into categories.
* Helps reduce the effect of minor observation errors.
* Useful for creating categorical features from numeric data for visualization or modeling.
