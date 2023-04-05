## Numpy Assignment
Student Name:KIRABO GLORIA

Reg No: 2022/HD07/2043U

## Instructions:
- Please complete the questions below.
- Please comment your code indicating how you approached the problem


```python
# What is NumPy, and what are some of its key features?
>NumPy stands for numeric python which is a python package for the computation 
and processing of the multidimensional and single dimensional array elements.
>Key features include; 
   1. Multidimensional arrays: NumPy provides a powerful ndarray object for representing
arrays of any number of dimensions. These arrays can be used to store and manipulate
large amounts of data efficiently.

   2. Fast element-wise operations: NumPy provides fast implementations of element-wise
operations such as addition, multiplication, and trigonometric functions. These operations
can be performed on entire arrays at once making them much faster than equivalent 

    3.Broadcasting: NumPy allows arrays with different shapes to be combined in element-wise operations.
     This is done through a process called broadcasting, which automatically aligns the shapes of the 
     arrays to perform the operation.

    4.Linear algebra: NumPy provides a wide variety of functions for performing linear algebra operations such as
   matrix multiplication, matrix inversion, and eigendecomposition.

    5.Fourier transforms: NumPy provides fast implementations of Fourier transforms, 
which are used in signal processing and many other applications.

    6.Integration with other libraries: NumPy is designed to work seamlessly with other 
Python libraries for scientific computing, such as SciPy, Pandas, and Matplotlib.
```


```python
#How do you create a NumPy array using Python's built-in range() function?
import numpy as np

b= np.array(range(12))
print(b)
#also arange can be used
a = np.arange(12)
print(a)
#also range function can be used to generate a range of integers
c = np.array(range(2,12,2))
print(c)

```


```python
#What is the difference between a scalar value and a vector in NumPy?
In NumPy, a scalar value is a single numerical value, such as an integer or a floating-point number,
that represents a magnitude but has no direction. A vector, on the other hand, is an array of numerical
values that represent both a magnitude and a direction. In other words, 
a vector is a quantity that has both magnitude and direction, while a scalar only has magnitude.

#Creating a scalar
import numpy as np
scalar = np.array(5)

#Creating a 1 dimension vector
vector = np.array(1,2,3)

```


```python
#How do you calculate the mean of a NumPy array using the mean() function?
import numpy as np

s = np.array([1, 2, 3, 4, 5])

mean_value = np.mean(s)

print(mean_value)

```

    3.0
    


```python
#What is broadcasting in NumPy, and how can it be useful?
#Broadcasting in NumPy is a feature that allows for element-wise operations between arrays of 
#different shapes and sizes. It is a way to perform mathematical operations on arrays with
#different shapes and sizes without the need to create additional copies of data or resize 
#the arrays.
#Broadcasting can be useful because it allows for more concise and readable code, as well as 
#avoiding the need to create additional copies of data or resize arrays. It can also be used to perform operations 
#between arrays of different shapes and sizes, which can be especially useful in scientific computing and data analysis.


import numpy as np

# Create a 2D array of shape (3, 3)
a = np.array([[1, 2, 3],
              [4, 5, 6],
              [7, 8, 9]])

# Create a 1D array of shape (3,)
b = np.array([1, 2, 3])

# Multiply the 2D array with the 1D array
c = a * b

print(c)

```

    [[ 1  4  9]
     [ 4 10 18]
     [ 7 16 27]]
    


```python
#How do you create a 2D array in NumPy using Python's built-in list of lists?
#You can create a 2D NumPy array using Python's built-in list of lists by passing
#the list to the numpy.array() 

import numpy as np

list_of_lists = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]

numpy_array = np.array(list_of_lists)

print(numpy_array)
```

    [[1 2 3]
     [4 5 6]
     [7 8 9]]
    


```python
#How can you slice a NumPy array to extract a subarray?
#To slice a NumPy array and extract a subarray, you can use 
#the slicing operator :. The basic syntax for slicing is:[new_array = original_array[start:end:step]]

import numpy as np

# create a 1D array
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])

# extract a subarray of elements from index 2 to index 6 (exclusive)
subarr = arr[2:6]

print(subarr) 
#Slicing from a 2D array
import numpy as np

# create a 2D array
arr = np.array([[1, 2, 3],
                [4, 5, 6],
                [7, 8, 9]])

# extract a subarray of elements from the first two rows and the first two columns
subarr = arr[:2, :2]

print(subarr) 

```

    [3 4 5 6]
    [[1 2]
     [4 5]]
    


```python
#What are some of the available functions for performing element-wise operations on NumPy arrays?

   1. numpy.add(): This function adds the corresponding elements of two arrays.

    2.numpy.subtract(): This function subtracts the corresponding elements of two arrays.

    3.numpy.multiply(): This function multiplies the corresponding elements of two arrays.

    4.numpy.divide(): This function divides the corresponding elements of two arrays.

    5.numpy.power(): This function raises each element in the array to the given power.

    6.numpy.exp(): This function computes the exponential of each element in the array.

    7.numpy.sqrt(): This function computes the square root of each element in the array.

    8.numpy.log(): This function computes the natural logarithm of each element in the array.

    9.numpy.sin(): This function computes the sine of each element in the array.

   10. numpy.cos(): This function computes the cosine of each element in the array.

    11.numpy.tan(): This function computes the tangent of each element in the array.
```


```python
#How do you reshape a NumPy array to have a different shape?
# we use the reshape() function.

c = np.array([2,3])
d = np.reshape(c, (2,1))
print(d)
```

    [[2]
     [3]]
    


```python
#How do you perform matrix multiplication on two NumPy arrays using the dot() function?

#The dot() function can be used to perform matrix multiplication
#on two-dimensional arrays (matrices) as well as on higher-dimensional arrays (tensors)

#Forexample, np.dot(A, B) performs matrix multiplication on arrays A and B, and returns
#the result in array C

import numpy as np

# Create two 2x3 arrays
A = np.array([[1, 2, 3], [4, 5, 6]])
B = np.array([[7, 8], [9, 10], [11, 12]])

# Perform matrix multiplication
C = np.dot(A, B)

# Print the result
print(C)
```

    [[ 58  64]
     [139 154]]
    


```python
#How can you use the where() function to apply a condition to a NumPy array?

#You can use the where() function to apply a condition to a NumPy array and return a new array with the same 
#shape and data type as the original array. The where() function takes three arguments:

#{numpy.where(condition, x, y)

import numpy as np

# Create a 1D array
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])

# Use where() to select only the even numbers from the array
new_arr = np.where(arr % 2 == 0, arr, 0)

print(new_arr)

```

    [ 0  2  0  4  0  6  0  8  0 10]
    


```python
#What is the difference between the flatten() and ravel() functions in NumPy?

    
import numpy as np

s = np.array([[1, 2, 3], [4, 5, 6]])

# using flatten()
s_flatten = s.flatten()
s_flatten[0] = 100 # modifying the first element of the flattened array
print(s) # original array is not affected


# using ravel()
s_ravel = s.ravel()
s_ravel[0] = 100 # modifying the first element of the raveled array
print(s) # original array is affected


```

    [[1 2 3]
     [4 5 6]]
    [[100   2   3]
     [  4   5   6]]
    


```python
#How do you use NumPy's advanced indexing capabilities to select specific elements from an array?

    #1.Boolean indexing: Use a boolean array to select elements from an array that meet certain conditions.

import numpy as np

a = np.array([1, 2, 3, 4, 5])
mask = np.array([True, False, True, False, True])

selected = a[mask]
print(selected) 


    #2.Integer indexing: Use an array of integers to select specific elements from an array.

c = np.array([1, 2, 3, 4, 5])
indices = np.array([0, 2, 4])

selected = c[indices]
print(selected) 

  # 3. Combining indexing: Use a combination of boolean and integer indexing to select specific elements from a
#multi-dimensional array.

import numpy as np

x = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
row_indices = np.array([0, 2])
col_indices = np.array([0, 2])

selected = x[row_indices[:, np.newaxis], col_indices]
print(selected) 



```

    [1 3 5]
    [1 3 5]
    [[1 3]
     [7 9]]
    


```python
#How can you use NumPy's broadcasting rules to perform operations on arrays with different shapes?
import numpy as np

a = np.array([1, 2, 3])
b = np.array([[4], [5], [6]])

c = a + b

print(c)

#In this example, a is a 1D array with shape (3,) and b is a 2D array with shape (3, 1). When we add them together,
# NumPy automatically broadcasts a to a shape of (3, 1)to match b, and then performs the addition operation element-wise.
# The result is a 2D array c with shape (3, 1)

```

    [[5 6 7]
     [6 7 8]
     [7 8 9]]
    


```python
#How do you perform element-wise division of two NumPy arrays while ignoring divide-by-zero errors?
#To perform element-wise division of two NumPy arrays while ignoring divide-by-zero errors, you can use the numpy.errstate
#context manager.This allows you to temporarily modify the error-handling behavior of NumPy.

import numpy as np

a = np.array([1, 2, 3])
b = np.array([0, 2, 0])

with np.errstate(divide='ignore', invalid='ignore'):
    c = np.true_divide(a, b)

print(c)


```

    [inf  1. inf]
    

### Project: Array Statistics Calculator
**Description:**

In this project, you will create a program that allows a user to enter a list of numbers, and then calculates and displays various statistics about those numbers using NumPy.

**Requirements:**

- The program should prompt the user to enter a list of numbers separated by commas.
- The program should use NumPy to convert the input into a 1D NumPy array.
- The program should calculate and display the following statistics:
- The mean of the numbers
- The median of the numbers
- The standard deviation of the numbers
- The maximum and minimum values of the numbers
- The program should use appropriate NumPy functions to calculate the statistics.
- The program should display the statistics with appropriate labels.

### Sample Output
```
Enter a list of numbers separated by commas: 2, 5, 7, 3, 1, 9
Statistics for the input array:
Mean: 4.5
Median: 4.0
Standard Deviation: 2.9154759474226504
Maximum: 9
Minimum: 1
```


```python
# Prompt the user to enter a list of numbers separated by commas
a = input("Enter a list of numbers separated by commas: ")

# Convert the input into a 1D NumPy array
a = np.array([float(x) for x in a.split(',')])

# Calculate the statistics using NumPy functions
mean = np.mean(a)
median = np.median(a)
std_dev = np.std(a)
max_val = np.max(a)
min_val = np.min(a)

# Display the statistics with appropriate labels
print("Statistics:")
print("Mean: ", mean)
print("Median: ", median)
print("Standard Deviation: ", std_dev)
print("Maximum Value: ", max_val)
print("Minimum Value: ", min_val)
```

    Enter a list of numbers separated by commas: 2, 5, 7, 3, 1, 9
    Statistics:
    Mean:  4.5
    Median:  4.0
    Standard Deviation:  2.8136571693556887
    Maximum Value:  9.0
    Minimum Value:  1.0
    


```python

```


```python

```
