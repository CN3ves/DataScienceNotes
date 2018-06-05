### Drill 1: Rømer temperature
You're writing an excruciatingly detailed alternate history novel set in a world where 
[Daniel Gabriel Fahrenheit](https://en.wikipedia.org/wiki/Daniel_Gabriel_Fahrenheit) was never born.

Since Fahrenheit never lived the world kept on using the 
[Rømer scale](https://en.wikipedia.org/wiki/R%C3%B8mer_scale), 
invented by fellow Dane 
[Ole Rømer](https://en.wikipedia.org/wiki/Ole_R%C3%B8mer) 
to this very day, skipping over the Fahrenheit and Celsius scales entirely.

Your magnum opus contains several thousand references to temperature, but those temperatures are all currently in degrees Celsius. You don't want to convert everything by hand, so you've decided to write a function, celsius_to_romer() that takes a temperature in degrees Celsius and returns the equivalent temperature in degrees Rømer.

For example: celsius_to_romer(24) should return 20.1.


```
# Initial code 
function celsiusToRomer(temp) {

}
    
# Solution
def celsius_to_romer(temp):
  return temp * 21 / 40 + 7.5

# Tests
describe("Celsius to Romer", function(){
  it("Basic testing", function(){
    Test.assertEquals(celsiusToRomer(24), 20.1);
    Test.assertEquals(celsiusToRomer(8), 11.7);
    Test.assertEquals(celsiusToRomer(29), 22.725);
  });
});
```

### Drill 2: Pixelart planning
You're laying out a rad pixel art mural to paint on your living room wall in homage to 
[Paul Robertson](http://68.media.tumblr.com/0f55f7f3789a354cfcda7c2a64f501d1/tumblr_o7eq3biK9s1qhccbco1_500.png), 
your favorite pixel artist.

You want your work to be perfect down to the millimeter. You haven't decided on the dimensions of your piece, how large you want your pixels to be, or which wall you want to use. You just know that you want to fit an exact number of pixels.

To help decide those things you've decided to write a function, is_divisible() that will tell you whether a wall of a certain length can exactly fit an integer number of pixels of a certain length.

Your function should take two arguments: the size of the wall in millimeters and the size of a pixel in millimeters. It should return True if you can fit an exact number of pixels on the wall, otherwise it should return False. For example is_divisible(4050, 27) should return True, but is_divisible(4066, 27) should return False.

Note: you don't need to use an if statement here. Remember that in Python an expression using the == comparison operator will evaluate to either True or False:

>>> def equals_three(num):
>>>     return num == 3
>>> equals_three(5)
False
>>> equals_three(3)
True


```
# Initial code 
function isDivisible(wallLength, pixelSize){
  //your code here
}
    
# Solution
def is_divisible(wall_length, pixel_size):
  return wall_length % pixel_size == 0

# Tests
Test.describe("Basic tests",_=>{
Test.assertEquals(isDivisible(4050, 27), true);
Test.assertEquals(isDivisible(4066, 27), false);
Test.assertEquals(isDivisible(10000, 20), true);
Test.assertEquals(isDivisible(10005, 20), false);
Test.assertEquals(isDivisible(10005, 1), true);
})
```

### Drill 3: Blue and red marbles
You and a friend have decided to play a game to drill your statistical intuitions. The game works like this:

You have a bunch of red and blue marbles. To start the game you grab a handful of marbles of each color and put them into the bag, keeping track of how many of each color go in. You take turns reaching into the bag, guessing a color, and then pulling one marble out. You get a point if you guessed correctly. The trick is you only have three seconds to make your guess, so you have to think quickly.

You've decided to write a function, guess_blue() to help automatically calculate whether you should guess "blue" or "red". The function should take four arguments:

    the number of blue marbles you put in the bag to start
    the number of red marbles you put in the bag to start
    the number of blue marbles pulled out so far, and
    the number of red marbles pulled out so far.

guess_blue() should return the probability of drawing a blue marble, expressed as a float. For example, guess_blue(5, 

```
# Initial code 
def guess_blue(blue_start, red_start, blue_pulled, red_pulled):
    # Your code here.
    
# Solution
def guess_blue(blue_start, red_start, blue_pulled, red_pulled):
    blue_remaining = blue_start - blue_pulled
    red_remaining = red_start - red_pulled
return blue_remaining / (blue_remaining + red_remaining)

# Tests
Test.assert_equals(guess_blue(5, 5, 2, 3), 0.6)
Test.assert_equals(guess_blue(5, 7, 4, 3), 0.2)
Test.assert_equals(guess_blue(12, 18, 4, 6), 0.4)
```

### Drill 4: Congo pizza
Your company, 
[Congo Pizza](http://interesting-africa-facts.com/Africa-Landforms/Congo-Rainforest-Facts.html), 
is the second-largest online frozen pizza retailer. You own a number of international warehouses that you use to store your frozen pizzas, and you need to figure out how many crates of pizzas you can store at each location.

Congo recently standardized its storage containers: all pizzas fit inside a cubic crate, 16-inchs on a side. The crates are super tough so you can stack them as high as you want.

Write a function box_capacity() that figures out how many crates you can store in a given warehouse. The function should take three arguments: the length, width, and height of your warehouse (in feet) and should return an integer representing the number of boxes you can store in that space.

For example: a warehouse 32 feet long, 64 feet wide, and 16 feet high can hold 13,824 boxes because you can fit 24 boxes across, 48 boxes deep, and 12 boxes high, so box_capacity(32, 64, 16) should return 13824.


```
# Initial code 
def box_capacity(length, width, height):
    # Your code here.
    
# Solution
def box_capacity(length, width, height):
    boxes_long = length * 12 // 16
    boxes_wide = width * 12 // 16
    boxes_high = height * 12 // 16
    return boxes_long * boxes_wide * boxes_high

# Tests
describe("Testing boxCapacity", function(){
  it("Basic tests", function(){
    Test.assertEquals(boxCapacity(32, 64, 16), 13824);
    Test.assertEquals(boxCapacity(20, 20, 20), 3375);
    Test.assertEquals(boxCapacity(80, 40, 20), 27000);
  });
});
```

### Drill 5: Quadratic formula
Remember all those quadratic equations you had to solve by hand in highschool? 
Well, no more! You're going to solve all the quadratic equations you might ever[1] have to 
wrangle with in the future once and for all by coding up the 
[quadratic formula](https://en.wikipedia.org/wiki/Almighty_formula) 
to handle them automatically.

Write a function quadratic_formula() that takes three arguments, a, b, and c that represent the coefficients in a formula of the form ax^2 + bx + c = 0. Your function shoud return a list with two elements where each element is one of the two roots. If the formula produces a double root the result should be a list where both elements are that value.

For example, quadratic_formula(2, 16, 1) should return the list [-0.06299606299409444, -7.937003937005906]. The order of the roots is not important.

[1] Well, not ever ever. You don't need to worry about getting quadratic equations with complex roots where you need the square root of a negative number. All the test cases will be for equations with real roots.


```
# Initial code 
def quadratic_formula(a, b, c):
    
    root1 = # Put -b + something something here.
    
    root2 = # Put -b - something something here.
    
    return [root1, root2]

    
# Solution
def quadratic_formula(a, b, c):
    
    root_of_square = ((b ** 2) - 4 * a * c) ** .5
    
    root1 = (-b + root_of_square) / (2 * a)
    root2 = (-b - root_of_square) / (2 * a)
    
return [root1, root2]

# Tests
def test_roots(actual, expected):
    a, b = sorted(actual), sorted(expected)
    Test.expect(almost_equals(a[0], b[0]) and almost_equals(a[1], b[1]),
        "roots should be almost equal\nRecieved {}\nExpected {}".format(a, b))

Test.describe("Basic tests")
test_roots(quadratic_formula(2, 16, 1), [-7.937003937005906, -0.06299606299409444])
test_roots(quadratic_formula(4, 21, 3), [-5.103028450199876, -0.14697154980012384])
test_roots(quadratic_formula(6, 81, 3), [-13.462860791048776, -0.037139208951224134])
```
