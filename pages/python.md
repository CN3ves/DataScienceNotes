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
There are two types of numbers in Python, **integers (int)** and **floating point numbers (float)**. 
Whole numbers that aren't written as a fraction or with a decimal point are integers. 
There is no maximum integer size: Python 3 can handle integers that are arbitrarily large (unlike many other languages).
On the other hand, numbers that do have decimal places are floating point numbers.

The main diference between these number representation is their internal representation. 
Floats in computer science are a fun topic.
Floating point numbers have a greater range than integer numbers, but they're not always as
precise as integer numbers. This is because computers represent everything internally in binary, and since it's impossible to precisely represent many decimal fractions in binary, it's easy to end up with 
[floating point issues](https://docs.python.org/3.5/tutorial/floatingpoint.html). 
That said, doing arithmetic with floats is asking for trouble. 
For example, to represent money (or quantities that have to be precise) only integers should be used, has binary representation has dificulties representing decimals and will result in errors for large calculations. 

```
# Floating points representation is less precise
print(1.03-0.42)
print(103-42)
print(.2 + .4)
# 0.6000000000000001
```

```
# Integer: Number without a fractional (decimal) part
print(type(5))
# Float: Number with both an integer and a fractional (decimal) separated by a point. A Real  number
print(type(5.0))
```



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
**multiplication(\*)** and **division(/)**, there is also support for more advanced operations such as 
**exponentiation (\*\*)**, **modulo (%)** and **integer division (//)**.  Like for mathematics, these opperators have
an order of evaluation, where parentheses override everything, followed by exponentiation,
multiplication and division/modulo and addition and subtraction for last. For similar priority operations, 
they are evaluated from left to right. 
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
should comment on why there are integers and floats and their representation at some point...

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
### Definition

A **list** is a ordered collection of data which is used to group values together, storing them in a single varaible. Lists can store values (elements) of any type, including any of the basic data types, other lists and even more advanced types, whithin the same variable. Lists instances can be initiated using the **list()** function or, more commonly, square brackets **[]**.

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
Dictionaries are another way to collect several pieces of data together.
While a list stores that data as an ordered sequence, dictionaries store that data as an unordered 
collection of key-value pairs.

To create a dictionary, wrap key-value pairs in curly braces, with each key is separated from its value by a colon :, and each key-value pair is separated from other pairs with a comma ,.
```
adventurer = {"name": "grae", "profession": "magician"}
```
Just like lists, you can use bracket notation to access the data in a dictionary. Unlike lists, where you use an index number, with dictionaries you look up data using a particular key.

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


# Flow control
##### (Patterns for code)
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

Conditional steps always start with the *if* reserved word followed by a condition that must evaluate to True or False and a colon (:). After the colon, the (sequential) conditional statements are in an indented block, which tells Python they are part of the conditional step. To finish the conditional, de-indent the code. 

```
# Conditional step
number = 11
if number > 50:
  print('Too big')
print('Checked number')
```
The *if* statment can be used for simple one-way decisions. However, it is very common that a two-way decision is required, that is, the program should either run one part of the code or the other. The reversed word *else* work as a catch-all step at the end of the conditional block. So, if all the previous conditions evaluates to *False*, the *else* statment always evaluated to *True* running as long as nothing else runs. 

```
# If-then-else block: note that else must be de-indented to the level of if
number = 11
if number > 50:
  print('Too big')
else:
  print('That's a good number')
print('Checked number')
```
In addition, a conditional block of code can be defined by multiple sequential comparisons using the reverved word *elif* (else if). It is important to keep in mind that only one condition will run, regardeless of how many would evaluated to *True*. The conditions are checked sequentially (not in parallel) and, as soon as one evaluates to *True*, Python exits the conditional block. A conditional block (started by a *if*) will trigger, at most, once.
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

The last conditional code is what's called the try and except structure. This is a more advanced conditional concept, usually associated with *catching errors* instead of flow control. However, it is in essence a speciallised if-the-else structure. 
Try and except structure is important to *catch* code that might fail (throw and error), setting up and alternative 
code to run. It is a structure equivalent to run this code if it does not throw an error, else run this other. This is fundamental to *catch* predictable tracebacks (errors), handling them and prevent Python from quitting. 

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
One important think to keep in mind is that the try/except block should be kept to a minimun size. If big blocks of code are included in the try statment, the reason for the traceback to occurs is not obvious and, if there is a traceback, it is actually important to know about. Small Try-except blocks are more informative and thus more useful. These blocks allow, for example, for specific information to be given back to the user without crushing the program or to print specific warnings associated with the traceback generated. 

## Repeat (Iteration)
The real power and the real benefit of computers comes when a series of steps needs to be repeated. This repeating code is called a loop or iteration. Loop blocks define parts of the code where a repetitive task is required. In Python, there are two keywords to define a loop: the **while** keyword and the **for** keyword. . A loop is created similarly to a conditional step, starting with the key work, follwed by and expression and a colon (:) which marks the beggining of indented code.

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


