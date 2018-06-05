### Drill 1: Longest word
Complete the function that takes one argument, a list of words, and returns the length of the longest word in the list.

For example:

['simple', 'is', 'better', 'than', 'complex'] ==> 7

Do not modify the input list.

```
# Initial code 
def longest(words):
    # Your code here
  
# Solution
def longest(words):
    result = 0
    for word in words:
        if len(word) > result:
            result = len(word)
    return result

# other
def longest(words):
    # Your code here
    lengths = [len(x) for x in words]
    return max(lengths)
    
# Tests
test.assert_equals(longest(['simple', 'is', 'better', 'than', 'complex']), 7)
test.assert_equals(longest(['explicit', 'is', 'better', 'than', 'implicit']), 8)
test.assert_equals(longest(['beautiful', 'is', 'better', 'than', 'ugly']), 9)

```

### Drill 2: Grade calculator

```
# Initial code 
def calculate_grade(scores):
    # Your code here.
  
# Solution
def calculate_grade(scores):
    total = 0
    for score in scores:
        total += score
    mean_score = total / len(scores)

    if mean_score >= 90:
        return "A"
    elif mean_score >= 80:
        return "B"
    elif mean_score >= 70:
        return "C"
    elif mean_score >= 60:
        return "D"
    else:
        return "F"

# Tests
test.assert_equals(calculate_grade([92, 94, 99]), "A")
test.assert_equals(calculate_grade([50, 60, 70, 80, 90]), "C")
test.assert_equals(calculate_grade([50, 55]), "F")

```

### Drill 3: Lists of lists
You have a two-dimensional list in the following format:

data = [[2, 5], [3, 4], [8, 7]]

Each sub-list contains two items, and each item in the sub-lists is an integer.

Write a function process_data() that processes each sub-list like so:

    [2, 5] --> 2 - 5 --> -3
    [3, 4] --> 3 - 4 --> -1
    [8, 7] --> 8 - 7 --> 1

and then returns the product of all the processed sub-lists: -3 * -1 * 1 --> 3.

For input, you can trust that neither the main list nor the sublists will be empty.


```
# Initial code 
def process_data(data):
    # Your code here
  
# Solution

def process_data(data):
    result = 1
    differences = []

    for sub_list in data:
        differences.append(sub_list[0] - sub_list[1])

    for difference in differences:
        result *= difference

    return result

# Other
def process_data(data):
    # Your code here
    result = 1
    for lst in data:
        result *= (lst[0] - lst[1])
    return result
    
    
# Tests
test.assert_equals(process_data([[2, 5], [3, 4], [8, 7]]), 3)
test.assert_equals(process_data([[2, 9], [2, 4], [7, 5]]), 28)

```

### Drill 4: Inverse slicer
You're familiar with [list slicing](https://docs.python.org/3/library/functions.html#slice) in Python and know, for example, that:

>>> ages = [12, 14, 63, 72, 55, 24]
>>> ages[2:4]
[63, 72]
>>> ages[2:]
[63, 72, 55, 24]
>>> ages[:3]
[12, 14, 63]

write a function inverse_slice() that takes three arguments: a list items, an integer a and an integer b. The function should return a new list with the slice specified by items[a:b] excluded. For example:

>>>inverse_slice([12, 14, 63, 72, 55, 24], 2, 4)
[12, 14, 55, 24]

The input will always be a valid list, a and b will always be different integers equal to or greater than zero, but they may be zero or be larger than the length of the list.

```
# Initial code 
def inverse_slice(items, a, b):
    # Your code here.
  
# Solution
def inverse_slice(items, a, b):
    return items[:a] + items[b:]

# Tests
test.assert_equals(inverse_slice([12, 14, 63, 72, 55, 24], 2, 4), [12, 14, 55, 24])
test.assert_equals(inverse_slice([12, 14, 63, 72, 55, 24], 0, 3), [72, 55, 24])
test.assert_equals(inverse_slice(['Intuition', 'is', 'a', 'poor', 'guide', 'when', 'facing', 'probabilistic', 'evidence'], 5, 13), ['Intuition', 'is', 'a', 'poor', 'guide'])

```
