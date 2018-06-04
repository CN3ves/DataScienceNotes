### Drill 1: Hello world
Complete the function body for this hello() function so that it takes one argument (person, a string) and returns a string saying hello to that person. The result should be formatted so that when you call the function like this:

hello('Grae')
you return a string that looks like this:
'Hello, Grae'

```
# Initial code 
def hello(name):
    # Insert your code below.
    # Don't forget to use `return`.
    
# Solution
def hello(name):
return 'Hello, ' + name

# Tests
Test.assert_equals(hello('World'), 'Hello, World')
Test.assert_equals(hello('Grae'), 'Hello, Grae')
Test.assert_equals(hello('Dan'), 'Hello, Dan')
Test.assert_equals(hello('Alex'), 'Hello, Alex')
Test.assert_equals(hello('Bethany'), 'Hello, Bethany')
Test.assert_equals(hello('Darrell'), 'Hello, Darrell')
```

### Drill 2: Quotable
This function should take two string parameters: a person's name (name) and a quote of theirs (quote), and return a string attributing the quote to the person in the following format:

'[name] said: "[quote]"'

For example, if name is 'Grae' and 'quote' is 'Practice makes perfect' then your function should return the string

'Grae said: "Practice makes perfect"'

Unfortunately, something is wrong with the instructions in the function body. Your job is to fix it so the function returns correctly formatted quotes.

```
# Inital code
def quotable(name, quote):
    return name + quote + '"'
    
# Solution
def quotable(name, quote):
    return name + ' said: "' + quote + '"'

# Tests
test.describe('Basic Tests')
test.assert_equals(quotable('Grae', 'Practice makes perfect'), 'Grae said: "Practice makes perfect"')
test.assert_equals(quotable('Dan', 'Get back to work, Grae'), 'Dan said: "Get back to work, Grae"')
test.assert_equals(quotable('Alex', 'Python is great fun'), 'Alex said: "Python is great fun"')
test.assert_equals(quotable('Bethany', 'Yes, way more fun than R'),'Bethany said: "Yes, way more fun than R"')
test.assert_equals(quotable('Darrell', 'What the heck is this thing?'), 'Darrell said: "What the heck is this thing?"') 
```


### Drill 3: Repeater
Write a function named repeater() that takes two arguments (a string and an integer), and returns a new string where the input string is repeated that many times. For example:

repeater('a', 5)

should return

'aaaaa'

and

repeater('Na', 16)

should return

'NaNaNaNaNaNaNaNaNaNaNaNaNaNaNaNa`



```
# Inital code
def repeater(string, n):
    # Your code goes here.
    
# Solution
def repeater(string, n):
  return string * n
  
# Tests
Test.assert_equals(repeater('a', 5), 'aaaaa')
Test.assert_equals(repeater('Na', 16), 'NaNaNaNaNaNaNaNaNaNaNaNaNaNaNaNa')
Test.assert_equals(repeater('Wub ', 6), 'Wub Wub Wub Wub Wub Wub ')
```

### Drill 4: Repeater, level 2

This challenge extends the previous repeater() challenge. Just like last time, your job is to write a function that accepts a string and a number as arguments. This time, however, you should format the string you return like this:

>>> repeater('yo', 3)
'"yo" repeated 3 times is: "yoyoyo"'
>>> repeater('WuB', 6)
'"WuB" repeated 6 times is: "WuBWuBWuBWuBWuB

```
# Inital code
def repeater(string, n):
    # Your code goes here.
    
# Solution
def repeater(string, n):
    repeated = string * n
    template = '"{}" repeated {} times is: "{}"'
return template.format(string, n, repeated)

# Tests
Test.assert_equals(repeater('yo', 3), '"yo" repeated 3 times is: "yoyoyo"')
Test.assert_equals(repeater('WuB', 6), '"WuB" repeated 6 times is: "WuBWuBWuBWuBWuBWuB"')
Test.assert_equals(repeater('code, eat, code, sleep... ', 2), '"code, eat, code, sleep... " repeated 2 times is: "code, eat, code, sleep... code, eat, code, sleep... "')
```

### Drill 5: Jedi name
You just took a contract with the Jedi council. They need you to write a function, greet_jedi(), which takes two arguments (a first name and a last name), works out the corresponding Jedi name, and returns a string greeting the Jedi.

A person's Jedi name is the first three letters of their last name followed by the first two letters of their first name. For example:

>>> greet_jedi('Beyonce', 'Knowles')
'Greetings, master KnoBe'

Note the capitalization: the first letter of each name is capitalized. Your input may or may not be capitalized. Your function should handle it and return the Jedi name in the correct case no matter what case the input is in:

>>> greet_jedi('grae', 'drake')
'Greetings, master DraGr'

You can trust that your input names will always be at least three characters long.

```
# Inital code
def greet_jedi(first, last):
    # Your code goes here.
    
# Solution
def greet_jedi(first, last):
    first = first.capitalize()
    last = last.capitalize()
    jedi_name = last[0:3] + first[0:2]
    return 'Greetings, master ' + jedi_name

# Tests
Test.assert_equals(greet_jedi('Beyonce', 'Knowles'), 'Greetings, master KnoBe')
Test.assert_equals(greet_jedi('Chris', 'Angelico'), 'Greetings, master AngCh')
Test.assert_equals(greet_jedi('grae', 'drake'), 'Greetings, master DraGr')

```

### Drill 6: Areacode extractor

You've got a bunch of textual data with embedded phone numbers. Write a function area_code() that finds and returns just the area code portion of the phone number.

>>> message = "The supplier's phone number is (555) 867-5309"
>>> area_code(message)
'555'

The returned area code should be a string, not a number. Every phone number is formatted like in the example, and the only non-alphanumeric characters in the string are apostrophes ' or the punctuation used in the phone number.

```
# Inital code
def area_code(text):
    # Your code goes here
    
# Solution
def area_code(text):
    start = text.find('(') + 1
    end = text.find(')')
return text[start : end]

# Tests
Test.assert_equals(area_code("The supplier's phone number is (555) 867-5309"), '555')
Test.assert_equals(area_code("Grae's cell number used to be (123) 456-7890"), '123')
Test.assert_equals(area_code("The 102nd district court's fax line is (124) 816-3264"), '124')
```

### Drill 7: Poem formatter

You have a collection of lovely poems. Unfortuantely they aren't formatted very well. They're all on one line, like this:

Beautiful is better than ugly. Explicit is better than implicit. Simple is better than complex. Complex is better than complicated.

What you want is to present each sentence on a new line, so that it looks like this:

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.

Write a function, format_poem() that takes a string like the one line example as an argument and returns a new string that is formatted across multiple lines with each new sentence starting on a new line when you print it out.

Try to solve this challenge with the str.split() and the str.join() string methods.

Every sentence will end with a period, and every new sentence will have one space before the previous period. Be careful about trailing whitespace in your solution.

```
# Inital code
def format_poem(poem):
    # Your code goes here.
    
    
# Solution
def format_poem(poem):
    sentences = poem.split('. ')
    result = '.\n'.join(sentences)
return result

# Tests
Test.assert_equals(format_poem('Beautiful is better than ugly. Explicit is better than implicit. Simple is better than complex. Complex is better than complicated.'), 'Beautiful is better than ugly.\nExplicit is better than implicit.\nSimple is better than complex.\nComplex is better than complicated.')
Test.assert_equals(format_poem("Flat is better than nested. Sparse is better than dense. Readability counts. Special cases aren't special enough to break the rules."), "Flat is better than nested.\nSparse is better than dense.\nReadability counts.\nSpecial cases aren't special enough to break the rules.")
Test.assert_equals(format_poem("Although practicality beats purity. Errors should never pass silently. Unless explicitly silenced. In the face of ambiguity, refuse the temptation to guess."), "Although practicality beats purity.\nErrors should never pass silently.\nUnless explicitly silenced.\nIn the face of ambiguity, refuse the temptation to guess.")

```
