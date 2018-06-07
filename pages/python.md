# Introduction to Python

One of the first steps to become a Data Scientists is to become a programmer. A Data Scientist needs to use computational tools efficiently, writing code that intereact with the data. 


Python is one of the most common programming tools used for Data Analysis.

## History

Part of being literate in a programming language is knowing a bit about its history and culture.
An overview of [Python history](https://en.wikipedia.org/wiki/Python_%28programming_language%29)

Python was conceived by Guido Van Rosson, a Dutch programmer, in the late 1980's. In the 80s, when Python started, most programming languages were very serious and very complex. They were difficult to figure out and required a lot of math. Guido thought he could probably write a programming language that wouldn't be that hard, would be enjoyable to use, but woould also be both powerful. Python's version 1.0 was released in 1994. What started as an hobby project, soon became a general purpose programming language. Even though Python is associated with the snake motif, it turns out that Python was not named after a snake. Instead, it was in honer of the [Monty Python's Flying Circus](https://www.youtube.com/watch?v=iV2ViNJFZC8) commedy. 
It was meant to be fun to use, thus the name. It turns out that's why Python is such a perfect language to use as a first programming language: it's designed to be easy but it's also powerful.  The Python community continues these values of irreverence and lightheartedness over stuffy formalism. For instance, the Zen of Python, a poem including guiding Python development principles, is built into the Python interpreter:
```
# Click the "play" button above and see the output on the right.
import this
``` 
The Zen of Python, by Tim Peters

Beautiful is better than ugly.  
Explicit is better than implicit.  
Simple is better than complex.  
Complex is better than complicated.  
Flat is better than nested.  
Sparse is better than dense.  
Readability counts.  
Special cases aren't special enough to break the rules.  
Although practicality beats purity.  
Errors should never pass silently.  
Unless explicitly silenced.  
In the face of ambiguity, refuse the temptation to guess.  
There should be one-- and preferably only one --obvious way to do it.  
Although that way may not be obvious at first unless you're Dutch.  
Now is better than never.  
Although never is often better than *right* now.  
If the implementation is hard to explain, it's a bad idea.  
If the implementation is easy to explain, it may be a good idea.  
Namespaces are one honking great idea -- let's do more of those!

## Why Python?
Nowadays, Python can be used to build practically any piece of software. This happaned because Python is open Source and Free! 
Also, it is very easy to build packages in Python. Thougout time, more and more of these packages were specifically build for data science.

Python is one of many programming languages. It's popular in part because of its clear, English-like syntax and because of the enormous ecosystem of open source Python tools for almost any aspect of scientific computing. Simply stated, Python is currently [eating other languages' lunch](http://www.talyarkoni.org/blog/2013/11/18/the-homogenization-of-scientific-computing-or-why-python-is-steadily-eating-other-languages-lunch/).

Welcome to being a Pythonista.

## Python Enhancement Proposal

The Zen of Python, poem comes from [PEP 20](https://www.python.org/dev/peps/pep-0020/). The "PEP", or "Python Enhancement Proposal", process is how the Python language continues to be developed. Tbout that process his process is described in 
[PEP 1](https://www.python.org/dev/peps/pep-0001/). Another good PEP to be aware of is 
[PEP 8](https://www.python.org/dev/peps/pep-0008/), the definitive style guide for Python that describes stylistic conventions adopted by the community. In addition to the nine PEP Editors (including Chris Angelico) Guido retains final say over language development as "Benevolent Dictator For Life".

Each PEP as well as the [Python documentation](https://docs.python.org/3.5/library/) is hosted on python.org. For the last several years the Python development community has been moving over from Python 2 to Python 3. There's still a lot of Python 2 in production so it's good to be aware that it's around. As such, there are two versions of Python, [2.7](https://docs.python.org/2.7/library/) and 3.5. They are pretty similar appart from some syntactical differences, and support for version 2 will fade overtime. 

## Install/Start Python
Python 3 can be installed from [python.org](https://www.python.org/downloads)

#### Installing Python 3 on a Mac.
If you have a mac you almost certainly have Python 2 pre-installed on your machine. You can check your version of Python by opening your terminal and running the command `$ python --version`


In adidtion, there a number of Python distibutions that may be relevant, like the Anaconda distribution, which includes many science and data analysis libraries. OTHERS ?

Once installed, Python files will be reconise by their extension *.py*. There are many ways to  to run Python. The pasic Python distribution already provides the IDLE Python Shell and other integrated development environments (IDE) such as Spyder (included with the Anaconda distribution) can be obtained. However, the basic way to use Python is by running the command line (see [command line](pages/bash.md) to learn how to use it). Python files can be run by entering `python3 file_name.py` (simply python for Python2). The Python will be run, if it is in the current directory, otherwise, it will not be found. On Windows, typing the file name on it's own will also run Python, as all files with .py are expected to be Python and it knows the Python interpreter where to run. . To check the Python version, enter `python3 --version`.

Besides Python itself, it is important to have a text editor. The classical text editors come with the operating systems, like Word or Text Edit will not do for more complex programming. Editors with syntax highlight, automatic identing and other useful options can make programming a much simplers exerience. There are a number of editors that cn be used, including Notepad Plus, jEdit, Atom, TextWrangler or Sublime.

## The Python Interface

Python can be run interactively by entering `python3` on the command line. This opens the Python shell which has a chevron (>>>) prompt, where commands can be entered (not that IDEs may have the shell inbedded already). Typing `print("Hello World")`) 
in the prompt and then *Enter* will run the Python command. To exit the Pythom promp, type `exit()` or `quit()`. So a series of statements can be typed in Python and processed interactively and it is possible to write entire programs interactively. However, this would require that it is typed perfectly from beginning to end. Once a program gets beyond a couple of lines of Python, it's much more common use a programming text editor and put all the code in a file. We call this a script or a Python program. Scripts are stored sets of instruction in text files that Python can run. Python scripts are identified by having an extention *.py*. Putting the code in Pyton scrips instead of manually typing it ineratively helps to keep structure ansd avoid retyping everything if one change is required


## Syntax
A big part of any programming language is the syntax.

## Comments

Before starting, it is important to be aware that **Comments** are important to any programming language. 
Comments are used to make sure that the code is understandandable and transmissable, improving reproductibility and, very importantly, debugging!
To add comments to a Python script,use the pound (**#**) sign. Any code after # will be ignored by Python, 
so it is a good way to add human-readable information to document the code. Comments are used to:

  * Describe particular parts of the code, introducing it and what it is expected to do.
  * Document who wrote the code, when it was written, the code version or any other ancilliary information
  * Turn off lines of code, for example, resuable debbuging code that is only temporarily needed.
 
Documenting the code properly is extremely important. Overtime, the details of the code will be forgotten and documented code will help figuring out the code. This will help understand, sharing, debbuging and up-dating the code after it has been written. As such, comments are used for future use. 

```
# Just greeting the whole world  
print("Hello World")
```
*Just greeting the whole world* is completely ignored during execution, but makes the propose of the following code clear to anyone. Note the use of the function **print()**. This function DOES SOMETIME I NEED TO DESCRIBE :)
The print function can be used with multiple values separated by commas, but every comma adds a space between the different values. This is the most common requirement however, if spaces are not required between the values, they need to be concatenated with +.

```
# Playing with print
print("Hello", "World")
print("Hello" + "World")
```

### Contants
Constants are fixed values that don't change their values, and thus are constant for all the program. There are different types of 
constants, which are related to basic object types ([see later](#Basic types)) 
such as numeric (integer and float) and text (string) constants.

**are these constants or literals?**

### Operators 
All programming languages have various operators. These operators historically come
from the kind of characters that were on computers keyboards in the 1960s, literally. 
These things called Teletypes, from the end of World War II, had key punches or rudimentary terminals 
with a certain set of characters which just couldn't represent the mathematical ccharacters. 
So these had to be mappped mathematical formulas and functions: 

  * Sum maps to +
  * Subtraction maps to -
  * Multiplication maps to *
  * Exponentiation maps to **
  * Division maps to /
  * Modulo maps to %



### Variables

Fundamental to any programming languase is the concept of **variable**, which is a named *"storage"* for values in the memory.
A Python variable is declared (created) with a specific, case-sensitive name. Variable declaration allocates a value to a bit of memory and "labels" it with a name. Once assigned to the memory, the computer can "remember" the value and Python retrive it by using a calling a variable that *points* to the stored value. This takes advantage of the great memory capacity of computers to simplifying the code and make it more reproducible and readable. As such, variables are used all the time in Python. 

There are two distinct moments when working with variables in Python: assigning a value to a variable, and retrieving the value from a variable. To declare a variable, the assignment operator **=** can be used to assigned the value on the right to the variable on the left. Note that, even though programming logic is rooting on mathmatics, programming notation may not strictly match mathematical notation. The assignment statement do not mean equality.  Once declared, a variable name can be used instead of the value. This is fundamental when working with complex objects. To access the value in a variable, you simply refer to the variable in your code. 

```
# Declaring variables
x = 5
my_name = "Guido van Rossum"

# Retrieving variables
print(x)
print("Hello world, my name is " + my_name + ".")


```
It's important to note that the = operator is assigning a value to a variable, not asserting that two different values are equal. When you see the = character in mathematical statements it's an "equals sign", and means that the value on both sides are equal. For example: 2 + 2 = 4 is a perfectly reasonable mathematical statement. But that's not how = works in Python. 

Variables open up two possibilities for programmers: 

  1. Provide a shorthand way to refer to values created elsewhere in a program. Once declared and defined, a variable can be used to passe a value around without having to rewrite the value each time.

```
# This URL is long. Let's write it just once and store it in a
# variable to use later.
base_url = "thinkful-students.slack.com/messages/"

# We're going to use newlines ("\n") to format things nicely.
empty_line = "\n"

print("The Thinkful Slack community is a great place to get help or share your work.")
print(empty_line)

print("#general-discussion is where everyone can chat about whatever they like")
print("You can get there by going to:")

# Now we're going to start using our `base_url` variable multiple
# times.
print(base_url + "general-discussion")
print(empty_line)

print("Data science specific conversation is good for #data-science, at:")
print(base_url + 'data-science')
print(empty_line)

print("There's also a #careers channel dedicated to job-hunting:")
print(base_url + "careers")
print(empty_line)

print("Be sure to find your mentor on Slack and introduce yourself to the community.")

# Be sure to click the "run" button at the top of this trinket if
# you haven't yet.
```
  2. Provide a way to manage the state in a program. The state is the abstract representation of values, wich may persiste or be modified values over time. Each set of values at a specific time (part of the code) defines a program a *state*.

```
# Ask the user for input and store the result in a variable.
bottle_count = int(input("How many bottles of beer are on the wall?"))

print("There are {} bottles of beer on the wall.".format(bottle_count))

if input("Would you like to take any down?") == "yes":
    removed_bottles = int(input("Ok, how many?"))
    bottle_count = bottle_count - removed_bottles
    print("There are now {} bottles on the wall".format(bottle_count))
else:
    print("Ok, there are still {} bottles on the wall.".format(bottle_count))

# Click "Run" above to run this program. If you break it just click
# "Run" again or choose "Reset" from the menu at the top left.
```

#### Naming rules

The names choosen for variables are important. There are some syntax **naming rules** for variables that must be followed in order for the Python interpreter to recognize them as variables. Python will only accept variable 
names: 

  * Starting with a letter or an underscores
  * Comtaining only a combination of letters, numbers, and underscores. 
  * Not a reversed word

```
# Valid variables
name = "Guido"
favorite_painter = "Mondrian"
__password__ = "hunter7"
job1 = "Programmer"
job2 = "Benevolent Dictator"

# Variable name doesn't start with a letter or underscore:
1st_name = "Guido"

# Variable name includes a disallowed character: `-`:
my-password = "hunter2"

# Variable names can't be keywords like `else`:
else = 1
```

In addition, variable names are case sensitive, so variables python; Python and PyThOn are all different.
```
#Case sensitive naming 
python = 'Snake'
Python = 'Language'
PyThOn = 3
python = 'Snake 2'

print(python)
print(Python)
print(PyThOn)
```

Simply ensuring that variable names are valid, leads to a number of confunsing possibilities, such 
as *PyThOn*. As such, there are stylistic conventions about how variables should be named which 
are taken as the standard *good practice* nomenclature. These best practices should be followed,  
not because the code would otherwise break, but because it will make the code look more familiar to 
other *Pythonistas*, thus clearer, more understandable and easier to maintain. 
[PEP 8](https://www.python.org/dev/peps/pep-0008/) contains most of the relevant Python style recommendations.
  
  * Python developers generally use lower_case_with_underscores ("snake case") for variable names. 
  A Python variable name should have lower case letter throughout with words separated by an underscore _ character. 
  * Upper case is used to signal specific types of varibles, in particular ALLCAPS for [constants](https://www.python.org/dev/peps/pep-0008/#constants). 
  * CamelCase, which uses a mixture of cases, with upper case being used to separate words in the variabe name, 
  instead of underscores, can be used for [classes](https://www.python.org/dev/peps/pep-0008/#class-names)
  * Avoid starting variable names with underscores. These variables are reserved for specific uses, particular for Python (*e.g.*  methods) internal purposes.
  * Above all, use distinct, mnemoric, non-redundant names. Even though Python doesn't care (or interpret) what name is given to a variable, using sensible human-readable names that describe the underlying value and reflect how the variable gets used
will improve code readability and thus, code debugging and code sharing and review. Variable naming is not intended to communicate any additional information to Python, but it is fundamental to clealy communicate the purpose of the code to a reader. Generally, names should be reader-friendly and communitate their purpose. A well chosen variable name can help other people reading the code to understand how the variable is intended to be used. For example, full words are generally better than single characters or abbreviations.

```
# Not valid names (syntax error)
1one = 1
number.one = 1
# Valid names
_x5yY8w = 5
# Good names
number_five = 5
n_five = 5
NumberFive = 5

# Bad:
p = 0
n = "Guido van Rossum"
b_btls = 99
# Good:
position = 0
name = "Guido van Rossum"
beer_bottles = 99
```

Naming variables is [more of an art than a science](https://medium.com/@drb/pep-8-beautiful-code-and-the-tyranny-of-guidelines-f96499f5ac17), but as a general rule of thumb, the more the code reads like an English sentence the better chosen are the variable names.

Variable assignment follows two steps:

  1. Evalute the expression on the right side to a value
  2. Store the value to the memory and create a pointer to that value

This means that it's possible to have the same variable on both sides of the assignment.  
The variable on the expression is evaluated and then its value is replaced (name points to a different value).
Again, note that this can lead to mathematically incorrect expressions, that are programmatically common place.

```
n = 2
print(number)
# Overwritting a variable value
n = 5
print(number)
# Incrementing a number (same operation)
n = n + 1
n += n
print(n)
# n = n + 1 is not an equality (and is mathematically non-sense)
```


### Reserved words

Reserved words are a special category of words that you're not allowed to use as variable names in a given programming language. For instance, in Python, you can't reassign the name True or the word def to a new value. See the documentation for the full list of [33 reserved words](https://docs.python.org/3.5/reference/lexical_analysis.html#keywords).


Every programming language has specific group of words that are associate with a specific meaning and are expected to have a sepecific function. These are know as reserved words and shouldn't be used for anything else but their original purpose. As such, reversed words can not and should not be used to name variables! There are a number of reserved words in Python that are important to know. As they are fundamental building blocks of the Python syntax they can be introduced as required.

Reserved words in Python include:

 | Col | Col | Col | Col |
 | --- | --- | --- | --- |
 | False | True | None | and | 
 | as | assert | break | class |
 | if | def | del | elif |
 | else | except | return | for |
 | from | global | try | import |
 | in | is | lambda | while |
 | not | or | pass | raise |
 | finally | continue | nonlocal | with | 
 | yield |  |  | 

### Sentences 

Now we lead these things into 
sentences or lines. And so these things. This is just another sequence of code, and it shows how you can also use
the variable on the right-hand side. 


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

### Syntax error 

At the begining, Python may seem to be difficult and it is very common to get a Syntax Error thrown back when running a script.
Even tought it may be demotivating at first, it is important to keep in mind that *Syntax error* means Python is lost, it does not reconise an instruction. When Python finds (*throws*) an error, the program stops and an error messages is displayed. 
This message tries to explain the problem and identify where (code and line) and why (error type) it occurs.


# Basic types

Variables can represent different types of values. For example, words and numbers are different types of data. A variable could refer to the number 42 or it could refer to the words "forty two". You can do math with the first one, but trying to subtract 5 from "forty two" in Python isn't going to fly.
Every object in Python has a type.
The type of any variable can be checked usint the **type()** function.

Python has many built-in data types, including "strings", "numbers" (including integers and floats)", "booleans", 
and "None". 

## Numbers


So far, most of the examples have used either numbers or text.
In Python there are two primary data types for representing numbersn, **integers (int)** and **floating point numbers (float)**. 
Whole numbers that aren't written as a fraction or with a decimal point are integers. 
On the other hand, numbers that do have decimal places (represent decimal fractions)  are floating point numbers.

The main diference between these number representation is their internal representation. 
Python 3 can represent integers up to any size. here is no maximum integer size: Python 3 can handle integers that are arbitrarily large (unlike many other languages). Floats, however, are limited on how precisely they can be represented. Floats in Python are "double precision" binary floating-point numbers that will represent decimal fractions as precisely as possible with the [52 bits](https://en.wikipedia.org/wiki/Double-precision_floating-point_format#IEEE_754_double-precision_binary_floating-point_format:_binary64). 

Floats in computer science are a fun topic.
Floating point numbers have a greater range than integer numbers, but they're not always as
precise as integer numbers. This is because computers represent everything internally in binary, and since it's impossible to precisely represent many decimal fractions in binary, it's easy to end up with 
[floating point issues](https://docs.python.org/3.5/tutorial/floatingpoint.html). 
That said, doing arithmetic with floats is asking for trouble. This imprecision makes math a bad idea when you need precise comparisons
For example, to represent money (or quantities that have to be precise) only integers should be used, has binary representation has dificulties representing decimals and will result in errors for large calculations. 
Even if you don't need complete precision floating point errors can quickly compound with one another, so be careful when using floats and know that they have significant limitations.
```
# Floating points representation is less precise
print(1.03-0.42)
print(103-42)
print(.2 + .4)
# 0.6000000000000001
>>> 0.2 + 0.4 == 0.6
False
```

```
# Integer: Number without a fractional (decimal) part
print(type(5))
# Float: Number with both an integer and a fractional (decimal) separated by a point. A Real  number
print(type(5.0))
```
```
# We can use Python as a calculator to do arithmetic. Let's do
# some simple math with numbers and assign the results to
# variables.
four_plus_two = 4 + 2
nine_minus_three = 9 - 3
three_times_four = 3 * 4

# You have two types of division: "true division" and
# "floor division"
true_division = 5 / 2
floor_division = 5 // 2

# The modulo operator `%` in action to get a remainder.
remainder = 5 % 2

# One way to do exponentiation is with the `**` operator.
five_squared = 5 ** 2
twenty_seven = 3 ** 3

# You can use the built-in `type()` function to see what kind of
# data you're dealing with. This is useful when you aren't sure
# whether you have an int or a float.
answer = 40 + 2
print(type(answer))

score = 6 / 2
print(type(score))

# Take a few minutes to add print statements throughout to see
# what values are being assigned to the variables above, then
# tinker with the numbers to see what happens.
```

### Arithmetic operators
Unlike strings, you can do math with numbers!
```
# Start by assigning some numbers to our variables.
count = 3
pi = 3.14

# Let's see what the built-in `type()`function does.
type_of_count = type(count)
type_of_pi = type(pi)
print(type_of_count)
print(type_of_pi)

# We can do math with numbers. The `%` operator is modulo.
print(count + 2)
print(count * 10 )
print(count / 2)
print(1337 % 2)

# Putting an int and a float together will give you a float.
print(count * pi)

# Be careful with floating point math.
print(.2 + .4)

# Numbers are *not* strings, even if they look similar.
print(10 == "10")

# Thankfully it's easy to convert numbers to strings when you
# need to:

print("Bring me " + str(count) + " shrubberies!")
```

One of the most basic used of Python is to do basic calculations. Apart from **addition (+)**, **subtraction(-)**, 
**multiplication(\*)** and **(true) division(/)**, there is also support for more advanced operations such as 
**exponentiation (\*\*)**, **modulo/modulus (remainder) (%)** and **integer (floor) division (//)**.  Like for mathematics, These opperators have
an order of evaluation.
Operations can be grouped, as in Algebra, with parentheses, where parentheses override all other operations, 
follwed by exponentiation,
multiplication and division/modulo and addition and subtraction for last. For similar priority operations, 
they are evaluated from left to right. 

Python handles order of operations, or [operator precedence](https://docs.python.org/3.5/reference/expressions.html#operator-precedence), via PEMDAS: parentheses, exponents, multiplication/division, addition/subtraction.

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
#precedence
print(6 / 2 * (1 + 2))
```

Integer division is actually one of the biggest non-upwards-compatible changes between Python 2 and Python 3. In Python 3 
**/** can result in a floating point. To force an integer division, **//** has to be used.

```
#examples of divisions

```

The modulo (remainder) operator is something that's not typically on calculators, but it's really important for computers. 
The modulo is the remainder of the integer division instead of giving the quotient. This is particularly usefull for cicling between a numeric range, such as cards (n % 52) or dice (n % 6), because the resulting remainder will reset to 0 as soon as tha multiple of the divisor is found. It is also a fundamnetal operator for testing an odd number
an even number (n %2) as even number do not have a remained when divided by 2 and odd number have a remainder of 1.

```
# example of modulos
```

### Assignment operators

It's very common to perform arithmetic with numbers assigned to variables and to then want to store the result back in the variable. One way to accomplish that is to use the syntax where we assign a new value to the variable based on a statement including current value of that variable. That might seem weird if you're coming from a math background. For instance, a math formula saying `x = x + 1` is just nonsense. So why does it work in programming? Because the = operator here is assigning a value to a variable, not comparing one value to another, as = does in math formulas. Reassigning values like this is incredibly common, so Python gives us compound assignment operators that will perform an operation and assign the result back to the variable all at once. Here are the assignment operators:

  * = add and assign
  * -= subtract and assign
  * *= multiply and assign
  * /= "true" divide and assign
  * //= "floor" divide and assign
  * %= modulo and assign
  * \*\*= exponentiate and assign

Unlike many other languages, Python does not have prefix and postfix operators like ++ and --. The more "Pythonic" way to increment and decrement numbers is to use the += and -= assignment operators.
```
# Let's demo different ways to work with numbers and assign the
# results back to a variable. here are some numbers to start with.
score = 99
hit_points = 99
level = 2

# These two methods are equivalent. They both increase the value
# assigned to the variable by one.
score = score + 1
hit_points += 1

# Jackpot! Triple our score.
score *= 3

# Oof, got hit for twenty damage.
hit_points -= 20

# Advance a level.
level += 1

# Think about what the values assigned above should be and insert
# print statements at different parts of the program to confirm
# your guesses.
```

### Comparing numbers

Numbers can be compared using the following comparison operators:

  * < less than
  * <= less than or equal to
  * > greater than
  * >= greater than or equal to
  * == equal
  * != not equal
  
The result of a comparison will be a boolean: True or False depending on how the comparison evaluates. Note that the == comparison operator works like the equals sign in math formulas like 2 + 2 = 4. That math formula is true, and the equivalent Python comparison 2 + 2 == 4 evaluates to True.
```
# Using comparson operators with numbers.
print(1 < 2)
print(1 <= 2)
print(2 <= 2)
print(3 <= 2)
print(1 == 1)
print(1 == 2)
print(1 != 2)
```

## Text
Textual data are known as **strings (str)** in Python. These data are defined by delineating quotes,either single or double quotes, as long as both the opening and the closing quote are the same kind.

Words, names, book chapters, emails, text files, all of these are textual data and can be represented by strings. 
As a programmer you'll frequently work with strings. Here are some common scenarios where you need to understand strings:

  * dealing with any textual data
  * handling and presenting output from your program
  * files like CSV's are basically one large string


```
# String: Represents text values. Can be defined within using either double ("") or single ('') quotes
print(type("Hello again"))
print(type('Hello again'))
# Boolean: Represents logical values (True or False). Numerically, these values can be converted to 0 for False and 1 for True
print(type(True))
print(type(False))
```

```
# Start by assigning a string to our variable.
food = "ham"

# Let's see what the built-in `type()`function does.
type_of_food = type(food)
print(type_of_food)

# We can access the characters of a string by index with bracket
# notation, starting at index zero.
first_letter = food[0]
second_letter = food[1]
print("The first letter is " + first_letter)
print("The second letter is " + second_letter)

# We can use the built-in `len()` function to get a string's
# "length", or the number of characters it contains.
print(len(food))

# We can concatenate two strings together into one string with
# the `+` operator.
superfood = food + " and eggs"
print("I like " + superfood)

# We can fill in strings using the `.format()` string method.
name = "Guido"
cost = 3
demand = "Bring me {} shrubberies, {}!"
print(demand.format(cost, name))
```

### What is a string?
A string is a sequence of characters. In Python, we can assign string values to variables by using either single or double quotes around our sequence of characters. Either single or double quotes are fine. The key is that the outermost quote delimiters must both be either single or double.

```
>>> spam = "Spam!"
>>> eggs = 'Eggs!'
>>> print(spam)
'Spam!'
>>> print(eggs)
'Eggs!'
```
You can also use triple quotes ''' to create big multi-line strings:
```
book_of_armaments = '''
And the Lord spake, saying, "First shalt thou take out the Holy Pin.
Then shalt thou count to three, no more, no less.
Three shall be the number thou shalt count, and the number of the counting shall be three.
Four shalt thou not count, neither count thou two, excepting that thou then proceed to three.
Five is right out.
'''
```
Strings are used to represent text. Python 3 handles strings much better than Python 2, which is one of Python 3's great strengths. Python should be able to handle just about any Unicode that you throw at it, so strings like "passé" and "schöne" and "ねこ" are all fair game.
```
Strings are used to represent text. Python 3 handles strings much better than Python 2, which is one of Python 3's great strengths. Python should be able to handle just about any Unicode that you throw at it, so strings like "passé" and "schöne" and "ねこ" are all fair game.
```

### Special Characters and Escaping

Some characters can be tricky to use. Let's say you want to use the " character inside of a string. Maybe you want to use double quotes to represent a quotation. One way to do that is to wrap your string in single quotes ', but what if that isn't an option? Or what if your string also includes an apostrophe?

This is a case where we need to use a \ backslash in order to escape a character. In other contexts, the backslash is used to indicate special characters, such as a line break (\n) or a tab (\t) character. For instance, 'name:\tJohn' would give us a string with "name:" and "John" separated by a tab.

```
# Internal quotation marks can really mess up your strings if you
# don't escape them with a backslash.

line = "He said, \"Sure, let's rock!\"";
print(line)

# You can also escape special characters like \n for newline
# and \t for tab.
employees = 'FIRST\tLAST\njohn\tcleese\neric\tidle'
print(employees)
```

### Concatenating and Repeating Strings

Python lets us use the + operator to concatenate — which just means "connect" — two strings into a bigger one.

You can also use the * operator to repeat a string.
```
# Use the `+` operator to concatenate.
beginning = 'The quick brown fox '
end = 'jumps over the lazy dog.'
full_sentence = beginning + end
print(full_sentence)

# Use the `*` operator to repeat.
print('Na' * 16 + " Batman!")

# Remember that strings aren't numbers, even when they may look like
# numbers, so trying to do math with them won't work the way you
# expect.
print("12" + "3")
print("100" * 2)
```
### Indexes and Slicing

Each character of a string has an index, starting at 0 for the first character. You can access each character in a string by index using bracket notation. You can also access larger chunks of a string using slicing. While using a single index will give you a single character, using two indexes separated by a colon : will give you a substring. The character at the start index is always included in the substring you get back, and the character at the end index is always excluded.
When slicing strings you can omit one of the indexes and Python will assume you want to start from the beginning or go all the way to the end, depending on which index you omit. You can also use negative numbers as indexes. When using negative numbers you start counting from the end, beginning with -1 as the last character in a string.

```
>>> 'Hello'[0]
'H'
>>> 'Hello'[4]
'o'
>>>'Monty Python'[0:5]
'Monty'
>>> 'Monty Python'[6:8]
'Py'
>>> 'Monty Python'[:5]
"Monty"
>>> 'Monty Python'[6:]
"Python"
>>>'Monty Python'[-1]
'n'
>>> 'Monty Python'[-3]
'h'
```

### Comparing Strings

You can use the == operator to compare two strings to see if they're identical. 


```
>>> food = 'eggs';
>>> breakfast = 'eggs';
>>> lunch = 'spam';

>>> food == breakfast
True
>>> breakfast == lunch
False
```


### String methods

All strings in Python share a number of [built-in methods](https://docs.python.org/3.5/library/stdtypes.html#string-methods). 
 Methods are called by following the string with a . , then the name of the method, and then parentheses ( ) surrounding arguments, if any, that you're passing in to the method. 
 
```
# Return a new string with a capitalized first character.
'hello'.capitalize()

# As you read through these make a guess about what the result
# will be, then check your guess by `print()`ing each statement
# and running the code.
print('hello'.capitalize())

# Return a new string where all characters are lower case
'Hello'.lower()
'WORLD'.lower()

# Check whether all characters are numeric.
'1337'.isdecimal()
'p2p'.isdecimal()

# Check whether all characters are alpha.
'hello'.isalpha()
'p2p'.isalpha()

# Find the index of the first occurance of a substring. 
'hello'.find('l')
'world'.find('l')

# Check the end of a string.
'hello'.endswith('o')
'world'.endswith('o')
'world'.endswith('rld')

# Split a string into a list of strings at each instance of a
# substring.
'The-quick-brown-fox'.split('-')

# Join a list of strings into one single string. Try passing a
# different string into this method.
'_'.join(['The', 'quick', 'brown', 'fox'])

# "Format" a string by replacing `{}` with the arguments you
# supply to the function.
'Player {} has {} hit points remaining'.format(1, 42)
'My favorite drink is {} with {} dashes of {}'.format('whiskey', 3, 'bitters')

# Use the space below to play around with these methods and print
#different things out.
```

 
## Booleans

There are also logical values known as **booleans (bool)**
Booleans signify truth and falsity. A boolean has just two possible values: True and False.

```
# Here we're assigning the boolean `True` to the variable
# `logged_in`. Try running this code, then changing True to False
# to see how that changes the program. (Note the capital "F" and
# lack of quotation marks.)
# What happens if you change the value of `logged_in` to a number
# or string instead of a boolean True or False?
logged_in = True

username = "Guido"

# These are conditional statements. We'll cover these later, but
# you might be able to make out how they're working here.
if logged_in == True:
    print("Welcome " + username + ", loading launch codes.")
elif logged_in == False:
    print("Sorry, I can't load the launch codes unless you log in.")
else:
    print("Hey pal, no trying to hack the mainframe login.")
```
Booleans are used for application logic.
Logical assertions allow us to write conditional logic into our programs, 
can tell our code to carry out one set of instructions if our assertion is true, 
and another if it is false.

Actually should probably be in type convertion...
To explore how Python thinks about truth and falsity, we're going to use the built in bool() function, which is used to convert a value into either True or False.
```
# Basics.
print(bool(True))
print(bool(False))

# Numbers and strings evaluate to True.
print(bool(1))
print(bool(2))
print(bool(-1))
print(bool('Hello'))
print(bool('    '))

# Except for 0 and empty string ''.
print(bool(0))
print(bool(''))

# Collections evaluate to True.
print(bool([1, 2, 3]))
print(bool({'arms': 2, 'legs': 2, 'sword': None}))

# Except for empty collections.
print(bool([]))
print(bool({}))

# `None` acts as you might expect.
print(bool(None))
```
Anything that represents "something" is true. Anything that represents "nothing" is false:

  * False
  * None
  * 0
  * empty string ''
  * empty list []
  * empty dictionary {}

If you're working with anything else, it'll be true. That means that negative numbers, strings of whitespace, and objects (which we'll learn about later) all evaluate to True.

### Logical operators 
(potentially repeated with flow control)
Logical operators are used to make assertions about two or more statements or values. Let's start with and (logical and), which is used to assert whether or not two statements both evaluate to True. ython evaluates the expression on each side of the and operator. If both expressions evaluate to True it returns True. Well, kind of. When the expressions on both sides of and evaluate to True, the second expression is returned. A similar thing goes on in the background when one of the expressions evaluates to False.Your intuition with and statements will get you a long way. But under the hood this is what's going on:
The expression x and y first evaluates x. If 'x' is false, x is returned. Otherwise, y is evaluated and y is returned.

```
# Basics.
print(False and False)
print(False and True)
print(True and False)

# When an `and` expression evaluates to False, what are we
# actually returning?
print(True and 0)
print(None and True)
print({} and '')

# Can you guess what these values will be before you print them?
collection = [] and {}
number = 1 and (0 and 2)
```

The logical or operator is the complement to and. It tells us whether at least one of the expressions on either side of or evaluates to True.Just like and expressions, or expressions actually return one of the expressions on either side of or
Let's drill down on or. Let's imagine we have the expression x or y in Python. When this code is executed, first x's Boolean value will be evaluated. If x is "truthy", x will be returned. Otherwise, y's value will be returned (even if y evaluates to False).

```
# `or` expressions only need one side to be `True`, so if the
# first expression is true that's what is returned.
print(1 or 2)
print(1 or False)
print('Chocolate' or 'Vanilla')

# If the first expression evaluates to `False` then an `or`
# expression moves to the second expression and returns that,
# no matter whether the second value evaluates to `True` or
# 'False'.
print(False or "Phew!")
print(0 or 3)
print([] or "Hello")

print('' or 0)
print(0 or [])
print(None or {})

# Can you guess what's going on here before printing?
example = False or ("Hmm..." or None)
name = '' or {} or []
logged_in = name or 'Guido'
```
Finally, we have the logical not operator, which evaluates an expression and gives the boolean opposite.
Perhaps more intuitively, not always returns a boolean True or False.
```
# Here we use `not` to evaulate and return the boolean opposite of
# some expressions.
print(not True)
print(not False)
print(not "Hello!")
print(not 0)
print(not 1)
```
### Assigning default values with logical OR

Why all this complication? Wouldn't it be simpler if and and or simply returned a boolean?

```
# Let's define a function that allows for default behavior.
def greet(person):
    # Line 4 is where the magic happens.
    person = person or 'world'
    return "Hello " + person

# Can you guess what the values below are before printing them?
greeting_1 = greet('Guido')
greeting_2 = greet('')
greeting_3 = greet(None)
```
In the first line of the function body, we reassign the value of person using an or operator. If the function is called with a value like Guido which evaluates to True, then person gets the same value again. However, if the function is called with a value like empty string '' or None which evaluates to False, then the default value 'world' is assigned instead.

Discuss lazy evaluation and guardian pattern ?

## None
None type value representes the absence of a value.
Strings, numbers, and booleans are useful for representing actual things, but sometimes you want to represent nothing. That is, you want to represent the absence of any value. For that Python gives us None.

You could have a deep philosophical debate about when it's appropriate to use None instead of False or 0 or an empty string "" or so on. We won't have that debate here. Just know that None is around to use when you want to represent the lack of a value.

```
# Let's assign some variables to start with, including `None`
# in a couple places.
 
name = None
species = "Human"
strength = 4
magic = 5
favorite_color = "Octarine"
profession = None

# Hm, maybe we haven't assigned a name yet...
if name is None:
    name = input("What is your name?")
    print("Fantastic, thanks {}".format(name))

# Every adventurer needs a profession.
if profession is None:
    print("{}, you are a {} who needs a profession".format(name, species))
    print("Your strength is {} and magic is {},".format(strength, magic))
    print("and your favorite color is {}".format(favorite_color))
    profession = input("What profession would you like?")

print("Welcome, {}. You are a {} {}.".format(name, species, profession))

# Once you've run the program go back and tweak your starting
# variables. Does that change the program's behavior?

# As a stretch goal, try setting `favorite_color` to None and
# getting user input by copying the logic for `name` and
# `profession`.
```


## Convertion between types 

Python carefully tracks not only what the value in a variable is but what kind of a value it is. 
Variable types are very important in Python as different types can show different behaviour for the same operation, so it is important to be aware of what type each value is.



```
# Sum integers: + works as a mathematical operator 
print(2 + 5)
# Sum strings: + works not as a mathematical operator but as a text paste (concatenaotr) operator
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
Converting types can be very useful for combining different sources of information. For example, integers can be converted to str for reporting as string can be converted to floats to allow calculations on user inputs 
using the buil-in functions [str](https://docs.python.org/3.5/library/functions.html#func-str), [int](https://docs.python.org/3.5/library/functions.html#int) and [float](https://docs.python.org/3.5/library/functions.html#float)
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

### Type error
In Python, if you try to perform an operation that expects a number on a string you'll get an error. For example, if you try to subtract the string "10" from the number 42 you'll get an error.
```
>>> 42 - "10"
TypeError: unsupported operand type(s) for -: 'int' and 'str'1

>>> "Number of magic beans: " + 42
TypeError: Can't convert 'int' object to str implicitly
```
That TypeError is telling you that you're trying to use data of a particular type (a string) that the - operator doesn't support. 

TypeError is ...

So, this works pretty well unless
the string that in question has no digits. So, if there's no digits,
it's going to blow up, it's like, whoa. Now, let's read it. Traceback means, I quit. Where? Line 1, it's always line 1 because
we're in this interactive environment. 

Can't convert an int object
to string implicitly, but an int is implicitly converted to a float.

### User input 

Data read from *outside* of Python (from user input, a file, a network, a database) comes in as strings. , we tend to get these things as strings. TO get user input in Python 3, the function **input()** (raw_input() for Python 2) can be used. 
The parameter to the input function is what's called a prompt.

Input is an essential part of a program pattern. This pattern is usually input, processing and output, which are the 
essential functions of computers: gather some input, do some work to it, and then produce something (*In-work-out*). The work is the hard part usually.  

```
# Convert elevator floors
# Europe ground floor is 0 but in US is 1
inp = input('Europe floor') # In
usf = int(inp) + 1          # Work
print('US floor', usf)      # Out
```

### ValueError
Note that, if the input given to this code is not a number (specifically, cannot be converted to integer). 
ValueError



# Compound types (collections)

The basic Python types allow for the storage of one single value. For scripts requiring a large number of values to be stored, it is inconvinient to create a new variable for each value. It would be impossible to assign a value to meaningfull and distinct names to each variable, making the code would be unreadable.
Storing a single value in a variable is not enough for higher complexity programs. 
More often, several related values are needed and defining a variable of each would be 
unfeasable. As such, compounded data types allow for storing collections of values on one single variable, 
generating  of values. 
Python gives you several great built-in data structures such as lists, dictionaries and tuples.


## List
When you're working with vanilla Python and dealing with a problem that involves collections of things, chances are good you're going to be dealing with lists. These could be collections of email addresses, numeric data, file names, etc.

### Definition
Lists are used to store a collection of data in an ordered sequence.
A **list** is a ordered collection of data which is used to group values together, storing them in a single varaible. Lists can store values (elements) of any type, including any of the basic data types, other lists and even more advanced types, whithin the same variable. Lists instances can be initiated using the **list()** function or, more commonly, square brackets **[]**.
To create a list, we use square brackets ([]). We separate items in the list with commas. It's customary to follow each comma with a space. Lists can be created with zero or more elements.You can also use list() on another iterable such as a string or a range (we'll cover ranges later) to generate lists:
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

```
list("Hello")
['H', 'e', 'l', 'l', 'o']
>>> list(range(10))
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

List items can be of different data types.List items can even be other lists, allowing for multidimensional matrices.
You can put any value into a list that you like, even another list. Just like the characters in a string, the elements in a list are ordered and can be accessed by index with bracket notation.

```
# Start by assigning some lists to variables.
inventory = ["beans", "coin", "tome"]
tome_dimensions = [8.5, 11, 2]

# Lists in lists...
random_stuff = [True, 3.14, ["pie", "pizza", "automobile"]]
battleship_board = [[1, 1, 0], [1, 0, 1], [0, 0, 1]]

# Just like with strings you can access list elements by index
# with bracket notation. We start counting at zero:
print(inventory[0])
print(random_stuff[2])

# With nested lists you can continue digging down with additional
# indexes:
print(random_stuff[2][0])

# Lists have a particular length.
inventory_size = len(inventory)
print("You have {} items in your inventory".format(inventory_size))

# Lists are easy to modify. We'll cover this in more detail later.
inventory.append("magic sword")
print(inventory)

# Can you think of a way to print 3.14 solely by referencing the
# variables above?
```

Note that a list of lists can be though of as a 2 dimentional matrix. The matrix is represented by the outer lists and each inner list is a row of values. The index in each row is consequently the column of the matrix. EXPLAIN WHAT A MATRIX IS?


### Subsetting

To acess the value of a list, Python uses a 0-index bases sytems. This means that, each value within a list is assigned a index value, starting from 0. As such, extracting a value from a list requires passing the index value to a list using square brackets **list[index]**. conviniently, Python additionally allows the using of negative indeces, that is, couting backwards from the last element of the list.
List contents are accessed by index using bracket notation; just like strings. 

Note in this example that we start counting list items at 0, just like we do with strings. This may still seem strange, but that's simply how we count sequences like lists and strings in Python. ZERO INDEXED
Similar syntax is used to update an item at a particular index in a list. 
```
x = ["a", "b", "c", "d"]
# Indexing a list
print(x[1])
print(x[-3]) # same result!

# Using the extracted values for other operation
print(x[1] + x[3])
```
```
>>> all_the_things = ['cats', 'dogs', 42, ['pizza', 'beer'], True]
>>> first_item = all_the_things[0]
>>> print("The first thing is '{}'.".format(first_item))
The first thing is 'cats'.
>>> all_the_things[0] = 'bears'
>>> print(all_the_things[0])
bears
```
Apart from *indexing*, that is, extracting a single from a list, multiple values can be selected by *slicing* by specifying a range using a colon **list[start:end]**. Note that, even though the start index is included, the end index is excluded when slicing. If either the start or end arguments are not provided, the slicing occurs from the first, or up to the last, element respectively. Slicing lists
Earlier when we covered strings you saw that you could access multiple characters in a string with slicing, using bracket notation and two indices separated by a colon :.



```
# Slice a list
x = ["a", "b", "c", "d"]
print(x[1:3])
# Slece from the begigging and all the way to the end
x[:2]
x[2:]
# Slice all elements (important for copying)
x[:]

>>> 'Monty Python'[:5]
'Monty'
```
```
# Here we create a list with square brackets.
id_numbers = [ 42, 43, 44, 45, 46]

# We can access one item in a list at a time using bracket
# notation and zero-indexing.
print(id_numbers[0])

# To access multiple items in a list at a time we create a slice
# of the list using bracket notation and two indices.
first_two = id_numbers[0:2]
middle_three = id_numbers[1:4]

print(first_two)
print(middle_three)

# Just like with string slicing, you can omit one of the index
# numbers (or both, if you like to live on the edge) when slicing
# and Python will provide reasonable defaults from the beginning
# or end of the list.
also_first_two = id_numbers[:2]
fourth_to_end = id_numbers[3:]

print(also_first_two)
print(fourth_to_end)

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
### list methods
Lists have about a [dozen methods](https://docs.python.org/3.5/tutorial/datastructures.html#more-on-lists). 
There are use cases for all of them, but here we want to draw your attention to some of the most commonly used methods.

Python has a built-in [len()](https://docs.python.org/3.5/library/functions.html#len) 
function that will tell you how long a list is by returning the number of items in a list.
```
>>> letters = ['a', 'b', 'c', 'd']
>>> print len(letters)
4
```
The .append() method is used to add, or "append", a value to the end of a list. Methods such as .append() are called by following the list you want to work with by a dot ., then the name of the method, then parentheses ( ) containing the argument(s) you want to pass in.

The .insert() method is used to insert a new value at any position in a list, including the beginning, middle, or end. You call it with two arguments: the index you want to insert at and the value you want to insert:

The .pop() method is the opposite of .append(): it removes and returns the final item in a list. This is the first list method we've seen that has a return value; .append() and .insert() modify the underlying list but don't themselves have a return value. No arguments are needed with .pop().

The .index() method is used to find out the first index number of a matching list item. There is one required argument (the item you want to match), followed by two optional start and stop index arguments in case you want to limit your search to a particular slice of the list. Like pop() it returns a value: the index number of the first matching element

The .sort() method is used to re-order a list. Like .append(), .sort() has no return value. It directly modifies the list you call it on and does not create and return a new sorted list.You can use optional arguments to change the default sorting behavior, but most often .sort() is called with zero arguments to automatically compare the elements directly as in the examples above.

```
# Interactive versions of the examples above.

letters = ['a', 'b', 'c', 'd']
letters.append('e')

numbers = ['one', 'two', 'four']
numbers.insert(2, 'three')

to_do = ["Conquer world", "Install Linux", "Change light bulb"]
current_task = to_do.pop()

fowl = ['duck', 'duck', 'goose', 'duck']
goose_index = fowl.index('goose')

words = ['car', 'boat', 'apple', 'banana']
words.sort()

ids = [15, 26, 41, 1]
ids.sort()

# Tinker with these lists and list methods and print things out
# to assess how well you understand what's going on.

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
Dictionaries are another way to collect several pieces of data together.
While a list stores that data as an ordered sequence, dictionaries store that data as an unordered 
collection of key-value pairs.
Dictionaries are a common and useful data structure that allow you to store data as an unordered collection of key: value pairs.

While lists make sense for collecting inherently sequenced data and are designed to simplify accessing items by index number, dictionaries make sense for data you reference by name, or "key", rather than by position, or "index".
```
greetings = {
    "english": "hello",
    "japanese": "こんにちは",
    "german": "hallo",
    "hindi": "नमस्ते",
    "leet": "h3ll0",
}

word_counts = {
    "the": 4,
    "and": 2,
    "word": 3,
    "beginning": 1,
    "god": 2,
    "in": 1,
    "with": 1,
    "was": 3,
}
```
Python dictionaries are known in other languages as "associative arrays" or "hash tables" (or "objects" in JavaScript :P), so if you've programmed in another language you likely know a lot about dictionaries.

ictionaries may initially be less intuitive to you than lists, and you might wonder why you'd want to use a dictionary when you could hack a list (or maybe a multidimensional list) into doing the job instead. There are two big reasons dictionaries might be the right tool for the job:

    Looking up or setting values by key rather than by index has incredibly different performance implications, and
    Writing code that refers to data by name rather than by index number can be much clearer and easier to understand.

The first point, about performance, will almost certainly come up during your technical interview process, and, if you're writing programs with large inputs, the performance differences between lists and dictionaries can mean the difference between code that executes in less than a second versus code that will keep running for days or years.

### Creating, accessing, and modifying
To create a dictionary, wrap key-value pairs in curly braces {}, with each key is separated from its value by a colon :, and each key-value pair is separated from other pairs with a comma ,.
```
adventurer = {"name": "grae", "profession": "magician"}
```

A key: value pair together are called an item. Each item is separated from the next with a comma. You'll find that you're generally using strings for your keys, though you may use any [immutable object](https://docs.python.org/3.5/reference/datamodel.html) as a key.



Just like lists, you can use bracket notation to access the data in a dictionary. Unlike lists, where you use an index number, with dictionaries you look up data using a particular key.
Dictionary values are accessed using bracket notation, just like with lists and strings, except that instead of using an index number you use a key. Updating the value associated with a key looks very much like assigning a value to a variable:
In fact, creating a new key: value pair looks the same as well. You specify the key using bracket notation and assign a value with the = operator.
```
# Here's a super simple dictionary:
person = {"name": "grae", "profession": "magician"}

# Dictionaries are great for grouping related data together.
# Let's make a dictionary with more data.

# Note how we split each key-value pair onto a new line. This
# can make dictionaries much easier to read.
hero = {
    "name": None,
    "species": "Human",
    "strength": 4,
    "magic": 5,
    "profession": None,
}

# Let's check the hero's name again. Just like lists, we use
# bracket notation.
if hero["name"] is None:
    # We modify dictionary values just like we access them.
    hero["name"] = input("What is your name?")
    print("Fantastic, thanks {}".format(hero["name"]))

# You can also add a new key-value pairs using the same bracket
# notation syntax.
hero["favorite_color"] = "Octarine"
print(hero["favorite_color"])

# Try inserting a line of code below this comment that changes
# the hero's `profession` from `None` to another value so the next
# print statement works well.

print("Ok {}, you are a {} {}.".format(hero["name"], hero["species"], hero["profession"]))
```
```
>>> stock = {"apples": 5, "oranges": 2}
>>> stock["apples"] = 20
>>> stock["oranges"] += 1
>>> stock["apples"]
20
>>> stock["oranges"]
3
```

You can delete items from a dictionary with the delkeyword, removing the key: value pair entirely.
```
>>> stock["pears"] = 10
stock["pears"]
10
>>> del stock["pears"]
>>> stock["pears"]
Traceback...
KeyError: 'pears'
```
### Boolean operations

You can use the key to get the value of a dictionary item with bracket notation, but what if you just want to know whether a key is in a dictionary at all? For that you can use the in and not in operators.As you saw above when we tried to check stock["pears"] after deleting it, trying to look up the value for a key that isn't in the dictionary will raise a KeyError. These boolean operations are useful for working with dictionaries without raising KeyErrors.

```
# As you read through the code below think about how the
# value of dictionary items might be changing, then check
# your understanding by printing the values out.

# Populate an initial dictionary.
stock = {
  "apples": 5,
  "oranges": 2,
  "pears": 10,
}

# Sell some apples.
stock["apples"] -= 2

# Use statements like print(stock["apples"]) to check
# the value of dictionary items along the way.

# Recieve a new shipment topping up your oranges.
stock["oranges"] = 20

# Begin carrying kale.
stock["kale"] = 20

# Stop carrying pears.
del stock["pears"]

# Check to see whether you carry pizzas
"pizza" in stock

# Spend a few minutes modifying the `stock` dictionary
# and printing out the results below.

```

### Methods and looping

There are three important dictionary methods you should know that map onto the three main concepts of dictionaries: keys, values, and items.

The .keys() dictionary method will return all the keys in a dictionary.

The .values() method will return all the values in a dictionary.

The .items() method will return all the key: value pairs (or "items") in a dictionary.
```
# Create an intial dictionary.
greetings = {
    "english": "hello",
    "japanese": "こんにちは",
    "german": "hallo",
    "hindi": "नमस्ते",
    "leet": "h3ll0",
}

# Use the `.keys()` method to create a list of each key.
languages = greetings.keys()
print(languages)

# Use the `.values()` method to create a list of each value.
translations = greetings.values()
print(translations)

# Use the `.items()` method to create a list of each key: value pair.
pairs = greetings.items()
print(pairs)

```

Each of these methods returns a dictionary view object that looks and acts a lot like a list but is actually a different kind of object. There are just two points we'll cover about view objects right now. First, you can easily convert them into real lists with the built-in list() function if you need a list.
```
>>> stock = {"apples": 5, "oranges": 2}
>>> list(stock.keys())
["apples", "oranges"]
```
And second, view objects provide a dynamic view of the underlying dictionary, so if you update the dictionary then the view object will show you the updated data:
```
>>> stock = {"apples": 5, "oranges": 2}
>>> items_for_sale = stock.keys()
>>> stock["pears"] = 10
>>> items_for_sale
dict_keys(['pears', 'oranges', 'apples'])
```
For more information on dictionary view objects check out the 
[Python documentation](https://docs.python.org/3/library/stdtypes.html#dictionary-view-objects) or see this Stack Overflow question for a discussion of the difference between these dictionary methods in [Python 2 and Python 3](https://stackoverflow.com/questions/8957750/what-are-dictionary-view-objects).


It's important to say again that dictionaries and their view objects are unordered. None of the items come before or after any of the other items. Printing out a dictionary or view objects will display the items in an essentially arbitrary order, and even in a different order when you print it different times. The same is true of the values generated by .keys(), .values(), and .items() above: the elements can come out in an arbitrary order. You won't know and shouldn't rely on them being in a particular order. If you need to look at collection of keys, values, or items use the built-in sorted() function on your relevant view object to create an ordered list:
```
>>> stock = {"apples": 5, "oranges": 2, "bananas": 4}
>>> list(sorted(stock.keys()))
["apples", "bananas", "oranges"]
```

# Flow control
##### (Patterns for code)
Control flow dictates how programs execute different sets of instructions based on differing conditions. You might have one branch of code that executes if a condition is true, and another branch that executes if the condition is false. That's control flow, and it's a powerful tool.

## Sequential
There are a couple of basic patterns that can be used for a program. The most basic pattern is what's called sequential. This is simply a coding pattern where statements follow one after the other in a sequence of commands that Python will obligatiry execute in order.
```
# Sequential pattern
number = 3
number += 2
print(number)
```

## Conditional step
For more complex program, running sequential code is not enough. It may be important to have some type of decision where the data is analysed and depending on it one thing or another is done. These are called conditional steps and it defines optional parts of the code that may or may not run. If a given **condition** is true, then the statement is run; if it is false, then the statement is skiped. So depending on the result of an expression, the code will either execute or not execute that is, depending on a condition the code may run. This is why it is called conditional.

One important concept for conditional steps is that of **comparison operators**. As with the mathematical operators before, the conditional operator symbol were defined around the limitations of the keyboards when most of programming languages were designed. Comparison operators can be used on boolean expression to compared two values to return a boolean value. These values can then be used as the condition for a conditional step. The comparison operator are
  
  * <: less than
  * >: greater than
  * ==: equal to
  * <=: less of equal to
  * >=: greater of equal to
  * !=: not equal to

Note that equality is not represented by *=*, which is the assignement operator. Also, the exclamation (bang) mark is used as a negation symbol, so that *!=* (bang equal!) is the negation of equality and thus, inequality.

```
print(3 > 5)
print('Hello' == 'hello')
print(3<=3)
print('Equal' != 'Not Equal)
```

Conditional steps always start with the *[if](https://docs.python.org/3.5/reference/compound_stmts.html#if)* reserved word followed by a condition that must evaluate to True or False and a colon (:). After the colon, the (sequential) conditional statements are in an indented block, which tells Python they are part of the conditional step. To finish the conditional, de-indent the code. Below that you indent a block of code to be executed if the condition evaluates to True.

```
# Conditional step
number = 11
if number > 50:
  print('Too big')
print('Checked number')
```
The *if* statement can be used for simple one-way decisions. However, it is very common that a two-way decision is required, that is, the program should either run one part of the code or the other. The reversed word *else* work as a catch-all step at the end of the conditional block. So, if all the previous conditions evaluates to *False*, the *else* statment always evaluated to *True* running as long as nothing else runs. 

```
# If-then-else block: note that else must be de-indented to the level of if
number = 11
if number > 50:
  print('Too big')
else:
  print('That's a good number')
print('Checked number')
```
In addition, a conditional block of code can be defined by multiple sequential comparisons using the reverved word *elif* (short for else if). The same syntax is used for elif (short for "else if") with the additional requirement that elif statements must follow an if statement. It is important to keep in mind that only one condition will run, regardeless of how many would evaluated to *True*. The conditions are checked sequentially (not in parallel) and, as soon as one evaluates to *True*, Python exits the conditional block. A conditional block (started by a *if*) will trigger, at most, once.
A multi-comparison conditional block starts with a *if*. If other conditions are to be tested after the first, then the *elif* word is used to indicate that these conditionals depend of the previous that is, will one be checked if and only if the previous evaluated to *False*. Note that both *elif* and *else* are optional and that *elif* can be used multiple times.

```
# Conditional step
number = 11
if number > 50:
  print('Too big')
elif number < 0:
  print('That's a negative number"!')
elif number < 5:
  print('Too small')
else:
  print('That's a good number')
```
The catch-all else statement can follow if and elif statements to end a conditional statement. To use an else statement you just use else: and begin with your indented code block below. The else clause is a catch-all, so you don't include a condition to test. 
```
# Here is the full if, elif, else conditional statement.
def greet_admin(user):
    if user == "Guido":
        return "Welcome, Guido."
    elif user == "Bethany":
        return "Welcome, Bethany."
    elif user == "Alex":
        return "Welcome, Alex."
    else:
        return "You are not authorized."

print(greet_admin("Guido"))
print(greet_admin("Alex"))
print(greet_admin("Grae"))

# Try inserting additional elif statements and changing the
# conditions that are being checked and printing the results.
```

### Identation

This style of indentation is best practice in most programming languages because it makes programs easier to read, but in Python indentation isn't just a good idea. It's the law. In Python indentation has semantic meaning. 
Indentation is an important part of the Python syntax. Not a lot of languages make the indenting of lines a syntactically meaningful thing, but that is how Python works. In other languages, like JavaScript, Java or C, the actual spacing doesn't matter. Indentation is used to visually keep track of blocks of text and make the code more human-readable and the program does not consider it. However, if an indentation is missing, Python will throw and **IndentationError** and quit. In Python, the spacing does matter and indentation is an integral part of Python. Indentation is more important in Python than in almost any other programming language. Indenting, de-indenting or maintaining indentation is a way of defining the start, end or body of a block of code, respectively. The common practice is to use a four space indentation for Python scripts. *Tabs* are strongly disencouradged as Python may not interpret them properly and trow an error. So, even tough it looks the same, using *spaces* is much more stable. The idea is not to put tabs in the code. For this reason, it is important to set the text editor options to auto-indent using spaced instead of tabs.

It may seem that assigning semantic meaning to indentation whitespace is an odd decision, particularly for programmer experienced working in other programming languages that are designed differently. The advantage of giving indentation semantic meaning, though, is that there is no need to use characters like ; to end statements or { and } characters surrounding code blocks to tell the interpreter where a code block starts and ends. Indentation should be used properly anyway, so Python enforces proper indentation and uses that indentation to allow the code to looks more like English.

```
number = 3

# Indent: Start block
if number == 3:
    print('number x is 3!')
# De-indent: End block
# Note: Indentation is not required for one line code 
if number == 3: print('number is 3!')
# but indentation is fundamental for multi-line blocks
# and to distinguish sequential conditionals

# Indent: Start block
if number >= 3: 
    # Maintain: Body of the block
    print('x is greater 3!')
    print('Wait! Maybe x is just equal to 3...')
# De-indent: End if step (not conditinal block!)
elif number == 3:
    print('number was 3 after all...')
# De-indent: End conditional block (made of multiple conditional steps)
```

### Try-except

The last conditional code is what's called the try and except structure. This is a more advanced conditional concept, usually associated with *catching errors* instead of flow control.Python gives us try and except statements for dealing with conditional logic in the case of exceptions. These language constructs allow us to specify a block of code to be tried (the try statement). If that block does not succeed, the code in the except block runs.
However, it is in essence a specialised if-the-else structure. 
Try and except structure is important to *catch* code that might fail (throw and error), setting up and alternative 
code to run. It is a structure equivalent to run this code if it does not throw an error, else run this other. This is fundamental to *catch* predictable tracebacks (errors), handling them and prevent Python from quitting. 
If we don't have anything here to "handle" the exception, so our program halts and prints out a stack trace (or traceback) with information about what went wrong.Using a try, except statement instead of an if statement lets us "try" executing code that might raise an exception and run code to "handle" the exception if it does occur. Try / except statements give the added benefit of letting your program continue to run. While unhandled exceptions halt your program with a traceback, handling an exception allows your program to gracefully continue along even when you raise an exception and conditionally run code when an exception does occur.
```
# Try-except
number = input('Enter a word')
try:
    number = float(number)
except:
    print('Oops, I meant a number!')
    number = -1
print('The numebr is', number)
```

```
# Here's another function that expects a number. Let's use a
# try / except statement to handle situations where we get
# something weird.
def modulo_five(num):
    try:
        result = num % 5
        return "{} modulo 5 is {}".format(num, result)
    except TypeError:
        return "{} isn't even a number!".format(num)
    

# Everything works fine when you pass an integer in as expected.
print(modulo_five(42))

# Floats are fine too.
print(modulo_five(3.414))

# Yay, we're properly handling exceptions and using them to
# control which code is executed.
print(modulo_five("Chaos Monkey"))
```

One important think to keep in mind is that the try/except block should be kept to a minimun size. If big blocks of code are included in the try statment, the reason for the traceback to occurs is not obvious and, if there is a traceback, it is actually important to know about. Small Try-except blocks are more informative and thus more useful. These blocks allow, for example, for specific information to be given back to the user without crushing the program or to print specific warnings associated with the traceback generated. 

## Repeat (Iteration)
The real power and the real benefit of computers comes when a series of steps needs to be repeated. This repeating code is called a loop or iteration. Loop blocks define parts of the code where a repetitive task is required. In Python, there are two keywords to define a loop: the **while** keyword and the **for** keyword. . A loop is created similarly to a conditional step, starting with the key work, follwed by and expression and a colon (:) which marks the beggining of indented code.

In programming, a loop is a construct that allows you to repeat a set of instructions a specific number of times, or until a specific condition is true. Loops give us a way to write a set of behavior once and then apply that behavior to each item in these collections or apply it a certain number of times. This is a valuable tool to have in our problem solving kit.

### Indefinite loops

The **while** loop functions like an if statement where it evaluates a conditional statment. As for conditional steps, if the statment evaluetes to *True*, the indented code is run, if it evalutates to *False* it is skipped. However, once the loop ends (de-indented code), the program goes back and re-evaluates the conditional statement, instead of terminating the while block, reapeating the code until the conditional evaluates to *False*. Indefinitife loops do not define the number of iterations to do at their start, depending solely on the evaluation of the conditional statment. If this statment neve evaluates to *False*, then the loop does not terminat. This is an **infinite loop**, which will run forever blocking (crashing) program until it is forced to quit. To prevent this from happening, **iteration variables** are used to ensure that the loop will evaluate to false.  These are variables that change with each iteration (repetition) of a loop. Iteration variables are used to control how long the iterations run and when the iterations stop, often corresponding to a sequence of numbers (count down to end). So an infinite loop is generally generated when the iteration vriable is not set up (updating) correctly. As opposed to the the infinite loops, 
**zero-trip loops** are those loops when the conditional statment always evaluates to *False* and so if will never run. 

```
# Infinite loop
n = 5
while n > 0:
    print ('Help me, I'm stuck!')
    
# Zero-trip loop
while n < 0:
    print ('Will I ever get my change?')
```

Infinite loops can be important (even if dangerous!) for programms that keep running until the user decidess to quit (a clear example is a [game loop](https://en.wikipedia.org/wiki/Game_programming#Game_structure)). In Python, the **break** reserved word is used to quit any loop, regardeless of the iteration variable. When this executable statement runs it ends the current loop and jumps to immediatly to the code following the loop. And as soon as the break executes, the loop is done. Even though the loop may be infinite, usually the break statment will be in a conditional block, effectively defining an *end condition* to the loop. As break can be used multiple times within a loop, it also can be used to define alternative *end conditions*, as *while* only defines one *end condition*. 

Similar to *break*, the **continue** reserved word can also be used to skip step in a loop. However, while *break* ends the loop, *continue* ends the current iteration and continues the loop on the next iteration. 

```
# Break and continue

n = 0 # Set up iteration variable 
while True: # infinite loop
    if n % 2 == 1: 
        continue
    if n > 10: 
        break
    print(n)
```
[while loops](https://docs.python.org/3.5/reference/compound_stmts.html#the-while-statement) are another, less common way to loop. We said that for loops execute a block of instructions a specific number of times. while loops are useful when you aren't sure how many times you need to loop and will continue to iterate as long as the logical condition you provide is true.
```
# Here we'll see a while loop in action.
n = 24
while n % 2 == 0:
    print(n)
    n = n // 2

# Now that our loop is done, let's see the result.
message = "After removing factors of two, the number is {}"
print(message.format(n))

while True:
    password = input("what is the password")
    if password == 'break':
        print("Yup.")
        break
```
To write a while loop you start with the while keyword, followed by an expression that evaluates to True or False. In the example above that expression is n % 2 == 0. If the condition evaluates to True, the loop will run; if not, it won't and execution of the program will continue on below.

Conceptually, while loops are meant to be used where the looped behavior does not have a known number of iterations, but instead a known logical condition where it should terminate. One common use is to gather and validate user input.

```
# We'll use the built-in input() function to get input from a
# user, repeating until we get a valid integer as input.

age = None
while not isinstance(age, int):
    try:
        age = int(input("What is your age?"))
    except ValueError:
        print("Sorry, we were expecting an integer. Try again.")
    
print("Fantastic, thank you!")
```

There's another common, but potentially confusing, use of the while loop you should be familiar with that uses the 
[break](https://docs.python.org/3.5/reference/simple_stmts.html#break) keyword:
Since the while condition here is True, which always evaluates to True, you might think that this loop would run forever. And that's exactly what would happen if you removed the break statement. Using break will terminate the enclosing loop, allowing the program to continue executing code further down. In the example above break is executed once the number grows larger than 32, then program execution continues on with the print() statement.
```
>>> n = 1
>>> while True:
>>>     n = n * 2
>>>     if n > 32:
>>>         break
>>> print(n)
64
```

### Definite loops

Sometimes it's a little tricky to make sure that the while loop will terminate, because these are indefinite loops. Definite loop, efined by the **for** reserved word explicetely define how many times the loop will run, not being dependent on the evaluatio of a conditional statmente. The *for loop* does not evaluate a conditional, but instead evaluates the idented code using a group of values provided (collection). These values are directly assigned one by one to an **iterator variable** that changes at each run (iteration) of the loop, until all values have been used. Definite loops have explicit iteration variables as parte of the syntax. to define the iteration variable, the reserved word **in** is used. The *for loop* will assigned each value of the collection to the iteration variable in order and run the loop. Unlike *while loops*, a *for loop* controls when to stop and what the value of the iteration variabe is automatically. However, any loop can be written as a definite or indefinite loop, as there are equivalent versions of both types. 

```
# Definite loops 
for i in [1,5,3,2,4]: # i stands for integer
    print(i)

# Using a variable
friends = ['Joseph', 'Gleen', 'Sally']
for friend in friends:
    print('Hello', friend)

# Equivalent Indefinite loop
i = 0
while i < len(friends):
    print('Hello', friends[i])
    i += 1
```

for loops are used to run through a block of instructions a specific number of times. As you can see, this code will loop over the list we assign to names and repeat the code inside the for loop once for each item in the list.

Let's dig into the syntax of this loop. First off you begin with for, which signals that you're starting a loop and indicates which kind of loop it is. Then we follow with the variable name we'd like to give to each item in the list. In our example the entire list is called names and we're calling each string inside the list name. Next use the in keyword followed by the collection you're iterating over. We end the line with a colon :, which indicates that we're ready to begin our indented block of code that will be executed each time the loop iterates.Using a plural name for a list and the singular of that name in a loop like this is very common. You might have a list of "area_codes" use a for loop that looks like for area_code in area_codes:, or a list of "users" and use a for loop like for user in users:. This style of naming is a useful convention, not a requirement.
```
>>> names = ["Bethany", "Alex", "Grae"]
>>> for name in names:
>>>     greeting = "Hello " + name
>>>     print(greeting)
Hello Bethany
Hello Alex
Hello Grae
```
Inside the indented code block we can run any code we like. The example above accesses and uses each item we're iterating over, but that doesn't need to be the case.
```
>>> names = ["Bethany", "Alex", "Grae"]
>>> for name in names:
...     print("There's no place like home.")
There's no place like home.
There's no place like home.
There's no place like home.
```
```
# Let's try for loops with other sequences and collections. Some
# of these may be new to you.

# Strings.
for character in "Howdy":
    print(character)
    
# Ranges.
for n in range(10):
    print("n is: {}".format(n))
    
# Dictionaries (more on these later).
user = {
    "name": "Grae",
    "role": "admin",
    "age": 35
}

for property in user:
    print(property)
    
# We can also do more than just print things.
even_numbers = []
odd_squares = []

for n in range(10):
    if n % 2 == 0:
        even_numbers.append(n)
    else:
        odd_squares.append(n ** 2)

print(even_numbers)
print(odd_squares)
```
se for loops whenever there is a block of operations that you want to perform on each value in a set of values, or when you want to perform a specific number of times. You'll find that happens very frequently.
If you're coming from another language with a C-like syntax for for loops that requires you to think about the index variable and looks like this: for (i = 0; i < list.length; i++) {} then it might feel weird to iterate without having to think about the index. While the more "Pythonic" solution to most problems usually doesn't require it, you can use the built-in 
[enumerate()](https://docs.python.org/3.5/library/functions.html#enumerate) 
function if you need to see which index you're working on inside the loop.


### Loop idioms
What if we're looking for the largest value or checking to see if 42 is a member of a set or something? Or looking for the largest letter, like the max function? And so we're going to construct loops sort of with an idea of doing something to each value in the set that we're iterating through. And then coming up with some kind of result. And the pattern that we're going to do is we're going to write a for loop. And actually, in this next two segments, I'm going to do the exact same for loop. But we're going to do something before the loop starts, set some variables to initial values. And then we're going to do something to every one of the values in our list. And then, we don't know what the largest value is while the loop is running. And our goal is, when the loop finally finishes, that we have something. Whether it's the maximum, the minimum, the average, the total, how many things there are, how many things match. And so, the iterations are getting us closer to knowing the answer. But they don't instantly know the answer, so we we have to work towards the answer. By setting something and then sort of checking it a bunch of times. And then we have sort of have absolute, the truth comes out at the bottom. 

the trick is "knowing" something about the whole loop when you are stuck writing code that only sees one entry at a time

1. set some initial value
2. for thing in data:
3. look for something or do something to each entry separately updating a variable
4. look at the variables



But what would be the precise technique that you'd use? And so here are the numbers. Now actually as a human, we love looking at these numbers. Like oh, 74 . But then you ask, like how did your mind exactly find them, right? Our minds go, like [SOUND] there's 74. Our mind doesn't look at them the way a computer looks at them. It just kind of zooms in on 74 and just kind of [SOUND]. But that's not how a computer looks them. A computer has to look at them as 3, 41, 12, 9, 74, 15. I conclude at the very end that 74 is the largest number, right? But a human's just [SOUND] 74. So humans think about this differently. And so we have to realize, the purpose of that last little exercise, was to think when we construct loops how computers are going to attack this kind of a problem. They attack it sequentially. They don't attack it magically the way we humans do. And the way that you do it is you create in your head, and you probably did it, some notion of what is the largest number I've seen so far. Like a variable. 
So what happens is at the end of the loop, the only thing we knew was the largest we saw so far and when I tell you we're all done. Then the largest we saw so far, like just poof, it is the largest, right? because it's all that we're ever going to see. So that's how you have to construct these loops in Python. So here's a bit of code that does this logical bit here, okay? And so I'm going to make a variable. 


largest_so_far = -1 # set up a flag value indicating no numbers were seen yet
print('Before', largest_so_far)
for n in [9,4,12,3,74,15]:
    if n > largest_so_far:
        largest_so_far = n
    print(largest_so_far, n)
print('After', largest_so_far)



We set something up before, we do something to each value, and then at the end we kind of get the payoff of what we were looking for in the first place. So up next we're going to talk about more of these loop idioms and how to find the smallest, and how to count things, and how to do averages and sums and stuff like that.

we make a variable that contains the largest number we have seen so far. if the current number we are looking at is larger, it is the new largest value we have seen so far

to count how many types we execute a loop, we introduce a counter variable that starts at 0 and we add one to it each time through the loop

counter = 0 
print('Before', counter)
for n in [9,4,12,3,74,15]:
    counter += 1
    print(counter, n)
print('After', counter)


to add up a value we encounter in a loop, we introduce a sum variable that starts at 0 and we add the value to the sum each time through the loop

sum = 0 
print('Before', sum)
for n in [9,4,12,3,74,15]:
    sum += n
    print(sum, n)
print('After', sum)

the difference between the counter and the sum is only one line!


an average just combines the counting and sum patterns and divided when the loop is done

counter = 0 
sum = 0 
print('Before', counter, sum)
for n in [9,4,12,3,74,15]:
    sum += n
    counter += 1
    print(counter, sum, n)
print('After', counter, sum, sum / counter)


filtering pattern
we use an if statmente in the loop to catch / filter the values we are looking for


print('Before')
for n in [9,4,12,3,74,15]:
    if n > 20:
        print('Large number', n)
print('After')

search using a boolean variable
if we just want to search and know if a value was found, we use a variable that starts at False and is set to True as soons as we find what we are looking for



found = FALSE  
print('Before', found)
for n in [9,4,12,3,74,15]:
    if n ==3:
        found = TRUE
        break #once it is found, not need to search more
    print(found, n)
print('After', found)


find smallest value

smallest = None # Flag value
print('Before', smallest)
for n in [9,4,12,3,74,15]:
    if smallest is None: # is is more strigt than ==, and implies "is the same as". It has to be the same value on memory, not just a equivalent value (?). (generally used for True, False and None) There is also is not
       smallest = n # prime (getting started)
    elif n < smallest:
        smallest = n
    print(smallest, n)
print('After', smallest)









### Nested code

And if we continue down, we haven't talked about loops yet but the for keyword is a loop and this is telling it to run this thing five times, and it ends in a colon. And then you go in and then you have some sequential code, then you have an if, this is called nested. That's a block within a block.

Loop can be defined within other loops, which is called nesting, and also with conditionals. Each nesting level requires a new indentation. Because both conditional and loops require indentation, sequential code is easily identifyed by not being indented in Python.


## Store and retrive (Functions)
For long programs, some lines of code need to be used many times in different places. Repetition of code makes it longer and more difficult to debugg and thus maintain as if one error is found in a piece of repeated code, it has to be manually changed everytime it occurs in the code. It is generally a good programming practice to avoid repetition (D-R-Y: don't repeat yourself). this is the basic essence of the store and reuse pattern, pecenting repeated code. In order to do this, some parts of the code can be stored as a **function** and then reused as required. 
Functions are one of the most important concepts in programming. A function describes a repeatable process or behavior. It is a set of instructions (behaviour) that is defined once, and can then be run and re-run as many times as needed. That's where functions shine: write code once and run it as many times as you like by simply calling the function.

There are two distinct moments to consider when working with functions: the initial definition of a function and the execution (or "call") of a function that has already been defined.

To define a function, the reserved keyword *def* (definition) is used, followed by a list of the function's parameters in brackets and a colon. This forms the header of the function. The lines of code to be reused are then indented on the function definition block, which is the main body of the function. One key feature of the function definition block is that its code is not executed. During the function definition, Python simply parses the code and stores it, creating a new function that can be called (invoked). So, there's a side effect *def*, but it doesn't actually run the code. Once you've defined a function you have a named block of code that you can execute when you call the function by name. To call a function, the name of the function need to be followed by parentheses and any compulsory arguments associated with it. This is exactly as when using the built-in functions *print()* or *input()*. By defining functions, Python's capacities are extended, and these functions can be thought as new reserves or function names. The naming conventions for function names is the same as for variables and it must still avoid reserved words. 

```
# Here's a function that calculates and returns the variance of
# a list of numbers. There's a lot going on here. Don't sweat the
# details.

def variance(numbers):
    length = len(numbers)
    mean = sum(numbers) / length
    square_differences_from_mean = []
    for number in numbers:
        square_differences_from_mean.append((number - mean) ** 2)
    sum_of_square_differences = sum(square_differences_from_mean)
    variance = sum_of_square_differences / length
    return variance
```

```
# Define fucntion
def greet(lang):
 if lang == 'es': 
  print('Hola')
 elif lang == 'fr':
  print('Bonjour')
 else:
  print('Hello')
  
# Invoke function
print(greet('fr'), 'person!')

# Zero parameter function
def hello():
  print('Hello!')
```

The **function parameters** are defined during the call definition and the function will expect them to be passed inside to the main body of the function when the function is called. However, these parameters are just placeholders for the values passed to the function during the invocation and are not real variables, as they do not have an associated piece of memory. These parameters used in the fucntion definition will take up (point to) the values of the **arguments** that are passed during the function call. Arguments are the function inputs (the values that is passed into the function) , and allow for different function results, while parameters are the *alias* for the arguments used in the function definition. So, , an argument is a value that gets passed to the function and assigned to a corresponding parameter, which is used inside the function.


In terms of program flow, when a function is called in Python, it pauses the execution, runs (jumps back to) the previous coded stored as a function and then continues from where the function was called. In addition, more than one parameter used in the functon definition, and the number of arguments on the function call need to match the number and order of these parameters (unless they are optional or named).

```
# Function with two parameters
def sum2numbers(a,b):
 try: 
  print(int(a)+int(b))
 except:
  print('were those numbers?')
  
# Invoke function
sum2numbers(2,3)
```

Often a function will take its arguments, do some computation and return a value to be used as the result of the calling expression, for example, by assigning it to a variable. These functions are known as "fruitful" functions as they produce  results (or return value). In Python, the reserved word *return* stops the function execution and "sends back" the results of the function, replacing the original function call by this residual value. Return statements tell your function that its job is done and will end the execution of the instructions in your function body. That means any code coming after your return statement inside the function body won't be executed. In opposition, non-fruitful functions do not return a value and are used for their side-effect.

```
# Fruitful version of sum2numbers
def sum2numbers(a,b):
 try: 
  return(int(a)+int(b))
 except:
  print('were those numbers?')
  
# Invoke function
s = sum2numbers(2,3)
print(s+4)
```
```
Return statements tell your function that its job is done and will end the execution of the instructions in your function body. That means any code coming after your return statement inside the function body won't be executed.
```
### Functions: programming vs. mathematics
In math, a function is a way to map each input onto a single output. The math function f(x) = 2x, for example, maps the input 3 onto the output 6 and the input 1337 onto the output 2674. Python functions, however, are a defined set of instructions that you can call and execute. You can write that set of instructions to behave like a math function and map arguments onto a return value, but that isn't necessary. In fact, Python functions don't even need to have input or output values at all. The print() function is an example: it displays a message to you but doesn't return any value at all.

In programming, functions that have this mathematical property of mapping arguments onto exactly one return value are called "determinate" functions. Using determinate functions makes your code easier to reason about because you don't need to keep the state of the rest of your program in mind in order to know how the function will act.
```
# Here is an example of a determinate function. It takes an input
# and maps it onto a single return value. Every time you call this
# function with the same input you'll get the same output.

def double(num):
    return num * 2
    
print(double(6))

# Here is an example of a function that isn't  determinate. It
# looks at data beyond the argument passed in and outputs a
# different value depending on what's happening' with an unrelated
# variable. 
secret_number = 100
def multiply_by_secret(num):
    return num * secret_number

# Here we'll call and print `multiply_by_secret`.
print(multiply_by_secret(13))

# Here we'll call it again but first change the value of
# `secret_number`. Note how line 19 and line 25 are identical but
# produce different output.
secret_number = 2
print(multiply_by_secret(13))

# Functions like this that can return a different value when
# called with the same argument are not "determinate" functions.

```
Speaking of state, if the state of your program affecting the output of your function means your function isn't determinate, what about the reverse case where your function affects the state of your program? In math that isn't possible, but since Python functions are just a collection of instructions it is possible to modify state of your program. A function that modifies the state of your program is said to have side effects. In general it's better to write your functions so they don't have unneeded side effects. In fact, Python intentionally makes it difficult to modify variables outside a function's scope (more on "scope" later) by requiring you to explicitly declare you want to do that with the global keyword as we did in the example above.
A Python function that is both determinate and has no side effects works essentially like a function in mathematics. Python functions with each of these two properties are called "pure functions".

```
# This global variable keeps track of the state of our program.
customer_count = 0

# This function has a side effect: it changes the state of the
# program  when it's called. Note that it doesn't even have a real
# return value.
def add_customers(n):
    global customer_count
    customer_count = customer_count + n
    print("Added {} new customers".format(n))
    return None
    
# First let's print the state of our program before changing it.
print(customer_count)

# Now let's call our function and see what happens.
add_customers(10)
add_customers(3)
print(customer_count)

# Here is a much better approach.
sale_count = 0

def add_sale(n, sale_count):
    return n + sale_count

sale_count = add_sale(40, sale_count)
sale_count = add_sale(2, sale_count)
print(sale_count)

# Stretch goal: Can you think of a way to rewrite the
# `add_customers()` function so that it doesn't rely on side
# effects and instead makes use of the function's return value?
# Hint: you'll also want to change the way you call the function
# once you use it.
```

### nomenclature

The name print() is well chosen. Just knowing the name of the function gives us a good sense of what it does. As with variables, a well chosen function name can make clear what might otherwise require multiple lines of comments to explain.

Well crafted functions like print() have a single responsibility. This means that they are designed to do one thing and do it well. print()'s sole responsibility is to display information to the user. When you are writing functions strive to keep each one as simple and focused as possible. If you have a big function doing lots of different things it might be time to split your function up into multiple smaller functions.

## Random?

# Functions (repeated)

A function is a piece of reusable code aimed at solving a particular task. For example, the function type() can be used to return the type of a variable. instead of writting the code everytime, functions can be called. THIS IS GOOD BECAUSE I SHOULD HAVE  DISCUSSED WHY REUSING CODE IS GOOD. Functions work like a black box where inputs are given the ouputs are generated without haveing to think about the computational steps involved, which makes the code easier to understand and cleaner.

Calling a function requires calling the function name and passing the  the required arguments (inputs) within brackets. 
any returned value (output) can be assigned durring the function call `output = function_name(input)`

There are a huge number of functions that can be used. The easiest way to find a function for a specific purpose it to use tin internet, including simply googling it, searching stackoverfolw AND OTHER STUFF. To consult the documentation of a function in Python (interactively), the function `help(function_name)` can be used.



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

# Objects
t's time to talk about something you've been using every time you write Python, but that you may not have been thinking about: objects.

You've been using objects all along because everything in Python is an object. 
Objects and "object-oriented programming" are deep topics that cut to the core of Python and computer science. But as a practical matter, data science isn't a very object-oriented discipline.

### What are objects?

Of course, saying "everything in Python is an object" doesn't tell you much about what an object actually is
Python objects are collections of attributes. Each attribute has a name and a value. You might be thinking that attributes of an object seem a lot like the items of a dictionary
In addition to attributes, each object has a unique id, which you can access with the 
built-in [id() function](https://docs.python.org/3/library/functions.html#id), 
and a type, which you can access with the built-in 
[type()](https://docs.python.org/3/library/functions.html#type) function.
We can get a list of the names for each attribute of an object by passing the object into the built-in dir() function

```
# Let's peer beneath the surface of integers with `dir()`.
print(dir(1))

# Try swapping out the integer above with a string, boolean, list, function, or any
# other object to see what attributes it has. Then try printing the results in
# an easier to read format by using a for loop to print each one out at a time.

```
### Accessing and using attributes

You can access object attributes using dot notation: follow the object with a . and then the name of the attribute you want to access. Let's try this with a string. If we call dir() on a string we see one of the attributes is upper.
```
"hello".upper
<built-in method upper of str object at 0x1015715e0>
"hello".upper()
'HELLO'
```
Just as you've been using objects this whole time without necessarily knowing that they've been objects, you've been accessing object attributes by using methods like the string method .upper() and the list method .append() without necessarily knowing that they were attributes of your object. "Method" is in fact just the special name we use for functions that are attached to an object as one of the object's attributes.

Attributes don't have to be functions, though. Sometimes they're other values.
```
# We'll store 1 in a variable so we can use dot notation.
one = 1

# See if 1 has an imaginary component.

print("The imaginary component of 1 is {}.".format(one.imag))

# Nope. Now check the real component.
print("The real component of 1 is {}.".format(one.real))

# Yup, there it is.

```


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


### Classes, types, and inheritance
Let's think about abstraction for a moment. Consider the statement 1 + 2 and the statement 1 + 'pizza'. We expect the first statement to work because both operands are numbers, and we (rightly) expect the second statement to fail because you can't add a number and a string. The operands in the second example aren't the same type of thing.

What do we mean when we say a number and a string aren't "the same type"? Similarly, what do we mean when we say something like "integers are a type of number"?

In both cases above we're making abstractions. Each integer has a whole bunch of attributes it shares with other integers, attributes it doesn't necessarily share with a string. For example numbers can be even or odd, composite or prime, but those concepts don't even make sense when talking about strings.

Similarly, different types of numbers share some attributes but not others. All integers are divisible by one, but other types of real numbers (like floats) don't have that attribute. "Number" is an abstract class that both integers and floats belong to, even though they're different from one another.

In all of these cases we can intellectually abstract away from specific instances of something (like 1 and 10 and 42) to create a "class" (in this case, integers) where we list out all the attributes that the instances share with one another. Whenever we chose a specific instance of the class you know that the instance inherits all of the properties of the class it belongs to.

All of this talk about abstraction is a bit heady, so let's look at the way Python creates different types of numbers using classes as a concrete example.

Integers and floats are both a type of number. Python has a 
[numbers class](https://docs.python.org/3/library/numbers.html#numbers.Number) 
that ints and floats belong to. They inherit the attributes of that class. Rational numbers are another type of number. Integers are rational numbers but floats aren't, so integers inherit the attributes of the 
[rational class](https://docs.python.org/3/library/numbers.html#numbers.Rational) 
but floats don't. You can read more detail about this and related numeric classes 
[here](https://docs.python.org/3/library/numbers.html), but the takeaway is that Python classes give us a way to define a type of object and allow all objects of a certain type to inherit the attributes of their class. All the unexpected attributes you saw on the object 1 above are inherited from the classes it belongs to.

### Custom objects

As a data scientist you can keep on using all of Python's built-in objects and the objects you import from the standard library and other modules (more on importing modules next) without needing to worry too much about making your own custom objects. But seeing how custom objects work will help you understand objects in general, so we'll look at an example of setting up your own custom objects.

Let's say you want to model a bunch of quarks. Each of your quarks will have its own color (red, green, or blue) and flavor (up, down, strange, charm, top, or bottom). All quarks will have the same baryon number (1 / 3) and will have a method to interact with another quark by exchanging colors (modeling the strong interaction).

Before you can start churning out quarks you first define what you mean by quark, or, in Python terms, you need to define the class. 

```
class Quark(object):

    def __init__(self, color, flavor):
        self.color = color
        self.flavor = flavor

    baryon_number = 1 / 3

    def interact(self, other_quark):
        self.color, other_quark.color = other_quark.color, self.color

    def __repr__(self):
        return "{} {} quark".format(self.color, self.flavor)

```
Let's break down this example piece by piece. In the first line we use the class keyword to start the definition of a new class. This works just like the def keyword when defining new functions. After that comes the name of our new class (Quark). It's customary to use ["CapWords"](https://www.python.org/dev/peps/pep-0008/#class-names) capitalization with custom classes. We follow the class name with parentheses containing the class we want "subclass" from. If you don't have a more specific class you'd like to subclass, the built-in object object has the most basic default attributes you want to inherit.

Inside the class definition we define three methods (__init__(), interact() and __repr__()) and the baryon_number attribute. Each object that we create from this class will inherit these attributes. The interact() method implements the color exchange we set out to do, while __init__() and __repr__() are special double-underscore or "dunder" methods.

The __init__() method is special. Python automatically calls an object's __init__() method when it's created. That means all of the code inside runs as a part of setting up each new object. In our example we're setting two attributes: the quark's color and the flavor.In an object, the self variable is used to refer to the object itself. Every method expects self as the first argument, and whenever you call a method self is passed in behind the scenes without you having to explicitly include it in your method call.

```
class Quark(object):

    # This method is automatically called whenever we create a new quark.
    # It sets the color and flavor attributes when we create an instance.
    def __init__(self, color, flavor):
        self.color = color
        self.flavor = flavor

    # Every quark has the same baryon number, so we set this outside the
    # init function.
    baryon_number = 1 / 3

    # This method models the way quarks interact with one another by
    # exchanging color.
    def interact(self, other_quark):
        self.color, other_quark.color = other_quark.color, self.color

    # The repr method controls how the object is represented by the
    # print() function and other representations of the object.
    def __repr__(self):
        return "{} {} quark".format(self.color, self.flavor)

# Now that we have the class set up, let's call Quark() to create two
# actual instances of quark objects.
q1 = Quark("red", "up")
q2 = Quark("blue", "down")

# Print each object to see what they look like.
print("q1 is a {}".format(q1))
print("q2 is a {}".format(q2))

# Test our interact() method by having q1 and q2 interact.
q1.interact(q2)

# Print them out again to see how they changed.
print("Now q1 is a {}".format(q1))
print("Now q2 is a {}".format(q2))

# Test how our object deals with the built-in type() function.
print("q1 is a {} object".format(type(q1)))
```

Unlike color and flavor, each quark has the same baryon number, so we can set that outside the __init__ function just like we do for the method attributes.

The interact() method is a straightforward function that manipulates both the object calling it and the object passed in as an argument. The __repr__() method is another useful dunder method that tells your object how to play nice with print() and other cases that require a representation of your object.


# Packages / Modules

Functions and methods allows for code to be easily transfered and reused. However, adding all functions that may be required to the same Python distribution would mean that most of the code would not be used by most users and it would make the maintenance aof the codebase a huge task. In order to avoid such a messy code, Python uses packages. Packages are, in essence, directories of Python scripts, with each scripts being called a **module**. Eahc module speficies functions, methods and new object types  all  all associated with a particular problem. Whidely used packages include Numpy for efficient work wiyth arrays, matplotlib, for data visualization and scikit-learn for machine learning. 

Your Python installation almost certainly includes the entire 
["standard library"](https://docs.python.org/3/library/): 
a library of modules that aren't loaded by default but that are available for you to import whenever you like.

In addition to the standard library, there is a vibrant ecosystem of open-source Python modules that you can download, install, and import into your programs. The best centralized reference for these is the 
[Python Package Index](https://pypi.org/), 
or "PyPI". For example, here is the 
[PyPI page for Pandas](https://pypi.org/project/pandas/0.19.2/), 
a module you'll use heavily as a data scientist. We'll install and dig into Pandas and other packages soon.

## Installing packages

As Packages are not included in the basic Python distributions, they have to be installed. Package installation is performed by pip, a package maintenance system for python. To install pip, download [get-pip.py](http://pip.readthedocs.org/en/stable/installing) and run the script from the terminal `python3 get-pip.py`. Once pip is installed, packages can be installed with `pip3 install package_name`. Now that the package is installed, it can be used in any python script. 

When you installed Python 3 you also got pip, the
[package manager for Python](https://en.wikipedia.org/wiki/Pip_%28package_manager%29), for free. 
You'll use pip frequently in your career to download and manage Python tools.
Let's confirm your install `$ pip --version`

#### NumPy

NumPy is the fundamental scientific computing package. Most other Python data science tools are built on top of NumPy and treat it as a dependency. You should be able to install NumPy with:

$ python -m pip install numpy

Numpy is big and may take a while to install. As of mid 2016 NumPy should also install successfully on Windows machines with the above command. Confirm your successful install by running pip freeze at your command prompt. This will list out all of the Python packages you've installed and should include NumPy.
#### Pandas

Pandas is the Python library for data manipulation. It gives you custom objects (particularly the data frame) that you'll use every day.

$ python -m pip install pandas

Run pip freeze to confirm your install.
#### Matplotlib

Matplotlib is the 2D plotting library you'll use to produce many of your visualizations. You'll use it both for data exploration and for presentation.

python -m pip install matplotlib

Confirm your install with pip freeze.
#### SciPy

SciPy adds algorithms, convenience functions, and is the basis for many other packages you'll install in the future.

python -m pip install scipy

Brrr, it's getting cold in here from all this pip freeze.
#### Install Jupyter Notebooks

Jupyter notebooks allow you to write, execute, and visualize Python interactively. You'll use Jupyter notebooks as your primary IDE for writing Python in the bootcamp.

python -m pip install jupyter

One last pip freeze for good measure.

To use Jupyter notebooks, run $ jupyter notebook from your command line. This will start the Jupyter server and open a browser tab that hits the server. You can kill the server by closing the terminal window it's running in or with control + c on a mac. If you close your browser but the server's still running you can open a new tab to the server at the address listed in your terminal that starts with http://localhost:8888/?token=.
## Importing package

However, it is still required that the packages are imported by Python (otherwise it doesn't know it has to use it). There are various ways to import a package into Python. The simplest way is to include the line `import package_name` at the top of the script. With the package imported, every function, method or object from that package can be used, but not directly. Python need to know that the function called belongs to an external package so it can find it. This can be done with the **. notation** as for methods. In this case, the function *belongs to* the package.
All you need to start using modules is an import statement at the top of your program. Here's how you'd import the built-in math and random modules
It's customary to put your import statements at the 
[top of your files](https://www.python.org/dev/peps/pep-0008/#imports).

Once imported, you'll have access to a math module object and a random module object. Just like every object, these contain attributes that you can work with. Some interesting attributes are the 
[math.pi constant](https://docs.python.org/3/library/math.html#math.pi) 
and the [random.choice()](https://docs.python.org/3/library/random.html#random.choice) 
method.

```
import numpy
import math
import random

array([1,2,3]) # NameError
numpy.array([1,2,3]) # Array is defined on the numpy workspace (is it a workspace here?)

# Let's import the math and the random modules.
import math
import random

# Module attributes are accessed like any other object attribute.
circumference = math.pi * 2
print(circumference)

# Module methods are functions and called like any other function.
secret_number = random.choice([1, 2, 3, 4, 5])
print(secret_number)

destination = random.choice(["Seattle", "New York", "Leipzig", "San Francisco"])
print(destination)
```
Other packages are imported just like modules in the standard library once you have them installed in your local Python environment. In this fundamentals course, we'll use the NumPy, Pandas, matplotlib and SciPy packages. You'll notice import statements like this a lot once we start doing real work:
```
import numpy as np
import scipy as sp
import pandas as pd
import matplotlib.pyplot as plt
```
We'll cover those new conventions later, and we'll cover installation in the next lesson.




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
# Built-in Math Methods

We won't cover it here, but you should know that the Python standard library includes a robust math module that will give you common functions like math.floor() and math.sqrt() and constants like math.pi and math.e. 
You can read more in the [math module docs](https://docs.python.org/3.5/library/math.html).

### Custom modules

Creating your own modules is easy once you're working with files on your local machine. In fact, every Python file (file with a .py extension) is also a module. The module name is the name of the file minus the .py part, so if you have a file called demo.py you can import it with import demo. All of the variables and functions in your file are available as attributes of the module. 

### Executable scripts

Sometimes you'll want to be able to execute a module from your command line as a script. 
We won't get into the [details](https://docs.python.org/3/tutorial/modules.html#executing-modules-as-scripts) 
here, but you can add this code to the end of your module:
```
if __name__ == "__main__":
    # Call functions here that you define above.
```
and all of the statements inside the if statement will be run when you call the module from your command line with python [your module name].py

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


