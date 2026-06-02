# TASK #1: DEFINE SINGLE AND MULTI-DIMENSIONAL  NUMPY ARRAYS


```python
# NumPy is a Linear Algebra Library used for multidimensional arrays
# NumPy brings the best of two worlds: (1) C/Fortran computational efficiency, (2) Python language easy syntax 

import numpy as np

# Let's define a one-dimensional array 
list_1 = [50, 60, 80, 100, 200, 300, 500, 600]
list_1
```




    [50, 60, 80, 100, 200, 300, 500, 600]




```python
# Let's create a numpy array from the list "my_list"
my_numpy_array =  np.array(list_1)
my_numpy_array
```




    array([ 50,  60,  80, 100, 200, 300, 500, 600])




```python
type(my_numpy_array)
```




    numpy.ndarray




```python
# Multi-dimensional (Matrix definition) 
my_matrix = np.array([[2, 5, 8], [7, 3, 6]])
my_matrix
```




    array([[2, 5, 8],
           [7, 3, 6]])



MINI CHALLENGE #1: 
- Write a code that creates the following 2x4 numpy array

```
[[3 7 9 3] 
[4 3 2 2]]
```


```python
x = np.array([[3, 7, 9, 3], [4, 3, 2, 2]])
x
```




    array([[3, 7, 9, 3],
           [4, 3, 2, 2]])



# TASK #2: LEVERAGE NUMPY BUILT-IN METHODS AND FUNCTIONS 


```python
# "rand()" uniform distribution between 0 and 1
x = np.random.rand(20)
x
```




    array([0.78926315, 0.37935246, 0.52377624, 0.70811757, 0.56438118,
           0.97999038, 0.36286627, 0.30856677, 0.19803061, 0.61393216,
           0.44110077, 0.15167577, 0.44498969, 0.12987994, 0.11511517,
           0.45071945, 0.95645986, 0.54470728, 0.8300531 , 0.83240872])




```python
# you can create a matrix of random number as well
x = np.random.rand(3, 3)
x
```




    array([[0.93647301, 0.59524573, 0.65875696],
           [0.59072049, 0.51251114, 0.72480295],
           [0.02596481, 0.40614027, 0.78641758]])




```python
# "randint" is used to generate random integers between upper and lower bounds
x = np.random.randint(1, 50)
x
```




    6




```python
# "randint" can be used to generate a certain number of random itegers as follows
x = np.random.randint(1, 100, 15)
x
```




    array([20, 17, 43, 14, 93, 41, 82, 81, 64, 84, 10, 34, 36,  3, 32])




```python
# np.arange creates an evenly spaced values within a given interval
x = np.arange(1, 50)
x
```




    array([ 1,  2,  3,  4,  5,  6,  7,  8,  9, 10, 11, 12, 13, 14, 15, 16, 17,
           18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34,
           35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49])




```python
# create a diagonal of ones and zeros everywhere else
x = np.eye(7)
x
```




    array([[1., 0., 0., 0., 0., 0., 0.],
           [0., 1., 0., 0., 0., 0., 0.],
           [0., 0., 1., 0., 0., 0., 0.],
           [0., 0., 0., 1., 0., 0., 0.],
           [0., 0., 0., 0., 1., 0., 0.],
           [0., 0., 0., 0., 0., 1., 0.],
           [0., 0., 0., 0., 0., 0., 1.]])




```python
# Matrix of ones
x = np.ones((7, 7))
x
```




    array([[1., 1., 1., 1., 1., 1., 1.],
           [1., 1., 1., 1., 1., 1., 1.],
           [1., 1., 1., 1., 1., 1., 1.],
           [1., 1., 1., 1., 1., 1., 1.],
           [1., 1., 1., 1., 1., 1., 1.],
           [1., 1., 1., 1., 1., 1., 1.],
           [1., 1., 1., 1., 1., 1., 1.]])




```python
# Array of zeros
x = np.zeros(8)
x
```




    array([0., 0., 0., 0., 0., 0., 0., 0.])



MINI CHALLENGE #2:
- Write a code that takes in a positive integer "x" from the user and creates a 1x10 array with random numbers ranging from 0 to "x"


```python
x = (input('Please enter a positve interger value: '))
```

    Please enter a positve interger value: 7



```python
x
```




    '7'




```python
x = np.random.randint(1, x, 10)
x
```




    array([2, 2, 3, 3, 2, 5, 6, 3, 1, 5])



# TASK #3: PERFORM MATHEMATICAL OPERATIONS IN NUMPY


```python
# np.arange() 93, returns an evenly spaced values within a given interval
x = np.arange(1, 93)
x
```




    array([ 1,  2,  3,  4,  5,  6,  7,  8,  9, 10, 11, 12, 13, 14, 15, 16, 17,
           18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34,
           35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51,
           52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68,
           69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 84, 85,
           86, 87, 88, 89, 90, 91, 92])




```python
y = np.arange(1, 93)
y
```




    array([ 1,  2,  3,  4,  5,  6,  7,  8,  9, 10, 11, 12, 13, 14, 15, 16, 17,
           18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34,
           35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51,
           52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68,
           69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 84, 85,
           86, 87, 88, 89, 90, 91, 92])




```python
# Add 2 numpy arrays together
sum = x + y
sum
```




    array([  2,   4,   6,   8,  10,  12,  14,  16,  18,  20,  22,  24,  26,
            28,  30,  32,  34,  36,  38,  40,  42,  44,  46,  48,  50,  52,
            54,  56,  58,  60,  62,  64,  66,  68,  70,  72,  74,  76,  78,
            80,  82,  84,  86,  88,  90,  92,  94,  96,  98, 100, 102, 104,
           106, 108, 110, 112, 114, 116, 118, 120, 122, 124, 126, 128, 130,
           132, 134, 136, 138, 140, 142, 144, 146, 148, 150, 152, 154, 156,
           158, 160, 162, 164, 166, 168, 170, 172, 174, 176, 178, 180, 182,
           184])




```python
squared = x ** 2
squared
```




    array([   1,    4,    9,   16,   25,   36,   49,   64,   81,  100,  121,
            144,  169,  196,  225,  256,  289,  324,  361,  400,  441,  484,
            529,  576,  625,  676,  729,  784,  841,  900,  961, 1024, 1089,
           1156, 1225, 1296, 1369, 1444, 1521, 1600, 1681, 1764, 1849, 1936,
           2025, 2116, 2209, 2304, 2401, 2500, 2601, 2704, 2809, 2916, 3025,
           3136, 3249, 3364, 3481, 3600, 3721, 3844, 3969, 4096, 4225, 4356,
           4489, 4624, 4761, 4900, 5041, 5184, 5329, 5476, 5625, 5776, 5929,
           6084, 6241, 6400, 6561, 6724, 6889, 7056, 7225, 7396, 7569, 7744,
           7921, 8100, 8281, 8464])




```python
sqrt = np.sqrt(squared)
sqrt
```




    array([ 1.,  2.,  3.,  4.,  5.,  6.,  7.,  8.,  9., 10., 11., 12., 13.,
           14., 15., 16., 17., 18., 19., 20., 21., 22., 23., 24., 25., 26.,
           27., 28., 29., 30., 31., 32., 33., 34., 35., 36., 37., 38., 39.,
           40., 41., 42., 43., 44., 45., 46., 47., 48., 49., 50., 51., 52.,
           53., 54., 55., 56., 57., 58., 59., 60., 61., 62., 63., 64., 65.,
           66., 67., 68., 69., 70., 71., 72., 73., 74., 75., 76., 77., 78.,
           79., 80., 81., 82., 83., 84., 85., 86., 87., 88., 89., 90., 91.,
           92.])




```python
z = np.exp(y)
z
```




    array([2.71828183e+00, 7.38905610e+00, 2.00855369e+01, 5.45981500e+01,
           1.48413159e+02, 4.03428793e+02, 1.09663316e+03, 2.98095799e+03,
           8.10308393e+03, 2.20264658e+04, 5.98741417e+04, 1.62754791e+05,
           4.42413392e+05, 1.20260428e+06, 3.26901737e+06, 8.88611052e+06,
           2.41549528e+07, 6.56599691e+07, 1.78482301e+08, 4.85165195e+08,
           1.31881573e+09, 3.58491285e+09, 9.74480345e+09, 2.64891221e+10,
           7.20048993e+10, 1.95729609e+11, 5.32048241e+11, 1.44625706e+12,
           3.93133430e+12, 1.06864746e+13, 2.90488497e+13, 7.89629602e+13,
           2.14643580e+14, 5.83461743e+14, 1.58601345e+15, 4.31123155e+15,
           1.17191424e+16, 3.18559318e+16, 8.65934004e+16, 2.35385267e+17,
           6.39843494e+17, 1.73927494e+18, 4.72783947e+18, 1.28516001e+19,
           3.49342711e+19, 9.49611942e+19, 2.58131289e+20, 7.01673591e+20,
           1.90734657e+21, 5.18470553e+21, 1.40934908e+22, 3.83100800e+22,
           1.04137594e+23, 2.83075330e+23, 7.69478527e+23, 2.09165950e+24,
           5.68572000e+24, 1.54553894e+25, 4.20121040e+25, 1.14200739e+26,
           3.10429794e+26, 8.43835667e+26, 2.29378316e+27, 6.23514908e+27,
           1.69488924e+28, 4.60718663e+28, 1.25236317e+29, 3.40427605e+29,
           9.25378173e+29, 2.51543867e+30, 6.83767123e+30, 1.85867175e+31,
           5.05239363e+31, 1.37338298e+32, 3.73324200e+32, 1.01480039e+33,
           2.75851345e+33, 7.49841700e+33, 2.03828107e+34, 5.54062238e+34,
           1.50609731e+35, 4.09399696e+35, 1.11286375e+36, 3.02507732e+36,
           8.22301271e+36, 2.23524660e+37, 6.07603023e+37, 1.65163625e+38,
           4.48961282e+38, 1.22040329e+39, 3.31740010e+39, 9.01762841e+39])



MINI CHALLENGE #3:
- Given the X and Y values below, obtain the distance between them

```
X = [5, 7, 20]
Y = [9, 15, 4]
```


```python
X = np.array([5, 7, 20])
Y = np.array([9, 15, 4])

Z = np.sqrt(X**2 + Y**2)
Z
```




    array([10.29563014, 16.55294536, 20.39607805])



# TASK #4: PERFORM ARRAYS SLICING AND INDEXING 


```python
my_numpy_array = np.array([3, 5, 6, 2, 8, 10, 20, 50])
my_numpy_array
```




    array([ 3,  5,  6,  2,  8, 10, 20, 50])




```python
# Access specific index from the numpy array
my_numpy_array[-1]
```




    50




```python
# Starting from the first index 0 up until and NOT including the last element
my_numpy_array[0:3]
```




    array([3, 5, 6])




```python
# Broadcasting, altering several values in a numpy array at once
my_numpy_array[0:4] = 7
my_numpy_array
```




    array([ 7,  7,  7,  7,  8, 10, 20, 50])




```python
# Let's define a two dimensional numpy array
matrix = np.random.randint(1, 10, (4, 4))
matrix
```




    array([[7, 2, 5, 7],
           [4, 1, 5, 2],
           [5, 2, 8, 4],
           [9, 4, 6, 5]])




```python
# Get a row from a mtrix
matrix[0]
```




    array([7, 2, 5, 7])




```python
# Get one element
matrix[0][2]
```




    5



MINI CHALLENGE #4:
- In the following matrix, replace the last row with 0

```
X = [2 30 20 -2 -4]
    [3 4  40 -3 -2]
    [-3 4 -6 90 10]
    [25 45 34 22 12]
    [13 24 22 32 37]
```




```python
X = np.array([[2, 30, 20, -2, -4],
             [3, 4,  40, -3, -2],
             [-3, 4, -6, 90, 10],
             [25, 45, 34, 22, 12],
             [13, 24, 22, 32, 37]])
```


```python
X[4] = 0
X
```




    array([[ 2, 30, 20, -2, -4],
           [ 3,  4, 40, -3, -2],
           [-3,  4, -6, 90, 10],
           [25, 45, 34, 22, 12],
           [ 0,  0,  0,  0,  0]])



# TASK #5: PERFORM ELEMENTS SELECTION (CONDITIONAL)


```python
matrix = np.random.randint(1, 18, (5, 5))
matrix
```




    array([[ 8,  7, 15, 11,  6],
           [ 2, 13, 15,  8, 16],
           [12,  8, 15,  3, 11],
           [ 6,  5,  7,  8, 15],
           [11,  6,  7,  6, 13]])




```python
new_matrix = matrix[matrix > 7]
new_matrix
```




    array([ 8, 15, 11, 13, 15,  8, 16, 12,  8, 15, 11,  8, 15, 11, 13])




```python
# Obtain odd elements only
new_matrix = matrix[matrix % 2 == 1]
new_matrix
```




    array([ 7, 15, 11, 13, 15, 15,  3, 11,  5,  7, 15, 11,  7, 13])



MINI CHALLENGE #5:
- In the following matrix, replace negative elements by 0 and replace odd elements with -2


```
X = [2 30 20 -2 -4]
    [3 4  40 -3 -2]
    [-3 4 -6 90 10]
    [25 45 34 22 12]
    [13 24 22 32 37]
```



```python
X = np.array([[2, 30, 20, -2, -4],
              [3, 4,  40, -3, -2],
              [-3, 4, -6, 90, 10],
              [25, 45, 34, 22, 12],
              [13, 24, 22, 32, 37]])
```


```python
X[X < 0] = 0
X[X % 2 == 1] = 1
X
```




    array([[ 2, 30, 20,  0,  0],
           [ 1,  4, 40,  0,  0],
           [ 0,  4,  0, 90, 10],
           [ 1,  1, 34, 22, 12],
           [ 1, 24, 22, 32,  1]])



# TASK #6: UNDERSTAND PANDAS FUNDAMENTALS


```python
# Pandas is a data manipulation and analysis tool that is built on Numpy.
# Pandas uses a data structure known as DataFrame (think of it as Microsoft excel in Python). 
# DataFrames empower programmers to store and manipulate data in a tabular fashion (rows and columns).
# Series Vs. DataFrame? Series is considered a single column of a DataFrame.
```


```python
import pandas as pd
```


```python
# Let's define a two-dimensional Pandas DataFrame
# Note that you can create a pandas dataframe from a python dictionary

bank_client_df = pd.DataFrame({'Bank Client ID':[111, 222, 333, 444], 
                               'Bank Client Name':['Chanel', 'Steve', 'Mitch', 'Ryan'],
                               'Net Worth [$]':[3500, 29000, 10000, 2000],
                               'Years with bank':[3, 4, 9, 5]})
bank_client_df                               
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Bank Client ID</th>
      <th>Bank Client Name</th>
      <th>Net Worth [$]</th>
      <th>Years with bank</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>111</td>
      <td>Chanel</td>
      <td>3500</td>
      <td>3</td>
    </tr>
    <tr>
      <th>1</th>
      <td>222</td>
      <td>Steve</td>
      <td>29000</td>
      <td>4</td>
    </tr>
    <tr>
      <th>2</th>
      <td>333</td>
      <td>Mitch</td>
      <td>10000</td>
      <td>9</td>
    </tr>
    <tr>
      <th>3</th>
      <td>444</td>
      <td>Ryan</td>
      <td>2000</td>
      <td>5</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Let's obtain the data type 
type(bank_client_df)
```




    pandas.core.frame.DataFrame




```python
# you can only view the first couple of rows using .head()
bank_client_df.head(2)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Bank Client ID</th>
      <th>Bank Client Name</th>
      <th>Net Worth [$]</th>
      <th>Years with bank</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>111</td>
      <td>Chanel</td>
      <td>3500</td>
      <td>3</td>
    </tr>
    <tr>
      <th>1</th>
      <td>222</td>
      <td>Steve</td>
      <td>29000</td>
      <td>4</td>
    </tr>
  </tbody>
</table>
</div>




```python
# you can only view the last couple of rows using .tail()
bank_client_df.tail(2)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Bank Client ID</th>
      <th>Bank Client Name</th>
      <th>Net Worth [$]</th>
      <th>Years with bank</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2</th>
      <td>333</td>
      <td>Mitch</td>
      <td>10000</td>
      <td>9</td>
    </tr>
    <tr>
      <th>3</th>
      <td>444</td>
      <td>Ryan</td>
      <td>2000</td>
      <td>5</td>
    </tr>
  </tbody>
</table>
</div>



MINI CHALLENGE #6:
- A porfolio contains a collection of securities such as stocks, bonds and ETFs. Define a dataframe named 'portfolio_df' that holds 3 different stock ticker symbols, number of shares, and price per share (feel free to choose any stocks)
- Calculate the total value of the porfolio including all stocks


```python
porfolio_df = pd.DataFrame({'stock ticker symbol': ['AAPL', 'AMZN', 'T'],
                           'price per share [$]': [3500, 200, 40],
                           'Number of stock': [3, 4, 9]})
```


```python
porfolio_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>stock ticker symbol</th>
      <th>price per share [$]</th>
      <th>Number of stock</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>AAPL</td>
      <td>3500</td>
      <td>3</td>
    </tr>
    <tr>
      <th>1</th>
      <td>AMZN</td>
      <td>200</td>
      <td>4</td>
    </tr>
    <tr>
      <th>2</th>
      <td>T</td>
      <td>40</td>
      <td>9</td>
    </tr>
  </tbody>
</table>
</div>




```python
stocks_dollar_value = porfolio_df['price per share [$]'] * porfolio_df['Number of stock']
stocks_dollar_value.sum()
```




    11660



# TASK #7: PANDAS WITH CSV AND HTML DATA


```python
!pip install lxml
```

    Requirement already satisfied: lxml in /opt/conda/lib/python3.10/site-packages (5.2.2)



```python
!python -m pip install --upgrade pip
```

    Requirement already satisfied: pip in /opt/conda/lib/python3.10/site-packages (26.1.2)



```python
# Read tabular data using read_html
house_price_df = pd.read_html('https://wowa.ca/reports/canada-housing-market')
house_price_df[2]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Province</th>
      <th>April 2026 Benchmark Home Price</th>
      <th>Monthly Change (%)</th>
      <th>Annual Change (%)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>British Columbia</td>
      <td>$889,800</td>
      <td>0.1%</td>
      <td>-5.7%</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Ontario</td>
      <td>$752,400</td>
      <td>0.4%</td>
      <td>-5.7%</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Quebec</td>
      <td>$550,800</td>
      <td>0.3%</td>
      <td>5.0%</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Alberta</td>
      <td>$514,000</td>
      <td>0.9%</td>
      <td>-2.4%</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Nova Scotia</td>
      <td>$440,800</td>
      <td>0.8%</td>
      <td>2.4%</td>
    </tr>
    <tr>
      <th>5</th>
      <td>PEI</td>
      <td>$378,900</td>
      <td>0.5%</td>
      <td>4.0%</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Saskatchewan</td>
      <td>$374,300</td>
      <td>0.1%</td>
      <td>4.5%</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Newfoundland</td>
      <td>$339,400</td>
      <td>1.6%</td>
      <td>9.8%</td>
    </tr>
    <tr>
      <th>8</th>
      <td>New Brunswick</td>
      <td>$324,400</td>
      <td>-1.5%</td>
      <td>1.3%</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Canada</td>
      <td>$666,400</td>
      <td>0.3%</td>
      <td>-4.1%</td>
    </tr>
  </tbody>
</table>
</div>



MINI CHALLENGE #7:
- Write a code that uses Pandas to read tabular US retirement data
- You can use data from here: https://www.ssa.gov/oact/progdata/nra.html 


```python
retirement_df = pd.read_html('https://www.ssa.gov/OACT/progdata/nra.html')
retirement_df
```


    ---------------------------------------------------------------------------

    HTTPError                                 Traceback (most recent call last)

    Cell In [89], line 1
    ----> 1 retirement_df = pd.read_html('https://www.ssa.gov/OACT/progdata/nra.html')
          2 retirement_df


    File /opt/conda/lib/python3.10/site-packages/pandas/util/_decorators.py:331, in deprecate_nonkeyword_arguments.<locals>.decorate.<locals>.wrapper(*args, **kwargs)
        325 if len(args) > num_allow_args:
        326     warnings.warn(
        327         msg.format(arguments=_format_argument_list(allow_args)),
        328         FutureWarning,
        329         stacklevel=find_stack_level(),
        330     )
    --> 331 return func(*args, **kwargs)


    File /opt/conda/lib/python3.10/site-packages/pandas/io/html.py:1205, in read_html(io, match, flavor, header, index_col, skiprows, attrs, parse_dates, thousands, encoding, decimal, converters, na_values, keep_default_na, displayed_only, extract_links)
       1201 validate_header_arg(header)
       1203 io = stringify_path(io)
    -> 1205 return _parse(
       1206     flavor=flavor,
       1207     io=io,
       1208     match=match,
       1209     header=header,
       1210     index_col=index_col,
       1211     skiprows=skiprows,
       1212     parse_dates=parse_dates,
       1213     thousands=thousands,
       1214     attrs=attrs,
       1215     encoding=encoding,
       1216     decimal=decimal,
       1217     converters=converters,
       1218     na_values=na_values,
       1219     keep_default_na=keep_default_na,
       1220     displayed_only=displayed_only,
       1221     extract_links=extract_links,
       1222 )


    File /opt/conda/lib/python3.10/site-packages/pandas/io/html.py:986, in _parse(flavor, io, match, attrs, encoding, displayed_only, extract_links, **kwargs)
        983 p = parser(io, compiled_match, attrs, encoding, displayed_only, extract_links)
        985 try:
    --> 986     tables = p.parse_tables()
        987 except ValueError as caught:
        988     # if `io` is an io-like object, check if it's seekable
        989     # and try to rewind it before trying the next parser
        990     if hasattr(io, "seekable") and io.seekable():


    File /opt/conda/lib/python3.10/site-packages/pandas/io/html.py:262, in _HtmlFrameParser.parse_tables(self)
        254 def parse_tables(self):
        255     """
        256     Parse and return all tables from the DOM.
        257 
       (...)
        260     list of parsed (header, body, footer) tuples from tables.
        261     """
    --> 262     tables = self._parse_tables(self._build_doc(), self.match, self.attrs)
        263     return (self._parse_thead_tbody_tfoot(table) for table in tables)


    File /opt/conda/lib/python3.10/site-packages/pandas/io/html.py:821, in _LxmlFrameParser._build_doc(self)
        819             pass
        820     else:
    --> 821         raise e
        822 else:
        823     if not hasattr(r, "text_content"):


    File /opt/conda/lib/python3.10/site-packages/pandas/io/html.py:802, in _LxmlFrameParser._build_doc(self)
        800 try:
        801     if is_url(self.io):
    --> 802         with urlopen(self.io) as f:
        803             r = parse(f, parser=parser)
        804     else:
        805         # try to parse the input in the simplest way


    File /opt/conda/lib/python3.10/site-packages/pandas/io/common.py:265, in urlopen(*args, **kwargs)
        259 """
        260 Lazy-import wrapper for stdlib urlopen, as that imports a big chunk of
        261 the stdlib.
        262 """
        263 import urllib.request
    --> 265 return urllib.request.urlopen(*args, **kwargs)


    File /opt/conda/lib/python3.10/urllib/request.py:216, in urlopen(url, data, timeout, cafile, capath, cadefault, context)
        214 else:
        215     opener = _opener
    --> 216 return opener.open(url, data, timeout)


    File /opt/conda/lib/python3.10/urllib/request.py:525, in OpenerDirector.open(self, fullurl, data, timeout)
        523 for processor in self.process_response.get(protocol, []):
        524     meth = getattr(processor, meth_name)
    --> 525     response = meth(req, response)
        527 return response


    File /opt/conda/lib/python3.10/urllib/request.py:634, in HTTPErrorProcessor.http_response(self, request, response)
        631 # According to RFC 2616, "2xx" code indicates that the client's
        632 # request was successfully received, understood, and accepted.
        633 if not (200 <= code < 300):
    --> 634     response = self.parent.error(
        635         'http', request, response, code, msg, hdrs)
        637 return response


    File /opt/conda/lib/python3.10/urllib/request.py:563, in OpenerDirector.error(self, proto, *args)
        561 if http_err:
        562     args = (dict, 'default', 'http_error_default') + orig_args
    --> 563     return self._call_chain(*args)


    File /opt/conda/lib/python3.10/urllib/request.py:496, in OpenerDirector._call_chain(self, chain, kind, meth_name, *args)
        494 for handler in handlers:
        495     func = getattr(handler, meth_name)
    --> 496     result = func(*args)
        497     if result is not None:
        498         return result


    File /opt/conda/lib/python3.10/urllib/request.py:643, in HTTPDefaultErrorHandler.http_error_default(self, req, fp, code, msg, hdrs)
        642 def http_error_default(self, req, fp, code, msg, hdrs):
    --> 643     raise HTTPError(req.full_url, code, msg, hdrs, fp)


    HTTPError: HTTP Error 403: Forbidden


# TASK #8: PANDAS OPERATIONS


```python
# Let's define a dataframe as follows:

bank_client_df = pd.DataFrame({'Bank Client ID':[111, 222, 333, 444], 
                               'Bank Client Name':['Chanel', 'Steve', 'Mitch', 'Ryan'],
                               'Net Worth [$]':[3500, 29000, 10000, 2000],
                               'Years with bank':[3, 4, 9, 5]})
bank_client_df 
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Bank Client ID</th>
      <th>Bank Client Name</th>
      <th>Net Worth [$]</th>
      <th>Years with bank</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>111</td>
      <td>Chanel</td>
      <td>3500</td>
      <td>3</td>
    </tr>
    <tr>
      <th>1</th>
      <td>222</td>
      <td>Steve</td>
      <td>29000</td>
      <td>4</td>
    </tr>
    <tr>
      <th>2</th>
      <td>333</td>
      <td>Mitch</td>
      <td>10000</td>
      <td>9</td>
    </tr>
    <tr>
      <th>3</th>
      <td>444</td>
      <td>Ryan</td>
      <td>2000</td>
      <td>5</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Pick certain rows that satisfy a certain criteria 

df_loyal = bank_client_df[bank_client_df["Years with bank"] >= 5]
df_loyal
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Bank Client ID</th>
      <th>Bank Client Name</th>
      <th>Net Worth [$]</th>
      <th>Years with bank</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2</th>
      <td>333</td>
      <td>Mitch</td>
      <td>10000</td>
      <td>9</td>
    </tr>
    <tr>
      <th>3</th>
      <td>444</td>
      <td>Ryan</td>
      <td>2000</td>
      <td>5</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Delete a column from a DataFrame

del bank_client_df["Bank Client ID"]
bank_client_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Bank Client Name</th>
      <th>Net Worth [$]</th>
      <th>Years with bank</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Chanel</td>
      <td>3500</td>
      <td>3</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Steve</td>
      <td>29000</td>
      <td>4</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Mitch</td>
      <td>10000</td>
      <td>9</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Ryan</td>
      <td>2000</td>
      <td>5</td>
    </tr>
  </tbody>
</table>
</div>



MINI CHALLENGE #8:
- Using "bank_client_df" DataFrame, leverage pandas operations to only select high networth individuals with minimum $5000 
- What is the combined networth for all customers with 5000+ networth?


```python
df_high_networth = bank_client_df[bank_client_df["Net Worth [$]"] >= 5000]
df_high_networth
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Bank Client Name</th>
      <th>Net Worth [$]</th>
      <th>Years with bank</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Steve</td>
      <td>29000</td>
      <td>4</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Mitch</td>
      <td>10000</td>
      <td>9</td>
    </tr>
  </tbody>
</table>
</div>




```python
df_high_networth["Net Worth [$]"].sum()
```




    39000



# TASK #9: PANDAS WITH FUNCTIONS


```python
# Let's define a dataframe as follows:
bank_client_df = pd.DataFrame({'Bank client ID':[111, 222, 333, 444], 
                               'Bank Client Name':['Chanel', 'Steve', 'Mitch', 'Ryan'], 
                               'Net worth [$]':[3500, 29000, 10000, 2000], 
                               'Years with bank':[3, 4, 9, 5]})
bank_client_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Bank client ID</th>
      <th>Bank Client Name</th>
      <th>Net worth [$]</th>
      <th>Years with bank</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>111</td>
      <td>Chanel</td>
      <td>3500</td>
      <td>3</td>
    </tr>
    <tr>
      <th>1</th>
      <td>222</td>
      <td>Steve</td>
      <td>29000</td>
      <td>4</td>
    </tr>
    <tr>
      <th>2</th>
      <td>333</td>
      <td>Mitch</td>
      <td>10000</td>
      <td>9</td>
    </tr>
    <tr>
      <th>3</th>
      <td>444</td>
      <td>Ryan</td>
      <td>2000</td>
      <td>5</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Define a function that increases all clients networth (stocks) by a fixed value of 20% (for simplicity sake) 

def networth_update(balance):
    return balance * 1.2
```


```python
# You can apply a function to the DataFrame 

bank_client_df['Net worth [$]'].apply(networth_update)
```




    0     4200.0
    1    34800.0
    2    12000.0
    3     2400.0
    Name: Net worth [$], dtype: float64




```python
bank_client_df["Bank Client Name"].apply(len)
```




    0    6
    1    5
    2    5
    3    4
    Name: Bank Client Name, dtype: int64



MINI CHALLENGE #9:
- Define a function that triples the stock prices and adds $200
- Apply the function to the DataFrame
- Calculate the updated total networth of all clients combined


```python
def networth_update(balance):
    return balance * 3 + 200
```


```python
result = bank_client_df['Net worth [$]'].apply(networth_update)
```


```python
result
```




    0    10700
    1    87200
    2    30200
    3     6200
    Name: Net worth [$], dtype: int64




```python
result.sum()
```




    134300



# TASK #10: PERFORM SORTING AND ORDERING IN PANDAS


```python
# Let's define a dataframe as follows:
bank_client_df = pd.DataFrame({'Bank client ID':[111, 222, 333, 444], 
                               'Bank Client Name':['Chanel', 'Steve', 'Mitch', 'Ryan'], 
                               'Net worth [$]':[3500, 29000, 10000, 2000], 
                               'Years with bank':[3, 4, 9, 5]})
bank_client_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Bank client ID</th>
      <th>Bank Client Name</th>
      <th>Net worth [$]</th>
      <th>Years with bank</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>111</td>
      <td>Chanel</td>
      <td>3500</td>
      <td>3</td>
    </tr>
    <tr>
      <th>1</th>
      <td>222</td>
      <td>Steve</td>
      <td>29000</td>
      <td>4</td>
    </tr>
    <tr>
      <th>2</th>
      <td>333</td>
      <td>Mitch</td>
      <td>10000</td>
      <td>9</td>
    </tr>
    <tr>
      <th>3</th>
      <td>444</td>
      <td>Ryan</td>
      <td>2000</td>
      <td>5</td>
    </tr>
  </tbody>
</table>
</div>




```python
# You can sort the values in the dataframe according to number of years with bank
bank_client_df.sort_values(by = "Years with bank")
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Bank client ID</th>
      <th>Bank Client Name</th>
      <th>Net worth [$]</th>
      <th>Years with bank</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>111</td>
      <td>Chanel</td>
      <td>3500</td>
      <td>3</td>
    </tr>
    <tr>
      <th>1</th>
      <td>222</td>
      <td>Steve</td>
      <td>29000</td>
      <td>4</td>
    </tr>
    <tr>
      <th>3</th>
      <td>444</td>
      <td>Ryan</td>
      <td>2000</td>
      <td>5</td>
    </tr>
    <tr>
      <th>2</th>
      <td>333</td>
      <td>Mitch</td>
      <td>10000</td>
      <td>9</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Note that nothing changed in memory! you have to make sure that inplace is set to True
bank_client_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Bank client ID</th>
      <th>Bank Client Name</th>
      <th>Net worth [$]</th>
      <th>Years with bank</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>111</td>
      <td>Chanel</td>
      <td>3500</td>
      <td>3</td>
    </tr>
    <tr>
      <th>1</th>
      <td>222</td>
      <td>Steve</td>
      <td>29000</td>
      <td>4</td>
    </tr>
    <tr>
      <th>2</th>
      <td>333</td>
      <td>Mitch</td>
      <td>10000</td>
      <td>9</td>
    </tr>
    <tr>
      <th>3</th>
      <td>444</td>
      <td>Ryan</td>
      <td>2000</td>
      <td>5</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Set inplace = True to ensure that change has taken place in memory 
bank_client_df.sort_values(by = "Years with bank", inplace = True)
```


```python
# Note that now the change (ordering) took place 
bank_client_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Bank client ID</th>
      <th>Bank Client Name</th>
      <th>Net worth [$]</th>
      <th>Years with bank</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>111</td>
      <td>Chanel</td>
      <td>3500</td>
      <td>3</td>
    </tr>
    <tr>
      <th>1</th>
      <td>222</td>
      <td>Steve</td>
      <td>29000</td>
      <td>4</td>
    </tr>
    <tr>
      <th>3</th>
      <td>444</td>
      <td>Ryan</td>
      <td>2000</td>
      <td>5</td>
    </tr>
    <tr>
      <th>2</th>
      <td>333</td>
      <td>Mitch</td>
      <td>10000</td>
      <td>9</td>
    </tr>
  </tbody>
</table>
</div>



# TASK #11: PERFORM CONCATENATING AND MERGING WITH PANDAS


```python
# Check this out: https://pandas.pydata.org/pandas-docs/stable/user_guide/merging.html
```


```python
df1 = pd.DataFrame({ 'A' : ['A0', 'A1', 'A2', 'A3'],
                     'B' : ['B0', 'B1', 'B2', 'B3'],
                     'C' : ['C0', 'C1', 'C2', 'C3'],
                     'D' : ['D0', 'D1', 'D2', 'D3']},
                   index = [0, 1, 2, 3])
```


```python
df1
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>A0</td>
      <td>B0</td>
      <td>C0</td>
      <td>D0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>A1</td>
      <td>B1</td>
      <td>C1</td>
      <td>D1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>A2</td>
      <td>B2</td>
      <td>C2</td>
      <td>D2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>A3</td>
      <td>B3</td>
      <td>C3</td>
      <td>D3</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2 = pd.DataFrame({ 'A' : ['A4', 'A5', 'A6', 'A7'],
                     'B' : ['B4', 'B5', 'B6', 'B7'],
                     'C' : ['C4', 'C5', 'C6', 'C7'],
                     'D' : ['D4', 'D5', 'D6', 'D7']},
                   index = [4, 5, 6, 7])
```


```python
df2
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>4</th>
      <td>A4</td>
      <td>B4</td>
      <td>C4</td>
      <td>D4</td>
    </tr>
    <tr>
      <th>5</th>
      <td>A5</td>
      <td>B5</td>
      <td>C5</td>
      <td>D5</td>
    </tr>
    <tr>
      <th>6</th>
      <td>A6</td>
      <td>B6</td>
      <td>C6</td>
      <td>D6</td>
    </tr>
    <tr>
      <th>7</th>
      <td>A7</td>
      <td>B7</td>
      <td>C7</td>
      <td>D7</td>
    </tr>
  </tbody>
</table>
</div>




```python
df3 = pd.DataFrame({ 'A' : ['A8', 'A9', 'A10', 'A11'],
                     'B' : ['B8', 'B9', 'B10', 'B11'],
                     'C' : ['C8', 'C9', 'C10', 'C11'],
                     'D' : ['D8', 'D9', 'D10', 'D11']},
                   index = [8, 9, 10, 11])
```


```python
df3
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>8</th>
      <td>A8</td>
      <td>B8</td>
      <td>C8</td>
      <td>D8</td>
    </tr>
    <tr>
      <th>9</th>
      <td>A9</td>
      <td>B9</td>
      <td>C9</td>
      <td>D9</td>
    </tr>
    <tr>
      <th>10</th>
      <td>A10</td>
      <td>B10</td>
      <td>C10</td>
      <td>D10</td>
    </tr>
    <tr>
      <th>11</th>
      <td>A11</td>
      <td>B11</td>
      <td>C11</td>
      <td>D11</td>
    </tr>
  </tbody>
</table>
</div>




```python
pd.concat([df1, df2, df3])
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>A0</td>
      <td>B0</td>
      <td>C0</td>
      <td>D0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>A1</td>
      <td>B1</td>
      <td>C1</td>
      <td>D1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>A2</td>
      <td>B2</td>
      <td>C2</td>
      <td>D2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>A3</td>
      <td>B3</td>
      <td>C3</td>
      <td>D3</td>
    </tr>
    <tr>
      <th>4</th>
      <td>A4</td>
      <td>B4</td>
      <td>C4</td>
      <td>D4</td>
    </tr>
    <tr>
      <th>5</th>
      <td>A5</td>
      <td>B5</td>
      <td>C5</td>
      <td>D5</td>
    </tr>
    <tr>
      <th>6</th>
      <td>A6</td>
      <td>B6</td>
      <td>C6</td>
      <td>D6</td>
    </tr>
    <tr>
      <th>7</th>
      <td>A7</td>
      <td>B7</td>
      <td>C7</td>
      <td>D7</td>
    </tr>
    <tr>
      <th>8</th>
      <td>A8</td>
      <td>B8</td>
      <td>C8</td>
      <td>D8</td>
    </tr>
    <tr>
      <th>9</th>
      <td>A9</td>
      <td>B9</td>
      <td>C9</td>
      <td>D9</td>
    </tr>
    <tr>
      <th>10</th>
      <td>A10</td>
      <td>B10</td>
      <td>C10</td>
      <td>D10</td>
    </tr>
    <tr>
      <th>11</th>
      <td>A11</td>
      <td>B11</td>
      <td>C11</td>
      <td>D11</td>
    </tr>
  </tbody>
</table>
</div>



# TASK #12: PROJECT AND CONCLUDING REMARKS

- Define a dataframe named 'Bank_df_1' that contains the first and last names for 5 bank clients with IDs = 1, 2, 3, 4, 5 
- Assume that the bank got 5 new clients, define another dataframe named 'Bank_df_2' that contains a new clients with IDs = 6, 7, 8, 9, 10
- Let's assume we obtained additional information (Annual Salary) about all our bank customers (10 customers) 
- Concatenate both 'bank_df_1' and 'bank_df_2' dataframes
- Merge client names and their newly added salary information using the 'Bank Client ID'
- Let's assume that you became a new client to the bank
- Define a new DataFrame that contains your information such as client ID (choose 11), first name, last name, and annual salary.
- Add this new dataframe to the original dataframe 'bank_df_all'.


```python
raw_data = {'Bank Client ID': ['1', '2', '3', '4', '5'],
            'First Name': ['Nancy', 'Alex', 'Shep', 'Max', 'Allen'], 
            'Last Name': ['Rob', 'Ali', 'George', 'Mitch', 'Steve']}

Bank_df_1 = pd.DataFrame(raw_data, columns = ['Bank Client ID', 'First Name', 'Last Name'])
Bank_df_1
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Bank Client ID</th>
      <th>First Name</th>
      <th>Last Name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>Nancy</td>
      <td>Rob</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>Alex</td>
      <td>Ali</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>Shep</td>
      <td>George</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>Max</td>
      <td>Mitch</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>Allen</td>
      <td>Steve</td>
    </tr>
  </tbody>
</table>
</div>




```python
raw_data = {
        'Bank Client ID': ['6', '7', '8', '9', '10'],
        'First Name': ['Bill', 'Dina', 'Sarah', 'Heather', 'Holly'], 
        'Last Name': ['Christian', 'Mo', 'Steve', 'Bob', 'Michelle']}

Bank_df_2 = pd.DataFrame(raw_data, columns = ['Bank Client ID', 'First Name', 'Last Name'])
Bank_df_2
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Bank Client ID</th>
      <th>First Name</th>
      <th>Last Name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>6</td>
      <td>Bill</td>
      <td>Christian</td>
    </tr>
    <tr>
      <th>1</th>
      <td>7</td>
      <td>Dina</td>
      <td>Mo</td>
    </tr>
    <tr>
      <th>2</th>
      <td>8</td>
      <td>Sarah</td>
      <td>Steve</td>
    </tr>
    <tr>
      <th>3</th>
      <td>9</td>
      <td>Heather</td>
      <td>Bob</td>
    </tr>
    <tr>
      <th>4</th>
      <td>10</td>
      <td>Holly</td>
      <td>Michelle</td>
    </tr>
  </tbody>
</table>
</div>




```python
raw_data = {
        'Bank Client ID': ['1', '2', '3', '4', '5', '6', '7', '8', '9', '10'],
        'Annual Salary [$/year]': [25000, 35000, 45000, 48000, 49000, 32000, 33000, 34000, 23000, 22000]}
bank_df_salary = pd.DataFrame(raw_data, columns = ['Bank Client ID','Annual Salary [$/year]'])
bank_df_salary
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Bank Client ID</th>
      <th>Annual Salary [$/year]</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>25000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>35000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>45000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>48000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>49000</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>32000</td>
    </tr>
    <tr>
      <th>6</th>
      <td>7</td>
      <td>33000</td>
    </tr>
    <tr>
      <th>7</th>
      <td>8</td>
      <td>34000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>9</td>
      <td>23000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>10</td>
      <td>22000</td>
    </tr>
  </tbody>
</table>
</div>




```python
bank_df_all = pd.concat([Bank_df_1, Bank_df_2])
bank_df_all
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Bank Client ID</th>
      <th>First Name</th>
      <th>Last Name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>Nancy</td>
      <td>Rob</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>Alex</td>
      <td>Ali</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>Shep</td>
      <td>George</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>Max</td>
      <td>Mitch</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>Allen</td>
      <td>Steve</td>
    </tr>
    <tr>
      <th>0</th>
      <td>6</td>
      <td>Bill</td>
      <td>Christian</td>
    </tr>
    <tr>
      <th>1</th>
      <td>7</td>
      <td>Dina</td>
      <td>Mo</td>
    </tr>
    <tr>
      <th>2</th>
      <td>8</td>
      <td>Sarah</td>
      <td>Steve</td>
    </tr>
    <tr>
      <th>3</th>
      <td>9</td>
      <td>Heather</td>
      <td>Bob</td>
    </tr>
    <tr>
      <th>4</th>
      <td>10</td>
      <td>Holly</td>
      <td>Michelle</td>
    </tr>
  </tbody>
</table>
</div>




```python
bank_df_all = pd.merge(bank_df_all, bank_df_salary, on = 'Bank Client ID')
bank_df_all
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Bank Client ID</th>
      <th>First Name</th>
      <th>Last Name</th>
      <th>Annual Salary [$/year]</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>Nancy</td>
      <td>Rob</td>
      <td>25000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>Alex</td>
      <td>Ali</td>
      <td>35000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>Shep</td>
      <td>George</td>
      <td>45000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>Max</td>
      <td>Mitch</td>
      <td>48000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>Allen</td>
      <td>Steve</td>
      <td>49000</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>Bill</td>
      <td>Christian</td>
      <td>32000</td>
    </tr>
    <tr>
      <th>6</th>
      <td>7</td>
      <td>Dina</td>
      <td>Mo</td>
      <td>33000</td>
    </tr>
    <tr>
      <th>7</th>
      <td>8</td>
      <td>Sarah</td>
      <td>Steve</td>
      <td>34000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>9</td>
      <td>Heather</td>
      <td>Bob</td>
      <td>23000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>10</td>
      <td>Holly</td>
      <td>Michelle</td>
      <td>22000</td>
    </tr>
  </tbody>
</table>
</div>




```python
new_client = {
        'Bank Client ID': ['11'],
        'First Name': ['Ryan'], 
        'Last Name': ['Ahmed'],
        'Annual Salary [$/year]' : [1000]}
new_client_df = pd.DataFrame(new_client, columns = ['Bank Client ID', 'First Name', 'Last Name', 'Annual Salary [$/year]'])
new_client_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Bank Client ID</th>
      <th>First Name</th>
      <th>Last Name</th>
      <th>Annual Salary [$/year]</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>11</td>
      <td>Ryan</td>
      <td>Ahmed</td>
      <td>1000</td>
    </tr>
  </tbody>
</table>
</div>




```python
new_df = pd.concat([bank_df_all, new_client_df], axis = 0)
new_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Bank Client ID</th>
      <th>First Name</th>
      <th>Last Name</th>
      <th>Annual Salary [$/year]</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>Nancy</td>
      <td>Rob</td>
      <td>25000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>Alex</td>
      <td>Ali</td>
      <td>35000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>Shep</td>
      <td>George</td>
      <td>45000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>Max</td>
      <td>Mitch</td>
      <td>48000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>Allen</td>
      <td>Steve</td>
      <td>49000</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>Bill</td>
      <td>Christian</td>
      <td>32000</td>
    </tr>
    <tr>
      <th>6</th>
      <td>7</td>
      <td>Dina</td>
      <td>Mo</td>
      <td>33000</td>
    </tr>
    <tr>
      <th>7</th>
      <td>8</td>
      <td>Sarah</td>
      <td>Steve</td>
      <td>34000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>9</td>
      <td>Heather</td>
      <td>Bob</td>
      <td>23000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>10</td>
      <td>Holly</td>
      <td>Michelle</td>
      <td>22000</td>
    </tr>
    <tr>
      <th>0</th>
      <td>11</td>
      <td>Ryan</td>
      <td>Ahmed</td>
      <td>1000</td>
    </tr>
  </tbody>
</table>
</div>


