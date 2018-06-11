# Statistics for Data Science

Statistics, or the collection, analysis, and interpretation of data, is an integral part of the data scientist's knowledge base.

## Summarizing Data

We'll start this introduction to statistics by describing the process of going from large datasets to compact summaries that people can understand and use. We will talk about how data scientists use statistical summaries to describe larger groups of interest, called populations, and how they choose the best statistics to summarize different aspects of a dataset.

### Population vs Sample

A major purpose of data science is to give us information about some group, known as a population. This population can be all the people living in a country, all the purchases made at a store, or any other unit from which information can be drawn. Often, it is difficult, prohibitively expensive, or simply impossible to get data from all members of a population.

Instead, we randomly extract a subset from the population (a random group of people, a random selection of purchases), called a sample, that we can study in detail to learn about the population as a whole.
Statisticians take data about a sample and reduce the complexity of that data into understandable and accurate summaries, known as statistics. Statisticians use the sample statistics to infer information about the entire population from which the sample is taken.

### Measures of Central Tendency

Statistics can describe either an individual variable or the relationships among two or more variables. A variable represents information about a particular measurable concept (temperature, price, size, etc). Each measurement within a variable is called a datapoint.
```
import pandas as pd

# Make a blank data frame.
df = pd.DataFrame()

# Populate it with data.
df['age'] = [28, 42, 27, 24, 35, 54, 35, 37]
```
When describing individual variables, the two characteristics of most interest are the central tendency and the variance. We'll cover central tendency in this assignment and variance in the next. 

The central tendency describes a point around which datapoints in a variable cluster. Central tendency can be measured in a number of ways. The most common measures are the mean the median, and the mode. 

Mean

The mean represents the average value within a variable, and is computed as the sum of the individual datapoints in a variable x divided by the total number of values in a variable n. It is sometimes also referred to as the "expected value" of a variable.

mean = sum(x) / n

Here are two ways you can compute the mean of our age data, first with built-in Python functionality and then with NumPy.

# Using built-in Python functionality.
sum(df['age']) / len(df['age'])

# Using NumPy
import numpy as np

np.mean(df['age'])

The mean is easy to understand and commonly used, but it's sensitive to extreme values: one abnormally large value in a set of otherwise small values will cause the mean to become much larger.
Median

The median represents the middle value in a variable when the values are ordered from least to greatest. If there are an odd number of values in a variable, then the median is the middle value, and if there are an even number of values in a variable, the median represents the average of the two middlemost values.

Here's how you can compute the median of our age data using the statistics module of the Python standard library or NumPy.

# Vanilla Python, using the built-in statistics module.
import statistics

statistics.median(df['age'])

# Using NumPy.
import numpy as np

np.median(df['age'])

The median, like the mean, easy to understand, and has the added benefit that it isn't sensitive to extreme values. However, the median has fewer useful mathematical properties than the mean as we'll see later.
Mode

The mode represents the value in a variable that occurs the most frequently.

# Return the mode using the statistics module.
import statistics
statistics.mode(df['age'])

If two or more values in a variable occur with equal frequency, there will be multiple modes. Note the code above will raise a StatisticsError if you run it on data containing multiple modes. Receiving this error, or generating and inspecting a list of counts beforehand, will show whether there is more than one mode to look for.

# Generate a list of unique elements along with how often they occur.
(values, counts) = np.unique(df['age'], return_counts=True)

# The location in the values list of the most-frequently-occurring element.
ind = np.argmax(counts)

# The most frequent element.
values[ind]

The code above will handle data with multiple modes without raising an exception, but you'll get back just the first mode. If you want to push your understanding of Python you can challenge yourself to revise it to give you all of the modes.
Quick note about bias

The mean, median and mode calculated from a sample are considered unbiased estimates of the population mean, median and mode. An estimate is "unbiased" if, across multiple representative samples, the sample estimates converge on the population value. A "biased" estimate would converge on a value that was either higher or lower than the population value.

Unbiased estimates are useful because they let us use a small group of observations to make generalizations about a much larger group.

### Measures of Variance

Variance

While measures of central tendency are important, on their own they are not enough to describe a variable. Another piece of information is equally vital: variance.

The variance of a variable describes how much values differ from the central tendency, and how much they differ from each other. If all the values in a variable are close to the central tendency, then variance is said to be low. If values in a variable vary widely, with some far away from the central tendency, variance is said to be high.

Another way to think of variance is that it gives a clue to how valuable each individual datapoint is within a variable. If variance is low and most datapoints are similar to the central tendency, then each individual datapoint provides little new information about the concept being measured. If variance is high, then each individual datapoint is more likely to provide unique information about the concept being measured.
While some people tend to be more interested in measures of central tendency like the mean, data scientists are usually just as excited about the variance. This is because data scientists generally want to answer questions about why things are different from each other: Why is this store's profit margin so much higher than the others? Why is this medicine's rate of side effects so much lower than others in the same trial? Why do some customers spend so much more time on the company website? A variable with lots of variance provides information about differences between observations that data scientists can use to understand and predict future outcomes.

Variance v is measured as the sum of the squared difference of each individual datapoint x from the mean, divided by the number of datapoints n minus 1.

v = sum((x - mean) ** 2) / (n - 1)

There are two peculiarities about how variance is calculated. First, why is the difference between x and the mean squared? And second, why divide by n - 1 and not n?

One point to note is that the average of the differences between each value and the mean is zero (approximately half the differences would be negative and half positive, and cancel each other out), which isn't very useful. Squaring the differences makes all values positive so that the negative values no longer cancel out the positive ones. Of course, we could just take the absolute value of each difference, which would be another way to solve the problem of negative and positive values canceling each other out. It turns out that squaring the differences has other mathematical advantages over taking the absolute value, however, that we will discuss later.

Estimates of sample variance divide by n - 1 because dividing by n would underestimate the population variance, creating bias. We'll cover bias in more depth later.

We can calculate the variance of an array with [numpy.var()](https://docs.scipy.org/doc/numpy/reference/generated/numpy.var.html) or with pandas syntax df['column'].var.

df['age'].var()
np.var(df.age)

Standard Deviation

The most common estimate of variability used by statisticians is the square root of the variance, called the standard deviation. The standard deviation has some useful mathematical properties that we will review in the Central Limit Theory lesson later in this Unit.

s = v ** 0.5

NumPy gives us the useful [np.std()](https://docs.scipy.org/doc/numpy-1.10.1/reference/generated/numpy.std.html) function for working with standard deviations. A tricky default in numpy is to calculate the population standard deviation, dividing by n, rather than the sample standard deviation, dividing by n - 1. To calculate the sample instead of the population standard deviation we need to manually set the "delta degrees of freedom" with the ddof named parameter:

np.std(df['age'], ddof=1)

Standard Error

Another useful estimate of variance is the standard error, which quantifies uncertainty in the estimate of the sample mean. While the standard deviation tells us about variance in the population, the standard error tells us about the precision of our sample mean estimate. One example of standard errors at work is poll results, where they are called the "margin of error". For example, a poll might report that 44% of respondents were in favor of measure X, with a margin of error (standard error) of 3%. In other words, if the poll were run over and over again with new samples of respondents, the average response would fall between 41% (44-3) and 47% (44+3). Smaller standard errors mean more precise estimates.

The formula for the standard error se of the mean is the standard deviation of the sample s divided by the square root of the sample size n.

se = s / (n ** 0.5)

Using Python and NumPy, this is:

np.std(df['age'] ,ddof=1) / np.sqrt(len(df['age']))

Let's examine sampling from different distributions of low and high variance. We'll create two variables, one with low variability and one with high variability, and see how they differ.

# First, create an empty dataframe to store your variables-to-be.
pop=pd.DataFrame()

# Then create two variables with mean = 60, one with a low standard
# deviation (sd=10) and one with a high standard deviation (sd=100).
pop['low_var']=np.random.normal(60, 10, 10000)
pop['high_var']=np.random.normal(60, 100, 10000)

# Finally, create histograms of the two variables.
pop.hist(layout=(2, 1), sharex=True)
plt.show()

# Calculate and print the maximum and minimum values for each variable.
print(pop.max())
print(pop.min())

The variable with high variance has a much wider range of possible values than the variable with low variance. If these variables represented two populations we wanted to study, we would take samples from each, then generalize from those samples to get information about the populations. Let's try that next.

# Take a random sample of 100 observations from each variable
# and store it in a new dataframe.
sample=pd.DataFrame()
sample['low_var'] = np.random.choice(pop['low_var'], 100)
sample['high_var']=np.random.choice(pop['high_var'], 100)

# Again, visualize the data. Note that here we're using a pandas method to 
# create the histogram.
sample.hist()
plt.show()

# Check how well the sample replicates the population.
sample.mean()
sample.std(ddof=1)

Since the sample is randomly drawn from the population, you can re-run the code as many times as you like and always get a new sample. Try this a few times. You will notice that the low variability samples are closer to the population mean and standard deviation than the high variability samples. Each time a sample is drawn from each population, there is a chance to draw values from the tail ends of the distribution – extremely high values, or extremely low values. Having extreme values in the sample can pull the sample mean away from the population mean. Since the high variability variable has values that are much more extreme than the low variability variable, the estimates have the potential to fall farther from the mean.

Happily, since the extreme values are spread equally across "extremely high" and "extremely low," even multiple samples from a high variability population will eventually converge on the true mean… it will just take a bit longer.

Food for thought: what would happen if you increased the sample size to 1000?

### Describing Data with Pandas

import numpy as np
import pandas as pd
%matplotlib inline

# Set up the data
data = pd.DataFrame()
data['gender'] = ['male'] * 100 + ['female'] * 100
data['height'] = np.append(np.random.normal(69, 8, 100), np.random.normal(64, 5, 100))
data['weight'] = np.append(np.random.normal(195, 25, 100), np.random.normal(166, 15, 100))

data.head()

Describing data with Pandas

So far in this lesson, we've discussed the various ways we can use statistics to describe a given dataset. Now, we're going to discuss how we can leverage the tools of data science, specifically the pandas package, to quickly and easily describe our data. This is what you'll actually be using day to day when you have to describe or summarize the data you're working with. Rather than draw out formulas or perform calculations you'll use the tools of programming to get the answers you want easily and efficiently.
What we've seen before

We've already shown some of the basic tools. We have NumPy methods like .mean() or .std() to calculate the mean and standard deviation of our data.

data.height.mean()

65.921110470114073

data.height.std()

7.125274567757093

Now, there are many more methods in pandas to describe data in simple aggregative forms. Things like median and variance all have associated pandas methods. As a general rule of thumb, if you're trying to compute a standard statistical measure (the kinds of measures you could find in a statistics book somewhere) Python probably has a coded up method for it somewhere already. Usually that method will be in NumPy and pandas, but not always. It is, however, always worth a quick Google and check of Stack Overflow to see if the work has already been done before you go off and create your own functions.
The .describe() method

So far we've mostly talked about methods with two kinds of output: it either stays the same shape with modified values (the iterative kinds of methods) or it condenses the data into a single value output (aggregative methods). There is another group of methods in Pandas, and they happen to be supremely useful for quickly and coherently summarizing data in a numeric rather than visual way.

In statistics, there are a lot of descriptive values that are often used in concert with each other. The most classic example is probably mean and standard deviation. Using the two of them together gets you a lot of information about how the data is distributed across values.

Pandas understands this. Sometimes you want more than one value, but less than all of them. You want a set of summary statistics that give you a good, standardized view into the data and its variables. Enter .describe().

data.describe()

	height 	weight
count 	200.000000 	200.000000
mean 	65.921110 	181.416225
std 	7.125275 	25.996945
min 	49.268448 	126.352513
25% 	61.194613 	162.815738
50% 	65.567748 	176.152202
75% 	69.586985 	198.285979
max 	91.566155 	253.611685

Let's look at what that did. Firstly, it returned a data frame, but not one of the same size or shape that we gave it. Instead it iterated over the columns and created these standard statistical measures for each column possible. We say each column possible because one is missing: Gender. That's because gender is a string, rather than a numeric value. We can't compute the means of strings.

Now, as for the values themselves. Count should be relatively self evident, as should min and max. Mean and std (standard deviation) we've also talked about before. The three percent values are percentiles. These values represent cutoff points, below which a certain percentage of the data lies. So, 25% of weights are below 162.82 and so on.

Together, these values give us a decent image of what each of the variables included looks like. We can get a numerical sense of what we might call their "shape". However, this is only one part of .describe()'s capabilities. As we covered in the toolkit unit, we can also group our data. This allows us to be even more insightful with our describe, letting us compare the summary statistics for two different groups of our data.

data.groupby('gender').describe()

		height 	weight
gender 			
female 	count 	100.000000 	100.000000
mean 	63.195078 	164.643079
std 	4.786304 	12.775653
min 	50.591490 	128.763644
25% 	59.987204 	153.933783
50% 	63.674985 	166.122162
75% 	66.576880 	173.270107
max 	74.507797 	192.725068
male 	count 	100.000000 	100.000000
mean 	68.647143 	198.189371
std 	8.008156 	25.038595
min 	49.268448 	126.352513
25% 	62.886700 	184.832311
50% 	68.617447 	198.401302
75% 	74.520715 	217.906158
max 	91.566155 	253.611685

Now we have twice the output. This may not be the easiest form to read it, but it does give us a sense of the difference between the two groups, male and female. In this case we can see that the distributions for height and weight are higher for men than for women, which is what we'd expect. This kind of grouping can give us another layer of insight to our analysis.
Value Counts

Sometimes, you aren't dealing with data that is best summarized in this form. The most common example of this is strings, where these kinds of methods do not apply. In that case what you're probably interested in is counts. Python gives you an easy way to go over a column of data and return the distinct values as well as the counts of each.

data.gender.value_counts()

female    100
male      100
Name: gender, dtype: int64

Now, the first thing to note is that this method is working on data.gender, which is a series object rather than a data frame object. This .value_counts() method cannot iterate over a whole data frame. Luckily each column and row in a data frame is a series and you can use this method simply by selecting a column as we did above.

There are several reasons to use this method. Firstly, it gives you another way to make sense of your data. In this case it shows us that our data is evenly balanced between males and females, with one hundred samples of each.

There are plenty of other ways this function could be useful. It can show outliers or possible malformed data. For example, if we were to see something like 'Mal' with a single entry, we'd have found a typo in the data. This method works over both numerical and object data, though it is not valuable to run over the numeric columns in this example. Can you think of why?

data.weight.value_counts().head()

175.143849    1
208.507849    1
169.185494    1
165.450584    1
165.087602    1
Name: weight, dtype: int64

As you can see, it's not useful because we're dealing with truly continuous random data, so no value is exactly repeated. We simply get a list of all the values with a count of 1 for each.

However, these two methods, .describe() and .value_counts(), do often provide incredibly easy and valuable insights into your dataset. You'll want to use them throughout the course as one of the ways to get a first, quick sense of the data before digging in more specifically on points of interest.

## Basics of Probability

One of the reasons data science is in such high demand is because organizations want to predict the future. With the right dataset, a data scientist can create models that give information about how likely certain outcomes will be. Those models help organizations steer toward desired outcomes and away from negative ones.

### Perspectives on Probability
Probability is a way of quantifying the likelihood of a future outcome. People use probabilities to make decisions all the time. Knowing the probability of rain tomorrow helps to decide whether to put the rainboots and umbrella in the car tonight.

There are two broad schools of thought about probability in statistics. The frequentist school of thought defines probability as describing how often a particular outcome would occur in an experiment if that experiment were repeated over and over. For example, each time a coin is flipped, the outcome is either 1 (heads) or 0 (tails). Each coin flip is an "experiment" with an outcome. Over many coin flips, the coin will come up heads about 50% of the time. For a frequentist, saying an outcome has a 50% probability is equivalent to saying that if the experiment were repeated many times, that outcome would occur 50% of the time.

The Bayesian school of thought defines probability as describing how likely an observer expects a particular outcome to be in the future, based on previous experience and expert knowledge. Each time the experiment is run, the probability is updated if the new data changes the belief about the likelihood of the outcome. The probability based on previous experiences is called the "prior probability," or the "prior," while the updated probability based on the newest experiment is called the "posterior probability."

Both Bayesian and frequentist approaches to probability are used to model data, 
depending on the question being asked. Disagreements between the two camps can 
[get](https://xkcd.com/1132/) [heated](www.smbc-comics.com/index.php?id=4127), 
but there's no need to take sides: Most of the time, the Bayesian and frequentist approaches arrive at the same answer. A good rule of thumb is that frequentists are trying to calculate the likelihood of getting the data you have in the context of a fixed, if unknown, "true" population value. Bayesians are trying to calculate the most likely population value, given the data you have. As the data changes, Bayesians beliefs about the population value change as well.

For a more in-depth discussion with complex examples of how frequentist and Bayesian
approaches can be used to answer a question, including code in Python, 
see this [series of articles by Jake Vanderplas](jakevdp.github.io/blog/2014/03/11/frequentism-and-bayesianism-a-practical-intro/)

### Randomness, Sampling and Selection Bias

The concept of probability is fundamental to data science. A lot of the value a data scientist brings comes from the ability to quantify uncertainty – to go from a vague and woolly "maybe it will rain" to a clear and precise "65% chance of rain with a margin of error of 3%." Quantified uncertainty not only defines what is known, but how confident we can be about that knowledge.

Probability is also the fundamental basis of another critical element of the data scientist's toolkit: Randomness. Randomness can be defined as a situation where all possible outcomes are equally likely. The flip of a balanced coin is random: 50% likely to be heads, 50% likely to be tails. The roll of a six-sided dice is also random, with a 1 in 6 chance of getting each number between 1 and 6.

As we mentioned in an earlier assignment, it is rarely possible to gather data from all elements of a population of interest (can't get questionnaires to all potential customers around the world, can't get information about purchasing decisions that haven't happened yet). Instead, data scientists leverage the concept of randomness to gather a representative sample from the population. Using randomness, each element of a population has an equal chance of being chosen for the sample.
In an ideal world, random sampling creates a smaller group (a sample) that is sufficiently similar to the population that anything we learn about the sample also applies to the population. Larger samples are more likely to resemble the population, because they are less swayed by the occasional extreme value. On the other hand, smaller samples may be cheaper and faster to collect. Deciding how large a sample to collect depends in part on how variable we think the population is: the more variability in the population, the larger sample we need to get to be confident that our sample is a good stand-in for the population. However, it is important to keep in mind that the sample is random: It may, through sheer dumb luck, sample enough unusual individuals to be unrepresentative.

In practice, random sampling depends on perfect access to the population, which is very rarely possible. When studying customers, for example, not all customers may be interested in or willing to participate in data collection. The sample, in that case, differs from the population of all customers: The customers in the sample are all people who are willing to be studied. Systematic differences between the sample and the population are known as selection bias. If the sampled individuals differ from the others in important ways, such as spending rates or purchasing behavior, then knowledge gained from their data might not apply to all customers.
Selection bias: A practical example

An example from US history illustrates the pitfalls of generalizing from a biased sample. The 1936 US Presidential election pitted Alfred Landon against Franklin D. Roosevelt. The largest pre-election poll of the time, conducted by the respected magazine Literary Digest, projected that Landon would beat Roosevelt by 14%. This projection was based on ballots sent to 10 million US citizens, nearly a quarter of all eligible voters at the time. Yet the Literary Digest turned out to be impressively wrong, with Roosevelt beating Landon by 24%. The poll was off by an astounding 38%. How did this happen?

The Literary Digest's sampling efforts, though broad, were flawed: they sampled people by drawing from the telephone directory. In the middle of the Great Depression, phones were luxuries many could not afford. The Digest's methods led to a sample that was considerably older and richer than the general population… with predictable results for their election forecast. When it comes to sampling, it is better to have a small but representative sample than a large and biased one.

For more details on the Literary Digest poll, see [this case study](https://www.math.upenn.edu/~deturck/m170/wk4/lecture/case1.html)

### Independence and Dependence
When talking about probabilities of events, whether Bayesian or frequentist, one important consideration is whether the events are independent or dependent of one another. An event is independent of other events in the sample space if the outcome of that event is not affected by the outcome of other events in the sample space. For example, imagine a bag of 10 marbles, containing 5 blue marbles and 5 red marbles. Without looking, you reach into the bag and draw out a red marble. Then you put the marble back in the bag, and draw a blue marble. The probability of drawing a red marble first is 5/10, or 50%. The probability that the second marble will be blue is also 5/10, or 50%. Because you put the first marble back, the probability of drawing the second marble is independent of the first. Neither event affects the other.

The probability of drawing and replacing a red marble:

P(red) = 1/2

P in the formula above means "probability".

The probability of drawing and replacing a blue marble after drawing and replacing the red marble):

P(red) = P(blue) = 1/2

The probability of two or more independent events can be calculated by multiplying the probabilities of each individual event. The probability of drawing a red marble and then a blue marble:

P(red ∩ blue) = P(red) * P(blue) = (1/2) * (1/2) = 1/4

When the probability of event B changes based on the outcome of event A, the probability of event B is said to be dependent on, or conditional on, event A. Returning to the bag of marbles, again you reach into the bag and take out a red marble. Again, the probability that the first marble will be red is 5/10 or 50%.

P(red) = 1/2

Next, without replacing the red marble, you draw a blue marble. Now, the probability of drawing a blue marble depends on the color of the first marble drawn. We use | to denote a condition on the probability we're talking about. This is where the information we already have can be disclosed.

If the first marble was blue, then the probability of drawing a red marble the second time is 5/9 (because one blue marble is missing from the bag).

P(red | blue) = 5/9

You can read the | symbol as "given", so P(red | blue) would read "the probability of red given blue".

If the first marble was blue, then the probability of drawing a blue marble the second time is 4/9 (because one blue marble is missing from the bag).

P(blue | blue) = 4/9

The probability of drawing a blue marble the second time is conditional on the outcome of the first draw.

The probability of two conditional events can be calculated by multiplying the probability of event A by the probability of event B conditioned on A.

P(A ∩ B) = P(A) * P(B | A)

The probability of drawing two blue marbles in a row without replacement:

P(blue) * P(blue | blue) = (1/2) * (4/9) = 2/9

The probability of drawing a red marble and then a blue marble without replacement:

P(red) * P(blue | red) = (1/2) * (5/9) = 5/18

In data, conditional variables (conditional and dependent are synonymous, however, because a 'dependent variable' has a specific meaning in experimental design, we will use conditional when referring to variables) in a dataset contribute less information than independent variables, because some information is duplicated among conditional variables. For example, a survey may ask four questions: 1) a customer's age, 2) their income, 3) whether they bought any widgets that month, and 4) how much money they spent on widgets that month. The age and income variables are independent in the sample space: While knowing someone's age may give some hints about their income, there is enough variability in incomes between people of the same age that every datapoint is giving new information. Similarly, while the income variable is probably related to how much money people have available to spend on widgets, people with the same income may buy different amounts of widgets (or no widgets at all), so each datapoint provides new information for both variables.
Questions three and four, on the other hand, are conditional. If someone says that they didn't buy any widgets in the last month, we already know they spent $0 on widgets. Conversely, if someone says they spent $0 on widgets last month, we already know they didn't buy any widgets. The two variables aren't perfect duplicates, since knowing someone did buy one or more widgets isn't the same as knowing how much money they spent, but for at least some cases, knowing the answer to question 3 means we can be 100% certain that we know the answer to question 4 (and vice versa). 

### Bayes' Rule

On a random day you see a pop up clinic for an instant test for a new disease you’ve heard of: Weapon X. It’s an incredibly rare disease with almost no symptoms for months and then you suddenly die. It’s affecting about one in a million people, from what you’ve heard. This test says it’s 99.99% accurate in both directions (false positives and false negatives), so you decide it’s worth taking the test.

It comes back positive.

Should you panic?

Bayes' Rule explains that, in actuality, you’re probably just fine.
Conditional Probability

In this scenario we’re not focused on the probability of an independent event. It’s not the probability that you are infected with Weapon X. It’s the probability that you’re infected given the condition that you get a positive test.

That positive test provides additional information about what’s going on, and we can use that information to improve our probability estimate.

For this example, let’s say we have a million people. Chances are one of them is infected, since the disease affects one in a million, and that person will likely get a positive test result. However, if we tested every one of those other 999,999 people, we’d expect about 100 people to get positive results.

Once you see that positive test, what do we know about your likelihood of being infected? Since we know you have a positive test, we can consider only the people in that group who have seen a positive test result. In that group are 101 people, only 1 of whom actually has the infection. This works out to roughly 1% chance that you’re infected.

Now, these counts are a bit of a simplification, using expected counts rather than probabilities. Bayes' rule gives you this relationship in terms of probabilities.
Bayes' Rule

Bayes' Rule can be put in its simplest and most abstract terms as follows:

P(A | B) = P(B | A) * P(A) / P(B)

OR

P(A | B) = P(B | A) * P(A) / [P(A)*P(B|A) + P(A~)*P(B|A~)]

In English, this formula says the probability of A given B equals the probability of B given A, times the probability of A, divided by the probability of B. We expand the probability of B in the second formula where A~ is the inverse of A, so in our case not being infected. The numerator is our scenario of interest, while the denominator represents the realm of scenarios that could give our condition.

We can put that in terms of our example pretty simply.

P(Infected| Positive Test) = P(Positive Test| Infected) * P(Infected) / P(Positive Test)

= .9999 * .000001/(.000001*.9999 + .999999*.0001) = .0099 or .99%

So that says it’s less than 1% that you’re actually infected, which is still reasonably unlikely.

This may seem like a detached example, but this really happens. In general, people can be very 
bad at this kind of probabilistic reasoning. In one example in New York and San Francisco, 
[clinics stopped using a rapid HIV test because it was scaring healthy people](https://www.nytimes.com/2005/12/10/health/false-positives-from-hiv-test.html?_r=0). It’s why a lot of these tests get run multiple times before their results are given. The first response to a test suggesting an individual has a rare disease is usually to run it again.

### Evaluating data sources
Not all data sources are created equal. It is tempting to look at a dataset and assume it is correct, or representative, or that because it's about the subject you're interested in it can answer the questions you have about the topic. That is not necessarily the case. Evaluating data both for quality and bias is an important skill of data science.
Bias

We've mentioned the notion of samples versus populations before. It is very common to look at a problem and not be able to get data on every relevant individual, so we take a sample. Whenever we're dealing with a sample, it is essential to ask if that sample is truly random. If you do the sampling yourself, that process can be pretty easy. You know the process you engaged in to sample from the population and you can thoroughly evaluate its credibility.

For example, if you wanted information about the popular kinds of cereal, you could go to your local grocery and make a list of the cereals that they have on the shelf. This will give you a dataset, but not a great one. It's a single sample, biased by things like geographic location. The same principle applies when scraping a website, it's a single sample with the biases associated with that website.

This process becomes much more difficult, however, when dealing with data collected by someone else, and particularly datasets available on the internet. Pay close attention to the method used to collect the data and evaluate what if any biases may be present because of that.
Quality

It's important when approaching a new data source to try to judge its objective quality. Are there are a lot of unexplained blanks? Is it unevenly distributed across time? Does the volume fluctuate seemingly without cause? All of these things, and many more, can be signals that the quality of the dataset is questionable. Engaging in this questioning early and explicitly will help prevent situations where the conclusions of your analysis are compromised or when poor data quality becomes your conclusion.
Exceptional Circumstance

What was the situation under which data was collected? This can greatly impact the data and therefore the quality of conclusions you can draw from it. Returning to the grocery example, if you were trying to analyze the eating habits of Americans, you could look at the shopping behaviors at grocery stores across the country. Let's say you obtained a large sample that accurately covered the whole of the country with data from a variety of cities and neighborhoods.

But what if that data was collected on the day before the Super Bowl? Your dataset would then be skewed because the data was collected in an exceptional circumstance. The shopping behaviors on that day are possibly quite different from normal. Thinking about that aspect of the dataset can again help catch its limitations early on in the process.
What to do?

So what can you do with data that has issues with its quality or source? There are many options.

Firstly if you can quantify the bias, you can adjust to it. For example, let's say you were interested in fishing numbers, but only had data from San Francisco for the given year. You can look at other databases and figure out how other cities typically compare to where you have your data and try to impute larger trends. We'll cover imputing data in more detail later in the bootcamp.

You can also limit your conclusions to the scope of the data. Be very clear about where your conclusions are applicable. If you scraped a single online retailer, understand and state that your conclusions only apply to that store. When using data from Amazon, you're talking about Amazon shopping behaviors, not retail consumption as a whole. That analysis can still be highly valuable.

## The Normal Distribution and the Central Limit Theorem
A whole host of commonly-used statistical methods are built on the assumption that data is "normal".

### Define Normality
Data is described as "normal," or "normally distributed," if most values cluster in the center of the range, with the rest tapering off symmetrically to the left and the right. The mean and median of a normally distributed variable are equal. The information in a normal distribution can be summarized by the mean μ ("mu") and standard deviation σ ("sigma"). The probability density function for a normally distributed variable is:

f(x|μ,σ2)=12σ2π⎯⎯⎯⎯⎯⎯⎯⎯√e−(x−μ)22σ2
f(x|μ,σ2)=12σ2πe−(x−μ)22σ2

e is [Euler’s number](http://mathforum.org/dr.math/faq/faq.e.html) (e=2.71828…), a mathematical constant.

While you don’t need to memorize the probability density function to work with normally distributed variables, it is good to be able to recognize it if you come across it while reading about other statistical concepts.

Approximately 68% of the values in a normally-distributed variable fall within 1 standard deviation above or below the mean, 95% of values fall within two standard deviations of the mean, and 99.7% of values fall within three standard deviations of the mean.

We can use Python to generate a normally distributed variable by providing a mean and standard deviation, which we graph as a histogram.

import numpy as np

import pandas as pd

import matplotlib.pyplot as plt

%matplotlib inline

# Making a standard normally distributed variable with 1000 observations, a mean of 0, and 

# a standard deviation of 1, and putting it in a data frame.

mean = 0 

sd = 1

n = 1000

​

df = pd.DataFrame({'rand': np.random.normal(mean, sd, 1000)})

​

# Plotting the variables in the data frame (here, just the variable "rand") as a histogram.

df.hist()

# Inline printing the histogram

plt.show()

The normal distribution is useful for data scientists because:

    It is easily summarized using just two statistics (mean and standard deviation).
    The area under the curve is 1, making it easy to calculate the probability of individual outcomes within the distribution.
    It describes many natural phenomena, such as blood pressure, height, weight, etc.
    In general, any variable that measures an outcome produced by many small effects acting additively and independently will have a close to normal distribution.
    Lots of common scores (percentiles, z-scores) and statistical tests (t-tests, ANOVAs, bell-curve grading) assume a normal distribution.

### Deviations from Normality and Descriptive Statistics

Unfortunately, the usefulness of the normal distribution means that it oftentimes becomes the "default" distribution in people’s minds. This isn’t helped by the fact that it is called "normal"! Real data (as opposed to idealized mathematical concepts) is never perfectly normal, but some data is more normal than others. When statistics that assume normality are used on non-normal data, the mis-match between statistics and data can result in inaccurate conclusions.

While there are statistical tests of non-normality, they are sensitive to sample size, meaning that whether or not the test says your data is normal has more to do with how much data you have than the distribution of your data. Instead, the best method of deciding if your data is normal is to inspect the data visually using histograms and quantile-quantile (QQ) plots.

QQ plots graph a variable with an unknown distribution against a variable with a known distribution. Values for each variable are sorted into ascending order, then plotted against each other with the known variable as the x-axis and the unknown variable as the y-axis. If the mystery variable shares the same distribution as the known variable, the result should be a straight line running from the lower left-hand corner to the upper right-hand corner of the plot. Deviations from the straight line indicate that the data does not fit the distribution.

Let’s try a QQ plot to check if data is normally distributed:

import numpy as np

import pandas as pd

import matplotlib.pyplot as plt

%matplotlib inline

# Making two variables.

rand1 = np.random.normal(50, 300, 1000)

rand2 = np.random.poisson(1, 1000)

​

# Sorting the values in ascending order.

rand1.sort()

rand2.sort()

​

# Making a standard normally distributed variable with 1000 observations,

# a mean of 0, and standard deviation of 1 that we will use as our “comparison.”

norm = np.random.normal(0, 1, 1000)

​

# Sorting the values in ascending order.

norm.sort()

# Plotting the variable rand1 against norm in qqplots.

plt.plot(norm, rand1, "o") 

plt.show() 

# Plotting the variable rand2 against norm in qqplots.

plt.plot(norm, rand2, "o") 

plt.show()

Looking at the QQ plot, it is clear that the values of "rand1" are normally distributed, while the values of "rand2" are not normally distributed. (In fact, "rand2" reflects a different probability distribution, "Poisson," which will be discussed in a later assignment.)

You may notice that with a QQ plot, the scales of the known and unknown variables do not have to match: What matters is the relationships between datapoints within each variable.

When data are not normal, the mean and standard deviation are no longer accurate or informative summaries. Let's make histograms of rand1 and rand2, then compute descriptive statistics to see how well they match up.

#Plot a histogram for rand1.

plt.hist(rand1, bins=20, color='c')

​

# Add a vertical line at the mean.

plt.axvline(rand1.mean(), color='b', linestyle='solid', linewidth=2)

​

# Add a vertical line at one standard deviation above the mean.

plt.axvline(rand1.mean() + rand1.std(), color='b', linestyle='dashed', linewidth=2)

​

# Add a vertical line at one standard deviation below the mean.

plt.axvline(rand1.mean()-rand1.std(), color='b', linestyle='dashed', linewidth=2) 

​

# Print the histogram.

plt.show()

# Plot the same histogram for rand2.

plt.hist(rand2, bins=20, color = 'c')

​

# Add a vertical line at the mean.

plt.axvline(rand2.mean(), color='b', linestyle='solid', linewidth=2)

​

# Add a vertical line at one standard deviation above the mean.

plt.axvline(rand2.mean() + rand2.std(), color='b', linestyle='dashed', linewidth=2)

​

#Add a vertical line at one standard deviation below the mean.

plt.axvline(rand2.mean() - rand2.std(), color='b', linestyle='dashed', linewidth=2)

​

# Print the histogram.

plt.show()

Because rand1 is normal, the mean is placed where the data clusters, with approximately 50% of the data falling on either side, and approximately 67% of the data falling within one standard deviation of the mean. For rand2, the mean is still placed where the data clusters, but the cluster is not centered, and the standard deviation does not encompass the same amount of data on each side of the mean. Put another way, for rand2 the mean is no longer a measure of "central" tendency, as it does not fall in the center, and the standard deviation no longer describes how much variance there is. Asymmetric probability distributions are described as "skewed."

### Other Distributions

So far, we’ve categorized data as either “normal” or “non-normal,” but there are many other probability distributions that also have useful characteristics for addressing particular statistical problems. We won’t review all of them (see here for a more comprehensive list) but here are brief introductions to some of the most common.
Bernoulli

The Bernoulli distribution represents two possible outcomes of an event (such as a coin flip). Summarized by p, the probability of the outcome k.

The probability mass function for the Bernoulli distribution is:

$$\begin{equation}
  f(k|p)=\left\{
  \begin{array}{@{}ll@{}}
    p, & \text{if}\ k=1 \\
    1-p, & \text{if}\ k=0
  \end{array}\right.
\end{equation}$$

Note that when a distribution is discrete (only takes integers), it has a probability mass function, while a continuous distribution has a probability density function.

import numpy as np

import pandas as pd

import matplotlib.pyplot as plt

%matplotlib inline

# Generate a bernoulli distribution with p =0.5.

bernoulli= np.random.binomial(1, .5, 1000)

​

#Plot a histogram.

plt.hist(bernoulli)

​

# Print the histogram

plt.show()

Binomial:

A binomial distribution counts the number of successes when an event with two possible outcomes is repeated many times (such as many coin flips). Summarized by p, the probability of getting k successes during n repetitions of the event. The probability mass function is:

f(k|n,p)=(nk)pk(1−p)(n−k)
f(k|n,p)=(nk)pk(1−p)(n−k)

# Generate a binomial distribution with n=20 and p=0.5.

binomial = np.random.binomial(20, 0.5, 1000)

​

# Plot a histogram.

plt.hist(binomial)

​

# Print the histogram.

plt.show()

Gamma

The gamma distribution represents the time until an event (such as lifespan until death), when the event starts out unlikely (few people die in youth), becomes more likely (more people die in old age), then becomes less likely again (few people die in extreme old age because most have already died). Summarized by a shape parameter (αα) and an inverse-scale parameter (ββ). The probability density function is:

f(x|α,β)=βαxα−1e−xβΓ(α)for x≥0 and α,β≥0
f(x|α,β)=βαxα−1e−xβΓ(α)for x≥0 and α,β≥0

# Generate a gamma distribution with shape =5 and scale = 1

gamma = np.random.gamma(5,1, 1000)

​

# Plot a histogram.

plt.hist(gamma)

​

# Print the histogram.

plt.show()

Poisson

The poisson distribution represents the number of times a given event (such as a phone call to a radio show) will occur during a given time interval. Data can range from 0 (no phone calls during the time period) to approaching infinity (the phone never stopped ringing during the time period). Summarized by λλ (“lambda”), the rate that events occur during a given time period. The probability mass function is:

f(k|λ)=λke−λk!
f(k|λ)=λke−λk!

# Generate a Poisson distribution with lambda = 3

poisson = np.random.poisson(3, 1000)

​

# Plot a histogram.

plt.hist(poisson)

​

# Print the histogram.

plt.show()

Identifying whether data has a distribution with known statistical properties requires visualizing the data through histograms and QQ plots, as well as knowing the source of the data (counts, probabilities, times, etc). When collecting and exploring new data as a data scientist you’ll make heavy use of visualizations like the ones we use above.
Conditional Distribution

Distributions can also be conditional. Consider an ecommerce site. For all of the customers, we have a distribution of the amount that they have spent on the website. It may look something like this:

# Creating a data frame to hold the simulated ecommerce data, and populating it with a

# normally distributed variable with mean 75 and standard deviation 25.

​

ecommerce = pd.DataFrame()

ecommerce['spending'] = np.random.normal(75, 25, 1000)

​

# Plot a histogram.

plt.hist(ecommerce['spending'])

plt.show()

But let's say we're actually interested in a subset of that population, for instance visitors who visited the site more than twice. That data may look like this:

# Adding a variable with counts of number of times visiting the site.

ecommerce['visit_count'] = np.random.randint(0, 5, 1000)

​

# Selecting only the cases where the visit count is greater than two and plotting those.

plt.hist(ecommerce[ecommerce['visit_count'] > 2]['spending'])

plt.show()

This is a conditional distribution, with the condition being that the user visited more than twice. This is an example of how we can use information about one aspect of a data set to inform another.
