# Introduction to Python

One of the first steps to become a Data Scientists is to become a programmer. A Data Scientist needs to use compotatuional tools efficiently, writing code that intereact with the data. The code itself is simply a sequence of stored instructions that are given to the computer. It is important to keep in mind that, unlike a human being, who has adapted to 
operate in an error-filled world, the computer is not tolerant to error. While the human brain automatically fix errors in the environment, some of which so efficiently that are unprecepive, a computer does not have any filtering mechanist and will simple stop. The computer is just not that smart, but it has a lot of flexibility in that, if given give it the right instructions, it can do "intelligent" things. So, the programmer is an intermediate between the hardware and the end user. 


Python is one of the most common programming tools used for Data Analysis.

 
## Why Python?

Python was conceived by Guido Van Rosson. What started as an hobby project, soon became a general purpose programming language. Even though Python is associated with the snake motif, it turns out that Python was not named after a snake. Instead, it was after the Monty Python's Flying Circus commedy. In the 80s, when Python started, most programming languages were very serious and very complex. They were difficult to figure out and required a lot of math. Guido thought he could probably write a programming language that wouldn't be that hard, would be enjoyable to use, but woould also be both powerful and enjoyable. It was meant to be fun to use, thus the name. It turns out that's why Python is such a perfect language to use as a first programming language: it's designed to be easy but it's also powerful.  

Nowadays, Python can be used to build practically any piece of software. This happaned because Python is open Source and Free! 
Also, it is very easy to build packages in Python. Thougout time, more and more of these packages were specifically build for data science.

Welcome to being a Pythonista.

## Install/Start Python
Currently, there are two versions of Python, 2.X and 3.X. They are pretty similar appart from some syntactical differences, 
but support for version 2 will fade overtime. Python 3 can be installed from [python.org](https://www.python.org/downloads)
In adidtion, there a number of Python distibutions that may be relevant, like the Anaconda distribution, which includes many science and data analysis libraries. OTHERS ?

Once installed, Python files will be reconise by their extension *.py*. There are many ways to  to run Python. The pasic Python distribution already provides the IDLE Python Shell and other integrated development environments (IDE) such as Spyder (included with the Anaconda distribution) can be obtained. However, the basic way to use Python is by running the command line (see [command line](pages/bash.md) to learn how to use it). Python files can be run by entering `python3 file_name.py` (simply python for Python2). The Python will be run, if it is in the current directory, otherwise, it will not be found. On Windows, typing the file name on it's own will also run Python, as all files with .py are expected to be Python and it knows the Python interpreter where to run. . To check the Python version, enter `python3 --version`.

Besides Python itself, it is important to have a text editor. The classical text editors come with the operating systems, like Word or Text Edit will not do for more complex programming. Editors with syntax highlight, automatic identing and other useful options can make programming a much simplers exerience. There are a number of editors that cn be used, including Notepad Plus, jEdit, Atom or Sublime.

## The Python Interface

Python can be run interactively by entering `python3` on the command line. This opens the Python shell which has a chevron (>>>) prompt, where commands can be entered (not that IDEs may have the shell inbedded already). Typing `print("Hello World")`) 
in the prompt and then *Enter* will run the Python command. To exit the Pythom promp, type `exit()` or `quit()`. So a series of statements can be typed in Python and processed interactively and it is possible to write entire programs interactively. However, this would require that it is typed perfectly from beginning to end. Once a program gets beyond a couple of lines of Python, it's much more common use a programming text editor and put all the code in a file. We call this a script or a Python program. Scripts are stored sets of instruction in text files that Python can run. Python scripts are identified by having an extention *.py*. Putting the code in Pyton scrips instead of manually typing it ineratively helps to keep structure ansd avoid retyping everything if one change is required

## Errors 

At the begining, Python may seem to be difficult and it is very common to get a Syntax Error thrown back when running a script.
Even tought it may be demotivating at first, it is important to keep in mind that *Syntax error* means Python is lost, it does not reconise an instruction. THIS MAY HAPPEN BECAUSE

## Comments

Before starting, it is important to be aware that **Comments** are important to any programming language. 
Comments are used to make sure that the code is understandandable and transmissable, improving reproductibility and, very importantly, debugging!
To add comments to a Python script,use the **#** tag. These comments are not run as Python code, 
so they will not influence your result. As an example, take the comment on the right, 
```
# Just greeting the whole world  
print("Hello World")
```
where *Just greeting the whole world* is completely ignored during execution, but makes the propose of the following code clear to anyone. Note the use of the function **print()**. This function DOES SOMETIME I NEED TO DESCRIBE :)

## Sentences 
SENTENCES OR STATMENTS ?
Sentences are the lines of code written on the script. A program is composed of a text file with sentence after sentence,
constructing paragraphs out of a series of lines. Sentenced are usually separated by a new line (break), but an 
alternative way, used for simple sentences, is to use semi-colon (;) sign is used to place sentences on the same line. So, the following two code chunks are equivalent:
```
# Same line
print('Hello'); print('World')

# Separate lines
print('Hello')
print('World')
```

## Operators 
we're using operators, this plus is what's called an operator, the equal sign is what's called an operator.
EXTEND

## Variables

Fundamental to any programming languase is the concept of **variable**, which is a *"storage"* for values in the memory.
A variable allows you to refer to a value with a name.
A Python variable is declared (created) with a specific, case-sensitive name. By using a calling a variable it is possible to recall the stored value, simplifying the code and making it more reproducible. 
As such, variables are used all the time in Python. To declare a variable, the assignment operator **=** (not equality!) can be used to assigned the value on the rght to the variable on the left. Once declared, a variable name com ve used instead of the value. This is fundamental when working with complex objects.
```
# Declaring a variable
five = 5
print(five)
```
Notice that the stored value can be changed, which allows for more complex computation to be performed without storing value
```
# Overwritting a variable value
number = 2
print(number)
number = number + 1
print(number)
```

COMMENT ON VARIABLE NAMING: do not name variables with reserved names. WHAT ARE THE BEST PRACTICES?

## Contants
## Reserved words

Every programming language has specific group of words that are associate with a specific meaning. These are know as reserved words and shouldn't be used for anything else but their original purpose. There are a number of reserved words in Python that are important to know. As they are fundamental building blocks of the Python syntax they can be introduced as required.

Reserved words in Python include: 
  * False
  * True
  * None
  * and
  * as 
  * assert
  * break
  * class
  * if
  * def
  * del
  * elif
  * else
  * except
  * return
  * for
  * from
  * global
  * try
  * import
  * in
  * is
  * lambda
  * while
  * not
  * or
  * pass
  * raise
  * finally
  * continue
  * nonlocal
  * with
  * yield

# Basic types
## Numbers
```
# Integer: Number without a fractional (decimal) part
print(type(5))
# Float: Number with both an integer and a fractional (decimal) separated by a point. A Real  number
print(type(5.0))
```

One of the most basic used of Python is to do basic calculations. Apart from **addition (+)**, **subtraction(-)**, 
**multiplication(\*)** and **division(/)**, there is also support for more advanced operations such as 
**exponentiation (\*\*)**, **modulo (%)** and **integer division (//)**.
```
# Addition: 
print(5 + 5)
# Subtraction:
print(5 - 5)
# Multiplication:  
print(3 * 5)
# Division
print(10 / 2)
# Division (integer)
print(11 // 2)
# Exponentiation: This operator raises the number to its left to the power of the number to its right. 
print(4 ** 2)
# Modulo: This operator returns the remainder of the division of the number to the left by the number on its right
print(18 % 7)
```

HOW DO THE OPERATORS WORK. ADD EXAMPLES IN MORE DETAIL: 10/2 is different than 10/2.0
Every object in Python has a type.
The type of any variable can be checked usint the **type()** function.
So far, most of the examples have used either numbers or text.
There are two types of numbers in Python, **integers (int)** and **floats (float)**. 


## Text
Text values are know as **strings (str)** in Python, There are also logical values know as **booleans (bool)**

should comment on why there are integers and floats and their representation at some point...
```
# String: Represents text values. Can be defined within using either double ("") or single ('') quotes
print(type("Hello again"))
print(type('Hello again'))
# Boolean: Represents logical values (True or False). Numerically, these values can be converted to 0 for False and 1 for True
print(type(True))
print(type(False))
```
## Booleans


## Convertion between types 
```
# Declare variable
value = 5
print(type(value), value)
# Integer to float
value = float(value)
print(type(value), value)
# Float to string
value = str(value)
print(type(value), value)
# String to boolean
value = bool(value)
print(type(value), value)
# Boolean to integer
value = int(value)
print(type(value), value)
```
Converting types can be very useful for combining different sources of information. For example, integers can be converted to str for reporting as string can be converted to floats to allow calculations on user inputs

``` 
# Gives a TypeError 
"I can add integers, like " + 5 + " to strings."
# Combines integers and strings
print("I can add integers, like " + str(5) + " to strings.")
print("I said " + ("Hey " * 2) + "Hey!")
# Converts string to floats
print(float("5.5") * 2)
# Converts boolean to integers
print(int(True)
```


## Note on type behaviours

Variable types are very important in Python as different types can show different bahaviour for the same operation. 
```
# Sum integers: + works as a mathematical operator 
print(2 + 5)
# Sum strings: + works not as a mathematical operator but as a text paste operatior
print('ab' + 'cb')
# Sum boolean: the booleans are converted to numerical values and + works as a mathematical operator operatior
print(True + False)
print(True + True + True)
```
As suggested in the previous example of the sum of booleans, object can be coverted between different types. 


# Compound types
## List
### Definition
The basic Python types allow for the storage of one single value. For scripts requiring a large number of values to be stored, it is inconvinient to create a new variable for each value. It would be impossible to assign a value to meaningfull and distinct names to each variable, making the code would be unreadable. A **list** one compound data type which is used to group values together, storing them in a single varaible. Lists can store values (elements) of any type, including any of the basic data types, other lists and even more advanced types, whithin the same variable. Lists instances can be initiated using the **list()** function or, more commonly, square brackets **[]**.

```
# Declaring list with list()
lst = list('a',1, True)
# Declaring list with []
lst = ['a',1, True]
# List of lists (2-dimention array)
lst = [[1, 2, 3], [4, 5, 7]]
lst = [1 + 2, "a" * 5, 3]
print(type(lst))
```

Note that a list of lists can be though of as a 2 dimentional matrix. The matrix is represented by the outer lists and each inner list is a row of values. The index in each row is consequently the column of the matrix. EXPLAIN WHAT A MATRIX IS?


### Subsetting

To acess the value of a list, Python uses a 0-index bases sytems. This means that, each value within a list is assigned a index value, starting from 0. As such, extracting a value from a list requires passing the index value to a list using square brackets **list[index]**. conviniently, Python additionally allows the using of negative indeces, that is, couting backwards from the last element of the list.

```
x = ["a", "b", "c", "d"]
# Indexing a list
print(x[1])
print(x[-3]) # same result!

# Using the extracted values for other operation
print(x[1] + x[3])
```
Apart from *indexing*, that is, extracting a single from a list, multiple values can be selected by *slicing* by specifying a range using a colon **list[start:end]**. Note that, even though the start index is included, the end index is excluded when slicing. If either the start or end arguments are not provided, the slicing occurs from the first, or up to the last, element respectively. 

```
# Slice a list
x = ["a", "b", "c", "d"]
print(x[1:3])
# Slece from the begigging and all the way to the end
x[:2]
x[2:]
# Slice all elements (important for copying)
x[:]
```
Subsetting unidimentinal lists, require passing only one index  value (or indeces range). Subsetting lists of lists also makes use of square brackets. In this case, the first index referes to the first list, and the second to the second list, that is, each list is subsetted one at a time.

```
x = [["a", "b", "c"],
     ["d", "e", "f"],
     ["g", "h", "i"]]
# Subset first list (row)
row = x[2]
print(row)
# Subset second list (columns)
print(row[0])

# Can also be done simultaneously
print(x[2][0])
# Slicing can also be used
print(x[2][:2])
```
### List manipulation

List are a very important data type to store values is Python, and the manipulation (updating) of these values will be essentional for most applications. Manipulation can involve a number of different operations, including addiong, removing and chaaging elements. To replacing list elements simply subset the list and assign new values to the subset. 
```
x = ["a", "b", "c", "d"]
x[1] = "r"
x[2:] = ["s", "t"]
```

As for strings and integers, the **+** operator also has a behaviour that is specific to lists. It is used to extend a list using other list. TO ADD APEEND VALUES  
```
x = ["a", "b", "c", "d"]
y = x + ["e", "f"]
```

To remove elements from your list, the **del** statement can be used. Note that, as soon as an element is removed from a list, the indexes of the elements that come after the deleted element will change.

```
x = ["a", "b", "c", "d"]
del(x[1])
```



### List as pointers/references

In Python, when a list is declared, the list itself is not stored in memory. This means that the list variable does not contain the values! In fact, a list is a reference to its values, storing only pointers to the values in memory. This does not seem very relevant for simple tasks, but it is fundamental to understand the copying behaviour of lists in Python. 

```
x = ["a", "b", "c", "d"]
# Simply assign a list to a new variable
y = x

# Change y
y[0] = 'z'
print(x); print(y)
```

This behaviour can lead to unexpected bugs. To copy a list in Python, it is necessary to duplicate the value in the memory and not to simply assign the pointers to a new variable.

```
x = ["a", "b", "c", "d"]
# Declare a new list from an existing list
y = list(x)
# Assign the sliced values of a list
z = x[:]

# Change y and z
y[0] = 'z'
z[0] = 'y'

print(x); print(y); print(z)
```

## Tuples

## Dictionaries

# Flow control

## Sequential
There are a couple of basic patterns that can be used for a program. The most basic pattern is what's called sequential. This is simply a coding pattern where statements follow one after the other in a sequence of commands that Python will obligatiry execute in order.
```
# Sequential pattern
number = 3
number += 2
print(number)
```

## Conditional
For more complex program, running sequential code is not enough. It may be important to have some type of decision where the data is analysed and depending on it one thing or another is done. These are called conditional steps and it defines optional parts of the code that may or may not run. If a given **condition** is true, then the statement is run; if it is false, then the statement is skiped. 
```
# Conditional step
number = 3
if number > 5:
  print('Too big')
elif number < 0:
  print('Too small')
else:
  print('That's a good number')
```

Conditional steps always start with the *if* reserved word followed by a condition that must evaluate to True or False and a colon (:). After the colon, the (sequential) conditional statements are in an indented block, which tells Python they are part of the conditional step. To finish the conditional, de-indent the code. SAY MORE

## Repeat 

**NOT DONE**
The real power of computers comes when a series of steps that need to be repeated. 

Now the most exciting pattern is the repeat. And it looks a little more busy because 
we can do more stuff with it. So the basic idea is there are a couple of different looping keywords, reserved words - the while and the for. The while loop basically says - it functions kind of like an if statement in that there's a question in it. It doesn't hurt n; n doesn't get changed by this, it just looks at n and asks the question is n greater than zero? If it is true, it runs this code. So just like an if. So up to here, it looks like an if - 
if n is true, n greater than zero is true, it runs this code. Now this is a little sequential bit. When you're done with this, what do you do? Oh, we just fall onto the next one. And you'll notice that this is indented at 
the same level as the print statement. And that's how we have repeating or even ifs 
with more than one statement in it. And then when it de-indents, that's the end of the loop. And what happens is it runs this and it runs that, but then what does it do? Well, it's at the end of the loop, so it actually goes back up to the top of the loop. So it goes back up to the while statement. And we actually printed n out, which was 5. And then n became 4 and then it reevaluates 
this question - is 4 greater than zero? 
So n becomes - is not greater than zero. So this switches from a true to a false. And false, it leaves - goes out and exits the loop. So over here, it goes 5, 4, 3, 2, 1 - and then out she comes. Okay? And as soon as this becomes false, then this loop exits. And so that's the way we tell a program that - you know, we tell the computer that we want it to keep going 
until something has happened. Some - we have achieved something. So loops have this notion of iteration variables to make sure that they are not infinite loops. And this variable n is carefully constructed to start and be checked and then be changed each time through the loop. And that's how we make sure this loop only runs 
five times and not forever. Because you can construct what we call infinite loops that run forever, but it's not too practical; you just run out of battery or whatever after awhile.

Now the for is another of the reserved words that a loop - so this has a colon and it says that's an indented block and there turns out to be a for within a for. This is called nesting. We'll get to that. And then this loop ends and it runs for awhile. And then there's more sequential stuff. There is a for, which is repeated code. And then there's an if nested within that for; that's conditional code. 

Because both conditional and loops require indentation, sequential code is easyly identifyed by not being indented in Python.

## Store and retrive 
And then the fourth pattern is the store and retrieve pattern.


# Functions

A function is a piece of reusable code aimed at solving a particular task. For example, the function type() can be used to return the type of a variable. instead of writting the code everytime, functions can be called. THIS IS GOOD BECAUSE I SHOULD HAVE  DISCUSSED WHY REUSING CODE IS GOOD. Functions work like a black box where inputs are given the ouputs are generated without haveing to think about the computational steps involved, which makes the code easier to understand and cleaner.

Calling a function requires calling the function name and passing the  the required arguments (inputs) within brackets. 
any returned value (output) can be assigned durring the function call `output = function_name(input)`

There are a huge number of functions that can be used. The easiest way to find a function for a specific purpose it to use tin internet, including simply googling it, searching stackoverfolw AND OTHER STUFF. To consult the documentation of a function in Python (interactively), the function `help(function_name)` can be used.

DEFINE ARGUMENT AND PARAMETERS

## Built-in functions

FROM NOW ON COMPLETE FUNCTION NAMES WITH THE ARGUMENTS AS SHOWN IN DOCUMENTATION
A number of functions are already built-in with any distribution of Python. A number of these function were already used! including print() and type() and the functions that to switch between data types str(), int(), bool() and float().
Other important functions include `round(number[, ndigits]) #Round a number to a given precision in decimal digits` 
and `complex(real[, imag])# Create a complex number from a real part and an optional imaginary part`. Notice how some functions are defined with arguments within square brackets. This indicates an optional value, which does not need to be defined. Onother way of representing optional values is to assign a default value to a fucntion parameter `sorted(iterable, key=None, reverse=False)# Return a new list containing all items from the iterable in ascending order`.  Also note that named parameters can be called as named arguments, instead of positional arguments
``` 
# Declare lists first and second
first = [11.25, 18.0, 20.0]
second = [10.75, 9.50]

# Paste together first and second: full
full = first + second

# Sort full in descending order: full_sorted
full_sorted = sorted(full, reverse = True)

# Print out full_sorted
print(full_sorted)
```
EXAMPLE OF DIFFERENCE BETWEEN POSITIONAL AND NAMED ARGUMENTS


Some function may accept different types of arguments, such as `max(iterable, *[, default=obj, key=func])` or `max(arg1, arg2, *args, *[, key=func])# Return the biggest item of an iterable or the largest argument of all provided arguments`, were it will return the maximun value of any iterable obkect (like lists) or the maximun amomgt all the provided arguments. The **\*** is used to represent a any number of arguments.


LIST MORE AND ADD A LINK TO THE PYTHON PAGE.

## Methods

A number of basic operations such as getting the index of sa sepecific  element in a list of reversing a list. These operations are included in Python but are not built-in functions. It is important ot note that all data structures in Python are objects and that each object has a object type in Python. Besides values, object can also have associated functions, which are called methods. Unlike functions, the call for a method is associated with the data structure with the **. notation** `variable.method(arguments)`, where the method *belongs* to the object. Again, `help(object_type)` contains more documentation on available methods. 

```
# String methods
room = "poolhouse"
print(room.upper()) # Capitalize all letters in string
print(room.capitalize()) # Capitalize the string (first letter only)
room.replace('oo', 'OO') # replace matching substring
```

Methods are specific for the object type they are associated with. A method defined for one object type, may not be defined for another object type such as the string method replace, which cannot be applied to lists. Also, objects of different types, can have methods with the same names, like index, wich can be used with lists and string objetcs, but will have different bahaviours on different object types (just as the + operator before!). 

```
room = "poolhouse"
print(type(room))
print(room.count('o')) # Count the number of occurences a given substring in a string
print(room.index('o')) # Get the index matching the substring 

areas = [11.25, 18.0, 20.0, 10.75, 9.50]
print(type(areas))
print(areas.count(14.5)) # Get the number of times an element appears in a list.
print(areas.index(20.0)) # Get the index of the first element of a list that matches its input
```


Additionally, some methods change the object theya re called on *"in place"*, that is, they do not return a value (generare output) but instead change an existing variable directly,
```
#List methods (change object)
areas.append(24.5) # Adds an element to the list it is called on.
areas.append(18.0) # Removes the first element of a list that matches the input.
areas.reverse() # Reverses the order of the elements in the list it is called on.
print(areas)

```

# Packages

Functions and methods allows for code to be easily transfered and reused. However, adding all functions that may be required to the same Python distribution would mean that most of the code would not be used by most users and it would make the maintenance aof the codebase a huge task. In order to avoid such a messy code, Python uses packages. Packages are, in essence, directories of Python scripts, with each scripts being called a **module**. Eahc module speficies functions, methods and new object types  all  all associated with a particular problem. Whidely used packages include Numpy for efficient work wiyth arrays, matplotlib, for data visualization and scikit-learn for machine learning. 

## Installing packages

As Packages are not included in the basic Python distributions, they have to be installed. Package installation is performed by pip, a package maintenance system for python. To install pip, download [get-pip.py](http://pip.readthedocs.org/en/stable/installing) and run the script from the terminal `python3 get-pip.py`. Once pip is installed, packages can be installed with `pip3 install package_name`. Now that the package is installed, it can be used in any python script. 

## Importing package

However, it is still required that the packages are imported by Python (otherwise it doesn't know it has to use it). There are various ways to import a package into Python. The simplest way is to include the line `import package_name` at the top of the script. With the package imported, every function, method or object from that package can be used, but not directly. Python need to know that the function called belongs to an external package so it can find it. This can be done with the **. notation** as for methods. In this case, the function *belongs to* the package.

```
import numpy

array([1,2,3]) # NameError
numpy.array([1,2,3]) # Array is defined on the numpy workspace (is it a workspace here?)
```
Other methods for importing packages include the option refer to the package with a different name, simplifying the function call.
```
import numpy as np
np.array([1,2,3]
```
Sometimes only a small number of functions from a package are required. This can be explecitely especified in Python. If imported in such manner, there is no need to specify the package of origin when calling the function. This can be usefull to limit the amount of coding, but the context of the functions is also lost which, for long scripts, may make the code less readable. .
```
from numpy import array
array([1,2,3]

from numpy import * # import everything
```
Examples of other packages:
```
# Import the math package
import math
# Definition of radius
r = 0.43
# Calculate circunference C
C = 2 * math.pi * r
# Calculate area A
A = math.pi * r**2
# Convert degrees to radians
math.radians(12)

# Import the function inv(), which is in the linalg subpackage of the scipy package.  
from scipy.linalg import inv as my_inv
```

# NumPy

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


