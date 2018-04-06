# Introduction to Python

## Why Python?

Python was conceived by Guid Van Rosson. What started as an hobby project, soon became a general purpose programming language. 
Nowadays, Python can be used to buold practically any piece of software. This happaned because Python is open Source and Free! 
Also, it is very easy to build packages in Python. Thougout time, more and more of these packages were specifically build for data science.
Currently, there are two versions of Python, 2.X and 3.X. They are pretty similar appart from some syntactical differences, 
but support for version 2 will fade overtime. Python 3 can be installed from [python.org](https://www.python.org/downloads)

## Install/Start Python


## The Python Interface

Python can be run interactively from the python shell by simply typing commands and hitting *Enter*. 
Open python and run `print("Hello World")`

Apart from interactively, Python can also be run from python scripts, which are simply text files with the extention .py, where a list of python commands are written and from where they are executed.
Putting the code in Pyton scrips instead of manually typing it ineratively 
will help to keep structure ansd avoid retyping everything if one change is required


## Comments

Before starting, it is important to be aware that **Comments** are important to any programming language. 
Comments are used to make sure that the code is understandandable and transmissable, improving reproductibility and, very importantly, debugging!
To add comments to a Python script,use the **#** tag. These comments are not run as Python code, 
so they will not influence your result. As an example, take the comment on the right, 
```
# Just greeting the whole world  
print("Hello World")
```
where *Just testing division* is completely ignored during execution, but makes the propose of the following code clear to anyone. Note the use of the function **print()**. This function DOES SOMETIME I NEED TO DESCRIBE :)

## Python as a calculator
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


## Variables

Fundamental to any programming languase is the concept of **variable**, which is a *"storage"* for values.
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


## Basic types

Every object in Python has a type.
The type of any variable can be checked usint the **type()** function.
So far, most of the examples have used either numbers or text.
There are two types of numbers in Python, **integers (int)** and **floats (float)**. Text values 
are know as **strings (str)** in Python, There are also logical values know as **booleans (bool)**

should comment on why there are integers and floats and their representation at some point...
```
# Integer: Number without a fractional (decimal) part
print(type(5))
# Float: Number with both an integer and a fractional (decimal) separated by a point
print(type(5.0))
# String: Represents text values. Can be defined within using either double ("") or single ('') quotes
print(type("Hello again"))
print(type('Hello again'))
# Boolean: Represents logical values (True or False). Numerically, these values can be converted to 0 for False and 1 for True
print(type(True))
print(type(False))
```
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

Can Python handle everything?

Now that you know something more about combining different sources of information, have a look at the four Python expressions below. Which one of these will throw an error? You can always copy and paste this code in the IPython Shell to find out!


print("I started with $" + savings + " and now have $" + result + ". Awesome!")
"I can add integers, like " + str(5) + " to strings."
press 1
"I said " + ("Hey " * 2) + "Hey!"
press 2
"The correct answer to this multiple choice exercise is answer number " + 2
press 3
True + False
