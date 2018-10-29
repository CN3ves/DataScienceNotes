# Introduction to Linear Algebra and to Mathematics for Machine Learning

In this first module we look at how linear algebra is relevant to machine learning and data science. 
Then we'll wind up the module with an initial introduction to vectors. 
Throughout, we're focussing on developing your mathematical intuition, not of 
crunching through algebra or doing long pen-and-paper examples. 
For many of these operations, there are callable functions in Python that can do the adding up - 
the point is to appreciate what they do and how they work so that, when things go wrong 
or there are special cases, you can understand why and what to do.

## Welcome to this course
### Introduction: Solving data science challenges with mathematics

The world is awash with huge amounts of data.
Most of us living in cities generate huge amounts of data as we go about our lives,
moving around, browsing on mobile phones,
using transit networks, and consuming energy.
If we just think about energy alone for a moment,
our society literally lights up our planet from space.
We can see where the people and economic activity are from the lights.
Zooming in to Europe and London here,
you can see how some of the world's great cities network together.
This takes a huge amount of energy.
And if we're going to figure out how we're going to generate
and use energy more sensibly in the future,
we're going to have to understand the data we have about energy much better.
If we don't want to damage our health with NOx and
particulates and if we want to combat global warming,
we're probably going to have to strongly cut back or even eliminate burning hydrocarbons,
as the leading approach to power in our society.
But where should we start?
Where were the opportunities to have the biggest impact soonest?
These questions we could answer better,
if we could analyze the energy and usage data we had better.
If we had good models of data,
then we could also make predictions.
Practically speaking, we could build software that tells you
how to take the fastest journey across your city and put in a map.
Or which web pages you might want to see in response to a search query.
And we don't necessarily need a physical model in order to make such predictions.
Real Networks are very accurate in
many applications at modeling data and making predictions.
And the process by which we optimize those network is called Machine Learning.

Now, it turns out that linear algebra,
how to solve systems of equations,
like this where the variables obey the rules of vectors
like these and then taking those forward and turning,
recasting them as matrices like these objects here.
This is very important in machine learning and data science.
And also being able to do optimizations in machine learning and data science,
in turn depends on understanding how a thing we're trying to optimize,
changes in response to changes in the primer to describe it, which is multivariable calculus.

The problem is, that machine learning and data science
have their origins in computer science and mathematics.
But more and more,
we're wanting to be used that maths by engineers and physical scientists,
and biologists and people working in medicine and social scientists and so on.
But one of the problems is that,
most courses on data science and machine learning presuppose
a level of familiarity with linear algebra and calculus that not everybody has.
So our aim in this course and in this specialization,
is to revisit the underpinnings in vectors and
matrices and calculus that you might have touched on in school,
but which you might never have applied.

To be clear, we're not really aiming to do a fundamental course,
where we do everything very rigorously.
As we would, if we are trying to set up for
graduate school class and apply mathematics later.
Nor are we aiming for the breadth of a linear algebra or
a calculus course that would apply everywhere across science and engineering.
We're just aiming to very quickly and in a way
strongly both motivated by machine learning problems,
give you enough underpinnings to get you going.
And more than anything else, we want to develop your mathematical intuition.
That is, we have computers to do all the mathematical operations for us now.
In Python or Matlab or R.
Doing the operations and crunching through them with pen and paper,
plugging the numbers and chugging your way to the answer,
it's just not a very useful skill in the world anymore.

So, linear algebra is defined to be,
the study of vectors,
vector spaces, a mapping between vector spaces.
It emerged from the study of systems of linear equations and
the realization that these could be solved using matrices and vectors.
So the first thing we'll do,
is look at vectors and the operations we can do
with vectors and then we'll move on to look at matrices.
So that's what this course Linear Algebra is all about.
And how it relates to the other courses in this specialization are
multivariate calculus for machine learning. 

## The relationship between machine learning, linear algebra, and vectors and matrices
### Motivations for linear algebra
In this video, we're going to look a bit more at
the types of problems we might want to solve,
and expose what Linear Algebra is and how it might help us to solve them.

  * The first problem I might think of is one of price discovery.
Say I go shopping on two occasions, and I buy apples and bananas,
and the first time I buy two apples and three bananas and they cost eight Euros.
And the second time I buy say, ten apples and one banana, and the cost is 13 Euros.

$2a + 3b = 8$  

$10a + 1b = 13$

And the As and the Bs here,
are the price of a single apple and a single banana.
And what I'm going to have to do is solve these what we call
**simultaneous equations** in order to discover the price of individual apples and bananas.
Now in the general case of lots of different types of items and lots of shopping trips,
then finding out the prices might be quite hard.
It might be quite difficult to solve all these equations by hand.
So, we might want a computer algorithm to do it for us, in the general case.
Now, this is an example of a Linear Algebra problem.
I have some constant linear coefficients here, these numbers 2,
10, 3, 1, that relate the input variables A and B,
to the output 8 and 13,
that is if I think about a vector [a,b],
that describes the prices of apples and bananas.
Then this gets translated into a cost by

$\begin{bmatrix} 2 & 3 \\10 & 1 \end{bmatrix} x 
\begin{bmatrix} a \\ b \end{bmatrix} = 
\begin{bmatrix} 8 \\ 13 \end{bmatrix}$

and then these are then matrices and vectors,
and what we're going to do over the course of modules one to three, is build up,
Looking at these different types of mathematical objects,
and understanding what they are and how to work with them,
these vectors and these matrices.

  * Another type of problem we might be interested in is fitting an equation to some data.
In fact, with neural networks and machine learning,
we want the computer in effect not only to fit the equation,
but to figure out what equation to use.
That's a highly inexact description really of what's going on,
but it gives the right sort of flavor.
But let's say, we have some data like this histogram here.
This looks like a population with an average and some variation here, some width.
How to find the optimal value of the parameters in the equation describing this line?
The ones that fit the data in the histogram best.
That might be really handy, then using that equation we'd have
an easy portable description of the population we could carry around,
without needing all the original data which would free us,
for example, from privacy concerns.
Now, we can plot how good the fit was in terms of the parameters,
and that's what we'll look at in the next video.
I
