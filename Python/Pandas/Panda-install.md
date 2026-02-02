# Installing Pandas
python --version
pip install pandas

# Verifying Installation
import pandas as pd
print(pd.__version__)

# Using Pandas DataFrame

A Pandas DataFrame is a two-dimensional, size-mutable, and potentially heterogeneous tabular data structure with labeled axes (rows and columns). It is one of the primary data structures in the Pandas library and is widely used for data manipulation and analysis.

## Creating a DataFrame

A DataFrame can be created from various data structures such as lists, dictionaries, and numpy arrays. Here are some examples:

From a Dictionary

import pandas as pd

# Creating DataFrame from a dictionary
data = {'Name': ['Tom', 'Nick', 'Krish', 'Jack'], 'Age': [20, 21, 19, 18]}
df = pd.DataFrame(data)
print(df)

## Output:

Name Age
0 Tom 20
1 Nick 21
2 Krish 19
3 Jack 18

From a List

# Creating DataFrame from a list
lst = ['Geeks', 'For', 'Geeks', 'is', 'portal', 'for', 'Geeks']
df = pd.DataFrame(lst)
print(df)

## Output:

0
0 Geeks
1 For
2 Geeks
3 is
4 portal
5 for
6 Geeks

From a Numpy Array

import numpy as np

# Creating DataFrame from a numpy array
data = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
df = pd.DataFrame(data, columns=['a', 'b', 'c'])
print(df)

## Output:

a b c
0 1 2 3
1 4 5 6
2 7 8 9

Accessing Data

You can access data in a DataFrame using various methods such as loc, iloc, and direct indexing.

Using loc

# Accessing rows using loc
print(df.loc[0]) # Accessing the first row

## Output:

a 1
b 2
c 3
Name: 0, dtype: int64

Using iloc

# Accessing rows using iloc
print(df.iloc[1]) # Accessing the second row

## Output:

a 4
b 5
c 6
Name: 1, dtype: int64

Direct Indexing

# Accessing columns directly
print(df['a']) # Accessing the 'a' column

## Output:

0 1
1 4
2 7
Name: a, dtype: int64

Handling Missing Data

Pandas provides several methods to handle missing data, such as isnull(), fillna(), and dropna().

Checking for Missing Values

# Checking for missing values
print(df.isnull())

Filling Missing Values

# Filling missing values with 0
df.fillna(0, inplace=True)

Dropping Missing Values

# Dropping rows with missing values
df.dropna(inplace=True)

Iterating Over Rows and Columns

You can iterate over rows and columns using methods like iterrows() and itertuples().

Iterating Over Rows

# Iterating over rows
for index, row in df.iterrows():
print(index, row)

Iterating Over Columns

# Iterating over columns
for col in df.columns:
print(df[col])

Pandas DataFrame is a powerful tool for data manipulation and analysis, offering a wide range of functionalities to handle, process, and analyze data efficiently.
