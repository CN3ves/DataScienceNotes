# What is programming? 

A program is a set of instructions for a computer to carry out, which could range from
instructions to collect data from the web, to systematically reformat or clean data, or to process and display a 
visualization. 

Programs are used to solve a specific problem or provide a specific experience. As such, programming is 
the process of translating a problem stated in plain language into a set of instructions for solving 
that problem (the algorithm), and then expressing this solution in terms that your computer 
can understand (a programming language). 

The skill of programming therefore has two steps: first, programming is finding solutions to problems; 
second, programming is implementing those solutions in a particular programming language such that the 
computer can understand and execute your solution.

Programmers by definition must master at least one programming languages, 
but the ability to move from high level language, to a clear set of instructions, 
to implementing the instructions using clean code is the key skill of any the programmer.
When programming, 
sometimes new algorithms need to be invented, other times simply implemented those already existing. 
Most of the time, you're doing a bit of both.


### The Fibonacci series example

The [Fibonacci sequence](https://en.wikipedia.org/wiki/Fibonacci_number) 
describes a series of numbers in which each number in the list is the sum of the previous two 
(with the exception of the first two numbers in the list, 0 and 1). 
This sequence of numbers has applications in mathematics and biology, 
and it is a well known algorithm.

How can a simple interface that calculates the Fibonacci sequence be created where the user 
is able to define how long of a list of Fibonacci numbers to display is?
This problem can be broken down into three main questions: 

  1. How to get the length of the list required by the user?
  2. How to calculate the sequence of numbers?
  3. How to represent these numbers to the user?
 
 Steps 1 and 3 can usially be easilly implemented using build-in programming language capacities. 
 Step 2 is more complex and would require an *algorithmic* approach to solve it. 
   1. The value `n` must be defined by the user input (step 1), which represents the length of the sequence
   2. Build the sequence from value 1 to value n (the last number) setting value 1 to 0 and value 2 to 1.
   3. Compute the next `n-2` values by summing the previous two values.
   4. Stop when the sequence has `n` numbers
 
 [implementation](fibonacci.md)
