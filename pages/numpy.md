
# NumPy
[NumPy](https://docs.scipy.org/doc/numpy/reference/) 
is the basic package for doing slightly more advanced math and storing data in an analytics-friendly form.
 we have to import the package into our current environment to actually use it. We do this with an import statement. When importing a package you also have the opportunity to set an abbreviation for recalling its functions. Many packages have standard shorthand, which we will follow. The shorthand for numpy is simply np. 
 ```
 import numpy as np
 ```

Even thought Python lists are very powerfull, they are problematic when quick, efficient mathematical operations over collections are required. Mathematical operations are not defined for list and it is inneficient to perform the calculations one by one ( as with a loop for example). NumPy (numeric Python) provides an alternative to regular Python lists: the NumPy array. The NumPy array is very similar to the Python lists, but it can perform calculations over entire arrays efficiently. NumPy considers an array as if it was a single values so it is easy to perform element-wide calculations. 

```
# Create lists
height = [1.8796, 1.8796, 1.8288, 1.905 , 1.905 , 1.8542]
weight = [81.64656, 97.52228, 95.25432, 92.98636, 86.18248, 88.45044]

# Import the NumPy package as np
import numpy as np

# Create a NumPy arrays
np_height = np.array(height)
print(type(np_height)) # note that ndarray stands for N-dimentional array
np_weight = np.array(weight)

# Compare multiplication between list and NumPy array
print(height * 2)
print(np_height * 2)

# Compare BMI clculation between list and NumPy array
print(weight / height ** 2) #Type Error
print(np_weight / np_height ** 2)
```
However, this can only be done efficiently because, unlike lists, NumPy arrays cannot contain elements with different types. If you try to build such a list, some of the elements' types are changed to end up with a homogeneous list. This is known as *type coercion*. Also, NumPy arrays are a new object type, it has its own methods that may behave differently from list methods. 
For example, the typical arithmetic operators, such as +, -, * and / have a different meaning for regular Python lists and NumPy arrays.

```
import numpy as np
# Consider the operation
np.array([True, 1, 2]) + np.array([3, 4, False])
# Type coersion will result in
np.array([1, 1, 2]) + np.array([3, 4, 0])
# The + operator does not extend the array as a it does for a list, instead, it is the same as
np.array([1+3, 1+5, 2+0])
```


### Arrays

As we said above, NumPy is the fundamental package for storing and manipulating mathematical data in Python. NumPy primarily accomplishes this with a new data structure: the array.
A NumPy array can be thought of as a Python list with additional mathematical functionality and properties. One of the great attributes of the array is that, like lists, it can have multiple dimensions. A single dimensional array works like an ordered set of values, with various data points entered in it. Arrays use bracket notation [ ] to access items by index, just like lists and strings. We can create an array by calling np.array() and passing in any iterable. A list, for example:

You can add multiple dimensions to your array by either manually creating an array of arrays or with np.arange(). Here are two ways to generate the same thing:
np.arange() ("arange" is short for "array range") works similarly to the basic Python range() function by generating a sequence of integers, starting at 0 by default and incrementing by 1. But instead of returning a range() object it returns an array. We're taking advantage of that by calling the .reshape()
[array method](https://docs.scipy.org/doc/numpy/reference/generated/numpy.ndarray.reshape.html) to reshape the initial eight-item array into two four-item arrays.

```
x = np.array([0, 1, 2, 3])
x
w = np.array([[0, 1, 2, 3],[4, 5, 6, 7]])
w
y = np.arange(8).reshape(2, 4)
y
```

### Element-wise and Aggregator functions
NumPy's primary value is the ability to do more sophisticated arithmetic than basic Python can do out of the box. NumPy allows you to do these computations in two ways: with element-wise functions that process array elements one at a time and then return a new array, and with aggregator functions that process the array into a single value the function returns.
```
x = np.array([0, 1, 2, 3])

# Square each value.
print(np.square(x))

# Square root of each value.
print(np.sqrt(x))

# Cosine of each value.
print(np.cos(x))
```
Note that these methods return arrays of the same length as the input array, just like the built-in Python function map(). Use element-wise functions when you want to transform each individual element in an array and get back a collection of all the results.
```
x = np.array([0, 1, 2, 3])

# Find the maximum value.
print(np.max(x))

# Find the minimum value.
print(np.min(x))

# Find the mean of the input array.
print(np.mean(x))

# Find the standard deviation of the input array.
print(np.std(x))
```
Note that these aggregator functions return single values, rather than arrays. That is what an aggregator does. It takes a set of multiple data values and condenses them (or aggregates them) into a single value according to some rule. So np.min() returns the minimum value of all the data given to it, np.mean() the mean, and so on.

These are some of the basic functions of NumPy, but there are many more. 
If you'd like to know more now you can look through the basic 
[NumPy documentation](https://docs.scipy.org/doc/numpy/user/quickstart.html)



## Subsetting NumPy array

Subsetting a NumPy array can be done the same way as lists. However, NumPy arrays offer an additional subsetting option: subsetting by an array of booleans.


```
# Create lists
x = [4 , 9 , 6, 3, 1]
import numpy as np
y = np.array(x)

# Subset array as list
print(x[3])
print(y[3])
print(x[:3])
print(y[:3])

# Subset array with boolean array
high = y > 5
print(y[high])
print(y[y > 5])
```
## 2D NumPy arrays

NumPy arrays work can be multidimentional and, unlike lists, the dimentionality is important when performing operations with NumPy arrays. In fact, a Numpy array can be tought of as the implementation of a mathematical matrix, where dimention is a fundamental property. A 2-dimentional array can be define das a list of same length lists.

```
# Declare list of lists
lst = [[1,2,3,4],[5,6,7,8], [9,10,11,12]]
# Define 2D array
impor numpy as np
2d_np = np.array(lst)
2d_np.shape
```
This way, a 2D array is an improved list of lists. As such, subsetting can be done in a similar way. However, there is an alternative way, with a more intuitive (matematically) syntax. Instead of using square brakets for each list, the rows and columns of an 2D array can be defined within a single square bracket and separacted by a comma.
```
# Define 2D array
import numpy as np
2d_np = np.array([[1,2,3,4],[5,6,7,8], [9,10,11,12]])
# Subset as list
print(2d_np[1][2])
# Subset as matrix
print(2d_np[1,2])
print(2d_np[:1,2:3])
print(2d_np[1,:])
```

As with matrices, 2D NumPy arrays can be combined with single numbers, with vectors, and with other matrices, facilitating the implementation of a number of mathemetical calculations.
```
import numpy as np
np_mat = np.array([[1, 2],
                   [3, 4],
                   [5, 6]])
print(np_mat * 2)
print(np_mat + np_mat)
print(np_mat + np.array([10, 10]))
print(np_mat + np.array([[10], [10]])) # ValueError
```

## Statistics with NumPy (maybe a different file?)

A typical first step to analyse the data, is to get to know the data. With Big data, this may require to crunch millions or billions of numbers, so simply staring at the numbers like a zombie will not provide any insights. However, it is possible to generate summarizing statistics about the data. The summarizing statistics very useful to provide a "sanity check".
OULIERS, DISTRIBUTIONS. NumPy includes some functions that are already in the basic Python distribution, such as sum and sort., but it provides an improved efficiency due to the optimized NumPy array data structure (made up of unique data types).


```
import numpy as np

# Generate data from normal distribution (mean, std,number)
height = np.round(np.random.normal(73.6, 2.3, 5000))
height[50:500] = 50000 # Introduce outliers
weight = np.round(np.random.normal(201.3, 20.8, 5000))

# Make dataset by pasting the tuple of columns
people = np.column_stack((height, weight))

# Check mean and median of height (median more robust to outliers)
print(np.mean(people[:,0])) # Absurd value
print(np.sum(people) / people.shape[0])
print(np.median(people[:,0]))

# Check other statistics
print(np.std(people[:,1]))
print(np.corrcoef(people[:,0],people[:,1]))
```


