 ## NumPy 
 - refers to Numerical Python. 
 - It is an open-source library in Python that aids in mathematical and numerical calculations and computations; 
 - and, scientific, engineering, and data science programming. NumPy is an essential library used to perform mathematical and statistical operations.
 - It is especially suited for multi-dimensional arrays and matrix multiplications.
 -  This NumPy tutorial focuses on the essential things you need to know to master NumPy.
 
 ### Installation
   - NumPy can be installed using pip, a Python package installer, with the following command:
   
   ```Python
   pip install numpy

   ```
### Importing NumPy
- After installation, you can import NumPy in your Python code using the following line:
-
```python
import numpy as np

```

### Creating NumPy Arrays
NumPy arrays can be created in multiple ways. Here are some examples:

```python
# Create an array from a list
arr1 = np.array([1, 2, 3, 4, 5])
print(arr1) # Output: [1 2 3 4 5]

# Create a 2D array from a list of lists
arr2 = np.array([[1, 2, 3], [4, 5, 6]])
print(arr2) # Output: [[1 2 3]
            #          [4 5 6]]

# Create an array with all zeros
zeros = np.zeros((2, 3)) # 2 rows, 3 columns
print(zeros) # Output: [[0. 0. 0.]
             #          [0. 0. 0.]]

# Create an array with all ones
ones = np.ones((3, 2)) # 3 rows, 2 columns
print(ones) # Output: [[1. 1.]
            #          [1. 1.]
            #          [1. 1.]]

# Create an identity matrix
identity = np.eye(3)
print(identity) # Output: [[1. 0. 0.]
                #          [0. 1. 0.]
                #          [0. 0. 1.]]

# Create a random array
rand_arr = np.random.rand(2, 3) # 2 rows, 3 columns
print(rand_arr) # Output: [[0.47359684 0.86144461 0.57547468]
                #          [0.11466386 0.81429667 0.01362177]]

```

### Accessing Elements of NumPy Arrays
Elements of NumPy arrays can be accessed by indexing and slicing.
```python
arr = np.array([1, 2, 3, 4, 5])

# Access the element at index 2
print(arr[2]) # Output: 3

# Access elements from index 1 to 3 (exclusive)
print(arr[1:3]) # Output: [2 3]

# Access elements from index 2 to the end
print(arr[2:]) # Output: [3 4 5]

```

#### For 2D arrays, we can access elements by specifying the row and column indices.
```python
arr = np.array([[1, 2, 3], [4, 5, 6]])

# Access the element in the first row and second column
print(arr[0, 1]) # Output: 2

# Access all elements in the second row
print(arr[1, :]) # Output: [4 5 6]

```
### NumPy Mathematical Operation
NumPy is a Python library that provides support for performing mathematical operations on arrays and matrices. Some common mathematical operations that can be performed using NumPy include:

- Addition and Subtraction
```python
import numpy as np
a = np.array([[1,2,3],[4,5,6],[7,8,9]])
b = np.array([[9,8,7],[6,5,4],[3,2,1]])
c = a + b
d = a - b
```
- Multiplication and Division
```python
import numpy as np
a = np.array([[1,2,3],[4,5,6],[7,8,9]])
b = np.array([[9,8,7],[6,5,4],[3,2,1]])
c = a * b
d = a / b
```
- Dot Product
```python
import numpy as np
a = np.array([[1,2,3],[4,5,6],[7,8,9]])
b = np.array([[2],[3],[4]])
c = np.dot(a,b)

```
- Transpose
```python
import numpy as np
a = np.array([[1,2,3],[4,5,6],[7,8,9]])
b = a.T

```

## NumPy Array functions
Here are some commonly used NumPy array functions:
- np.array() - Creates a NumPy array from a list or tuple.
- np.arange() - Generates a sequence of evenly spaced values within a given interval.
- np.zeros() - Creates an array filled with zeros.
- np.ones() - Creates an array filled with ones.
- np.empty() - Creates an array without initializing its elements to any particular value.
-  np.linspace() - Generates a sequence of evenly spaced numbers over a specified interval.
-  np.eye() - Creates a 2D array with ones on the diagonal and zeros elsewhere.
-  np.random.rand() - Generates an array of random numbers uniformly distributed over [0,1].
-  np.random.randn() - Generates an array of random numbers following a standard normal distribution.
-  np.reshape() - Reshapes an array into a specified shape.
-  np.transpose() - Transposes an array (rows become columns, and vice versa).
-  np.dot() - Computes the dot product of two arrays.
-  np.sum() - Computes the sum of the elements in an array.
-  np.mean() - Computes the mean of the elements in an array.
-  np.std() - Computes the standard deviation of the elements in an array.
-  np.min() - Computes the minimum element in an array.
-  np.max() - Computes the maximum element in an array.
-  np.argsort() - Returns the indices that would sort an array.
-  np.concatenate() - Concatenates two or more arrays along a specified axis.
-  np.split() - Splits an array into multiple sub-arrays along a specified axis.
These are just a few examples of the many functions available in NumPy. NumPy is a very powerful 
library for working with arrays and has a lot of functionality for mathematical operations, data analysis, and more.


