## Week 3
### When Python is running in the interactive mode and displaying the chevron prompt (>>>) - what question is Python asking you?

  * *What Python statement would you like me to run?*
  * What Python script would you like me to run?
  * What is the next machine language instruction to run?
  * What is your favourite color?
  
### What will the following program print out:

```
x = 15
x = x + 5
print(x)
```

  * *20*
  * 5
  * 15
  * "print x"
  * x + 5

## Python scripts (files) have names that end with:

  * .doc
  * .exe
  * *.py*
  * .png

### Which of these words is a reserved word in Python ?

  * *while*
  * payroll
  * names
  * pizza

### What is the proper way to say “good-bye” to Python?

  * *quit()*
  * while
  * // stop
  * #EXIT

### Which of the parts of a computer actually executes the program instructions?

  * Main Memory
  * Input/Output Devices
  * Secondary Memory
  * *Central Processing Unit*
  
### What is "code" in the context of this course?

  * A way to encrypt data during World War II
  * *A sequence of instructions in a programming language*
  * A password we use to unlock Python features
  * A set of rules that govern the style of programs

### A USB memory stick is an example of which of the following components of computer architecture?

 * Output Device
 * Main Memory 
 * Central Processing Unit
 * *Secondary Memory*

### What is the best way to think about a "Syntax Error" while programming?

  * The computer has used GPS to find your location and hates everyone from your town
  * The computer is overheating and just wants you to stop to let it cool down
  * *The computer did not understand the statement that you entered*
  * The computer needs to have its software upgraded

### Which of the following is not one of the programming patterns covered in Chapter 1?

  * Sequential Steps
  * Repeated Steps
  * *Random steps*
  * Conditional Steps

### Write a program that uses a print statement to say 'hello world'.
**Desired Output**: hello world

```
# the code below almost works
prinq("hello world")

# Solution
print("hello world")
```


## Week 4
### In the following code, `print(98.6)`, What is "98.6"?

  * *A constant*
  * A variable
  * An iteration / loop statement
  * A conditional statement

### What does the following code print out? `print("125" + "abc")`

  * hello world
  * *123abc*
  * 123+abc
  * This is a syntax error because you cannot add strings
  
### Which of the following variables is the "most mnemonic"?

  * x
  * x1q3z9ocd
  * *hours*
  * variable_173
  
### Which of the following is not a Python reserved word?

  * *iterate*
  * continue
  * else
  * break
  
### Assume the variable x has been initialized to an integer value (e.g., x = 3). What does the following statement do? `x = x +2`

  * Increase the speed of the program by a factor of 2
  * Exit the program
  * *Retrieve the current value for x, add two to it, and put the sum back into x*
  * This would fail as it is a syntax error
  
### Which of the following elements of a mathematical expression in Python is evaluated first?

  * Addition +
  * *Parentheses ( )*
  * Multiplication *
  * Subtraction -

### What is the value of the following expression `42 % 10`. Hint - the "%" is the remainder operator

  * 4210
  * 42
  * *2*
  * 420
  
### What will be the value of x after the following statement executes: `x = 1 + 2 * 3 - 8/4`

  * 4
  * 2.0
  * 8
  * *5.0*
  
### What will be the value of x when the following statement is executed: `x = int(98.6)`

  * 6
  * 100
  * *98*
  * 99
  
### What does the Python input() function do?

  * *Pause the program and read data from the user*
  * Connect to the network and retrieve a web page.
  * Read the memory of the running program
  * Take a screen shot from an area of the screen

### Write a program that uses input to prompt a user for their name and then welcomes them. Enter Sarah in the pop-up box when you are prompted so your output will match the desired output.

**Desired Output**: Hello Sarah

```
# The code below almost works
name = input("Enter your name")
print("Howdy")

# Solution
name = input("Enter your name")
print("Hello", name)
```


### Write a program to prompt the user for hours and rate per hour using input to compute gross pay. Use 35 hours and a rate of 2.75 per hour to test the program (the pay should be 96.25). You should use input to read a string and float() to convert the string to a number. Do not worry about error checking or bad user data.
**Desired Output**: Pay: 96.25

```
# This first line is provided for you
hrs = input("Enter Hours:")

# Solution
hrs = input("Enter Hours:")
r = input("Enter Rate:")
print('Pay:', float(hrs)*float(r)
```

## Week 5
### What do we do to a Python statement that is immediately after an if statement to indicate that the statement is to be executed only when the if statement is true?

  * Begin the statement with a curly brace {
  * Start the statement with a "#" character
  * *Indent the line below the if statement*
  * Underline all of the conditional code
  
### Which of these operators is not a comparison / logical operator?

  * ==
  * !=
  * <
  * *=*
  * >=
  
### What is true about the following code segment:

```
if  x == 5 :
    print('Is 5')
    print('Is Still 5')
    print('Third 5')
```
  * *Depending on the value of x, either all three of the print statements will execute or none of the statements will execute*
  * The string 'Is 5' will always print out regardless of the value for x.
  * The string 'Is 5' will never print out regardless of the value for x.
  * Only two of the three print statements will print out if the value of x is less than zero.
  
### When you have multiple lines in an if block, how do you indicate the end of the if block?

  * You omit the semicolon ; on the last line of the if block
  * *You de-indent the next line past the if block to the same level of indent as the original if statement*
  * You capitalize the first letter of the line following the end of the if block
  * You use a curly brace { after the last line of the if block
  
### You look at the following text. It looks perfect but Python is giving you an 'Indentation Error' on the second print statement. What is the most likely reason?
```
if x == 6 :
    print('Is 6')
    print('Is Still 6')
    print('Third 6')
```

  * Python has reached its limit on the largest Python program that can be run
  * In order to make humans feel inadequate, Python randomly emits 'Indentation Errors' on perfectly good code - after about an hour the error will just go away without any changes to your program
  * *You have mixed tabs and spaces in the file*
  * Python thinks 'Still' is a mis-spelled word in the string
  
### What is the Python reserved word that we use in two-way if tests to indicate the block of code that is to be executed if the logical test is false?

  * iterate
  * break
  * except
  * *else*
  
### What will the following code print out?
```
x = 0
if x < 2 :
    print('Small')
elif x < 10 :
    print('Medium')
else :
    print('LARGE')
print('All done')
```
  * Small
  Medium
  LARGE
  All done
  * All done
  * LARGE
  All done
  * *Small
  All done*

### For the following code, What value of 'x' will cause 'Something else' to print out?
```
if x < 2 :
    print('Below 2')
elif x >= 2 :
     print('Two or more')
else :
    print('Something else')
```
  * x = 22
  * x = -2.0
  * x = 2.0
  * *This code will never print 'Something else' regardless of the value for 'x'*

### In the following code (numbers added) - which will be the last line to execute successfully?
```
(1)   astr = 'Hello Bob'
(2)   istr = int(astr)
(3)   print('First', istr)
(4)   astr = '123'
(5)   istr = int(astr)
(6)   print('Second', istr)
```
  * *1*
  * 6
  * 3
  * 2
  
### For the following code, What will the value be for istr after this code executes?
```
astr = 'Hello Bob'
istr = 0
try:
    istr = int(astr)
except:
    istr = -1
```
  * It will be the 'Not a number' value (i.e. NaN)
  * false
  * It will be a random number depending on the operating system the program runs on
  * *-1*

### Write a program to prompt the user for hours and rate per hour using input to compute gross pay. Pay the hourly rate for the hours up to 40 and 1.5 times the hourly rate for all hours worked above 40 hours. Use 45 hours and a rate of 10.50 per hour to test the program (the pay should be 498.75). You should use input to read a string and float() to convert the string to a number. Do not worry about error checking the user input - assume the user types numbers properly. 

**Desired Output**: 498.75
```
# Starting code
hrs = input("Enter Hours:")
h = float(hrs)

# Solution
hrs = input("Enter Hours:")
h = float(hrs)

r = input("Enter Rate:")
r = float(r)

print(str((2*h-40)*r + (h-40) * r*1.5))
```

###  Write a program to prompt for a score between 0.0 and 1.0. If the score is out of range, print an error. If the score is between 0.0 and 1.0, print a grade using the following table:
### Score Grade
### >= 0.9 A
### >= 0.8 B
### >= 0.7 C
### >= 0.6 D
### < 0.6 F
### If the user enters a value out of range, print a suitable error message and exit. For the test, enter a score of 0.85. 

**Desired Output**: B

```
# Initial code
score = input("Enter Score: ")

# Solution
score = input("Enter Score: ")

try:
    score=float(score)
except:
    print('numeric')
    
if score > 1.0: 
    print('above 1')
elif score >=0.9:
    print('A')
elif score >=0.8:
    print('B')
elif score >=0.7:
    print('C')
elif score >=0.6:
    print('D')
else:
    print('F')
```

## Week 6
### Which Python keyword indicates the start of a function definition?

  * *def*
  * continue
  * return
  * sweet
  
### In Python, how do you indicate the end of the block of code that makes up the function?

  * You put the colon character (:) in the first column of a line
  * You add the matching curly brace that was used to start the function }
  * You add a line that has at least 10 dashes
  * *You de-indent a line of code to the same indent level as the def keyword*
  
### In Python what is the input() feature best described as?

  * A conditional statement
  * A way to retrieve web pages over the network
  * The central processing unit
  * *A built-in function*
  
### What does the following code print out?
```
def thing():
    print('Hello') 

print('There')
```
  * thing
  Hello
  There
  * thing
  * def
  thing
  * *There*
  
### In the following Python code, which of the following is an "argument" to a function?
```
x = 'banana'
y = max(x)
print(y)
```
  * *x*
  * 'banana'
  * print
  * max
  
### What will the following Python code print out?
```
  def func(x) :
    print(x)

func(10)
func(20)
```
  * x
  10
  x
  20
  * *10
  20*
  * x
  20
  * def
  x
  func
  func
  
### Which line of the following Python program will never execute?
```
def stuff():
    print('Hello')
    return
    print('World')

stuff()
```
  * stuff()
  * def stuff():
  * print('Hello')
  * return
  * *print ('World')*
  
### What will the following Python program print out?
```
def greet(lang):
    if lang == 'es':
        return 'Hola'
    elif lang == 'fr':
        return 'Bonjour'
    else:
        return 'Hello'

print(greet('fr'),'Michael')
```
  * *Bonjour Michael*
  * def
  Hola
  Bonjour
  Hello
  Michael
  * Hola Michael
  * Hola
  Bonjour
  Hello
  Michael
  
### What does the following Python code print out? (Note that this is a bit of a trick question and the code has what many would consider to be a flaw/bug - so read carefully).
```
def addtwo(a, b):
    added = a + b
    return a

x = addtwo(2, 7)
print(x)
```
  * 7
  * 14
  * Traceback
  * *2*
  
### What is the most important benefit of writing your own functions?

  * To avoid having more than 10 lines of sequential code without an indent or de-indent
  * Following the rule that no function can have more than 10 statements in it
  * Following the rule that whenever a program is more than 10 lines you must use a function
  * *Avoiding writing the same non-trivial code more than once in your program*
  
### Write a program to prompt the user for hours and rate per hour using input to compute gross pay. Award time-and-a-half for the hourly rate for all hours worked above 40 hours. Put the logic to do the computation of time-and-a-half in a function called computepay() and use the function to do the computation. The function should return a value. Use 45 hours and a rate of 10.50 per hour to test the program (the pay should be 498.75). You should use input to read a string and float() to convert the string to a number. Do not worry about error checking the user input unless you want to - you can assume the user types numbers properly. Do not name your variable sum or use the sum() function. 

**Desired Output:** 498.75

```
def computepay(h,r):
    return 42.37

hrs = input("Enter Hours:")
p = computepay(10,20)
print("Pay",p)

# Solution
def computepay(h,r):
    if h >= 40: pay =  40 *r + (h-40) *r*1.5
    else: pay = h * r
        
    return pay

hrs = input("Enter Hours:")
r = input("Enter Rate:")
p = computepay(float(hrs),float(r))
print(p)
```

## Week 7
### What is wrong with this Python loop:
```
n = 5
while n > 0 :
    print(n)
print('All done')
```

  * *This loop will run forever*
  * The print('All done') statement should be indented four spaces
  * There should be no colon on the while statement
  * while is not a Python reserved word

### What does the break statement do?

  * *Exits the currently executing loop*
  * Resets the iteration variable to its initial value
  * Exits the program
  * Jumps to the "top" of the loop and starts the next iteration

### What does the continue statement do?

  * *Jumps to the "top" of the loop and starts the next iteration*
  * Exits the currently executing loop
  * Resets the iteration variable to its initial value
  * Exits the program

### What does the following Python program print out?
```
tot = 0 
for i in [5, 4, 3, 2, 1] :
    tot = tot + 1
print(tot)
```

  * 15
  * 0
  * 10
  * *5*

### What is the iteration variable in the following Python code:
```
friends = ['Joseph', 'Glenn', 'Sally']
for friend in friends :
     print('Happy New Year:',  friend)
print('Done!')
```

  * *friend*
  * Glenn
  * Sally
  * friends

### What is a good description of the following bit of Python code?
```
zork = 0
for thing in [9, 41, 12, 3, 74, 15] :
    zork = zork + thing
print('After', zork)
```

  * Find the smallest item in a list
  * *Sum all the elements of a list*
  * Count all of the elements in a list
  * Find the largest item in a list

### What will the following code print out?
### Hint: This is a trick question and most would say this code has a bug - so read carefully
```
smallest_so_far = -1
for the_num in [9, 41, 12, 3, 74, 15] :
   if the_num < smallest_so_far :
      smallest_so_far = the_num
print(smallest_so_far)
```

  * *-1*
  * 74
  * 42
  * 3

### What is a good statement to describe the is operator as used in the following if statement:
```
if smallest is None :
     smallest = value
 ```
 
   * Looks up 'None' in the smallest variable if it is a string
  * Is true if the smallest variable has a value of -1
  * *matches both type and value*
  * The if statement is a syntax error

### Which reserved word indicates the start of an "indefinite" loop in Python?

  * break
  * indef
  * def
  * for
  * *while*

### How many times will the body of the following loop be executed?
```
n = 0
while n > 0 :
    print('Lather')
    print('Rinse')
print('Dry off!')
```

  * *0*
  * 1
  * This is an infinite loop
  * 5
  
### Write a program that repeatedly prompts a user for integer numbers until the user enters 'done'. Once 'done' is entered, print out the largest and smallest of the numbers. If the user enters anything other than a valid number catch it with a try/except and put out an appropriate message and ignore the number. Enter 7, 2, bob, 10, and 4 and match the output below. 

**Desired Output**:
Invalid input
Maximum is 10
Minimum is 2

```
# Initial code
largest = None
smallest = None
while True:
    num = input("Enter a number: ")
    if num == "done" : break
    print(num)

print("Maximum", largest)

# Solution
largest = None
smallest = None
while True:
    num = input("Enter a number: ")
    
    if num == "done" : break
    
    try:
        num = int(num)
    except:
        print("Invalid input")
        continue
      
    if largest is None or num > largest: largest = num
    
    if smallest is None or num < smallest: smallest = num

print("Maximum is", largest)
print("Minimum is", smallest)
```
