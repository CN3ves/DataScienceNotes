### Drill 1: Vectors
Create a Vector class with x and a y attributes that represent component magnitudes in the x and y directions.

Your vectors should handle vector additon with an .add() method that takes a second vector as an argument and returns a new vector equal to the sum of the vector you call .add() on and the vector you pass in.

For example:

>>> a = Vector(3, 4)
>>> a.x
3
>>> a.y
4
>>> b = Vector(1, 2)
>>> c = a.add(b)
>>> c.x
4
>>> c.y
6

Adding vectors when you have their components is easy: just add the two x components together and the two y components together to get the x and y components for the vector sum.


```
# Initial code 
class Vector(object):

# Solution
class Vector(object):
    def __init__(self, x, y):
        self.x = x
        self.y = y
        
    def add(self, b):
        return Vector(self.x + b.x, self.y + b.y)


# Tests
test.describe("Basic tests")
test.it("Vectors have correct x attributes.")
test.assert_equals(Vector(3, 4).x, 3)
test.it("Vectors have correct y attributes.")
test.assert_equals(Vector(3, 4).y, 4)
test.expect(hasattr(Vector(3, 4), "add"), "Vectors should have an .add() method.")
test.expect(isinstance(Vector(3, 4).add(Vector(1, 2)), Vector), ".add should return a vector.")
test.it("Vectors add x components correctly.")
test.assert_equals(Vector(3, 4).add(Vector(1, 2)).x, 4)
test.it("Vectors add y components correctly.")
test.assert_equals(Vector(3, 4).add(Vector(1, 2)).y, 6)


```

### Drill 2: Puzzlebox
You're given a mystery puzzlebox object. Examine it to make the tests pass and solve this kata.

```
# Initial code 
def answer(puzzlebox):
    # Print statements are your friend.
    pass
    
# Solution


The trick to this drill is finding the puzzlebox's attributes with the dir() function, then exploring each those. The attributes are answer, hint, hint_two, lock and key. The hints are designed to get you to call puzzlebox.lock(puzzlebox.key) and print the result, which tells you that the solution to the kata is to return 42 in your answer() function.

Here is example code that you could run to pass this kata is below. Your own solution (if you solved it before looking here) likely includes several additional print statements. The important part is the return value.

def answer(puzzlebox):
    return 42

The full puzzlebox class is listed below in case you're curious about it:

import random

class Puzzlebox(object):
    """Puzzlebox for codewars kata."""

    def __init__(self):
        self.key = random.randint(1, 99)

    answer = "Ha, not quite that easy.\n"

    hint = "How do you normally unlock things?\n"
        
    hint_two = "The lock attribute is a method. Have you called it with anything yet?\n"

    def lock(self, *args):
        if len(args) != 1:
            return "This method expects one argument.\n"
        elif type(args[0]) != int:
            return "This method expects an integer.\n"
        elif args[0] != self.key:
            return "Did you know the key changes each time you print it?\n"
        else:
            return "You put the key in the lock! The answer is, of course, 42. Return that number from your answer() function to pass this kata.\n"

    def __repr__(self):
        return "The built-in dir() function is useful. Continue adding print statements till you know the answer.\n"

puzzlebox = Puzzlebox()




# Tests
# No hints here, sorry.

```

### Drill 3: Quarks
Background

You're modelling the interaction between a large number of quarks and have decided to create a Quark class so you can generate your own quark objects.

[Quarks](https://en.wikipedia.org/wiki/Quark) are fundamental particles and the only fundamental particle to experience all four fundamental forces.
Your task

Your Quark class should allow you to create quarks of any valid color ("red", "blue", and "green") and any valid flavor ('up', 'down', 'strange', 'charm', 'top', and 'bottom').

Every quark has the same baryon_number (BaryonNumber in C#): 1/3.

Every quark should have an .interact() (.Interact() in C#) method that allows any quark to interact with another quark via the strong force. When two quarks interact they exchange colors.
Example

>>> q1 = Quark("red", "up")
>>> q1.color
"red"
>>> q1.flavor
"up"
>>> q2 = Quark("blue", "strange")
>>> q2.color
"blue"
>>> q2.baryon_number
0.3333333333333333
>>> q1.interact(q2)
>>> q1.color
"blue"
>>> q2.color
"red"


```
# Initial code 
class Quark(object):
    # Your code here.

# Solution
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



# Tests
q1 = Quark("red", "up")
q2 = Quark("blue", "strange")

test.describe("Object initialization")
test.assert_equals(q1.color, "red")
test.assert_equals(q2.flavor, "strange")

test.describe("Class attributes")
test.assert_equals(q2.baryon_number, 1.0 / 3)

test.describe("Quarks trade colors when interacting")
q1.interact(q2)
test.assert_equals(q1.color, "blue")
test.assert_equals(q2.color, "red")

```
