# Pandas

Pandas is probably the most heavily utilized package in Python for data scientists. Built on top of NumPy, it is essential to data manipulation, organization, and modeling. Here we'll introduce some of its core functionalities as well as its primary data structure: the data frame. First we have to import the package, which typically gets the abbreviation pd. We'll also import NumPy here.

import pandas as pd

import numpy as np

The Data Frame

The data frame is like a NumPy array, with a few additional features like column names and row indexing. It is probably the primary way data scientists handle data. You can create a data frame in many different ways, either from csv files, by querying databases, or explicitly. For your first data frame, let's recall the 2-dimensional array we created in the previous assignment. To create a data frame use the pd.DataFrame() function and pass in a NumPy array:

my_array = np.array([[0, 1, 2, 3], [4, 5, 6, 7]])

df = pd.DataFrame(my_array)

df

	0 	1 	2 	3
0 	0 	1 	2 	3
1 	4 	5 	6 	7

Now you have your first data frame!

If you're familiar with Excel, much of Pandas may be familiar to you. Data frames are organized into rows and columns that are nameable. Columns are labeled with column names, rows with an index number (starting with zero by default). You can set both column names and indexes explicitly during the creation of the data frame or after the fact. Let's set both for df from above.

df.columns = ['first', 'this', 'that', 'last']

df.index = ['row_1', 'row_2']

df

	first 	this 	that 	last
row_1 	0 	1 	2 	3
row_2 	4 	5 	6 	7

There, that looks better.

You can also set column and index names through the column= or index= keyword arguments when you call the pd.DataFrame() function to initially construct the data frame.

df2 = pd.DataFrame(

    my_array,

    columns=['first', 'this', 'that', 'last'],

    index=['row_1', 'row_2'])

df2

	first 	this 	that 	last
row_1 	0 	1 	2 	3
row_2 	4 	5 	6 	7

Whichever method you use, we now have a data frame with labeled rows and columns. This will be useful for working with data frames, because it makes these elements easily callable and makes your code more natural to write and simpler to read.
Note: you're probably used to seeing a space around = when used for assignment and ==, which is used for comparison. 
In Python, the custom is to [omit spaces](https://www.python.org/dev/peps/pep-0008/#other-recommendations) 
around = with keyword arguments to improve readability and make it easy to distinguish keyword arguments from variable assignments.
Adding More Data

To show what data frames can really do we're going to need to make something a little bit bigger. Let's assemble a data frame with named columns via lists. You can create an empty data frame by calling the pd.DataFrame() function and passing in the indexes you'd like to use for row names, then add columns using df['COLUMN_NAME'] = [LIST_OF_VALUES]. For example:

# This list will become our row names.

names = ['George',

         'John',

         'Thomas',

         'James',

         'Andrew',

         'Martin',

         'William',

         'Zachary',

         'Millard',

         'Franklin']

​

# Create an empty data frame with named rows.

purchases = pd.DataFrame(index=names)

​

# Add our columns to the data frame one at a time.

purchases['country'] = ['US', 'CAN', 'CAN', 'US', 'CAN', 'US', 'US', 'US', 'CAN', 'US']

purchases['ad_views'] = [16, 42, 32, 13, 63, 19, 65, 23, 16, 77]

purchases['items_purchased'] = [2, 1, 0, 8, 0, 5, 7, 3, 0, 5]

purchases 

	country 	ad_views 	items_purchased
George 	US 	16 	2
John 	CAN 	42 	1
Thomas 	CAN 	32 	0
James 	US 	13 	8
Andrew 	CAN 	63 	0
Martin 	US 	19 	5
William 	US 	65 	7
Zachary 	US 	23 	3
Millard 	CAN 	16 	0
Franklin 	US 	77 	5

Let's say this is the purchase and browsing history for several users of an ecommerce website for a given year. Page views is the number of pages they've loaded on the site and purchases is the number of items they've bought that year.

Now we have a data frame we can do something with. First note that you can call out a column as a series using either dot notation or bracket notation: df.column_name or df['column_name'] both work. So purchases['Name'] returns the names of users who visited the ecommerce website, as does purchases.Name. Bracket notation is generally preferred and we'll use bracket notation here.

Pandas also makes it very easy to create a new column out of our previous data. Let's say we want to create a column of the average items purchased per page view, and call the column items_purch_per_view. We can do that with this one-liner:

purchases['items_purch_per_ad'] = purchases['items_purchased'] / purchases['ad_views']

purchases

	country 	ad_views 	items_purchased 	items_purch_per_ad
George 	US 	16 	2 	0.125000
John 	CAN 	42 	1 	0.023810
Thomas 	CAN 	32 	0 	0.000000
James 	US 	13 	8 	0.615385
Andrew 	CAN 	63 	0 	0.000000
Martin 	US 	19 	5 	0.263158
William 	US 	65 	7 	0.107692
Zachary 	US 	23 	3 	0.130435
Millard 	CAN 	16 	0 	0.000000
Franklin 	US 	77 	5 	0.064935

If we just want to see those values and don't need to store them as a new column in our data frame we can just run that function without assigning it to purchases['items_purch_per_ad'] and it will return labeled values giving the name and the purchases per ad for each user.

purchases['items_purchased'] / purchases['ad_views']

George      0.125000
John        0.023810
Thomas      0.000000
James       0.615385
Andrew      0.000000
Martin      0.263158
William     0.107692
Zachary     0.130435
Millard     0.000000
Franklin    0.064935
dtype: float64

This is a brief introduction to how indexes and columns can work together in Pandas to create robust but easy to use data frames. We'll do much more with these throughout the course.


## Selecting and Grouping
import pandas as pd

import numpy as np

​

# Reload example data from last assignment. 

names = ['George',

         'John',

         'Thomas',

         'James',

         'Andrew',

         'Martin',

         'William',

         'Zachary',

         'Millard',

         'Franklin']

purchases = pd.DataFrame(index=names)

purchases['country'] = ['US', 'CAN', 'CAN', 'US', 'CAN', 'US', 'US', 'US', 'CAN', 'US']

purchases['ad_views'] = [16, 42, 32, 13, 63, 19, 65, 23, 16, 77]

purchases['items_purchased'] = [2, 1, 0, 8, 0, 5, 7, 3, 0, 5]

A data frame is great in and of itself. As we've shown, it allows you to easily store data with clearly labeled rows and indexes. However, sometimes you just want to work with a subset of that data. For that you will want to either select or group data.

We've actually already introduced the most basic form of indexing, or "selection" with the bracketed selection of column names. Recall what we did before on our purchases data:

purchases['country']

George       US
John        CAN
Thomas      CAN
James        US
Andrew      CAN
Martin       US
William      US
Zachary      US
Millard     CAN
Franklin     US
Name: country, dtype: object

Which returns the data from the column named "country". However, for more sophisticated selection we will need to use the Pandas dataframe indexing methods.
Basic Selects with .loc and .iloc

.loc is a selector that indexes over rows and columns. It selects over the row index first, then the column name (if included). .iloc does the same thing but over indices. For example, to select the row for 'George' in our purchases data frame, we just pass the string 'George' in to purchases.loc with bracket notation:

purchases.loc['George']

country            US
ad_views           16
items_purchased     2
Name: George, dtype: object

To select the column 'country' we would use:

purchases.loc[:, 'country']

George       US
John        CAN
Thomas      CAN
James        US
Andrew      CAN
Martin       US
William      US
Zachary      US
Millard     CAN
Franklin     US
Name: country, dtype: object

The : above works just like it would when slicing a list or string, and selects all rows from start to finish of the data frame.

Lastly to select George's country, we'd combine the two like this:

purchases.loc['George', 'country']

'US'

As we mentioned above, you can also do integer indexing, as done on lists, over both rows and columns using .iloc. For example:

purchases.iloc[1:3, 1]

John      42
Thomas    32
Name: ad_views, dtype: int64

Note we used the slicing syntax again above, this time starting with the second row and going up to, but not including, the fourth row, and then the second column (with the index not counting as a column).
Conditional Selection

You can also use .loc for conditional selection, or selecting all the entries that meet a given criteria. This will use lambda, which is a construction that allows for defining anonymous, unnamed functions at runtime. We use the lambda function to create a condition on the row or column.
Note: We'll introduce the lambda syntax below but won't use it much in the prep course and won't go deeply 
into it here. If you're interested in learning more about using lambda to create anonymous functions 
see the terse [Python documentation tutorial section on lambda](https://docs.python.org/3.6/tutorial/controlflow.html#lambda-expressions), 
or this [more detailed tutorial](https://pythonconquerstheuniverse.wordpress.com/2011/08/29/lambda_tutorial/).

Let's return once more to the purchases data frame. For our example, let's say we want all the columns for individuals who made more than one purchase. That ends up being a relatively simple line of code.

purchases.loc[lambda df: purchases['items_purchased'] > 1, :]

	country 	ad_views 	items_purchased
George 	US 	16 	2
James 	US 	13 	8
Martin 	US 	19 	5
William 	US 	65 	7
Zachary 	US 	23 	3
Franklin 	US 	77 	5

We are selecting rows, so the lambda is the first item in the brackets. We define the input df as it takes a data frame. Then we define the condition for which each row will be evaluated on. The , : is the same slicing syntax and means we want all columns using the same logic as above.

There is a simpler way to do this, using boolean logic, and it is also quite common.

purchases[purchases['items_purchased'] > 1]

	country 	ad_views 	items_purchased
George 	US 	16 	2
James 	US 	13 	8
Martin 	US 	19 	5
William 	US 	65 	7
Zachary 	US 	23 	3
Franklin 	US 	77 	5

This is a similar logic, but the lack of explicit indexing makes it slightly less robust. 
The first example with .loc using explicit indexing is more robust, but this latter 
[boolean indexing](http://pandas.pydata.org/pandas-docs/stable/indexing.html#boolean-indexing) 
may be more common and is easily readable. Choose your tradeoffs wisely.
Groups

There's one last thing we'll introduce here, and that is grouping and aggregation. You can create groups in your data frame using the .groupby() method and passing in the column name. Let's try it.

If we wanted to group by the country of the site user, all we'd have to do is:

purchases.groupby('country')

<pandas.core.groupby.DataFrameGroupBy object at 0x106fb9048>

But wait, when you run that line, it doesn't return your data any more. It returns a line that references a grouped object, but not the object.

That's because if we want it to return something we have to do something on those groups. There are several methods that you can use here. Some are built in like .sum() or .count(). For even greater possibilities you can use .aggregate(numpy_function). Let's use this to find out which group has more page views and purchases.

purchases.groupby('country').aggregate(np.mean)

​

# Don't want to take the mean of all columns? Try this:

# purchases.groupby('country')['column_name'].mean()

	ad_views 	items_purchased
country 		
CAN 	38.25 	0.25
US 	35.50 	5.00

Now you can see the mean of each column. Seems like Canadian visitors view slightly more ads per person but purchase far fewer items...

These are the fundamentals of selecting data inside a data frame. 
For a deep dive, see the [pandas documentation on Indexing and Selecting Data](http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing).

## Working with Files
In the examples so far we built Pandas data frames by manually typing or pasting in text. 
Doing that with actual data sets would be tedious or impossible, so you'll almost always be loading 
your data into Pandas from files (like CSV files), from the web using APIs, or from databases and other 
large data stores.

We'll cover APIs and databases in the bootcamp. In this assignment we'll show you how to load 
CSV, JSON, and XML files you've generated or downloaded into Pandas. 
We'll also briefly discuss working with files using vanilla Python.

When your files are well-encoded and correctly formatted and your data is clean, loading files is pretty straightforward. But that's not always the case. Dealing with malformed data is one of the largest challenges of being a data scientist, and there's no one-size-fits-all solution. Here we're going to cover the easy cases and point you towards further reading if you need it for your capstone. Your goal in this assignment is not to memorize the process for dealing with every use case, but to get an overview of the process, be comfortable working with simple files, and have a reference that you can come back to later if and when you need it.

We'll give you several example files to play with in this assignment. Go ahead and create a 
directory on your computer now where you'll store these files. You can download a 
zip with each example [here](https://gist.github.com/Grae-Drake/89c19c54077b818ea69d314e74bb6fbf), or download each file one by one below.
Opening files with Pandas
CSV files

CSV files, or "Comma Separated Values" files, are a common file format for structured tabular data. They're easy to produce from Microsoft Excel, Google Sheets, and Python scripts. They're also simple to work with: you can open and read them in any text editor. If you do that you'll see that a CSV is just a text file where the values in each column are separated by commas, and the rows are separated from one another with newlines. Because of their convenient structure and simplicity CSV's are extremely common to work with.

Here's a sample CSV file with the same [purchase data](https://gist.githubusercontent.com/Grae-Drake/89c19c54077b818ea69d314e74bb6fbf/raw/b259f6241c5ca9c5a3b6235bdfb260eb0d99314f/purchases.csv) you saw in the previous assignment. If you don't have it already, save a copy of this file by right-clicking in your browser and choosing "Save As". Name it purchases.csv and place it in the same directory as your Python files.

The basics of loading a CSV into Pandas are simple. You can load the purchases.csv file you just saved with this one-liner:

>>> import pandas as pd
>>> df = pd.read_csv('purchases.csv')
>>> print(df)
  Unnamed: 0 country  ad_views  items_purchased
0     George      US        16                2
1       John     CAN        42                1
2     Thomas     CAN        32                0
3      James      US        13                8
4     Andrew     CAN        63                0
5     Martin      US        19                5
6    William      US        65                7
7    Zachary      US        23                3
8    Millard     CAN        16                0
9   Franklin      US        77                5

The Pandas read_csv() method takes a string representing the path to the file you want to read and returns a data frame object. In the example above the CSV file we're working with is in the same directory as the script we're running. If you saved your file elsewhere or with a different name you'll have a different path than 'purchases.csv'.

Try loading purchases.csv in your own Jupyter notebook now.
If your environment isn't set up for that yet or you're running into trouble you can play 
with this [interactive example](https://trinket.io/python3/27033bfb61).

The only required argument for read_csv() is the file path, but there are dozens of optional 
keyword arguments available that are useful in different contexts. 
You can read about those in the[ documentation](http://pandas.pydata.org/pandas-docs/stable/io.html#csv-text-files).

Working as a data scientist you'll frequently want to output data to a file. CSV's are likely your best bet for that. To create a CSV file and write your data frame to it use .to_csv():

>>> df.to_csv('my_data.csv')

The only argument passed in to .to_csv()above is the path for the file you'd like to output,
but there are a number of [optional keyword arguments](http://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.to_csv.html)
you can use to tweak your output file. You can also omit the path entirely to skip the file creation and return a string that you could paste or pipe elsewhere.

Time for you to give this a shot. Choose a file name and location where you'd like to output a CSV. Look over the .to_csv() options linked above and choose some options you'd like to tinker with. Then, using the appropriate path, your data frame in your Jupyter notebook, and the options you've chosen, create a CSV file. Find and open your file using your favorite text editor. Did it work? Does everything look like you'd expect?
JSON

While CSV files give you a nice (but rigid), built-in tabular structure with rows and columns, other common formats like JSON and XML allow for more customizable and flexible data storage. Unlike raw unstructured text, JSON and XML do have some structure requirements and are known as semi-structured files.

This flexibility of semi-structured data often comes at the cost of additional complexity. 
JSON data can be deeply nested and may take substantial processing before you can get it into 
the form you want to work with. We'll cover that in more detail in the bootcamp. 
For now we'll give you the same purchases data you've been using in JSON format. 
If you don't already have it, download this [purchases.json](https://gist.githubusercontent.com/Grae-Drake/89c19c54077b818ea69d314e74bb6fbf/raw/27aba85593a688b47ec141d0d6e7f60a9e9d33a9/purchases.json) file.

JSON stands for "JavaScript Object Notation" and is a way to represent a JavaScript object as a string. "Objects" in JavaScript are just collections of key-value pairs, exactly like Python dictionaries. Almost everything you know about Python dictionaries translates directly to JavaScript objects, so you can imagine that "JSON" stands for "Python Dictionary Notation" and treat JSON as if it's a string representation of a Python dictionary.

Like CSV files, JSON files are human readable and you should be able to open and explore them with your favorite text editor. This is particularly useful when you work with new JSON and you aren't sure how it's structured. Opening files in your text editor can get tricky with very large JSON files which are too big to fit in your computer's memory, but we won't worry about that for now.

You can create a data frame from a JSON file with read_json():

>>> import pandas as pd
>>> df = pd.read_json('purchases.json')

Again, the only required argument is the file path, but you can pass in other keyword arguments 
to run read_json() with different options. 
[See the docs](https://courses.thinkful.com/data-201-prepv1/assignment/2.1.4) 
for more details, and look into pandas.io.json.json_normalize() for 
[normalizing](http://pandas.pydata.org/pandas-docs/stable/io.html#normalization) nested JSON.

Try loading purchases.json in your own Jupyter notebook, or see this interactive example if needed.

You should generally prefer CSV for outputting your data frames into files, but you can use .to_json to output a data frame as a JSON file:

>>> df.to_json('my_data.json')

The more common use case is to send JSON data over the web. For that we'd call to_json() 
without a path argument to create a JSON string that we'd later process and send:

>>> serialized_purchases = df.to_json()

We'll cover networking and using JSON like this in the bootcamp. If you'd like a preview of that check out the 
Requests module, the only [Non-GMO HTTP library for Python](http://docs.python-requests.org/en/master/).
XML

XML, or "eXtensible Markup Language", like JSON, is a hierarchical semi-structured data format. They are both widely used to transfer data over the web, but the newer JSON format is more common these days than the older and clunkier XML format. If you've worked with HTML then the XML syntax of opening and closing tags wrapping, or "marking up", data will be familiar. Here's an XML file with our purchases data: [purchases.xml](https://gist.githubusercontent.com/Grae-Drake/89c19c54077b818ea69d314e74bb6fbf/raw/a0b46f7f996dd0c5e6a7bfdd9af192108f3f3060/purchases.xml).

Pandas doesn't have an XML equivalent to read_csv() and read_json, so we'll use the xml module from the Python standard library to read in XML files and convert them to an element tree. Once we have an element tree we'll manually process it into a list that we can feed into Pandas.
```
# Import Pandas and a part of the xml module.
import pandas
import xml.etree.ElementTree as ET


# Load and parse the XML file into a tree.
tree = ET.parse('purchases.xml')

# Find the root of the tree. This is the node of the tree where we'll
# start our iteration.
root = tree.getroot()

# Define a custom function to loop over our tree, extract values, and
# return a two-dimensional list.
def xml_to_list(root):
    result = []
    for row in root:
        row_list = []
        for column in row:
            row_list.append(column.text)
        result.append(row_list)
    return result
    
# Feed our two-dimensional list into Pandas.
df = pandas.DataFrame(xml_to_list(root))
print(df)

```
The custom xml_to_list() function above is designed for the specific XML file we're working with. If you're working with differently structured XML then you'll need to iterate over your XML tree differently.

We aren't going to go into detail here about element trees and iterating over tree objects.
You can read more at the official 
[xml.etree.ElementTree tutorial](https://docs.python.org/3.6/library/xml.etree.elementtree.html) 
if you like. If you find yourself working with XML in any detail you'll want to check out the 
[lxml package](http://lxml.de/index.html), 
a fast and useful collection of tools for working with XML.

As a data scientist you frequently don't get to choose the format of data files you're given, which is why we're covering XML here. When generating data files you should probably avoid XML because it can take more work to process. CSV's are the top choice for writing data to a file. If you need a semi-structured format, prefer JSON over XML.

Python open()

Each of the file loading techniques we covered above are package-specific ways to open and load files of one particular type (CSV, JSON, XML). Python offers a more general-purpose way to open any files you like with the built-in open() function. Here's a simple text file for you to play with if you don't already have it: [poem.txt](https://gist.githubusercontent.com/Grae-Drake/89c19c54077b818ea69d314e74bb6fbf/raw/27aba85593a688b47ec141d0d6e7f60a9e9d33a9/poem.txt)

```
# Let's open the poem.txt file, create a file object, and print out the
# file text line by line.
# Note the poem.txt tab above.
with open('poem.txt') as poem_file:
    text = poem_file.readlines()
    print("This file is {} lines long".format(len(text)))
    for line in text:
        print(line)

# Try loading and printing the purchases.csv file line by line just
# just like we did for poem.txt.



```
In the example above we use the [open()](https://docs.python.org/3/library/functions.html#open) 
function to create a file object that we can then work with. We then use the .readlines() method of the file object to create list of strings, where each element of the list is a line of text from our input file. You can read more about .readlines() and other file object methods in the [I/O documentation](https://docs.python.org/3/library/io.html#i-o-base-classes).

Opening a file with open() will leave it open until you close it. The .close() file object method will close a file. It's super easy to forget to manually close files, which can keep resources tied up and cause unexpected trouble. 
Luckily, Python gives us the [with](https://docs.python.org/3/reference/compound_stmts.html#with) statement you see used above so we don't have to remember to use .close(), because files opened in a with statement will automatically be closed once the with statement exits. Using with when manually opening files is best practice and you should plan on doing that each time you use open() unless you have a compelling reason not to.

Almost all of the data files you produce as a data scientist will be CSV or JSON files, so we won't cover using built-in Python I/O to write to files. If you'd like additional resources on any of these topics check out the 
[reading and writing files](https://docs.python.org/3/tutorial/inputoutput.html#reading-and-writing-files) section of the official Python tutorial.

A word about encoding

All of the files you've worked with seem to be made of human-readable characters, but when you get down to it everything is stored as bits, collections of ones and zeros. Which of course raises the questions: how do you know which characters you can use, and how do you translate the ones and zeros into those particular characters?

Today there is a clear answer: Unicode and UTF-8. All strings in Python 3 are Unicode strings, and 
[UTF-8](https://en.wikipedia.org/wiki/UTF-8) is the default encoding Python uses whenever possible. However, you're certain to run across files created with different encodings, whether that's because the files are old, the software used to create them is old, or because the 
[proprietary software used to create your CSV files](https://stackoverflow.com/questions/508558/what-charset-does-microsoft-excel-use-when-saving-files) 
is mired in legacy cruft. Unfortunately, it's not possible to automatically determine a file's encoding and then decode it correctly. When encountering encoding errors you'll need to make educated guesses about the likely encoding and use trial and error to test.

As hinted above, Microsoft Windows is a big culprit here. 
English-language versions of Windows use the[ cp1252](https://en.wikipedia.org/wiki/Windows-1252) encoding, 
Cyrillic versions of Windows use [cp1251](https://en.wikipedia.org/wiki/Windows-1251), and so on. 
Here is a full reference list of [Windows "Code Pages"](https://en.wikipedia.org/wiki/Windows_code_page), 
and here is a larger list of [historical encodings](http://unicodebook.readthedocs.io/historical_encodings.html). 
If you're unable to manually determine the encoding of your file you can attempt a statistical detection with 
[Chardet](https://pypi.python.org/pypi/chardet).

Unicode is a deep topic that's closely tied to the history of computing. If you're interested in a quick practical and historical overview the [Unicode HOWTO in the Python documentation](https://docs.python.org/3/howto/unicode.html) makes for excellent reading.
