# Python Data Science Lab Practical Record

---

## 1. Loading a CSV File Using Pandas and Exploring Basic Data Frame Operations

### Aim
To load a CSV file using Pandas and perform basic DataFrame operations.

### Algorithm
1. Import the pandas library.
2. Create sample student data.
3. Save the data into a CSV file.
4. Load the CSV file using `read_csv()`.
5. Display the DataFrame.
6. Perform basic operations like displaying rows, columns, shape, and column names.

### Data Table

| RollNo | Name   | Age | Marks |
|--------|--------|-----|-------|
| 101    | Arun   | 19  | 85    |
| 102    | Bala   | 20  | 90    |
| 103    | Charan | 19  | 78    |
| 104    | Divya  | 21  | 88    |

### Program

```python
import pandas as pd

# Creating sample data
student_data = {
    'RollNo': [101, 102, 103, 104],
    'Name': ['Arun', 'Bala', 'Charan', 'Divya'],
    'Age': [19, 20, 19, 21],
    'Marks': [85, 90, 78, 88]
}

# Creating DataFrame
_df = pd.DataFrame(student_data)

# Saving to CSV
_df.to_csv('students.csv', index=False)

# Loading CSV file
students = pd.read_csv('students.csv')

# Displaying DataFrame
print("Student Data:\n")
print(students)

# Basic DataFrame Operations
print("\nShape of DataFrame:", students.shape)
print("\nColumn Names:")
print(students.columns)
```

### Output

```
Student Data:

   RollNo    Name  Age  Marks
0     101    Arun   19     85
1     102    Bala   20     90
2     103  Charan   19     78
3     104   Divya   21     88

Shape of DataFrame: (4, 4)

Column Names:
Index(['RollNo', 'Name', 'Age', 'Marks'], dtype='object')
```

### Explanation
- `to_csv()` saves the data into a CSV file.
- `shape` displays rows and columns count.
- `columns` displays all column names.

### Result
Thus the CSV file was loaded successfully and basic DataFrame operations were performed.

---

## 2. Performing Basic Data Inspection using head(), info(), and describe() in Pandas

### Aim
To inspect the dataset using `head()`, `info()`, and `describe()` functions.

### Algorithm
1. Import pandas.
2. Create sample employee dataset.
3. Create DataFrame.
4. Use `head()` to display first rows.
5. Use `info()` to display dataset information.
6. Use `describe()` for statistical summary.

### Data Table

| EmpID | Name    | Salary | Experience |
|-------|---------|--------|------------|
| 1     | Ravi    | 35000  | 2          |
| 2     | Priya   | 45000  | 4          |
| 3     | Karthik | 50000  | 5          |
| 4     | Meena   | 42000  | 3          |

### Program

```python
import pandas as pd

employee = {
    'EmpID': [1, 2, 3, 4],
    'Name': ['Ravi', 'Priya', 'Karthik', 'Meena'],
    'Salary': [35000, 45000, 50000, 42000],
    'Experience': [2, 4, 5, 3]
}

emp_df = pd.DataFrame(employee)

print("First Rows:\n")
print(emp_df.head())

print("\nInformation About Dataset:\n")
print(emp_df.info())

print("\nStatistical Summary:\n")
print(emp_df.describe())
```

### Output

```
First Rows:

   EmpID     Name  Salary  Experience
0      1     Ravi   35000           2
1      2    Priya   45000           4
2      3  Karthik   50000           5
3      4    Meena   42000           3

Information About Dataset:

<class 'pandas.core.frame.DataFrame'>
RangeIndex: 4 entries, 0 to 3
Data columns (total 4 columns):
EmpID         4 non-null int64
Name          4 non-null object
Salary        4 non-null int64
Experience    4 non-null int64

Statistical Summary:

          EmpID        Salary  Experience
count  4.000000      4.000000    4.000000
mean   2.500000  43000.000000    3.500000
std    1.290994   6204.836823    1.290994
min    1.000000  35000.000000    2.000000
max    4.000000  50000.000000    5.000000
```

### Explanation
- `head()` displays first five rows.
- `info()` shows datatype and null values.
- `describe()` gives statistical information.

### Result
Thus the dataset inspection was performed successfully.

---

## 3. Using Basic NumPy Functions for Array Creation and Manipulation

### Aim
To create and manipulate arrays using NumPy functions.

### Algorithm
1. Import NumPy.
2. Create arrays.
3. Perform arithmetic operations.
4. Reshape array.
5. Display results.

### Program

```python
import numpy as np

arr1 = np.array([1, 2, 3, 4, 5])
arr2 = np.array([10, 20, 30, 40, 50])

print("Array 1:", arr1)
print("Array 2:", arr2)

print("\nAddition:", arr1 + arr2)
print("Subtraction:", arr2 - arr1)
print("Multiplication:", arr1 * arr2)

reshaped = arr1.reshape(5, 1)
print("\nReshaped Array:\n", reshaped)
```

### Output

```
Array 1: [1 2 3 4 5]
Array 2: [10 20 30 40 50]

Addition: [11 22 33 44 55]
Subtraction: [ 9 18 27 36 45]
Multiplication: [ 10  40  90 160 250]

Reshaped Array:
 [[1]
 [2]
 [3]
 [4]
 [5]]
```

### Explanation
- `np.array()` creates arrays.
- Arithmetic operations are performed element-wise.
- `reshape()` changes array dimensions.

### Result
Thus NumPy array creation and manipulation were performed successfully.

---

## 4. Importing and Visualizing a Dataset using Matplotlib (Basic Plots)

### Aim
To visualize a dataset using Matplotlib.

### Algorithm
1. Import pandas and matplotlib.
2. Create sample sales dataset.
3. Plot line graph.
4. Display graph.

### Data Table

| Month | Sales |
|-------|-------|
| Jan   | 120   |
| Feb   | 150   |
| Mar   | 180   |
| Apr   | 200   |

### Program

```python
import pandas as pd
import matplotlib.pyplot as plt

sales = {
    'Month': ['Jan', 'Feb', 'Mar', 'Apr'],
    'Sales': [120, 150, 180, 200]
}

sales_df = pd.DataFrame(sales)

plt.plot(sales_df['Month'], sales_df['Sales'])
plt.title('Monthly Sales')
plt.xlabel('Month')
plt.ylabel('Sales')
plt.show()
```

### Output
A line graph showing monthly sales is displayed.

### Explanation
- `plt.plot()` creates a line plot.
- `title()`, `xlabel()`, and `ylabel()` add labels.
- `show()` displays the graph.

### Result
Thus the dataset was visualized successfully using Matplotlib.

---

## 5. Manipulation and Filtering of Lists, Dictionaries, and Tuples in Python

### Aim
To manipulate and filter lists, dictionaries, and tuples.

### Algorithm
1. Create list, dictionary, and tuple.
2. Perform list filtering.
3. Access dictionary values.
4. Display tuple elements.

### Program

```python
# List
numbers = [10, 15, 20, 25, 30]

# Filtering even numbers
filtered = [x for x in numbers if x % 2 == 0]

print("Original List:", numbers)
print("Filtered Even Numbers:", filtered)

# Dictionary
student = {'Name': 'Arun', 'Age': 19, 'Marks': 85}

print("\nDictionary Values:")
for key, value in student.items():
    print(key, ":", value)

# Tuple
colors = ('Red', 'Green', 'Blue')

print("\nTuple Elements:")
for c in colors:
    print(c)
```

### Output

```
Original List: [10, 15, 20, 25, 30]
Filtered Even Numbers: [10, 20, 30]

Dictionary Values:
Name : Arun
Age : 19
Marks : 85

Tuple Elements:
Red
Green
Blue
```

### Explanation
- List comprehension filters even numbers.
- Dictionary items are displayed using loop.
- Tuple elements are immutable and accessed using iteration.

### Result
Thus manipulation and filtering of Python data structures were performed successfully.

---

## 6. Create and Index a Pandas Series and Data Frame

### Aim
To create and index a Pandas Series and DataFrame.

### Algorithm
1. Import pandas.
2. Create a Series.
3. Create a DataFrame.
4. Access elements using indexing.

### Program

```python
import pandas as pd

series = pd.Series([100, 200, 300], index=['A', 'B', 'C'])
print("Series:\n")
print(series)

student = {
    'Name': ['Arun', 'Bala'],
    'Marks': [85, 90]
}

_df = pd.DataFrame(student)

print("\nDataFrame:\n")
print(_df)

print("\nAccessing First Row:")
print(_df.loc[0])
```

### Output

```
Series:

A    100
B    200
C    300
dtype: int64

DataFrame:

   Name  Marks
0  Arun     85
1  Bala     90

Accessing First Row:
Name     Arun
Marks      85
Name: 0, dtype: object
```

### Explanation
- `Series()` creates a one-dimensional labeled array.
- `DataFrame()` creates tabular data.
- `loc[]` accesses rows using index.

### Result
Thus Pandas Series and DataFrame were created and indexed successfully.

---

## 7. Perform Data Selection and Slicing in Pandas Data Frame

### Aim
To perform data selection and slicing in a Pandas DataFrame.

### Algorithm
1. Create DataFrame.
2. Select columns.
3. Slice rows.
4. Display output.

### Program

```python
import pandas as pd

student = {
    'Name': ['Arun', 'Bala', 'Charan', 'Divya'],
    'Marks': [85, 90, 78, 88],
    'Age': [19, 20, 19, 21]
}

_df = pd.DataFrame(student)

print("Complete DataFrame:\n")
print(_df)

print("\nSelecting Name Column:\n")
print(_df['Name'])

print("\nSlicing First Two Rows:\n")
print(_df[0:2])
```

### Output

```
Complete DataFrame:

     Name  Marks  Age
0    Arun     85   19
1    Bala     90   20
2  Charan     78   19
3   Divya     88   21

Selecting Name Column:

0      Arun
1      Bala
2    Charan
3     Divya
Name: Name, dtype: object

Slicing First Two Rows:

   Name  Marks  Age
0  Arun     85   19
1  Bala     90   20
```

### Explanation
- Columns are selected using column names.
- Rows are sliced using index ranges.

### Result
Thus data selection and slicing were performed successfully.

---

## 8. Group and Aggregate Data in Pandas using groupby() Operations

### Aim
To group and aggregate data using `groupby()`.

### Algorithm
1. Create sales dataset.
2. Group data by product.
3. Calculate total sales.
4. Display output.

### Data Table

| Product | Sales |
|---------|-------|
| Pen     | 100   |
| Pencil  | 50    |
| Pen     | 150   |
| Pencil  | 70    |

### Program

```python
import pandas as pd

sales = {
    'Product': ['Pen', 'Pencil', 'Pen', 'Pencil'],
    'Sales': [100, 50, 150, 70]
}

sales_df = pd.DataFrame(sales)

result = sales_df.groupby('Product')['Sales'].sum()

print(result)
```

### Output

```
Product
Pen      250
Pencil   120
Name: Sales, dtype: int64
```

### Explanation
- `groupby()` groups rows based on column values.
- `sum()` aggregates grouped data.

### Result
Thus grouping and aggregation were performed successfully.

---

## 9. Sort and Filter Data Based on Multiple Conditions in Pandas

### Aim
To sort and filter data using multiple conditions.

### Algorithm
1. Create employee dataset.
2. Filter employees with salary greater than 40000.
3. Sort salaries in descending order.
4. Display results.

### Program

```python
import pandas as pd

employee = {
    'Name': ['Ravi', 'Priya', 'Karthik', 'Meena'],
    'Salary': [35000, 45000, 50000, 42000],
    'Experience': [2, 4, 5, 3]
}

emp_df = pd.DataFrame(employee)

filtered = emp_df[emp_df['Salary'] > 40000]
sorted_df = filtered.sort_values('Salary', ascending=False)

print(sorted_df)
```

---

## 10. Handling Missing Data using fillna(), dropna(), and Interpolation in Pandas

### Aim
To handle missing data using `fillna()`, `dropna()`, and `interpolate()` functions in Pandas.

### Algorithm
1. Import pandas and numpy libraries.
2. Create a dataset containing missing values.
3. Display the original dataset.
4. Use `fillna()` to replace missing values.
5. Use `dropna()` to remove missing values.
6. Use `interpolate()` to estimate missing values.
7. Display the results.

### Data Table

| Index | Marks |
|-------|-------|
| 0     | 85    |
| 1     | NaN   |
| 2     | 78    |
| 3     | NaN   |
| 4     | 90    |

### Program

```python
import pandas as pd
import numpy as np

marks = {
    'Marks': [85, np.nan, 78, np.nan, 90]
}

df = pd.DataFrame(marks)

print("Original Data:\n")
print(df)

print("\nUsing fillna():\n")
print(df.fillna(80))

print("\nUsing dropna():\n")
print(df.dropna())

print("\nUsing interpolation():\n")
print(df.interpolate())
```

### Output

```
Original Data:

   Marks
0   85.0
1    NaN
2   78.0
3    NaN
4   90.0

Using fillna():

   Marks
0   85.0
1   80.0
2   78.0
3   80.0
4   90.0

Using dropna():

   Marks
0   85.0
2   78.0
4   90.0

Using interpolation():

   Marks
0   85.0
1   81.5
2   78.0
3   84.0
4   90.0
```

### Explanation
- `fillna()` replaces missing values with specified values.
- `dropna()` removes rows containing missing values.
- `interpolate()` estimates missing values automatically.

### Result
Thus missing data was handled successfully using Pandas functions.

---

## 11. Identify and Remove Duplicate Records in a Dataset using Pandas

### Aim
To identify and remove duplicate records in a dataset using Pandas.

### Algorithm
1. Import pandas library.
2. Create a dataset with duplicate records.
3. Display duplicate rows using `duplicated()`.
4. Remove duplicates using `drop_duplicates()`.
5. Display the final dataset.

### Data Table

| Name  | Marks |
|-------|-------|
| Arun  | 85    |
| Bala  | 90    |
| Arun  | 85    |
| Divya | 88    |

### Program

```python
import pandas as pd

student = {
    'Name': ['Arun', 'Bala', 'Arun', 'Divya'],
    'Marks': [85, 90, 85, 88]
}

df = pd.DataFrame(student)

print("Original Data:\n")
print(df)

print("\nDuplicate Rows:\n")
print(df.duplicated())

print("\nAfter Removing Duplicates:\n")
print(df.drop_duplicates())
```

### Output

```
Original Data:

    Name  Marks
0   Arun     85
1   Bala     90
2   Arun     85
3  Divya     88

Duplicate Rows:

0    False
1    False
2     True
3    False
dtype: bool

After Removing Duplicates:

    Name  Marks
0   Arun     85
1   Bala     90
3  Divya     88
```

### Explanation
- `duplicated()` identifies repeated rows.
- `drop_duplicates()` removes duplicate records from the dataset.

### Result
Thus duplicate records were identified and removed successfully.

---

## 12. Reshape Data using melt() and pivot() Functions in Pandas

### Aim
To reshape data using `melt()` and `pivot()` functions in Pandas.

### Algorithm
1. Import pandas library.
2. Create a dataset.
3. Convert wide format into long format using `melt()`.
4. Convert long format back into wide format using `pivot()`.
5. Display the outputs.

### Data Table

| Name | Maths | Science |
|------|-------|---------|
| Arun | 85    | 88      |
| Bala | 90    | 92      |

### Program

```python
import pandas as pd

data = {
    'Name': ['Arun', 'Bala'],
    'Maths': [85, 90],
    'Science': [88, 92]
}

df = pd.DataFrame(data)

print("Original Data:\n")
print(df)

melted = pd.melt(df, id_vars=['Name'],
                 var_name='Subject',
                 value_name='Marks')

print("\nMelted Data:\n")
print(melted)

pivoted = melted.pivot(index='Name',
                       columns='Subject',
                       values='Marks')

print("\nPivoted Data:\n")
print(pivoted)
```

### Output

```
Original Data:

   Name  Maths  Science
0  Arun     85       88
1  Bala     90       92

Melted Data:

   Name  Subject  Marks
0  Arun    Maths     85
1  Bala    Maths     90
2  Arun  Science     88
3  Bala  Science     92

Pivoted Data:

Subject  Maths  Science
Name
Arun        85       88
Bala        90       92
```

### Explanation
- `melt()` converts columns into rows.
- `pivot()` reshapes rows back into columns.

### Result
Thus data reshaping was performed successfully using Pandas.

---

## 13. Merge Multiple Datasets and Perform Data Alignment using Pandas

### Aim
To merge multiple datasets and perform data alignment using Pandas.

### Algorithm
1. Import pandas library.
2. Create two datasets.
3. Merge datasets using common column.
4. Display merged data.

### Data Table 1

| ID | Name   |
|----|--------|
| 1  | Arun   |
| 2  | Bala   |
| 3  | Charan |

### Data Table 2

| ID | Marks |
|----|-------|
| 1  | 85    |
| 2  | 90    |
| 3  | 78    |

### Program

```python
import pandas as pd

student = {
    'ID': [1, 2, 3],
    'Name': ['Arun', 'Bala', 'Charan']
}

marks = {
    'ID': [1, 2, 3],
    'Marks': [85, 90, 78]
}

student_df = pd.DataFrame(student)
marks_df = pd.DataFrame(marks)

merged = pd.merge(student_df, marks_df, on='ID')

print("Merged Data:\n")
print(merged)
```

### Output

```
Merged Data:

   ID    Name  Marks
0   1    Arun     85
1   2    Bala     90
2   3  Charan     78
```

### Explanation
- `merge()` combines datasets based on a common column.
- `on='ID'` specifies the matching column.

### Result
Thus multiple datasets were merged successfully.

---

## 14. Compute Summary Statistics (Mean, Median, Standard Deviation) using Python

### Aim
To compute mean, median, and standard deviation using Python.

### Algorithm
1. Import statistics module.
2. Create a list of numbers.
3. Calculate mean using `mean()`.
4. Calculate median using `median()`.
5. Calculate standard deviation using `stdev()`.
6. Display the results.

### Program

```python
import statistics

numbers = [10, 20, 30, 40, 50]

mean_value = statistics.mean(numbers)
median_value = statistics.median(numbers)
std_dev = statistics.stdev(numbers)

print("Numbers:", numbers)
print("Mean:", mean_value)
print("Median:", median_value)
print("Standard Deviation:", std_dev)
```

### Output

```
Numbers: [10, 20, 30, 40, 50]

Mean: 30
Median: 30
Standard Deviation: 15.811388300841896
```

### Explanation
- `mean()` calculates average value.
- `median()` finds the middle value.
- `stdev()` calculates standard deviation.

### Result
Thus summary statistics were computed successfully.

---

## 15. Create Basic Visualizations (Line Plot, Bar Chart) using Matplotlib in Python

### Aim
To create basic visualizations using line plot and bar chart in Matplotlib.

### Algorithm
1. Import matplotlib library.
2. Create dataset.
3. Draw line plot.
4. Draw bar chart.
5. Display charts.

### Data Table

| Product | Sales |
|---------|-------|
| Pen     | 100   |
| Pencil  | 80    |
| Book    | 150   |
| Eraser  | 60    |

### Program

```python
import matplotlib.pyplot as plt

products = ['Pen', 'Pencil', 'Book', 'Eraser']
sales = [100, 80, 150, 60]

# Line Plot
plt.plot(products, sales)
plt.title('Product Sales - Line Plot')
plt.xlabel('Products')
plt.ylabel('Sales')
plt.show()

# Bar Chart
plt.bar(products, sales)
plt.title('Product Sales - Bar Chart')
plt.xlabel('Products')
plt.ylabel('Sales')
plt.show()
```

### Output
A line plot and bar chart displaying product sales are shown.

### Explanation
- `plot()` creates line graph.
- `bar()` creates bar chart.
- `show()` displays graphs.

### Result
Thus basic visualizations were created successfully using Matplotlib.
