### Drill 1: Order filler
You're running an online business and a big part of your day is fulfilling orders. As your volume picks up that's been taking more of your time, and unfortunately lately you've been running into situations where you take an order but can't fulfill it.

You've decided to write a function fillable() that takes three arguments: a dictionary stock representing all the merchandise you have in stock, a string merch representing the thing your customer wants to buy, and an integer n representing the number of units of merch they would like to buy. Your function should return True if you have the merchandise in stock to complete the sale, otherwise it should return False.

Valid data will always be passed in and n will always be >= 1.


```
# Initial code 
def fillable(stock, merch, n):
    # Your code goes here.

# Solution
def fillable(stock, merch, n):
    try:
        return stock[merch] >= n
    except KeyError:
        return False


# Tests
stock = {
    'football': 4,
    'boardgame': 10,
    'leggos': 1,
    'doll': 5,
}
test.assert_equals(fillable(stock, 'football', 3), True)
test.assert_equals(fillable(stock, 'leggos', 2), False)
test.assert_equals(fillable(stock, 'action figure', 1), False)

```

### Drill 2: User contacts
You're putting together contact information for all the users of your website to ship them a small gift. You queried your database and got back a list of users, where each user is another list with up to two items: a string representing the user's name and their shipping zip code. Example data might look like:

[["Grae Drake", 98110], ["Bethany Kok"], ["Alex Nussbacher", 94101], ["Darrell Silver", 11201]]

Notice that one of the users above has a name but doesn't have a zip code.

Write a function user_contacts() that takes a two-dimensional list like the one above and returns a dictionary with an item for each user where the key is the user's name and the value is the user's zip code. If your data doesn't include a zip code then the value should be None.

For example, using the input above, user_contacts() would return this dictionary:

{
    "Grae Drake": 98110,
    "Bethany Kok": None,
    "Alex Nussbacher": 94101,
    "Darrell Silver": 11201,    
}

You don't have to worry about leading zeros in zip codes.


```
# Initial code 
def user_contacts(data):
    # Your code here.

# Solution
def user_contacts(data):
    result = {}
    for user in data:
        name = user[0]
        try:
            zip = user[1]
        except IndexError:
            zip = None
        result[name] = zip
return result

def user_contacts(data):
    result = {}
    for user in data:
        if len(user) == 2:
            result[user[0]] = user[1]
        else:
            result[user[0]] = None
    return result
    
# Tests
data = [["Grae Drake", 98110], ["Bethany Kok"], ["Alex Nussbacher", 94101], ["Darrell Silver", 11201]]
expected_result = {'Grae Drake': 98110, 'Darrell Silver': 11201, 'Alex Nussbacher': 94101, 'Bethany Kok': None}
test.assert_equals(user_contacts(data), expected_result)

```

### Drill 3: Multiple modes.
This drill is particularly challenging. If you're struggling with it, think about how you might use a dictionary to keep track of the number of times each letter appears in a string, using the character as the key and using the count as the value

You probably know that the "mode" of a set of data is the data point that appears most frequently. Looking at the characters that make up the string "sarsaparilla" we can see that the letter "a" appears four times, more than any other letter, so the mode of "sarsaparilla" is "a".

But do you know what happens when two or more data points occur the most? For example, what is the mode of the letters in "tomato"? Both "t" and "o" seem to be tied for appearing most frequently.

Turns out that a set of data can, in fact, have multiple modes, so "tomato" has two modes: "t" and "o". It's important to note, though, that if all data appears the same number of times there is no mode. So "cat", "redder", and [1, 2, 3, 4, 5] do not have a mode.

Your job is to write a function modes() that will accept one argument data that is a sequence like a string or a list of numbers and return a sorted list containing the mode(s) of the input sequence. If data does not contain a mode you should return an empty list.

For example:

>>> modes("tomato")
["o", "t"]
>>> modes([1, 3, 3, 7])
[3]
>>> modes(["redder"])
[]

You can trust that your input data will always be a sequence and will always contain orderable types (no inputs like [1, 2, 2, "a", "b", "b"]).


```
# Initial code 
def modes(data):
    # Your code here.

# Solution
def modes(data):

    # Empty dict we'll use to store item counts.
    counts = {}

    # Populate the dict.
    for value in data:
        if value in counts:
            counts[value] += 1
        else:
            counts[value] = 1

    # Find the number of times the mode appears.
    max_occurrence = max(counts.values())

    # Short-circuit if there is no mode.
    min_occurrence = min(counts.values())
    if max_occurrence == min_occurrence:
        return []

    # Initialize an empty list to populate and return.
    result = []
    for key in counts.keys():
        if counts[key] == max_occurrence:
            result.append(key)

return sorted(result)


# Tests
test.assert_equals(modes("tomato"), ["o", "t"])
test.assert_equals(modes([1, 3, 3, 7]), [3])
test.assert_equals(modes(["redder"]), [])

```

